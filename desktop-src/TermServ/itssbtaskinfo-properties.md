---
title: Propriedades de ITsSbTaskInfo
description: A interface ITsSbTaskInfo expõe as propriedades a seguir.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638496"
---
# <a name="itssbtaskinfo-properties"></a>Propriedades de ITsSbTaskInfo

A interface [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) expõe as propriedades a seguir.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**Propriedade de contexto**](itssbtaskinfo-context.md)
</dt> <dd>

Recupera os bytes de contexto associados à tarefa.

</dd> <dt>

[**Propriedade prazo**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Recupera a hora pela qual a tarefa deve ser iniciada. Isso é usado para priorizar patches. O patch com o prazo mais antigo será iniciado primeiro.

</dd> <dt>

[**Propriedade EndTime**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Recupera a hora mais recente em que o agente de tarefa pode iniciar a tarefa.

</dd> <dt>

[**Propriedade do identificador**](itssbtaskinfo-identifier.md)
</dt> <dd>

Recupera um GUID que é usado como um identificador exclusivo pelo agente de tarefa.

</dd> <dt>

[**Propriedade do rótulo**](itssbtaskinfo-label.md)
</dt> <dd>

Recupera o rótulo que descreve a finalidade da tarefa.

</dd> <dt>

[**Propriedade plugin**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Recupera o nome de exibição do agente de tarefa.

</dd> <dt>

[**Propriedade StartTime**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Recupera a hora mais antiga em que o agente de tarefa pode iniciar a tarefa.

</dd> <dt>

[**Propriedade de status**](itssbtaskinfo-status.md)
</dt> <dd>

Recupera um valor de enumeração de [**\_ \_ status da tarefa RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa o estado da tarefa.

</dd> <dt>

[**Propriedade TargetId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Recupera o identificador de destino.

</dd> </dl>

 

 




