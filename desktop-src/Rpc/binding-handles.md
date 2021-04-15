---
title: Identificadores de associação
description: A associação é o processo de criação de uma conexão lógica entre um programa cliente e um programa de servidor. As informações que compõem a associação entre o cliente e o servidor são representadas por uma estrutura chamada identificador de associação.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499064"
---
# <a name="binding-handles"></a>Identificadores de associação

A associação é o processo de criação de uma conexão lógica entre um programa cliente e um programa de servidor. As informações que compõem a associação entre o cliente e o servidor são representadas por uma estrutura chamada identificador de associação.

Um identificador de associação é análogo a um identificador de arquivo que a função de biblioteca de tempo de execução fopen C retorna, ou um identificador de janela que a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) retorna.

Assim como acontece com esses identificadores, seu aplicativo não pode acessar e manipular diretamente as informações no identificador de associação. As informações em uma estrutura de dados de identificador de associação estão disponíveis somente para as bibliotecas de tempo de execução RPC. Você fornece o identificador, as bibliotecas de tempo de execução acessam e manipulam os dados apropriados.

Esta seção apresenta uma discussão sobre identificadores de associação nos seguintes tópicos:

-   [Tipos de identificadores de associação](types-of-binding-handles.md)
-   [Associação do lado do cliente](client-side-binding.md)
-   [Associação do lado do servidor](server-side-binding.md)
-   [Identificadores totalmente e parcialmente ligados](fully-and-partially-bound-handles.md)
-   [Interpretando informações de associação](interpreting-binding-information.md)
-   [Extensões de Binding-Handle RPC da Microsoft](microsoft-rpc-binding-handle-extensions.md)
-   [Funções de identificador de associação](binding-handle-functions.md)
-   [O banco de dados do serviço de nome RPC](the-rpc-name-service-database.md)

 

 