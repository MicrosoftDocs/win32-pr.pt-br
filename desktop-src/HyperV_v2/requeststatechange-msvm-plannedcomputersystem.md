---
description: Solicita que o estado do sistema planejado seja alterado para o valor especificado.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Método RequestStateChange da classe Msvm_PlannedComputerSystem classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54ff75630e93392805d835032ca3405f97e0a26e58c1c61ab06ba18bb1a88856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083086"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a>Método RequestStateChange da classe Msvm \_ PlannedComputerSystem

Solicita que o estado do sistema planejado seja alterado para o valor especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RequestedState* \[ Em\]
</dt> <dd>

O estado solicitado para o sistema planejado.

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

Esse parâmetro não é usado e deve ser **Nulo.**

</dd> <dt>

*TimeoutPeriod* \[ Em\]
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.



| Valor/código de retorno                                                                                                                      | Descrição                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>0</dt> </dl>     | Êxito<br/>                                                                 |
| <dl> <dt></dt><dt>4096</dt> </dl>  |                                                                                    |
| <dl> <dt></dt><dt>32768</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32769</dt> </dl> | Acesso negado<br/>                                                          |
| <dl> <dt></dt><dt>32770</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32771</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32772</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32773</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32774</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32775</dt> </dl> | Não há suporte para o valor especificado *no parâmetro RequestedState.*<br/> |
| <dl> <dt></dt><dt>32776</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32777</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32778</dt> </dl> |                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




