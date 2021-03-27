---
title: Como criar um sombreador envoltória
description: Este tópico mostra como criar um sombreador envoltória.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635129"
---
# <a name="how-to-create-a-hull-shader"></a>Como: criar um sombreador envoltória

Um sombreador envoltória é o primeiro de três estágios que trabalham juntos para implementar o [mosaico](direct3d-11-advanced-stages-tessellation.md). As saídas do envoltória-Shader direcionam o estágio Tessellator, bem como o estágio Domain-Shader. Este tópico mostra como criar um sombreador envoltória.

Um sombreador envoltória transforma um conjunto de pontos de controle de entrada (de um sombreador de vértice) em um conjunto de pontos de controle de saída. O número de pontos de entrada e saída pode variar no conteúdo e no número, dependendo da transformação (uma transformação típica seria uma transformação base).

Um sombreador envoltória também gera informações constantes de patch, como fatores de mosaico, para um sombreador de domínio e o Tessellator. O estágio Tessellator de função fixa usa os fatores de mosaico, bem como outro Estado declarado em um sombreador envoltória para determinar o quanto a incluí.

**Para criar um sombreador envoltória**

1.  Criar um sombreador envoltória. Consulte [como: criar um sombreador envoltória](direct3d-11-advanced-stages-hull-shader-design.md).
2.  Compilar o código do sombreador
3.  Crie um objeto envoltória-Shader usando [**ID3D11Device:: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Inicialize o estágio do pipeline usando [**ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

Um sombreador de domínio deve ser associado ao pipeline se um sombreador envoltória estiver associado. Em particular, não é válido transmitir diretamente pontos de controle do sombreador envoltória com o sombreador Geometry.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Visão geral do mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




