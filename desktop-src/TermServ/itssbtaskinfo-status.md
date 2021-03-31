---
title: Propriedade de status ITsSbTaskInfo
description: Recupera um \_ \_ valor de enumeração de status da tarefa RDV que representa o estado da tarefa.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de status
- Propriedade de status Serviços de Área de Trabalho Remota, interface ITsSbTaskInfo
- Serviços de Área de Trabalho Remota de interface ITsSbTaskInfo, Propriedade status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644602"
---
# <a name="itssbtaskinfostatus-property"></a>Propriedade ITsSbTaskInfo:: status

Recupera um valor de enumeração de [**\_ \_ status da tarefa RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa o estado da tarefa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a>Valor da propriedade

Um valor de enumeração de [**\_ \_ status da tarefa RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa o estado da tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| INSERI<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





