---
description: Uma extensão de snap-in de anexo deve permitir que o usuário modifique as informações de configuração sobre o serviço.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modificando informações de configuração na interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6158d76d0f5114bd2d7b483e0af3d00f8f2439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811784"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modificando informações de configuração na interface do usuário

Uma extensão de snap-in de anexo deve permitir que o usuário modifique as informações de configuração sobre o serviço. As informações modificadas devem ser armazenadas pela extensão de snap-in de anexo até que o snap-in de configuração de segurança chame os métodos da interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para recuperar as informações.

Para evitar vazamentos de memória, memória livre alocada pela extensão do snap-in chamando [**ISceSvcAttachmentPersistInfo:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



