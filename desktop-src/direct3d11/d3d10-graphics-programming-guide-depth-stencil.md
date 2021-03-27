---
title: Configurando Depth-Stencil funcionalidade
description: Esta seção abrange as etapas para configurar o buffer de estêncil de profundidade e o estado de estêncil de profundidade para o estágio de fusão de saída.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641460"
---
# <a name="configuring-depth-stencil-functionality"></a>Configurando Depth-Stencil funcionalidade

Esta seção abrange as etapas para configurar o buffer de estêncil de profundidade e o estado de estêncil de profundidade para o estágio de fusão de saída.

-   [Criar um recurso de Depth-Stencil](#create-a-depth-stencil-resource)
-   [Criar Depth-Stencil estado](#create-depth-stencil-state)
-   [Associar dados de Depth-Stencil ao estágio de OM](#bind-depth-stencil-data-to-the-om-stage)

Assim que você souber como usar o buffer de estêncil de profundidade e o estado de estêncil de profundidade correspondente, consulte [técnicas avançadas de estêncil](#advanced-stencil-techniques).

## <a name="create-a-depth-stencil-resource"></a>Criar um recurso de Depth-Stencil

Crie o buffer de estêncil de profundidade usando um recurso de textura.


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a>Criar estado de estêncil de profundidade

O estado de estêncil de profundidade informa o estágio de fusão de saída sobre como realizar o [teste de profundidade e estêncil](d3d10-graphics-programming-guide-output-merger-stage.md). O teste de profundidade e estêncil determina se um determinado pixel deve ser desenhado.


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



DepthEnable e StencilEnable habilitam (e desabilitam) o teste de profundidade e de estêncil. Defina DepthEnable como **false** para desabilitar o teste de profundidade e impedir a gravação no buffer de profundidade. Defina StencilEnable como **false** para desabilitar o teste de estêncil e impedir a gravação no buffer de estêncil (quando DepthEnable for **false** e StencilEnable for **true**, o teste de profundidade sempre passa na operação de estêncil).

O DepthEnable só afeta o estágio de mesclagem de saída-ele não afeta recorte, tendência de profundidade ou fixação MSS de valores antes que os dados sejam inseridos em um sombreador de pixel.

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>Associar dados de estêncil de profundidade ao estágio de OM

Associar o estado de estêncil de profundidade.


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



Associe o recurso de estêncil de profundidade usando um modo de exibição.


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



Uma matriz de exibições de destino de renderização pode ser passada em [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), mas todas as exibições de destino de renderização corresponderão a uma exibição de estêncil de profundidade única. A matriz de destino de renderização no Direct3D 11 é um recurso que permite que um aplicativo seja processado em vários destinos de renderização simultaneamente no nível primitivo. As matrizes de destino de renderização oferecem maior desempenho em relação à configuração individual de destinos de renderização com várias chamadas para **ID3D11DeviceContext:: OMSetRenderTargets** (essencialmente o método empregado no Direct3D 9).

Os destinos de renderização devem todos ser do mesmo tipo de recurso. Se a suavização de várias amostras for usada, todos os destinos de renderização associados e buffers de profundidade devem ter as mesmas contagens de amostra.

Quando um buffer é usado como um destino de renderização, os testes de estêncil de profundidade e os destinos de renderização múltiplos não são permitidos.

-   Até 8 destinos de renderização podem ser vinculados ao mesmo tempo.
-   Todos os destinos de renderização devem ter o mesmo tamanho em todas as dimensões (largura e altura e profundidade para 3D ou tamanho da matriz para \* tipos de matriz).
-   Cada destino de renderização pode ter um formato de dados diferente.
-   As máscaras de gravação controlam quais dados são gravados em um destino de renderização. As máscaras de gravação de saída controlam, a um nível de componente e de destino de renderização, quais dados são gravados nos destinos de renderização.

## <a name="advanced-stencil-techniques"></a>Técnicas avançadas de estêncil

A parte de estêncil do buffer de estêncil de profundidade pode ser usada para criar efeitos de renderização como composição, decalque e contornos.

-   [Composição](#compositing)
-   [Decaling](#decaling)
-   [Contornos e silhuetas](#outlines-and-silhouettes)
-   [Estêncil de duas pontas](#two-sided-stencil)
-   [Lendo o buffer de Depth-Stencil como uma textura](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>Composição

Seu app pode usar o buffer de estêncil para compor imagens 2D ou 3D em uma cena 3D. Uma máscara no buffer de estêncil é usada para ocultar uma área da superfície de destino de renderização. Informações armazenadas 2D, como texto ou bitmaps, podem então ser escritas na área obstruída. Como alternativa, seu app pode renderizar objetos primitivos 3D adicionais para a região mascarada por estêncil da superfície do destino de renderização. Ele pode até mesmo renderizar uma cena inteira.

Jogos geralmente são compostos por diversas cenas 3D juntas. Por exemplo, jogos de direção normalmente exibem um espelho retrovisor. O espelho contém o modo de exibição da cena 3D atrás do condutor. Ele é essencialmente uma segunda cena 3D composta pela visão frontal do condutor.

### <a name="decaling"></a>Decalque

Aplicativos Direct3D usam decalque para controlar quais pixels de uma determinada imagem primitiva são desenhados na superfície de destino de renderização. Os apps aplicam os decalques às imagens de objetos primitivos para permitir que polígonos coplanares sejam renderizados corretamente.

Por exemplo, ao aplicar marcas de pneus e linhas amarelas em uma estrada, as marcas devem aparecer diretamente sobre a pista. No entanto, os valores z das marcas e da estrada são os mesmos. Portanto, o buffer de profundidade pode não produzir uma separação clara entre os dois. Alguns pixels da parte primitiva traseira podem ser renderizados na parte superior da parte primitiva frontal e vice-versa. A imagem resultante parece tremida de quadro a quadro. Esse efeito é chamado luta z ou flimmering.

Para resolver esse problema, use um estêncil para mascarar a seção da parte traseira primitiva onde aparecerá o decalque. Desligue o buffer z e renderize a imagem da parte primitiva dianteira na área sem máscara da superfície de destino de renderização.

Várias mesclagens de textura podem ser usadas para resolver esse problema.

### <a name="outlines-and-silhouettes"></a>Contornos e silhuetas

Você pode usar o buffer de estêncil para efeitos mais abstratos, como contornos e silhuetas.

Se seu app realiza duas passagens de renderização - uma para gerar a máscara de estêncil e a segunda para aplicar a máscara de estêncil à imagem, mas com os primitivas um pouco menores na segunda passagem - a imagem resultante conterá apenas contorno da primitiva. O app pode preencher a área com máscara de estêncil da imagem com uma cor sólida, dando à primitiva uma aparência em alto-relevo.

Se a máscara de estêncial tiver o mesmo tamanho e formato da primitiva que está sendo renderizado, a imagem resultante terá um buraco onde o primitivo deveria estar. Seu app poderá preencher o buraco com cor preta para produzir uma silhueta da primitiva.

### <a name="two-sided-stencil"></a>Estêncil de dois lados

Os volumes de sombra são usados para desenhar sombras com o buffer de estêncil. O app calcula os volumes de sombra convertidos sobrepondo a geometria, calculando as bordas da silhueta e afastando-as da luz em um conjunto de volumes 3D. Em seguida, esses volumes são renderizados duas vezes no buffer de estêncil.

A primeira renderização desenha polígonos voltados para frente e aumenta os valores de buffer de estêncil. A segunda renderização desenha polígonos voltados para trás do volume de sombra e diminui os valores de buffer de estêncil. Normalmente, todos os valores incrementados e decrementados cancelam um ao outro. No entanto, a cena já foi renderizada com geometria normal, fazendo com que alguns pixels falhem no teste de buffer z, conforme o volume de sombra é renderizado. Os valores restantes no buffer de estêncil correspondem aos pixels que estão na sombra. Esse conteúdo restante do buffer de estêncil é usado como uma máscara, para fazer a combinação alfa de um quadrupleto preto grande e abrangente na cena. Com o buffer de estêncil atuando como uma máscara, o resultado será o escurecimento dos pixels que estão nas sombras.

Isso significa que a geometria de sombra é desenhada duas vezes por fonte de luz, exercendo assim pressão sobre a taxa de transferência de vértice da GPU. O recurso de estêncil de dois lados foi projetado para atenuar essa situação. Nesta abordagem, existem dois conjuntos de estado de estêncil (nomeados abaixo), um conjunto para os triângulos voltados para a frente e outro para os triângulos voltados para trás. Dessa forma, somente uma única passagem é desenhada por volume de sombra, por luz.

Um exemplo de implementação de estêncil de dois lados pode ser encontrado no [exemplo ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>Ler o buffer de estêncil de profundidade como uma textura

Um buffer de estêncil de profundidade inativo pode ser lido por um sombreador como uma textura. Um app que lê um buffer de estêncil de profundidade como uma textura renderiza em duas passagens, a primeira passagem grava o buffer de estêncil de profundidade e a segunda passagem lê do buffer. Isso permite que um sombreador compare os valores de profundidade ou estêncil gravados anteriormente no buffer com o valor do pixel que está sendo renderizado atualmente. O resultado da comparação pode ser usado para criar efeitos, como o mapeamento de sombra ou partículas suaves em um sistema de partículas.

Para criar um buffer de estêncil de profundidade que pode ser usado como um recurso de estêncil de profundidade e um recurso de sombreador, algumas alterações precisam ser feitas para o código de exemplo na seção [criar um Depth-Stencil recurso](#create-a-depth-stencil-resource) .

-   O recurso de estêncil de profundidade deve ter um formato não tipado, como o \_ formato dxgi \_ R32 \_ .
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   O recurso de estêncil de profundidade deve usar os sinalizadores de associação de recurso do estêncil de profundidade de D3D10 \_ e do d3d10 BIND \_ \_ \_ \_ Shader \_ .
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

Além disso, um modo de exibição de recursos do sombreador precisa ser criado para o buffer de profundidade usando uma estrutura [**desc de exibição de \_ recursos do sombreador \_ \_ \_ D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) e [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview). O modo de exibição de recursos do sombreador usará um formato tipado, como o **\_ formato dxgi \_ R32 \_ float** que é equivalente ao formato de tipo informativo especificado quando o recurso de estêncil de profundidade foi criado.

No primeiro processamento, passe o buffer de profundidade associado, conforme descrito na seção [associar dados Depth-Stencil à etapa de OM](#bind-depth-stencil-data-to-the-om-stage) . Observe que o formato passado para [**a \_ exibição de estêncil de profundidade D3D11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). O formato usará um formato tipado, como o **\_ formato dxgi \_ D32 \_ float**. Após a primeira passagem de renderização, o buffer de profundidade conterá os valores de profundidade para a cena.

Na segunda passagem de renderização, a função [**ID3D11DeviceContext:: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) é usada para definir a exibição de estêncil de profundidade como **nula** ou um recurso de estêncil de profundidade diferente e a exibição de recurso do sombreador é passada para o sombreador usando [**ID3D11EffectShaderResourceVariable:: setresource**](id3dx11effectshaderresourcevariable-setresource.md). Isso permite que o sombreador pesquise os valores de profundidade calculados na primeira passagem de renderização. Observe que será necessário aplicar uma transformação para recuperar valores de profundidade se o ponto de vista da primeira passagem de renderização for diferente da segunda passagem de renderização. Por exemplo, se uma técnica de mapeamento de sombra estiver sendo usada, a primeira passagem de renderização será da perspectiva de uma fonte de luz enquanto a segunda passagem de renderização irá da perspectiva do visualizador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estágio de fusão de saída](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 