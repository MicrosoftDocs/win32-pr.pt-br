---
description: Solicita que o estado do trabalho seja alterado para o estado especificado.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Método RequestStateChange da classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768501"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>Método RequestStateChange da classe Msvm \_ ConcreteJob

Solicita que o estado do trabalho seja alterado para o estado especificado. Invocar o método **RequestStateChange** várias vezes pode fazer com que as solicitações anteriores sejam substituídas ou perdidas. Se 0 for retornado, a tarefa será concluída com êxito. Qualquer outro código de retorno indica uma condição de erro.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Requestedstate* \[ no\]
</dt> <dd>

Tipo: **UInt16**

O novo estado de um trabalho.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)


</dt> <dd>

Altera o estado para "em execução".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)


</dt> <dd>

Interrompe o trabalho temporariamente. A intenção é reiniciar subsequentemente o trabalho com "Start". Pode ser possível inserir o estado "serviço" ao ser suspenso. (Isso é específico do trabalho.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)


</dt> <dd>

Interrompe o trabalho corretamente, salvando os dados, preservando o estado e desligando todos os processos subjacentes de maneira ordenada.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)


</dt> <dd>

Coloca o trabalho em um estado de serviço específico do fornecedor. Pode ser possível reiniciar o trabalho.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado**


</dt> <dd>

Reservado.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado**


</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

Tipo: **DateTime**

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha. O formato do intervalo deve ser usado para especificar o período de tempo limite. Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (uso do parâmetro timeout sem suporte) deverá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Erro desconhecido/não especificado** (2)
</dt> <dt>

**Não é possível concluir dentro do período de tempo limite** (3)
</dt> <dt>

**Com falha** (4)
</dt> <dt>

**Parâmetro inválido** (5)
</dt> <dt>

**Em uso** (6)
</dt> <dt>

**DMTF reservado** (7 4095)
</dt> <dt>

**Parâmetros de método verificados-transição iniciada** (4096)
</dt> <dt>

**Transição de estado inválida** (4097)
</dt> <dt>

**Não há suporte para o uso do parâmetro timeout** (4098)
</dt> <dt>

**Ocupado** (4099)
</dt> <dt>

**Método reservado** (4100 32767)
</dt> <dt>

**Específico do fornecedor** (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe [**Msvm \_ ConcreteJob**](msvm-concretejob.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

