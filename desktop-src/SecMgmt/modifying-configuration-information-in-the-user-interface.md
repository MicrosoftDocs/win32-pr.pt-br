---
description: Uma extensão de snap-in de anexo deve permitir que o usuário modifique informações de configuração sobre o serviço.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modificando informações de configuração no Interface do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 414e2ab1475ec1c3241d60b96d182a522c299a9f5cf6134f50339c2088c99d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005114"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modificando informações de configuração no Interface do Usuário

Uma extensão de snap-in de anexo deve permitir que o usuário modifique informações de configuração sobre o serviço. As informações modificadas devem ser armazenadas pela extensão de snap-in de anexo até que o snap-in configuração de segurança chama métodos da interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para recuperar as informações.

Para evitar vazamentos de memória, a memória livre alocada pela extensão de snap-in chamando [**ISceSvcAttachmentPersistInfo::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



