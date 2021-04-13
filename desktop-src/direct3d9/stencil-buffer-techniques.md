---
description: Os aplicativos usam o buffer de estêncil para mascarar pixels em uma imagem. A máscara controla se o pixel é desenhado ou não. Alguns dos efeitos mais comuns são mostrados abaixo.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Técnicas de buffer de estêncil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370332"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a>Técnicas de buffer de estêncil (Direct3D 9)

Os aplicativos usam o buffer de estêncil para mascarar pixels em uma imagem. A máscara controla se o pixel é desenhado ou não. Alguns dos efeitos mais comuns são mostrados abaixo.

-   [Composição](compositing.md)
-   [Decaling](decaling.md)
-   [Dessolucionar, esmaecer e passar o dedo](dissolves--fades--and-swipes.md)
-   [Contornos e silhuetas](outlines-and-silhouettes.md)
-   [Estêncil de duas pontas](two-sided-stencil.md)

O buffer de estêncil habilita ou desabilita o desenho na superfície de destino de renderização em uma base de pixel por pixel. No nível mais fundamental, ele permite que aplicativos mascarem seções da imagem renderizada para que elas não sejam exibidas. Aplicativos geralmente usam buffers de estêncil de efeitos especiais, como desintegração, decalque e contorno.

Informações de buffer de estêncil são incorporadas nos dados do buffer z. Seu aplicativo pode usar o método [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) para verificar o suporte ao estêncil de hardware, conforme mostrado no exemplo de código a seguir.


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



[**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) permite que você escolha um dispositivo para criar com base nos recursos do dispositivo. Nesse caso, os dispositivos que não dão suporte a buffers de estêncil de 8 bits são rejeitados. Observe que esse é apenas um possível uso para **IDirect3D9:: CheckDeviceFormat**; para obter detalhes, consulte [determinando o suporte de hardware (Direct3D 9)](determining-hardware-support.md).

## <a name="how-the-stencil-buffer-works"></a>Como o buffer de estêncil funciona

O Direct3D realiza um teste no conteúdo do buffer de estêncil em uma base de pixel por pixel. Para cada pixel na superfície do destino, ele executa um teste usando o valor correspondente no buffer de estêncil, um valor de referência de estêncil e um valor de máscara de estêncil. Se o teste for aprovado, o Direct3D executa uma ação. O teste é realizado usando as seguintes etapas.

1.  Execute uma operação AND bit a bit do valor de referência do estêncil com a máscara de estêncil.
2.  Execute uma operação AND bit a bit do valor de buffer do estêncil do pixel atual com a máscara de estêncil.
3.  Compare o resultado da etapa 1 com o resultado da etapa 2, usando a função de comparação.

Essas etapas são mostradas no exemplo de código a seguir.


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



é o conteúdo do buffer de estêncil para o pixel atual. Este exemplo de código usa o símbolo de e comercial (&) para representar o bit e a operação.


```
StencilMask
```



representa o valor da máscara do estêncil e


```
StencilRef
```



representa o valor de referência do estêncil.


```
CompFunc
```



é a função de comparação.

O pixel atual é escrito na superfície de destino se o teste de estêncil for aprovado, caso contrário, é ignorado. O comportamento de comparação padrão é gravar o pixel, não importa a diferença entre cada operação de bit de bits (D3DCMP \_ Always). Você pode alterar esse comportamento alterando o valor do estado de \_ RENDERIZAÇÃO D3DRS STENCILFUNC, passando um membro do tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) para identificar a função de comparação desejada.

Seu aplicativo pode personalizar a operação do buffer de estêncil. Ele pode definir a função de comparação, a máscara de estêncil e o valor de referência de estêncil. Ele também pode controlar a ação que o Direct3D executa quando o teste de estêncil passa ou falha. Para obter mais informações, consulte o [estado do buffer do estêncil (Direct3D 9)](stencil-buffer-state.md).

## <a name="examples"></a>Exemplos

Os exemplos de código a seguir demonstram como configurar o buffer de estêncil.


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



Por padrão, o valor de referência do estêncil é zero. Qualquer valor inteiro é válido. O Direct3D executa uma e/ou um valor de referência de estêncil e uma máscara de estêncil antes do teste de estêncil.

Você pode controlar quais informações de pixel são gravadas dependendo da comparação do estêncil.


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



Você pode escrever sua própria fórmula para o valor que deseja gravar no buffer do estêncil, conforme mostrado no exemplo a seguir.


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de pixel](pixel-pipeline.md)
</dt> </dl>

 

 
