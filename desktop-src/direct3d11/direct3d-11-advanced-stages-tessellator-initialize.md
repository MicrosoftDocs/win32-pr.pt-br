---
title: Como inicializar o estágio do mosaico
description: Este tópico mostra como inicializar o estágio do mosaico.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f842b1095a4053ad35838864bac6d6677194d85f48e0a78e2fc6975af1e3b8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096276"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>Como inicializar o estágio do Mosaico

Em geral, o mosaico expande o modelo compacto e definido pelo usuário de um patch em geometria que contém uma quantidade programável de detalhes. A geometria normalmente é um conjunto de triângulos que representa geometria de superfície detalhada. Este tópico mostra como inicializar o estágio do mosaico.

O estágio do mosaico é o segundo de três estágios que trabalham juntos para manter ou lado a lado uma superfície. O primeiro estágio é o estágio de sombreador de chassi; ele opera uma vez por patch e configura como o próximo estágio (o mosaico de função fixa) se comporta. Um sombreador de chassi também gera saídas definidas pelo usuário, como pontos de controle de saída e constantes de patch que são enviadas após o mosaico diretamente para o terceiro estágio, o estágio de sombreador de domínio. Um sombreador de domínio é invocado uma vez por ponto de estágio do mosaico e avalia as posições da superfície.

O estágio do mosaico é um estágio de função fixo, não há sombreador a ser gerado e nenhum estado a ser definido. Ele recebe todo o estado de instalação do estágio de sombreador de casca; depois que o estágio do sombreador de chassi tiver sido inicializado, o estágio do mosaico será inicializado automaticamente.

**Para inicializar o estágio do mosaico**

-   Inicialize o estágio de sombreador de chassi usando [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppClassInstances* é um ponteiro para uma matriz de interfaces de sombreador, representada por ponteiros [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) e o número de interfaces, representado por *NumClassInstances*. Se não for usado, esses parâmetros poderão ser definidos como **NULL** e 0, respectivamente.

Depois que o estágio do sombreador de chassi for inicializado, você também deverá inicializar o estágio do sombreador de domínio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Visão geral do mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




