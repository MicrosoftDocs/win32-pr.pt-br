---
title: Alças de associação
description: Associação é o processo de criação de uma conexão lógica entre um programa cliente e um programa de servidor. As informações que compõem a associação entre o cliente e o servidor são representadas por uma estrutura chamada de alça de associação.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09eae434fde790531a6f723cab6dc0b0613ee2fc99d680478d697cb550d6a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932336"
---
# <a name="binding-handles"></a>Alças de associação

Associação é o processo de criação de uma conexão lógica entre um programa cliente e um programa de servidor. As informações que compõem a associação entre o cliente e o servidor são representadas por uma estrutura chamada de alça de associação.

Um alça de associação é análogo a um alça de arquivo que a função de biblioteca em tempo de executar fopen C retorna ou a um alça de janela que a [**função CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) retorna.

Assim como com esses alças, seu aplicativo não pode acessar e manipular diretamente as informações no alça de associação. As informações em uma estrutura de dados de alça de associação estão disponíveis apenas para as bibliotecas de tempo de executar RPC. Você fornece o handle, as bibliotecas de tempo de run time acessam e manipulam os dados apropriados.

Esta seção apresenta uma discussão sobre os alças de associação nos tópicos a seguir:

-   [Tipos de alças de associação](types-of-binding-handles.md)
-   [Associação do lado do cliente](client-side-binding.md)
-   [Associação do lado do servidor](server-side-binding.md)
-   [Alças totalmente e parcialmente vinculadas](fully-and-partially-bound-handles.md)
-   [Interpretando informações de associação](interpreting-binding-information.md)
-   [Extensões de Binding-Handle RPC da Microsoft](microsoft-rpc-binding-handle-extensions.md)
-   [Funções de alça de associação](binding-handle-functions.md)
-   [O banco de dados do serviço de nome RPC](the-rpc-name-service-database.md)

 

 