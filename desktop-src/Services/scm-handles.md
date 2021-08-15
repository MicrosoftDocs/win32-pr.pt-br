---
description: O SCM dá suporte a tipos de identificadores para permitir o acesso aos objetos a seguir.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Identificadores SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6830063e57b2135c32bf01b4fdc0b4cf6207de32198d9f88d97667f4b403fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889184"
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

 

 



