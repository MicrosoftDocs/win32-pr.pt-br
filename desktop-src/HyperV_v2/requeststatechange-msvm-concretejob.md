---
description: Solicita que o estado do trabalho seja alterado para o estado especificado.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Método RequestStateChange da classe Msvm_ConcreteJob classe
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
ms.openlocfilehash: 579ad52bd83bd43dc3071f704914eb7b5f9cae4f0be89f018e56b9608b1c12be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501126"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>Método RequestStateChange da classe Msvm \_ ConcreteJob

Solicita que o estado do trabalho seja alterado para o estado especificado. Invocar o método **RequestStateChange** várias vezes pode resultar em solicitações anteriores sendo substituídas ou perdidas. Se 0 for retornado, a tarefa será concluída com êxito. Qualquer outro código de retorno indica uma condição de erro.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RequestedState* \[ Em\]
</dt> <dd>

Tipo: **uint16**

O novo estado de um trabalho.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Iniciar** (2)


</dt> <dd>

Altera o estado para "Em execução".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)


</dt> <dd>

Interrompe o trabalho temporariamente. A intenção é reiniciar o trabalho posteriormente com "Iniciar". Pode ser possível inserir o estado "Serviço" enquanto suspenso. (Isso é específico do trabalho.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Encerrar** (4)


</dt> <dd>

Interrompe o trabalho corretamente, salvando dados, preservando o estado e desligando todos os processos subjacentes de maneira organizada.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)


</dt> <dd>

Coloca o trabalho em um estado de serviço específico do fornecedor. Talvez seja possível reiniciar o trabalho.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado**


</dt> <dd>

Reservado.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor Reservado**


</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ Em\]
</dt> <dd>

Tipo: **datetime**

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo estado leve. O formato de intervalo deve ser usado para especificar o período de tempo." Um valor de 0 ou **Null** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contém 0 ou **Null** e a implementação não dá suporte a esse parâmetro, um código de retorno de 4098 (Uso do parâmetro de tempoout sem suporte) deve ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Erro desconhecido/não especificado** (2)
</dt> <dt>

**Não é possível concluir dentro do período de tempo** (3)
</dt> <dt>

**Falha** (4)
</dt> <dt>

**Parâmetro inválido** (5)
</dt> <dt>

**Em uso** (6)
</dt> <dt>

**DMTF Reservado** (7 4095)
</dt> <dt>

**Parâmetros de método verificados – Transição iniciada** (4096)
</dt> <dt>

**Transição de estado inválida** (4097)
</dt> <dt>

**Uso do parâmetro timeout sem suporte** (4098)
</dt> <dt>

**Ocupado** (4099)
</dt> <dt>

**Método Reservado** (4100 32767)
</dt> <dt>

**Específico do** fornecedor (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à [**classe Msvm \_ ConcreteJob**](msvm-concretejob.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

