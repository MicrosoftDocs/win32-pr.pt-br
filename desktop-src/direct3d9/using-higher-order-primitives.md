---
description: Esta seção mostra como usar primitivos de ordem superior em seu aplicativo.
ms.assetid: 7aa4f3ab-cfce-4f8f-a538-384f038fd324
title: Usando Higher-Order primitivos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7d7a7b7f619c033665f8cb9894db5d60d5d6ecf9116de4ada230accc476c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797281"
---
# <a name="using-higher-order-primitives-direct3d-9"></a>Usando Higher-Order primitivos (Direct3D 9)

Esta seção mostra como usar primitivos de ordem superior em seu aplicativo.

-   [Determinando o Higher-Order primitivo](#determining-higher-order-primitive-support)
-   [Patches de desenho](#drawing-patches)
-   [Gerando normais e coordenadas de textura](#generating-normals-and-texture-coordinates)

## <a name="determining-higher-order-primitive-support"></a>Determinando o Higher-Order primitivo

O membro DevCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pode ser consultado para determinar o nível de suporte para operações que envolvem primitivos de ordem superior. A tabela a seguir lista as funcionalidades do dispositivo relacionadas a primitivos de ordem superior no Direct3D 9.



| Funcionalidade do dispositivo             | Descrição                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS \_ NPATCHES          | O dispositivo dá suporte a N patches e é baseado em [triângulos PN curvados](https://alex.vlachos.com/graphics/CurvedPNTriangles.pdf) (um tipo especial de triângulos bézier cúbicos). |
| D3DDEVCAPS \_ SORTICRTPATCHES  | O dispositivo dá suporte a curvas bezier e B-splines.                                                                                                         |
| D3DDEVCAPS \_ RTPATCHES         | O dispositivo dá suporte a patches retangulares e triangulares (patches RT).                                                                                             |
| D3DDEVCAPS \_ RTPATCHHANDLEZERO | Patches RT podem ser desenhados com eficiência usando o handle zero.                                                                                                     |



 

Observe que D3DDEVCAPS RTPATCHHANDLEZERO não significa que um patch com o handle \_ zero pode ser desenhado. Um patch de alça zero sempre pode ser desenhado, independentemente de essa funcionalidade do dispositivo estar definida ou não. Quando essa funcionalidade é definida, a arquitetura de hardware não requer o cache de nenhuma informação e os patches sem cache (handle zero) são desenhados com a mesma eficiência que os armazenados em cache.

## <a name="drawing-patches"></a>Patches de desenho

O Direct3D 9 dá suporte a dois tipos de primitivos de ordem superior ou patches. Elas são conhecidas como patches N-Patches e Rect/Tri. N-patches podem ser renderizados usando qualquer chamada de renderização de triângulo habilitando N-patches por meio da chamada para [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)( nSegments ) com valor nSegments maior que 1.0. Os patches Rect/Tri devem ser renderizados usando os seguintes pontos de entrada explícitos.

Você pode usar os métodos a seguir para desenhar patches.

-   [**IDirect3DDevice9::D rawRectPatch.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) Para entender melhor como os dados de patch são referenciados no buffer de vértice, consulte [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md).
-   [**IDirect3DDevice9::D rawTriPatch.**](/windows/desktop/api) Para entender melhor como os dados de patch são referenciados no buffer de vértice, consulte [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

[**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) desenha um patch de ordem alta retangular especificado pelo parâmetro pRectPatchInfo usando os fluxos definidos no momento. O parâmetro Handle é usado para associar o patch a um handle, para que na próxima vez que o patch for desenhado, não seja necessário respecificar pRectPatchInfo. Isso possibilita pré-comutar e armazenar em cache coeficientes de diferença de encaminhamento ou outras informações, que, por sua vez, permitem chamadas subsequentes para **IDirect3DDevice9::D rawRectPatch** usando o mesmo alça para executar com eficiência.

Para patches estáticos, um aplicativo definiria o sombreador de vértice e os fluxos apropriados, forneceria informações de patch no parâmetro pRectPatchInfo e especificaria um alça para que o Direct3D possa capturar e armazenar informações em cache. Em seguida, o aplicativo pode chamar [**IDirect3DDevice9::D rawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) subsequentemente com pRectPatchInfo definido como **NULL** para desenhar com eficiência o patch. Ao desenhar um patch armazenado em cache, os fluxos atualmente definidos são ignorados. No entanto, é possível substituir o pNumSegs armazenado em cache especificando novos valores para pNumSegs. Além disso, é necessário definir o mesmo sombreador de vértice ao renderizar um patch armazenado em cache como foi definido quando ele foi capturado.

Para patches dinâmicos, os dados de patch mudam para cada renderização do patch, portanto, não é eficiente armazenar informações em cache. O aplicativo pode transmitir isso ao Direct3D definindo Handle como 0. Nesse caso, o Direct3D desenha o patch usando os fluxos definidos no momento e os valores pNumSegs e não armazena em cache nenhuma informação. Não é válido definir simultaneamente Handle como 0 e pPatch como **NULL.**

Ao respecificar pRectPatchInfo para o mesmo handle, o aplicativo pode substituir as informações armazenadas em cache anteriormente.

[**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api) é semelhante a [**IDirect3DDevice9::D rawRectPatch,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch) exceto que ele desenha um patch de ordem alta triangular.

## <a name="generating-normals-and-texture-coordinates"></a>Gerando normais e coordenadas de textura

Se você estiver usando um sombreador FVF (formato de vértice flexível), a geração automática de normais e coordenadas de textura não será possível.

Para os normais, você pode fornecer diretamente ou fazer com que o Direct3D os calcule para você.

As coordenadas geradas para patches retangulares são coordenadas baseadas em spline, conforme mostrado nas ilustrações a seguir.

![ilustração de uma textura original e a textura com coordenadas baseadas em spline](images/texturespline.png)

As coordenadas geradas para patches triangulares são coordenadas baseadas em spline centradas em barras, conforme mostrado nas ilustrações a seguir.

![ilustração de uma textura original e a textura com coordenadas baseadas em spline centradas em barras](images/texturebarycentricspline.png)

Se um aplicativo precisa alterar o intervalo das coordenadas de textura geradas, isso pode ser feito usando as transformação de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos de ordem superior](higher-order-primitives.md)
</dt> </dl>

 

 
