---
title: Propriedades de ITsSbTaskInfo
description: A interface ITsSbTaskInfo expõe as propriedades a seguir.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d91b24b95b6b19cb439350c0c6823306c66a8fab5fe47f0f9e9fb739df64e3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128060"
---
# <a name="itssbtaskinfo-properties"></a>Propriedades de ITsSbTaskInfo

A interface [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) expõe as propriedades a seguir.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**Propriedade context**](itssbtaskinfo-context.md)
</dt> <dd>

Recupera os bytes de contexto associados à tarefa.

</dd> <dt>

[**Propriedade Deadline**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
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

[**Propriedade Label**](itssbtaskinfo-label.md)
</dt> <dd>

Recupera o rótulo que descreve a finalidade da tarefa.

</dd> <dt>

[**Propriedade do plug-in**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Recupera o nome de exibição do agente de tarefa.

</dd> <dt>

[**Propriedade StartTime**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Recupera a primeira vez que o agente de tarefa pode iniciar a tarefa.

</dd> <dt>

[**Propriedade Status**](itssbtaskinfo-status.md)
</dt> <dd>

Recupera um valor [**de enumeração \_ \_ STATUS da TAREFA RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa o estado da tarefa.

</dd> <dt>

[**Propriedade TargetId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Recupera o identificador de destino.

</dd> </dl>

 

 




