---
description: No Direct3D 10, os recursos de textura são acessados com uma exibição, que é um mecanismo para a interpretação de hardware de um recurso na memória.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Exibições de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc420e39c4d577947cae657f3296b15f0052db9e823e07d3a3ba1ccb641fb6b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101333"
---
# <a name="texture-views-direct3d-10"></a>Exibições de textura (Direct3D 10)

No Direct3D 10, os recursos de textura são acessados com uma exibição, que é um mecanismo para a interpretação de hardware de um recurso na memória. Um modo de exibição permite que um estágio de pipeline específico acesse somente os [sub-recursos](d3d10-graphics-programming-guide-resources-types.md) de que precisa, na representação desejada pelo app.

Uma exibição dá suporte à noção de um recurso sem tipo. Um recurso sem tipo é um recurso criado com um tamanho específico, mas não um tipo de dados específico. Os dados são interpretados dinamicamente quando são associados ao pipeline.

A ilustração a seguir mostra um exemplo de associação de uma matriz de texturas 2D a 6 texturas como um recurso sombreador, criando uma exibição de recurso sombreador para isso. Em seguida, o recurso é tratado como uma matriz de texturas. (Observação: um sub-recurso não pode ser associado como entrada e saída ao pipeline simultaneamente.)

![ilustração de uma matriz com seis texturas](images/d3d10-cube-texture-faces.png)

Ao usar uma matriz de texturas 2D como destino de renderização, o recurso pode ser exibido como uma matriz de texturas 2D (6 neste exemplo) com níveis de mipmap (3 neste exemplo).

Crie um objeto de exibição para um destino de renderização chamando CreateRenderTargetView. Em seguida, chame OMSetRenderTargets para definir a exibição do destino de renderização para o pipeline. Renderize os destinos de renderização chamando Draw e usando RenderTargetArrayIndex para indexar à textura adequada na matriz. Você pode usar um sub-recurso (uma combinação de nível de mipmap e índice de matriz) para associar a qualquer matriz de sub-recursos. Você pode associar o segundo nível de mipmap e só atualizar esse nível de mipmap específico se quiser, como na ilustração a seguir.

![ilustração de associação somente ao segundo nível de mipmap de uma matriz de texturas](images/d3d10-cube-texture-faces-subresource.png)



Diferenças entre o Direct3D 9 e o Direct3D 10:

- No Direct3D 10, você não associa mais um recurso diretamente ao pipeline, cria uma exibição de um recurso e, em seguida, define a exibição para o pipeline. Isso permite que a validação e o mapeamento no tempo de execução e o driver ocorram na criação da exibição, minimizando a verificação de tipo no momento da associação.



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




