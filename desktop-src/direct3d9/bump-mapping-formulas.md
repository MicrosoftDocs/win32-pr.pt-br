---
description: O Direct3D aplica as fórmulas a seguir aos componentes DU e DV em cada pixel do mapa de relevo.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Fórmulas de mapeamento de relevo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089686"
---
# <a name="bump-mapping-formulas-direct3d-9"></a><span data-ttu-id="334c4-103">Fórmulas de mapeamento de relevo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="334c4-103">Bump Mapping Formulas (Direct3D 9)</span></span>

<span data-ttu-id="334c4-104">O Direct3D aplica as fórmulas a seguir aos componentes D<sub>U</sub> e d<sub>V</sub> em cada pixel do mapa de relevo.</span><span class="sxs-lookup"><span data-stu-id="334c4-104">Direct3D applies the following formulas to the D<sub>U</sub> and D<sub>V</sub> components in each bump map pixel.</span></span>

![fórmulas de transformações de matriz de mapeamento de relevo](images/dudv-transform.png)

<span data-ttu-id="334c4-106">Nessas fórmulas, as variáveis D<sub>U</sub> e d<sub>V</sub> são obtidas diretamente de um pixel de mapa de relevo e transformadas por uma matriz 2x2 para produzir os valores Delta de saída D<sub>U</sub>' e D<sub>V</sub>'.</span><span class="sxs-lookup"><span data-stu-id="334c4-106">In these formulas, the D<sub>U</sub> and D<sub>V</sub> variables are taken directly from a bump map pixel and transformed by a 2x2 matrix to produce the output delta values D<sub>U</sub>' and D<sub>V</sub>'.</span></span> <span data-ttu-id="334c4-107">O sistema usa os valores de saída para modificar as coordenadas de textura que abordam o mapa de ambiente no próximo estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="334c4-107">The system uses the output values to modify the texture coordinates that address the environment map in the next texture stage.</span></span> <span data-ttu-id="334c4-108">Os coeficientes da matriz de transformação são definidos por meio dos \_ Estados D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 e D3DTSS \_ BUMPENVMAT11 de estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="334c4-108">The coefficients of the transformation matrix are set though the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT10, D3DTSS\_BUMPENVMAT01, and D3DTSS\_BUMPENVMAT11 texture stage states.</span></span>

<span data-ttu-id="334c4-109">Além dos valores Delta de você e v, o sistema pode calcular um valor de luminância que ele usa para modular a cor do mapa de ambiente no próximo estágio de mesclagem, conforme mostrado na fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="334c4-109">In addition to the u and v delta values, the system can compute a luminance value that it uses to modulate the color of the environment map in the next blending stage, as shown in the following formula.</span></span>

![fórmula para luminância de saída, computada do fator de escala e do deslocamento](images/l-transform.png)

<span data-ttu-id="334c4-111">Nesta fórmula, L ' é a luminância de saída sendo computada.</span><span class="sxs-lookup"><span data-stu-id="334c4-111">In this formula, L' is the output luminance being computed.</span></span> <span data-ttu-id="334c4-112">A variável L é o valor de luminância obtido de um pixel de mapa de relevo, que é multiplicado pelo fator de dimensionamento, S e offset pelo valor na variável O. Os \_ Estados de estágio de textura D3DTSS BUMPENVLSCALE e D3DTSS \_ BUMPENVLOFFSET controlam os valores das variáveis S e o na fórmula.</span><span class="sxs-lookup"><span data-stu-id="334c4-112">The L variable is the luminance value taken from a bump map pixel, which is multiplied by the scaling factor, S, and offset by the value in the variable O. The D3DTSS\_BUMPENVLSCALE and D3DTSS\_BUMPENVLOFFSET texture stage states control the values for the S and O variables in the formula.</span></span> <span data-ttu-id="334c4-113">Esta fórmula só é aplicada quando a operação de mesclagem de textura para o estágio que contém o mapa de relevo é definida como D3DTOP \_ BUMPENVMAPLUMINANCE.</span><span class="sxs-lookup"><span data-stu-id="334c4-113">This formula is only applied when the texture blending operation for the stage that contains the bump map is set to D3DTOP\_BUMPENVMAPLUMINANCE.</span></span> <span data-ttu-id="334c4-114">Ao usar D3DTOP \_ BUMPENVMAP, o sistema usa um valor de 1,0 para L '.</span><span class="sxs-lookup"><span data-stu-id="334c4-114">When using D3DTOP\_BUMPENVMAP, the system uses a value of 1.0 for L'.</span></span>

<span data-ttu-id="334c4-115">Depois de computar os valores Delta de saída D<sub>U</sub>' e D<sub>V</sub>', o sistema os adiciona às coordenadas de textura no próximo estágio de textura e modula a cor escolhida pela luminância para produzir a cor aplicada ao polígono.</span><span class="sxs-lookup"><span data-stu-id="334c4-115">After computing the output delta values D<sub>U</sub>' and D<sub>V</sub>', the system adds them to the texture coordinates in the next texture stage, and modulates the chosen color by the luminance to produce the color applied to the polygon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="334c4-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="334c4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="334c4-117">Mapeamento de relevo</span><span class="sxs-lookup"><span data-stu-id="334c4-117">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



