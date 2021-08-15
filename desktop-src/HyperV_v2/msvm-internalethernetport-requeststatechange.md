---
description: O método RequestStateChange da classe Msvm_InternalEthernetPort-solicita uma alteração de estado.
ms.assetid: 34f226a2-392b-4b3c-898e-308af52b71a2
title: Método RequestStateChange da classe Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b85073877826dab37158cc296c23cda5ca8f91de318dd9c30a74f041b3e87acd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117811703"
---
# <a name="requeststatechange-method-of-the-msvm_internalethernetport-class"></a>Método RequestStateChange da classe Msvm \_ InternalEthernetPort

Solicita uma alteração de estado.

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

O novo estado. As informações serão colocadas na propriedade **requestedstate** da instância se o código de retorno do método **RequestStateChange** for 0 ou 4096. Para obter mais informações, consulte a descrição das propriedades **enabledstate** e **requestedstate** para o elemento. Deve ser um dos valores a seguir.

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

Pode conter uma referência para o [**CIM \_ ConcreteJob**](cim-concretejob.md) criado para acompanhar a transição de estado iniciada pela invocação de método.

</dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha. O formato do intervalo deve ser usado para especificar o período de tempo limite. Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ InternalEthernetPort**](msvm-internalethernetport.md)
</dt> </dl>

 

 




