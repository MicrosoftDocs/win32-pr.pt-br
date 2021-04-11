---
title: Contextos de renderização
description: Um contexto de renderização OpenGL é uma porta pela qual todos os comandos OpenGL são aprovados. Cada thread que faz chamadas OpenGL deve ter um contexto de renderização atual. Os contextos de renderização vinculam OpenGL aos sistemas de janelas do Windows.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL no Windows, contextos de renderização
- contextos de renderização OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac2ac6c5948da2b7372d600377666cd9e4e074
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292435"
---
# <a name="rendering-contexts"></a>Contextos de renderização

Um *contexto de renderização* OpenGL é uma porta pela qual todos os comandos OpenGL são aprovados. Cada thread que faz chamadas OpenGL deve ter um contexto de renderização atual. Os contextos de renderização vinculam OpenGL aos sistemas de janelas do Windows.

Um aplicativo especifica um contexto de dispositivo do Windows quando ele cria um contexto de renderização. Esse contexto de renderização é adequado para desenhar no dispositivo referenciado pelo contexto do dispositivo especificado. Em particular, o contexto de renderização tem o mesmo formato de pixel que o contexto do dispositivo. Para obter mais informações, consulte [processando funções de contexto](rendering-context-functions.md).

Apesar dessa relação, um contexto de renderização não é o mesmo que um contexto de dispositivo. Um contexto de dispositivo contém informações pertinentes ao componente de gráficos (GDI) do Windows. Um contexto de renderização contém informações pertinentes ao OpenGL. Um contexto de dispositivo deve ser especificado explicitamente em uma chamada GDI. Um contexto de renderização é implícito em uma chamada OpenGL. Você deve definir o formato de pixel de um contexto de dispositivo antes de criar um contexto de renderização.

Um thread que faz chamadas OpenGL deve ter um contexto de renderização atual. Se um aplicativo fizer chamadas OpenGL de um thread que não tem um contexto de renderização atual, nada acontecerá; a chamada não tem nenhum efeito. Um aplicativo normalmente cria um contexto de renderização, define-o como o contexto de renderização atual de um thread e, em seguida, chama as funções OpenGL. Quando termina de chamar as funções OpenGL, o aplicativo separa o contexto de renderização do thread e, em seguida, exclui o contexto de renderização. Uma janela pode ter vários contextos de renderização desenhando ao mesmo tempo, mas um thread pode ter apenas um contexto de renderização ativo atual.

Um contexto de renderização atual tem um contexto de dispositivo associado. Esse contexto de dispositivo não precisa ser o mesmo contexto de dispositivo usado quando o contexto de renderização foi criado, mas ele deve referenciar o mesmo dispositivo e ter o mesmo formato de pixel.

Um thread pode ter apenas um contexto de renderização atual. Um contexto de renderização pode ser atual para apenas um thread.

 

 




