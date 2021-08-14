---
title: Clonando um efeito
description: A clonagem de um efeito cria uma segunda cópia praticamente idêntica do efeito.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195b4e9a42e595558acc4c512f8662c11b2acde7873e123b242ee272eeea7e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538000"
---
# <a name="cloning-an-effect"></a>Clonando um efeito

A clonagem de um efeito cria uma segunda cópia praticamente idêntica do efeito. Consulte o único qualificador a seguir para obter uma explicação de por que não é exato. Uma segunda cópia de um efeito é útil quando um deseja usar a estrutura de efeitos em vários threads, pois o tempo de execução do efeito não é thread-safe para manter o alto desempenho.

Como os contextos de dispositivo também são não-seguros, threads diferentes devem passar contextos de dispositivo diferentes para o método ID3DX11EffectPass:: apply.

Um efeito pode ser clonado com a seguinte sintaxe:


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



No exemplo acima, a cópia clonada encapsulará o mesmo estado que o efeito original, independentemente de qual estado o efeito original está. Especialmente:

1.  Se pEffect for otimizado, o efeito de pCloned será otimizado
2.  Se pEffect tiver algumas variáveis gerenciadas pelo usuário, o efeito de pCloned terá as mesmas variáveis gerenciadas pelo usuário (consulte a descrição única abaixo)
3.  Todas as atualizações de variáveis pendentes (até que uma chamada de aplicação atualiza o estado do dispositivo) em pEffect estarão pendentes em pClonedEffect

Os seguintes objetos de dispositivo do Direct3D 11 são imutáveis ou nunca são atualizados pela estrutura de efeitos, portanto, o efeito clonado apontará para os mesmos objetos que o efeito original:

1.  Objetos de bloco de estado (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Sombreadores
3.  Instâncias de classe
4.  Texturas (não incluindo buffers de textura)
5.  Exibições de acesso não ordenado

Os seguintes objetos de dispositivo do Direct3D 11 são imutáveis e modificados pelo tempo de execução de efeito (a menos que seja gerenciado pelo usuário ou único em um efeito clonado); novas cópias desses objetos são criadas quando não único:

1.  Buffers de constantes
2.  Buffers de textura

## <a name="single-constant-buffers-and-texture-buffers"></a>Buffers de única constante e buffers de textura

Observe que essa discussão se aplica a buffers de constante e texturas, mas os buffers de constante são assumidos para facilitar a leitura.

Pode haver casos em que um buffer de constante é atualizado apenas por um thread, mas o estado do dispositivo definido por efeitos clonados usará esses dados. Por exemplo, o efeito principal pode atualizar o mundo e exibir matrizes que são referenciadas de sombreadores em efeitos clonados que não alteram o mundo e exibem matrizes. Nesses casos, os efeitos clonados precisam fazer referência ao buffer de constantes atual em vez de recriar um.

Há duas maneiras de atingir esse resultado desejado:

1.  Use ID3DX11EffectConstantBuffer:: SetConstantBuffer no efeito clonado para torná-lo gerenciado pelo usuário
2.  Marcar o buffer de constantes como "único" no código HLSL, forçando o tempo de execução de efeito a tratar é como gerenciado pelo usuário após a clonagem

Há duas diferenças entre os dois métodos acima. Primeiro, no método 1, um novo ID3D11Buffer será criado e o usuário antes de SetConstantBuffer é chamado. Além disso, depois de chamar UndoSetConstantBuffer no efeito clonado, a variável no método 1will aponta para o buffer recém-criado (que os efeitos serão atualizados quando aplicados), enquanto a variável no método 2 continuará a apontar para o buffer original (não atualizá-lo na aplicação).

Consulte o exemplo a seguir em HLSL:


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



Durante a clonagem, o efeito clonado criará um novo ID3D11Buffer para objectdata e preencherá seu conteúdo em aplicar, mas fará referência ao ID3D11Buffer original de ViewData. O único qualificador pode ser ignorado no processo de clonagem definindo o sinalizador de D3DX11 de \_ clonagem de efeito de \_ clone não \_ \_ único.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




