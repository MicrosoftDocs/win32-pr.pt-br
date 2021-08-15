---
title: Clonando um efeito
description: Clonar um efeito cria uma segunda cópia quase idêntica do efeito.
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

Clonar um efeito cria uma segunda cópia quase idêntica do efeito. Confira o qualificador único a seguir para ver uma explicação sobre por que ele não é exato. Uma segunda cópia de um efeito é útil quando se deseja usar a estrutura de efeitos em vários threads, já que o runtime de efeito não é thread-safe para manter o alto desempenho.

Como os contextos de dispositivo também não são thread-safe, threads diferentes devem passar contextos de dispositivo diferentes para o método ID3DX11EffectPass::Apply.

Um efeito pode ser clonado com a seguinte sintaxe:


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



No exemplo acima, a cópia clonada encapsulará o mesmo estado que o efeito original, independentemente do estado em que o efeito original está. Especialmente:

1.  Se pEffect for otimizado, o efeito pCloned será otimizado
2.  Se pEffect tiver algumas variáveis gerenciadas pelo usuário, o efeito pCloned terá as mesmas variáveis gerenciadas pelo usuário (consulte a descrição única abaixo)
3.  Todas as atualizações de variáveis pendentes (até que uma chamada Aplicar atualize o estado do dispositivo) em pEffect estarão pendentes em pClonedEffect

Os seguintes objetos de dispositivo Direct3D 11 são imutáveis ou nunca atualizados pela estrutura de efeitos, portanto, o efeito clonado apontará para os mesmos objetos que o efeito original:

1.  Objetos de bloco de estado (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Sombreadores
3.  Instâncias de classe
4.  Texturas (sem incluir buffers de textura)
5.  Exibições de acesso não organizado

Os seguintes objetos de dispositivo Direct3D 11 são imutáveis e modificados pelo runtime de efeito (a menos que gerenciado pelo usuário ou único em um efeito clonado); novas cópias desses objetos são criadas quando não são individuais:

1.  Buffers constantes
2.  Buffers de textura

## <a name="single-constant-buffers-and-texture-buffers"></a>Buffers constantes individuais e buffers de textura

Observe que essa discussão se aplica a buffers constantes e texturas, mas buffers constantes são assumidos para facilitar a leitura.

Pode haver casos em que um buffer constante é atualizado apenas por um thread, mas o estado do dispositivo definido por efeitos clonados usará esses dados. Por exemplo, o efeito principal pode atualizar o mundo e exibir matrizes que são referenciadas de sombreadores em efeitos clonados que não alteram o mundo e visualizam matrizes. Nesses casos, os efeitos clonados precisam referenciar o buffer constante atual em vez de recriar um.

Há duas maneiras de obter esse resultado desejado:

1.  Use ID3DX11EffectConstantBuffer::SetConstantBuffer no efeito clonado para torná-lo gerenciado pelo usuário
2.  Marcar o buffer constante como "único" no código HLSL, forçar o runtime de efeito a tratar é como gerenciado pelo usuário após a clonagem

Há duas diferenças entre os dois métodos acima. Primeiro, no método 1, um novo ID3D11Buffer será criado e o usuário antes de SetConstantBuffer ser chamado. Além disso, depois de chamar UndoSetConstantBuffer no efeito clonado, a variável no método 1 apontará para o buffer recém-criado (quais efeitos serão atualizados em Aplicar), enquanto a variável no método 2 continuará a apontar para o buffer original (não atualizando-o em Aplicar).

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



Durante a clonagem, o efeito clonado criará um novo ID3D11Buffer para ObjectData e preencherá seu conteúdo em Aplicar, mas fará referência ao ID3D11Buffer original para ViewData. O qualificador único pode ser ignorado no processo de clonagem definindo o sinalizador D3DX11 \_ EFFECT \_ CLONE FORCE \_ \_ NONSINGLE.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




