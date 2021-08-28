---
description: Solicita que o estado do serviço convidado seja alterado para o valor especificado.
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: Msvm_GuestService::RequestStateChange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7685ec7c1740f869b251124920233ed9d6d8a97060c097f138493f371ee4fc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501096"
---
# <a name="msvm_guestservicerequeststatechange-method"></a>Método Msvm \_ GuestService::RequestStateChange

Solicita que o estado do serviço convidado seja alterado para o valor especificado.

## <a name="syntax"></a>Sintaxe


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RequestedState* \[ Em\]
</dt> <dd>

O novo estado. As informações são colocadas na propriedade **RequestedState** da instância se o código de retorno do **método RequestStateChange** for 0 ou 4096. Para obter mais informações, consulte a descrição das **propriedades EnabledState** e **RequestedState** para o elemento. Esse deve ser um dos valores a seguir.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Desligar** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Teste** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Adiar** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Quiesce** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Reinicializar** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Redefinir** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor Reservado** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Uma referência opcional a um [**objeto \_ ConcreteJob CIM**](cim-concretejob.md) que será retornado se a operação for executada de forma assíncrona. Se estiver presente, a referência retornada poderá ser usada para monitorar o progresso e obter o resultado do método .

</dd> <dt>

*TimeoutPeriod* \[ Em\]
</dt> <dd>

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo estado leve. O formato de intervalo deve ser usado para especificar o período de tempo." Um valor de 0 ou **Null** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contém 0 ou **Null** e a implementação não dá suporte a esse parâmetro, um código de retorno de 4098 ( Uso do parâmetro **de** tempoout sem suporte ) deve ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.



| Valor/código de retorno                                                                                                                                                                       | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>                           | Êxito.<br/>                                                                |
| <dl> <dt>**Sem suporte**</dt> <dt>1</dt> </dl>                                     |                                                                                    |
| <dl> <dt>**Parâmetros de método verificados – Transição iniciada**</dt> <dt>4096</dt> </dl> | A transição é assíncrona.<br/>                                         |
| <dl> <dt>**Uso do parâmetro timeout sem suporte**</dt> <dt>4098</dt> </dl>         |                                                                                    |
| <dl> <dt>**Acesso negado**</dt> <dt>32769</dt> </dl>                                 | Acesso negado<br/>                                                          |
| <dl> <dt>**Estado inválido para esta operação**</dt> <dt>32775</dt> </dl>              | Não há suporte para o valor especificado *no parâmetro RequestedState.*<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\\\Virtualização \\ raiz \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




