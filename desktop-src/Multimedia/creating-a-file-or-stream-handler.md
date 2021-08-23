---
title: Criando um manipulador de arquivos ou fluxos
description: Criando um manipulador de arquivos ou fluxos
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6732c572e390f3401f6e0472659bec7c522189b357b04d8ef7def20a7d9519b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785786"
---
# <a name="creating-a-file-or-stream-handler"></a>Criando um manipulador de arquivos ou fluxos

Em um aplicativo escrito na linguagem de programação C, um manipulador de arquivo ou fluxo geralmente cria uma função para cada método. Seu aplicativo acessa essas funções por meio de uma matriz de ponteiros de função que o manipulador de fluxo cria. Uma **estrutura IAVIStreamVtbl** contém a matriz de ponteiros de função. Um manipulador de fluxo pode atribuir qualquer nome que queira para funções que ele cria para os métodos. A posição do ponteiro de função na estrutura implica a correspondência da função com o método . Por exemplo, o primeiro ponteiro de função na estrutura corresponde ao **método QueryInterface.** O manipulador de fluxo deve fornecer todas as funções de uma interface.

 

 




