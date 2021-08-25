---
description: Repositórios de política de autorização, aplicativos e escopos representam diferentes níveis de organização da política do Gerenciador de autorização.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Repositórios de política, aplicativos e escopos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db06b291ef81f391fed1a0094b73c9b31d0342f59bce22d93779c7bfa48a80b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907566"
---
# <a name="policy-stores-applications-and-scopes"></a>Repositórios de política, aplicativos e escopos

Repositórios de política de autorização, aplicativos e escopos representam diferentes níveis de organização da política do Gerenciador de autorização. Um repositório de políticas pode conter um ou mais aplicativos, e um aplicativo pode conter um ou mais escopos.

-   [Repositórios de política de autorização](#authorization-policy-stores)
-   [Aplicativos](#policy-stores-applications-and-scopes)
-   [Escopos](#policy-stores-applications-and-scopes)
-   [Delegação](#delegation)
-   [Tópicos relacionados](#related-topics)

## <a name="authorization-policy-stores"></a>Repositórios de política de autorização

Na API do Gerenciador de autorização, um repositório de política de autorização é representado por um objeto [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . O repositório de políticas de autorização contém definições e atribuições de aplicativos, escopos, operações, tarefas, funções e grupos de usuários.

Um repositório de diretivas de autorização pode ser armazenado como um arquivo XML ou em Active Directory.

Um aplicativo deve inicializar um repositório de política de autorização antes de alterar as informações na loja ou usar a política de armazenamento para verificar o acesso do cliente aos recursos.

Um repositório de diretivas de autorização pode conter um ou mais objetos [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que representam uma política de autorização para um aplicativo específico.

## <a name="applications"></a>Aplicativos

Na API do Gerenciador de autorização, um aplicativo é representado por um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) . Um repositório de diretivas de autorização pode conter informações de política de autorização para muitos aplicativos. O uso de objetos **IAzApplication** permite que você armazene diferentes políticas de autorização para diferentes aplicativos em um único repositório de políticas.

Um repositório de política de autorização deve conter pelo menos um aplicativo.

## <a name="scopes"></a>Escopos

Na API do Gerenciador de autorização, um escopo é representado por um objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) . Os escopos fornecem um nível opcional adicional de organização para uma política de autorização. Um aplicativo pode conter um ou mais escopos, mas não precisa conter nenhum (o Gerenciador de autorização fornece um escopo padrão de todo o aplicativo).

Um escopo é uma subdivisão em um aplicativo que separa recursos de outros recursos que são usados por esse aplicativo. Se você tiver grupos do Gerenciador de autorização, atribuições de função, definições de função ou definições de tarefa que não deseja aplicar a um aplicativo inteiro, poderá criá-los no nível de escopo.

## <a name="delegation"></a>Delegação

Os repositórios de diretiva de autorização armazenados no Active Directory dão suporte à delegação de administração. A administração pode ser delegada a usuários e grupos na loja, no aplicativo ou no nível de escopo. Cada nível define funções administrativas para a política nesse nível. Para delegar o controle a um usuário ou grupo, atribua-os à função de administrador; para permitir que um usuário ou grupo Leia a política, atribua-os à função leitor.

Os administradores de um repositório, aplicativo ou escopo podem ler e modificar o repositório de políticas no nível delegado. Os leitores podem ler o repositório de políticas no nível delegado, mas não podem modificar o repositório.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um objeto de repositório de política de autorização em C++](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[Criando um objeto de aplicativo em C++](creating-an-application-object-in-c--.md)
</dt> <dt>

[Delegando a definição de permissões em C++](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



