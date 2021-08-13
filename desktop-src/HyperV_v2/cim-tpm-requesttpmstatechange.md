---
description: Solicita que o estado do TPM seja alterado para o valor especificado no parâmetro RequestedTPMState.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Método RequestTPMStateChange da classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 94af1d619ffa686b2fb4546987c6b825e4c658a5ae045d84fe5c6181716e95e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646444"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>Método RequestTPMStateChange da classe CIM \_ TPM

Solicita que o estado do TPM seja alterado para o valor especificado no parâmetro *RequestedTPMState* . Se a invocação do método for concluída com êxito, a propriedade **TPMState** deverá ser igual ao parâmetro **RequestedTPMState** . Invocar o método **RequestTPMStateChange** várias vezes pode resultar em solicitações anteriores sendo substituídas ou perdidas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RequestedTPMState* \[ no\]
</dt> <dd>

Os Estados de TPM solicitados.

<dt>

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


</dt> <dd></dd> </dl> </dd> <dt>

*AuthorizationToken* \[ no\]
</dt> <dd>

Token de autorização que pode ser necessário para que a ação entre em vigor. O parâmetro *AuthorizationToken* pode ser necessário para estabelecer a presença física ou para passar o OwnerAuth, a senha de autorização do proprietário definido pelo TCG. No caso do OwnerAuth, o SharedCredential CIM \_ com valor não nulo do CIM \_ SharedCredential. Secret pode ser necessário. A \_ Propriedade CIM SharedCredential. Algorithm também pode ser especificada com base na propriedade CIM \_ TPMCapabilities. SupportedPasswordAlgorithms.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Pode conter uma referência para o [**CIM \_ ConcreteJob**](cim-concretejob.md) criado para acompanhar a transição de estado iniciada pela invocação de método.

</dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha. O formato do intervalo deve ser usado para especificar o *TimeoutPeriod*. Um valor 0 ou um parâmetro nulo indica que o cliente não tem requisitos de tempo para a transição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Erro desconhecido ou não especificado** (2)
</dt> <dt>

**Não é possível concluir dentro do período de tempo limite** (3)
</dt> <dt>

**Com falha** (4)
</dt> <dt>

**Parâmetro inválido** (5)
</dt> <dt>

**Em uso** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Transição de estado inválida** (4097)
</dt> <dt>

**Não há suporte para o uso do parâmetro timeout** (4098)
</dt> <dt>

**Ocupado** (4099)
</dt> <dt>

**Método reservado** (4100.. 32767)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TPM CIM**](cim-tpm.md)
</dt> </dl>

 

 




