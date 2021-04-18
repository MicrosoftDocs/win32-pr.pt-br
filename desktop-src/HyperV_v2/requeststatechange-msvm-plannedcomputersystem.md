---
description: Solicita que o estado do sistema planejado seja alterado para o valor especificado.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Método RequestStateChange da classe Msvm_PlannedComputerSystem
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
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757403"
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

*Requestedstate* \[ no\]
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

**Defer** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Desativar** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Reinicializar** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Redefinir** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Esse parâmetro não é usado e deve ser **nulo**.

</dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.



| Código/valor de retorno                                                                                                                      | Descrição                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>0</dt> </dl>     | Êxito<br/>                                                                 |
| <dl> <dt></dt><dt>4096</dt> </dl>  |                                                                                    |
| <dl> <dt></dt><dt>32768</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32769</dt> </dl> | Acesso negado.<br/>                                                          |
| <dl> <dt></dt><dt>32770</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32771</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32772</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32773</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32774</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32775</dt> </dl> | Não há suporte para o valor especificado no parâmetro *requestedstate* .<br/> |
| <dl> <dt></dt><dt>32776</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32777</dt> </dl> |                                                                                    |
| <dl> <dt></dt><dt>32778</dt> </dl> |                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




