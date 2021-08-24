---
description: Método RequestStateChange da classe Msvm_SyntheticKeyboard - Solicita uma alteração de estado.
ms.assetid: 984e8a68-bc95-4a8b-99d6-ac248e96c45e
title: Método RequestStateChange da classe Msvm_SyntheticKeyboard classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3a16710adafaf3c9a4d04658f556592c485fd3ce1fa5b88c198b8913dadda543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146715"
---
# <a name="requeststatechange-method-of-the-msvm_synthetickeyboard-class"></a>Método RequestStateChange da classe Msvm \_ SyntheticKeyboard

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

*RequestedState* \[ Em\]
</dt> <dd>

O estado solicitado para o elemento. Essas informações serão colocadas na propriedade **RequestedState** da instância se o código de retorno do método RequestStateChange for 0 ('Completed with No Error') ou 4096 (0x1000) ('Job Started'). Consulte a descrição das **propriedades EnabledState** e **RequestedState** para ver as explicações detalhadas dos *valores RequestedState.*

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

Pode conter uma referência ao [**\_ ConcreteJob CIM**](cim-concretejob.md) criado para acompanhar a transição de estado iniciada pela invocação de método.

</dd> <dt>

*TimeoutPeriod* \[ Em\]
</dt> <dd>

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo estado leve. O formato de intervalo deve ser usado para especificar o TimeoutPeriod. Um valor de 0 ou um parâmetro nulo indica que o cliente não tem requisitos de tempo para a transição.

Se essa propriedade não contém 0 ou nulo e a implementação não dá suporte a esse parâmetro, um código de retorno de 'Uso do parâmetro de tempoout não suportado' deverá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna 0; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
</dt> </dl>

 

 




