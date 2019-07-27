##### Jawaban nomer satu saya buat dengan jjava untuk mereturn menjadi JSON, Silahkan dicompile lwat cmd atau IDE Java

public class DataDiri {

	private int id;
	private String name;
	private String age;
	private String address;
	private String hobbies;
	private String is_married;
	private String interest_in_coding ;
	public int getId() {
		return id;
	}
	public void setId(int id) {
		this.id = id;
	}
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public String getAge() {
		return age;
	}
	public void setAge(String age) {
		this.age = age;
	}
	public String getAddress() {
		return address;
	}
	public void setAddress(String address) {
		this.address = address;
	}
	public String getHobbies() {
		return hobbies;
	}
	public void setHobbies(String hobbies) {
		this.hobbies = hobbies;
	}
	public String getIs_married() {
		return is_married;
	}
	public void setIs_married(String is_married) {
		this.is_married = is_married;
	}
	public String getInterest_in_coding() {
		return interest_in_coding;
	}
	public void setInterest_in_coding(String interest_in_coding) {
		this.interest_in_coding = interest_in_coding;
	}
}
import java.util.HashMap;
import java.util.Map;

import com.arka.nsatu.DataDiri;
import com.fasterxml.jackson.core.JsonProcessingException;
import com.fasterxml.jackson.databind.ObjectMapper;

public class Main {

	public static void main(String args[]) {
		
		DataDiri dataDiri = new DataDiri();
		dataDiri.setId(1);
		dataDiri.setName("Arka");
		dataDiri.setAge("17");
		dataDiri.setAddress("Boothcamp");
		dataDiri.sethobbies("Code to the ding");
		dataDiri.setIs_married("Belum");
		dataDiri.setInterest_in_coding("Ya");
			
		ObjectMapper objectMapper = new ObjectMapper();
		
		try {
			String jsonStr = objectMapper.writeValueAsString(map);
			System.out.println(jsonStr);
		} catch (JsonProcessingException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	}
}

---
### hasil JSON 
---

{"id":1,"name":"Arka","Age":"17","address":"Boothcamp","hobbies":"code","is_married":"Belum","interest_in_coding":"Ya"}
