### Menggunakan REGEX 

        ---
const patterns = {
        telephone: /^\d{11}$/,
        slug: /^[a-z0-9-]+$/,
        username: /^[a-z]{5,12}$/i,
        password: /^[a-z0-9_-]{8,20}$/,
        email: /^([a-z\d\.-]+)@([a-z\d-]+)\.([a-z]{2,8})(\.[a-z]{2,8})?$/
        //             yourname @ domain   .  com          ( .uk )
};
        ---

// validation function
function validate(field, regex){

    if(regex.test(field.value)){
        field.className = 'valid';
    } else {
        field.className = 'invalid';
    }
        ---
