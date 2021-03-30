---
title: Criando um manipulador de arquivo ou de fluxo
description: Criando um manipulador de arquivo ou de fluxo
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005383"
---
# <a name="creating-a-file-or-stream-handler"></a>Criando um manipulador de arquivo ou de fluxo

Em um aplicativo escrito na linguagem de programação C, um manipulador de arquivo ou fluxo geralmente cria uma função para cada método. Seu aplicativo acessa essas funções por meio de uma matriz de ponteiros de função que o manipulador de fluxo cria. Uma estrutura **IAVIStreamVtbl** contém a matriz de ponteiros de função. Um manipulador de fluxo pode atribuir qualquer nome que desejar para funções que ele cria para os métodos. A posição do ponteiro de função na estrutura implica a correspondência da função para o método. Por exemplo, o primeiro ponteiro de função na estrutura corresponde ao método **QueryInterface** . Seu manipulador de fluxo deve fornecer todas as funções de uma interface.

 

 




