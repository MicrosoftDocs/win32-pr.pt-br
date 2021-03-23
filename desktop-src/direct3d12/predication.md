---
title: Predicação
description: Predicação é um recurso que habilita a GPU em vez da CPU para determinar não desenhar, copiar ou distribuir um objeto.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548293"
---
# <a name="predication"></a>Predicação

Predicação é um recurso que habilita a GPU em vez da CPU para determinar não desenhar, copiar ou distribuir um objeto.

-   [Visão geral](#overview)
-   [SetPredication](#setpredication)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

O uso típico de predicação é com oclusão; se uma caixa delimitadora for desenhada e for obstruído, obviamente, não há nenhum ponto no desenho do objeto em si. Nessa situação, o desenho do objeto pode ser "predicado", permitindo a remoção do processamento real pela GPU.

A princípio, isso pode parecer Redudant e acima do teste de profundidade padrão mais um passo de profundidade inicial. Mas predicação pode remover a sobrecarga do próprio estado do comando Draw, além da rasterização. Embora uma passagem de profundidade inicial remova pixels desnecessários, ele ainda pode executar os sombreadores de vértice, envoltória, domínio e geometria e invocar o Assembler de entrada de função fixa, o tesselator e o rasterizador. Ao desenhar uma caixa delimitadora simples ou um volume delimitador semelhante &mdash; , que é mais simples de processar e rasterizar do que o modelo real &mdash; , você evita a rasterização e o processamento desnecessários.

Ao contrário do Direct3D 11, o predicação é dissociado de consultas e é expandido no Direct3D 12 para permitir que um aplicativo para objetos de predicado com base em qualquer motivo pelo qual o desenvolvedor do aplicativo possa decidir (não apenas oclusão).

## <a name="setpredication"></a>SetPredication

Predicação pode ser definido com base no valor de 64 bits em um buffer (consulte [**D3D12 \_ predicação \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).

Quando a GPU executa um comando [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , ele ajusta o valor no buffer. Alterações futuras nos dados no buffer não afetam retroativamente o estado predicação.

Se o buffer de parâmetro de entrada for nulo, predicação será desabilitado.

As dicas de predicação não estão presentes na API do Direct3D 12; e predicação é permitido em listas de comando direta, de computação e de cópia. O buffer de origem pode estar em qualquer tipo de heap (padrão, carregar, readback, personalizado).

O tempo de execução principal validará o seguinte:

-   *AlignedBufferOffset* é um múltiplo de 8 bytes
-   O recurso é um buffer
-   A operação é um membro válido da enumeração
-   [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) não pode ser chamado de dentro de um pacote
-   O tipo de lista de comandos dá suporte a predicação
-   O deslocamento não excede o tamanho do buffer

A camada de depuração emitirá um erro se o buffer de origem não estiver na [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (que é a mesma do estado [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)e simplesmente um alias).

O conjunto de operações que podem ser preparadas são:

-   [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) não é predicado. Em vez disso, as operações individuais da lista acima que estão contidas no lado do grupo são predicadas.

Os métodos ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) não são predicados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contadores e consultas](counters-and-queries.md)
</dt> <dt>

[Medição de desempenho](performance-measurement.md)
</dt> <dt>

[Passo a passo de consultas do predicação](predication-queries.md)
</dt> </dl>

 

 




