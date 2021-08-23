---
description: Solicita que o estado do elemento seja alterado.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Método RequestStateChange da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 457ed1e98714a2a20169fd1139b7f42475e5d893756591930b6a25147f756897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522236"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a>Método RequestStateChange da classe de \_ teclado Msvm

Solicita que o estado do elemento seja alterado.

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

O novo estado solicitado para o elemento. Essas informações serão colocadas na propriedade **requestedstate** da instância se o código de retorno for 0 (' concluído sem erro '), 3 (' timeout ') ou 4096 (0x1000) (' trabalho iniciado '). Para obter explicações detalhadas dos valores *requestedstate* , consulte a descrição das propriedades **enabledstate** e **requestedstate** .

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

Uma referência ao trabalho. Esse parâmetro poderá ser **nulo** se a tarefa for concluída.

</dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

A quantidade máxima de tempo que o cliente espera que a transição para o novo estado seja executada. O formato do intervalo deve ser usado para especificar esse período de tempo limite. Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno de 4098 ("uso de parâmetro de tempo limite não suportado") será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Teclado Msvm**](msvm-keyboard.md)
</dt> </dl>

 

 




