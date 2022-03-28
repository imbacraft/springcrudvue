<template>
  <el-dialog type="warning" title="Διαχείριση Προμηθευτή" :visible="visible" :modal="true"
             :close-on-click-modal="false"
             :close-on-press-escape="false" :modal-append-to-body="false" :show-close="false" width="75%"
             @close="clearValidation">

    <el-card>
    <el-form ref="supplierForm" :model="supplier" :rules="rules" label-position="top">

      <el-row :gutter="20">
        <!-- LEFT COLUMN -->
        <el-col :span="12">

          <el-form-item label="Εισάγετε όνομα εταιρείας"
                        prop="companyName">
            <el-input prefix-icon="fa fa-user"
                      v-model="supplier.companyName"
                      placeholder="Όνομα εταιρείας"
                      autoComplete="companyName">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε το κύριο όνομα"
                        prop="name">
            <el-input prefix-icon="fa fa-user"
                      v-model="supplier.firstName"
                      placeholder="Κύριο Όνομα"
                      autoComplete="firstName">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε το επίθετο"
                        prop="name">
            <el-input prefix-icon="fa fa-user"
                      v-model="supplier.lastName"
                      placeholder="Επίθετο"
                      autoComplete="lastName">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε ΑΦΜ"
                        prop="vatNumber">
            <el-input prefix-icon="fa fa-phone"
                      v-model="supplier.vatNumber"
                      placeholder="ΑΦΜ"
                      autoComplete="vatNumber">
            </el-input>
          </el-form-item>

           <el-form-item label="Εισάγετε ΔΟΥ"
                        prop="irsOffice">
            <el-input prefix-icon="fa fa-phone"
                      v-model="supplier.irsOffice"
                      placeholder="ΔΟΥ"
                      autoComplete="irsOffice">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε τη διεύθυνση"
                        prop="address">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.address"
                      type="address"
                      placeholder="Διεύθυνση"
                      autoComplete="address">
            </el-input>
          </el-form-item>

           <el-form-item label="Εισάγετε τον Ταχυδρομικό Κώδικα"
                        prop="zipCode">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.zipCode"
                      type="zipCode"
                      placeholder="Ταχυδρομικός Κώδικας"
                      autoComplete="zipCode">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε την Πόλη"
                        prop="city">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.city"
                      type="city"
                      placeholder="Πόλη"
                      autoComplete="city">
            </el-input>
          </el-form-item>

          <el-form-item label="Εισάγετε την Χώρα"
                        prop="country">
            <el-input prefix-icon="fa fa-envelope"
                      v-model="supplier.country"
                      type="country"
                      placeholder="Χώρα"
                      autoComplete="country">
            </el-input>
          </el-form-item>

        </el-col>
      </el-row>

    </el-form>

      <el-row>
        <el-col style="text-align: right">
          <el-button type="success"
                     icon="fa fa-save"
                     @click="save"> Αποθήκευση </el-button>

          <el-button type="danger"
                     icon="fa fa-remove"
                     @click="confirmDelete"
                     :disabled="!isDeletable"> Διαγραφή </el-button>
        </el-col>
      </el-row>
    </el-card>

    <div slot="footer" class="dialog-footer card-footer">
      <el-button type="warning"
                 icon="el-icon-back"
                 @click="cancel"> Επιστροφή </el-button>
    </div>

  </el-dialog>
</template>
<script src="./supplierVM.js"></script>
