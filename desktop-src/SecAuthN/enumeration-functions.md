---
description: Se o seu provedor de rede precisar dar suporte à navegação de seus recursos de rede, ele deverá implementar as funções a seguir. O MPR chama essas funções para enumerar os recursos.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Funções de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010430"
---
# <a name="enumeration-functions"></a>Funções de enumeração

Se o seu provedor de rede precisar dar suporte à navegação de seus recursos de rede, ele deverá implementar as funções a seguir. O MPR chama essas funções para enumerar os recursos.

Um provedor de rede não é necessário para implementar nenhuma das funções de enumeração. No entanto, se um provedor de rede implementar [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)ou [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), ele também deverá implementar as outras duas funções de enumeração.



| Função                                                     | Descrição                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | Abre uma enumeração de recursos de rede ou conexões existentes.                                                                                                  |
| [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | Executa uma enumeração em um identificador retornado por [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).                                                                                   |
| [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | Fecha uma enumeração.                                                                                                                                              |
| [**NPGetResourceInformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | Determina se o provedor é o provedor correto para responder a uma solicitação de um recurso de rede especificado e retorna informações sobre o tipo do recurso. |
| [**NPGetResourceParent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | Retorna o pai de um recurso de rede especificado na hierarquia de procura.                                                                                         |



 

 

 



