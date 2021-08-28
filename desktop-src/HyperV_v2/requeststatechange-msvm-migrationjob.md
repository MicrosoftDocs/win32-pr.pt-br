---
description: Solicita que o estado do trabalho de migração seja alterado para o estado especificado.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Método RequestStateChange da classe Msvm_MigrationJob classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a7a5934049860e92aa9986a301fe3d75bed8022bda064653ee9e405ad16f6619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014314"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a>Método RequestStateChange da classe Msvm \_ MigrationJob

Solicita que o estado do trabalho de migração seja alterado para o estado especificado. Invocar o método **RequestStateChange** várias vezes pode resultar em solicitações anteriores sendo substituídas ou perdidas. Se 0 for retornado, a tarefa será concluída com êxito. Qualquer outro código de retorno indica uma condição de erro.

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

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo estado leve. O formato de intervalo deve ser usado para especificar o período de tempo." Um valor de 0 ou **Null** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contém 0 ou **Null** e a implementação não dá suporte a esse parâmetro, um código de retorno de 4098 (Uso do parâmetro de tempoout sem suporte) deve ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

<dl> <dt>

  acima (0)
</dt> <dt>

 (32768)
</dt> <dt>

 (32769)
</dt> <dt>

 (32770)
</dt> <dt>

 (32771)
</dt> <dt>

 (32772)
</dt> <dt>

 (32773)
</dt> <dt>

 (32774)
</dt> <dt>

 (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> </dl>

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

[**Msvm \_ MigrationJob**](msvm-migrationjob.md)
</dt> </dl>

 

 




