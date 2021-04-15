---
description: Antes de poder enfileirar as operações de arquivo, você deve abrir uma fila de arquivos. Chamar a função SetupOpenFileQueue retorna um identificador para um arquivo de fila. Esse identificador é usado pelas funções de fila subsequentes para fazer referência à fila aberta e adicionar operações a ela ou examiná-las.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Abrindo e fechando uma fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753918"
---
# <a name="opening-and-closing-a-queue"></a>Abrindo e fechando uma fila

Antes de poder enfileirar as operações de arquivo, você deve abrir uma fila de arquivos. Chamar a função [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) retorna um identificador para um arquivo de fila. Esse identificador é usado pelas funções de fila subsequentes para fazer referência à fila aberta e adicionar operações a ela ou examiná-las.

Depois que todas as operações de arquivo especificadas tiverem sido enfileiradas e confirmadas, você deverá chamar a função [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) para liberar recursos alocados durante a chamada para [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).

> [!Note]  
> A função [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) não confirma a fila de arquivos. Todas as operações que não forem confirmadas quando **SetupCloseFileQueue** for chamado não serão executadas.

 

 

 



