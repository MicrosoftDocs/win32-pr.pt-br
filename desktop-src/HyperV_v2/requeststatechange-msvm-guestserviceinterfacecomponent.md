---
description: Solicita que o estado do componente de interface do serviço de convidado seja alterado para o valor especificado.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Método Msvm_GuestServiceInterfaceComponent:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759399"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a>\_Método Msvm GuestServiceInterfaceComponent:: RequestStateChange

Solicita que o estado do componente de interface do serviço de convidado seja alterado para o valor especificado.

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

*Requestedstate* \[ no\]
</dt> <dd>

Tipo: **UInt16**

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

Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Uma referência opcional a um objeto [**Msvm \_ ConcreteJob**](msvm-concretejob.md) que é retornado se a operação é executada de forma assíncrona. Se estiver presente, a referência retornada poderá ser usada para monitorar o progresso e obter o resultado do método.

</dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

Tipo: **DateTime**

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha. O formato do intervalo deve ser usado para especificar o período de tempo limite. Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retorna um dos valores a seguir.



| Código/valor de retorno                                                                                                                                                                       | Descrição         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>                           | Êxito.<br/> |
| <dl> <dt>**Sem suporte**</dt> <dt>1</dt> </dl>                                     |                     |
| <dl> <dt>**Erro desconhecido/não especificado**</dt> <dt>2</dt> </dl>                         |                     |
| <dl> <dt>**Não é possível concluir dentro do período de tempo limite**</dt> <dt>3</dt> </dl>            |                     |
| <dl> <dt>**Com falha**</dt> <dt>4</dt> </dl>                                            |                     |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>5</dt> </dl>                                 |                     |
| <dl> <dt>**Em uso**</dt> <dt>6</dt> </dl>                                            |                     |
| <dl> <dt>**DMTF reservado**</dt> <dt>..</dt> </dl>                                    |                     |
| <dl> <dt>**Parâmetros de método verificados-transição iniciada**</dt> <dt>4096</dt> </dl> |                     |
| <dl> <dt>**Transição de estado inválida**</dt> <dt>4097</dt> </dl>                       |                     |
| <dl> <dt>**Uso do parâmetro timeout sem suporte**</dt> <dt>4098</dt> </dl>         |                     |
| <dl> <dt>**Ocupado**</dt> em <dt>4099</dt> </dl>                                           |                     |
| <dl> <dt>**Método reservado**</dt> <dt>4100.. 32767</dt> </dl>                         |                     |
| <dl> 32768 <dt>**específicos do fornecedor**</dt> <dt>. 65535</dt> </dl>                        |                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

