---
description: Sua extensão de snap-in deve exibir as informações atuais de configuração e análise para os usuários.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Exibindo informações de configuração e análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784134"
---
# <a name="displaying-configuration-and-analysis-information"></a>Exibindo informações de configuração e análise

Sua extensão de snap-in deve exibir as informações atuais de configuração e análise para os usuários.

Para exibir informações, o nó de extensão de snap-in de anexos deve estender os snap-ins de configuração de segurança usando o nó serviços. O nó serviços é o snap-in do MMC que administra os serviços instalados no sistema.

Os tipos de nó que podem ser estendidos são os seguintes:

-   NodeType dos serviços de configuração = {24a7f717-1f0c-11D1-affb-00C04FB984F9}
-   Nó de serviços de inspeção = {678050c7-1ff8-11D1-affb-00C04FB984F9}

Quando o nó serviços é expandido, o MMC notifica todas as extensões de snap-in registradas. Cada snap-in de anexo deve se inserir no nó serviços e executar as seguintes tarefas:

-   Chame **QueryInterface** para obter um ponteiro para a interface [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) exposta pelos snap-ins de configuração de segurança.
-   Chame [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para informar os snap-ins de configuração de segurança que a extensão do snap-in está carregada e para estabelecer um contexto para comunicações.
-   Chame [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) para recuperar as informações de configuração do banco de dados. Essa etapa pode ser executada quando a extensão do snap-in é inicializada ou quando o usuário abre seu nó.

Para obter mais informações, consulte [adicionando um nó de extensão de snap-in de anexo](adding-an-attachment-snap-in-extension-node.md).

 

 



