---
title: Interfaces QMGR
description: Use as seguintes interfaces do Gerenciador de filas (QMGR) para baixar arquivos e monitorar trabalhos na fila de download.
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17bd3c27fad81416b916b52b055bc879b44f251113d43b6118e179b609762fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679990"
---
# <a name="qmgr-interfaces"></a>Interfaces QMGR

\[As interfaces do Gerenciador de filas (QMGR) estão disponíveis para uso nos sistemas operacionais especificados na seção requisitos de um tópico. Eles podem ter sido alterados ou não estarem disponíveis em versões subsequentes. Em vez disso, use as [interfaces bits](bits-interfaces.md).\]

Use as seguintes interfaces do Gerenciador de filas (QMGR) para baixar arquivos e monitorar trabalhos na fila de download.



| Interface                                                                 | Descrição                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | Implemente para receber notificações quando ocorrerem eventos.<br/>                                                                                               |
| [**IBackgroundCopyGroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | Use o para gerenciar o grupo. Por exemplo, adicione um trabalho ao grupo, defina as propriedades do grupo e inicie e interrompa o grupo na fila de download.<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | Use para adicionar arquivos ao trabalho e recuperar o status do trabalho.<br/>                                                                                         |
| [**IBackgroundCopyQMgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | Use para criar um novo grupo, recuperar um grupo existente ou enumerar todos os grupos na fila.<br/>                                                       |
| [**IEnumBackgroundCopyGroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | Use para recuperar uma lista de grupos na fila de download.<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | Use para recuperar uma lista de trabalhos no grupo.<br/>                                                                                                       |



 

 

 





