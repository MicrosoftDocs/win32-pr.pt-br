---
description: Um método para eliminar esse trabalho e todos os processos subjacentes e remover quaisquer associações de pendente. Esse método é preterido; Use RequestChangeState em vez disso.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Método KillJob da classe CIM_Job
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921543"
---
# <a name="killjob-method-of-the-cim_job-class"></a>Método KillJob da classe de \_ trabalho CIM

Um método para eliminar esse trabalho e quaisquer processos subjacentes e remover quaisquer associações ' pendente '. Esse método é preterido; Use **RequestChangeState** em vez disso. O **KillJob** está sendo preterido porque não há nenhuma distinção entre um desligamento ordenado e uma eliminação imediata. [**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() fornece as opções ' Terminate ' e ' Kill ' para permitir essa distinção.

## <a name="syntax"></a>Sintaxe


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DeleteOnKill* \[ no\]
</dt> <dd>

Indica se o trabalho deve ou não ser excluído automaticamente após o encerramento. Esse parâmetro tem precedência sobre a propriedade **DeleteOnCompletion** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Desconhecido** (2)
</dt> <dt>

**Tempo limite** (3)
</dt> <dt>

**Com falha** (4)
</dt> <dt>

**Acesso negado** (6)
</dt> <dt>

**Não encontrado** (7)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
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

[**Trabalho do CIM \_**](cim-job.md)
</dt> </dl>

 

 




