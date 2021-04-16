---
description: Esta seção mostra como usar primitivos de ordem superior em seu aplicativo.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Usando primitivos de Higher-Order (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8d1447635c38e5e5df3d16ebca5ee3ee142020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550355"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Usando primitivos de Higher-Order (Direct3D 9)

Esta seção mostra como usar primitivos de ordem superior em seu aplicativo.

-   [Determinando Higher-Order suporte primitivo](#determining-higher-order-primitive-support)
-   [Patches de desenho](#drawing-patches)
-   [Gerando coordenadas normais e de textura](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Determinando Higher-Order suporte primitivo

O membro DevCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pode ser consultado para determinar o nível de suporte para operações que envolvem primitivos de ordem superior. A tabela a seguir lista os recursos de dispositivo relacionados a primitivos de ordem superior no Direct3D 9.



| Funcionalidade do dispositivo             | Descrição                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ NPATCHES          | O dispositivo dá suporte a N-patches e é baseado em [triângulos de PN curvos](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (um tipo especial de triângulos Bézier cúbicos). |
| D3DDEVCAPS \_ QUINTICRTPATCHES  | O dispositivo dá suporte a curvas de Bézier QUINTIC e a linhas B.                                                                                                         |
| D3DDEVCAPS \_ RTPATCHES         | O dispositivo dá suporte a patches retangulares e triangulares (RT-patches).                                                                                             |
| D3DDEVCAPS \_ RTPATCHHANDLEZERO | RT-patches podem ser desenhados com eficiência usando o identificador zero.                                                                                                     |



 

Observe que D3DDEVCAPS \_ RTPATCHHANDLEZERO não significa que um patch com o identificador zero possa ser desenhado. Um patch de manipulação zero sempre pode ser desenhado, independentemente de essa capacidade de dispositivo ser definida ou não. Quando esse recurso é definido, a arquitetura de hardware não exige o armazenamento em cache de nenhuma informação e que patches não armazenados em cache (identificador zero) sejam desenhados com eficiência como em cache.

## <a name="drawing-patches"></a>Patches de desenho

O Direct3D 9 dá suporte a dois tipos de primitivos de ordem superior ou patches. Eles são chamados de patches N-patches e RECT/tri. N-os patches podem ser renderizados usando qualquer chamada de renderização de triângulo habilitando N-patches por meio da chamada para [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)(nSegments) com valor nSegments maior que 1,0. Patches Rect/Tri devem ser renderizados usando os seguintes pontos de entrada explícitos.

Você pode usar os métodos a seguir para desenhar patches.

-   [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch). Para entender melhor como os dados de patch são referenciados no buffer de vértice, consulte [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).
-   [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api). Para entender melhor como os dados de patch são referenciados no buffer de vértice, consulte [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

[**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) desenha um patch de ordem superior Retangular especificado pelo parâmetro pRectPatchInfo usando os fluxos definidos no momento. O parâmetro Handle é usado para associar o patch a um identificador, de forma que na próxima vez que o patch for desenhado, não seja necessário reespecificar pRectPatchInfo. Isso possibilita que pré-calcular e coeficientes de diferença de encaminhamento em cache ou outras informações que, por sua vez, habilitam chamadas subsequentes para **IDirect3DDevice9::D rawrectpatch** usando o mesmo identificador para ser executado com eficiência.

O objetivo é que, para patches estáticos, um aplicativo defina o sombreador de vértice e os fluxos apropriados, forneça informações de patch no parâmetro pRectPatchInfo e especifique um identificador para que o Direct3D possa capturar e armazenar informações em cache. O aplicativo pode então chamar [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) subsequentemente com pRectPatchInfo definido como **NULL** para desenhar o patch com eficiência. Ao desenhar um patch em cache, os fluxos definidos atualmente são ignorados. No entanto, é possível substituir o pNumSegs armazenado em cache especificando novos valores para pNumSegs. Além disso, é necessário definir o mesmo sombreador de vértice ao renderizar um patch em cache como foi definido quando ele foi capturado.

Para patches dinâmicos, os dados de patch são alterados para cada renderização do patch, portanto, não é eficiente armazenar informações em cache. O aplicativo pode transmitir isso para o Direct3D definindo o identificador como 0. Nesse caso, o Direct3D desenha o patch usando os fluxos atualmente definidos e os valores de pNumSegs e não armazena em cache nenhuma informação. Não é válido definir simultaneamente o identificador como 0 e pPatch como **nulo**.

Ao reespecificar pRectPatchInfo para o mesmo identificador, o aplicativo pode substituir as informações armazenadas em cache anteriormente.

[**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) é semelhante a [**IDirect3DDevice9::D rawrectpatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) , exceto que ele desenha um patch triangular de ordem superior.

## <a name="generating-normals-and-texture-coordinates"></a>Gerando coordenadas normais e de textura

Se você estiver usando um sombreador FVF (formato de vértice flexível), a geração automática de normais e coordenadas de textura não será possível.

Para os normais, você pode fornecê-los diretamente ou fazer com que o Direct3D os calcule para você.

As coordenadas geradas para patches retangulares são coordenadas baseadas em spline, conforme mostrado nas ilustrações a seguir.

![ilustração de uma textura original e a textura com coordenadas baseadas em spline](images/texturespline.png)

As coordenadas geradas para patches triangulares são coordenadas baseadas em spline barycentric, conforme mostrado nas ilustrações a seguir.

![ilustração de uma textura original e a textura com coordenadas baseadas em spline barycentric](images/texturebarycentricspline.png)

Se um aplicativo precisar alterar o intervalo das coordenadas de textura geradas, isso poderá ser feito usando transformações de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos de ordem superior](higher-order-primitives.md)
</dt> </dl>

 

 
