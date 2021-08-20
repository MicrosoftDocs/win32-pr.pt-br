---
description: Antes de poder enfileirar as operações de arquivo, você deve abrir uma fila de arquivos. Chamar a função SetupOpenFileQueue retorna um identificador para um arquivo de fila. Esse identificador é usado pelas funções de fila subsequentes para fazer referência à fila aberta e adicionar operações a ela ou examiná-las.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Abrindo e fechando uma fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8465446842521adbd320816a76d7f545819eebf68b55aee0c3a057fc0ca3ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965149"
---
# <a name="opening-and-closing-a-queue"></a>Abrindo e fechando uma fila

Antes de poder enfileirar as operações de arquivo, você deve abrir uma fila de arquivos. Chamar a função [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) retorna um identificador para um arquivo de fila. Esse identificador é usado pelas funções de fila subsequentes para fazer referência à fila aberta e adicionar operações a ela ou examiná-las.

Depois que todas as operações de arquivo especificadas tiverem sido enfileiradas e confirmadas, você deverá chamar a função [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) para liberar recursos alocados durante a chamada para [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).

> [!Note]  
> A função [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) não confirma a fila de arquivos. Todas as operações que não forem confirmadas quando **SetupCloseFileQueue** for chamado não serão executadas.

 

 

 



