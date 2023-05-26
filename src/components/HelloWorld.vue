<template>
  <div class="contact-block">
    <div class="contact-form">
      <h3>Contact Us</h3>
      <form>
        <div class="field-wrap">
          <label for="email">E-Mail-Adresse *</label>
          <input
            type="email"
            id="email"
            name="email"
            class="form-input"
            placeholder="ex. name@email.com"
          />
        </div>
        <div class="field-wrap">
          <label for="auftrags-id">Auftrags ID *</label>
          <input
            id="auftrags-id"
            name="auftrags-id"
            placeholder="Ex . #000000"
            class="form-input"
          />
        </div>
        <div class="field-wrap">
          <label for="subject">Subject *</label>
          <input
            id="subject"
            class="form-input"
            name="subject"
            placeholder="subject"
          />
        </div>
        <div class="field-wrap">
          <label for="message">Message *</label>
          <textarea
            cols="2"
            rows="10"
            placeholder="Bitte schreiben Sie uns Ihr Anliegen"
          ></textarea>
        </div>
        <div class="field-wrap form-checkbox">
          <input type="checkbox" id="agree" name="agree" value="agree" />
          <label for="agree"
            >I agree to Terms & Conditions and Privacy Policy.</label
          >
        </div>
      </form>
    </div>
    <input
      type="submit"
      class="form-btn"
      value="Rücksendeantrag abschicken"
      v-on:click="openConfirmationBox"
    />
    <div class="confirmation-box" id="box">
      <div class="box-content">
        <span class="close" v-on:click="closeConfirmationBox">&times;</span>
        <div class="row">
          <div class="col-md-6">
            <div class="modal-img">
              <img src="../assets/Frame.png" />
            </div>
          </div>
          <div class="col-md-6 bg-blue">
            <div class="form modal-form">
              <h3>Subscribe to morgenland</h3>
              <div class="field-wrap">
                <label for="subject">E-Mail-Adresse</label>
                <input
                  id="email"
                  class="form-input"
                  name="email"
                  placeholder="ex.name@email.com"
                />
              </div>
              <input type="submit" class="form-btn" value="Subscribe" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    openConfirmationBox: function () {
      document.getElementById("box").style.display = "block";
    },

    closeConfirmationBox: function () {
      document.getElementById("box").style.display = "none";
    },
  },
};
</script>

<style scoped>
.contact-block {
  max-width: 530px;
  padding: 24px 32px;
  margin: 0 auto;
  background-color: #fff;
  border: 1px solid #cfcfcf;
}

.contact-form h3 {
  font-size: 24px;
  font-weight: 700;
  line-height: 52px;
  text-transform: capitalize;
  color: #212529;
  margin-bottom: 16px;
}

form label {
  display: block;
  font-weight: 500;
  font-size: 14px;
  color: #212529;
  margin-bottom: 8px;
}

form input {
  padding: 12px 16px;
  border: 1px solid #b5b5b5;
  border-radius: 4px;
  height: 52px;
  background: white;
  font-weight: 400;
  font-size: 16px;
  color: #686f75;
  outline: none;
  resize: none;
}

.form-input {
  width: 100%;
}

form .field-wrap {
  margin-bottom: 20px;
}

form textarea {
  height: 171px;
  outline: none;
  resize: none;
  width: 100%;
  border-color: #b5b5b5;
  padding-top: 6px;
  padding-left: 4px;
}

form .form-checkbox {
  display: flex;
  align-items: center;
}

form .form-checkbox #agree {
  height: 23px;
  width: 23px;
}

form .form-checkbox label {
  padding-left: 17px;
  margin-bottom: 0;
}

.form-btn {
  text-align: center;
  font-size: 17px;
  line-height: 26px;
  border-radius: 4px;
  padding: 16px 32px;
  border: none;
  font-weight: 900;
  background-color: #141414;
  color: white;
  cursor: pointer;
  width: 100%;
}

.contact-block .field-wrap label {
  font-weight: 500;
  font-size: 14px;
  line-height: 17px;
  color: #212529;
}

.confirmation-box {
  display: none;
  position: fixed;
  z-index: 1;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgb(0, 0, 0);
  background-color: rgba(0, 0, 0, 0.4);
}

.box-content {
  background-color: #fefefe;
  margin: auto;
  padding: 20px;
  border: 1px solid #888;
  width: 80%;
}

.close {
  color: #aaaaaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.box-content {
  max-width: 1085px;
}

.box-content .row {
  display: flex;
  flex-wrap: wrap;
  margin-right: -15px;
  margin-left: -15px;
}
.col-md-6 {
  position: relative;
  width: 100%;
  padding-left: 15px;
  padding-right: 15px;
}
@media (min-width: 768px) {
  .col-md-6 {
    flex: 0 0 50%;
    max-width: 50%;
  }
}
.modal-img {
  padding: 1rem;
}
img {
  max-width: 100%;
  height: auto;
}
.modal-form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
}
.modal-form h3 {
  font-size: 24px;
  font-weight: 700;
  line-height: 52px;
  text-transform: capitalize;
  color: #212529;
  margin-bottom: 16px;
}
.modal-form .field-wrap {
  margin-bottom: 16px;
}
.modal-form label {
  display: block;
  font-weight: 500;
  font-size: 14px;
  color: #212529;
  margin-bottom: 8px;
}
.modal-form .field-wrap .form-input {
  padding: 12px 16px;
  border: 1px solid #b5b5b5;
  border-radius: 4px;
  height: 52px;
  background: white;
  font-weight: 400;
  font-size: 16px;
  color: #686f75;
  outline: none;
  resize: none;
  margin-bottom: 16px;
}
</style>
