---
description: O método RequestStateChange da classe Msvm_StorageJob-solicita uma alteração de estado.
ms.assetid: 2960bc44-f2af-49c6-9c33-5d9e1ad8056c
title: Método RequestStateChange da classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e15f28af892e713f8bd6897b2d75b6b227886ad1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111344"
---
# <a name="requeststatechange-method-of-the-msvm_storagejob-class"></a>Método RequestStateChange da classe Msvm \_ StorageJob

Solicita uma alteração de estado.

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

RequestStateChange altera o estado de um trabalho. Os valores possíveis são os seguintes:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)


</dt> <dd>

Altera o estado para ' running '.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)


</dt> <dd>

Interrompe o trabalho temporariamente. A intenção é reiniciar subsequentemente o trabalho com ' Start '. Pode ser possível inserir o estado ' serviço ' ao ser suspenso. (Isso é específico do trabalho.)

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)


</dt> <dd>

Interrompe o trabalho corretamente, salva os dados, preserva o estado e desliga todos os processos subjacentes de maneira ordenada.

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

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha. O formato do intervalo deve ser usado para especificar o período de tempo limite. Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

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
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Msvm \_ StorageJob**](msvm-storagejob.md)
</dt> </dl>

 

 




