---
description: As nuvens, a fumaça e as trilhas de vapor podem ser criadas por uma extensão da técnica de mensagem.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Nuvens, fumaça e trilhas Vapors (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569697"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Nuvens, fumaça e trilhas Vapors (Direct3D 9)

As nuvens, a fumaça e as trilhas de vapor podem ser criadas por uma extensão da técnica de mensagem. Consulte a [mensagem (Direct3D 9)](billboarding.md). Ao girar o mural em dois eixos em vez de um, seu aplicativo pode permitir que o usuário exiba uma mensagem de qualquer ângulo. Normalmente, um aplicativo gira o mural nos eixos horizontal e vertical.

Para fazer uma nuvem simples, seu aplicativo pode girar um primitivo retangular em um ou dois eixos para que o primitivo gire o usuário. Uma textura semelhante à de nuvem pode ser aplicada ao primitivo com transparência. Para obter detalhes sobre como aplicar texturas transparentes a primitivos, consulte [mesclagem de textura (Direct3D 9)](texture-blending.md). Você pode animar a nuvem aplicando uma série de texturas ao longo do tempo.

Um aplicativo pode criar nuvens mais complexas formando-as a partir de um grupo de primitivos. Cada parte da nuvem é um primitivo retangular. Os primitivos podem ser movidos independentemente ao longo do tempo para dar a aparência de uma névoa dinâmica. A ilustração a seguir mostra esse conceito.

![ilustração de primitivos que formam nuvens mais complexas](images/cloud.png)

A aparência da fumaça é exibida de maneira semelhante às nuvens. Normalmente, ele requer vários murals, como nuvens complexas. A fumaça geralmente billows e aumenta com o tempo, portanto, os murals que compõem a fumaça Plume precisam se mover de acordo. Talvez seja necessário adicionar mais murals à medida que o Plume aumentar e dispersar.

Uma trilha de vapor é uma plume de fumaça que não aumenta. No entanto, como uma plume de fumaça, ela se espalha ao longo do tempo. A ilustração a seguir mostra a técnica de usar os murals para simular uma trilha de vapor.

![ilustração de murals que simulam uma trilha vapor](images/vapor.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos alfa](alpha-examples.md)
</dt> </dl>

 

 



