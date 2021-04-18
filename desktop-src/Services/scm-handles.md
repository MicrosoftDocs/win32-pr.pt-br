---
description: O SCM dá suporte a tipos de identificadores para permitir o acesso aos objetos a seguir.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Identificadores SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749452"
---
# <a name="scm-handles"></a>Identificadores SCM

O SCM dá suporte a tipos de identificadores para permitir o acesso aos objetos a seguir.

-   O banco de dados dos serviços instalados.
-   Um serviço.
-   O bloqueio do banco de dados.

Um objeto SCManager representa o banco de dados dos serviços instalados. É um objeto de contêiner que mantém objetos de serviço. A função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) retorna um identificador para um objeto SCManager em um computador especificado. Esse identificador é usado ao instalar, excluir, abrir e enumerar serviços e ao bloquear o banco de dados de serviços.

Um objeto de serviço representa um serviço instalado. As funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) retornam identificadores para os serviços instalados.

As funções [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)e [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) podem solicitar tipos diferentes de acesso a SCManager e a objetos de serviço. O acesso solicitado é concedido ou negado, dependendo do token de acesso do processo de chamada e do descritor de segurança associado ao objeto SCManager ou Service.

A função [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) fecha identificadores para SCManager e objetos de serviço. Quando você não precisar mais desses identificadores, não deixe de fechá-los.

 

 



