---
title: Contenção/delegação
description: O mecanismo mais comum para reutilização de objeto em COM é contenção/delegação.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292778"
---
# <a name="containmentdelegation"></a>Contenção/delegação

O mecanismo mais comum para reutilização de objeto em COM é *contenção/delegação*. Esse tipo de reutilização é um conceito familiar encontrado na maioria das linguagens e sistemas orientados a objetos. O objeto externo, que precisa fazer uso do objeto interno, atua como um cliente de objeto para o objeto interno. O objeto externo "contém" o objeto interno e, quando o objeto externo requer os serviços do objeto interno, o objeto externo delega a implementação explicitamente para os métodos do objeto interno. Ou seja, o objeto externo usa os serviços do objeto interno para implementar a si mesmo.

Não é necessário que os objetos externos e internos ofereçam suporte às mesmas interfaces, embora certamente seja razoável conter um objeto que implemente uma interface que o objeto externo não e implemente os métodos do objeto externo simplesmente como chamadas para os métodos correspondentes no objeto interno. No entanto, quando a complexidade dos objetos externos e internos difere muito, o objeto externo pode implementar alguns dos métodos de suas interfaces delegando chamadas para métodos de interface implementados no objeto interno.

É simples implementar a contenção de um objeto externo. O objeto externo cria os objetos internos que ele precisa para usar como faria com qualquer outro cliente. Isso não é nada novo – o processo é como um objeto C++ que, por sua vez, contém um objeto de cadeia de caracteres C++ que ele usa para executar determinadas funções de cadeia de caracteres, mesmo que o objeto externo não seja considerado um objeto de cadeia de caracteres em seu próprio direito. Em seguida, usando seu ponteiro para o objeto interno, uma chamada para um método no objeto externo gera uma chamada para um método de objeto interno.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agregação](aggregation.md)
</dt> </dl>

 

 




