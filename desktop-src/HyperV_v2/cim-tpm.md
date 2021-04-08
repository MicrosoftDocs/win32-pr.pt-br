---
description: Descreve um dispositivo Trusted Platform Module (TPM).
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: Classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f2d35d42e864a247ca042ec81813ff7d1ac5c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010834"
---
# <a name="cim_tpm-class"></a>\_Classe TPM CIM

Descreve um dispositivo Trusted Platform Module (TPM).

## <a name="syntax"></a>Sintaxe

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a>Membros

A classe **CIM \_ TPM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **CIM \_ TPM** tem esses métodos.



| Método                                                         | Descrição                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**ChangeOwnerAuth**](cim-tpm-changeownerauth.md)             | Altera a credencial de autorização do proprietário de um dispositivo TPM.<br/>                                                  |
| [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) | Solicita que o estado do TPM seja alterado para o valor especificado no parâmetro **RequestedTPMState** .<br/> |



 

### <a name="properties"></a>Propriedades

A classe **CIM \_ TPM** tem essas propriedades.

<dl> <dt>

**AvailableRequestedTPMStates**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ TPM CIM**.**RequestTPMStateChange**, CIM \_ TPMCapabilities. RequestedTPMStatesSupported ")
</dt> </dl>

Os valores possíveis para o parâmetro *RequestedTPMState* do método [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 habilitado – ativo-de propriedade** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 desabilitado-ativo-proprietário** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 habilitado-inativo-de propriedade** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**S4 desabilitado-inativo-de propriedade** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 habilitado-ativo-sem proprietário** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 desabilitado – ativo-sem proprietário** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 habilitado – inativo – sem proprietário** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 desabilitado-inativo – sem proprietário** (9)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**TPMManafucturerMajorRevision**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| seção 5,3 \| versão \| revMajor ")
</dt> </dl>

A revisão principal do fabricante do TPM.

</dd> <dt>

**TPMManufacturerId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| Part 2 v1dot2 \| seção 21,6 \| TPM \_ Cap \_ informações de versão \_ \| tpmVendorID ")
</dt> </dl>

A ID do fabricante do TPM.

</dd> <dt>

**TPMManufacturerInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| Part 2 v 1.2. TCG \| seção 21,6 \| TPM \_ Cap \_ version \_ info \| vendorSpecific ")
</dt> </dl>

As informações adicionais definidas pelo fabricante do TPM.

</dd> <dt>

**TPMManufacturerMinorRevision**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| seção 5,3 \| versão \| revMinor ")
</dt> </dl>

A revisão mínima do fabricante do TPM.

</dd> <dt>

**TPMSpecMajorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| Part 2 v1dot2 \| seção 5,3 \| versão \| principal "," TSS. O TCG \| nível 1 v 1.2 \| seção 2.3.2.18 ")
</dt> </dl>

A versão principal do TPM.

</dd> <dt>

**TPMSpecMinorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| seção 5,3 \| versão \| secundária "," TSS. O TCG \| nível 1 v 1.2 \| seção 2.3.2.18 ")
</dt> </dl>

A versão secundária do TPM.

</dd> <dt>

**TPMState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 1 v1dot2 \| seção 9,4 "," TPM. TCG \| parte 2 v1dot2 \| seção 7,1 \| \_ sinalizadores permanentes do TPM \_ "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ TPM do CIM**.**RequestTPMStateChange**","**\_ TPM CIM**.**TransitioningToTPMState**")
</dt> </dl>

O estado operacional do TPM.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 habilitado – ativo-de propriedade** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 desabilitado-ativo-proprietário** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 habilitado-inativo-de propriedade** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**S4 desabilitado-inativo-de propriedade** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 habilitado-ativo-sem proprietário** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 desabilitado – ativo-sem proprietário** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 habilitado – inativo – sem proprietário** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 desabilitado-inativo – sem proprietário** (9)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Não aplicável** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**TransitioningToTPMState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ TPM CIM**.**RequestTPMStateChange**","**\_ TPM CIM**.**TPMState**")
</dt> </dl>

O estado de destino para o qual o TPM está em transição.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 habilitado – ativo-de propriedade** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 desabilitado-ativo-proprietário** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 habilitado-inativo-de propriedade** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 desabilitado-inativo-de propriedade** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 habilitado-ativo-sem proprietário** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 desabilitado – ativo-sem proprietário** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 habilitado – inativo – sem proprietário** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 desabilitado-inativo – sem proprietário** (9)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (10)


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Nenhuma alteração** (11)


</dt> <dd></dd> <dt>



 12


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

