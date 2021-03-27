---
title: Como inicializar o estágio Tessellator
description: Este tópico mostra como inicializar o estágio Tessellator.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988498"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>Como inicializar o estágio Tessellator

Em geral, o mosaico expande o modelo definido pelo usuário e compacto de um patch em geometria que contém uma quantidade de detalhes programável. A geometria normalmente é um conjunto de triângulos que representa a geometria de superfície detalhada. Este tópico mostra como inicializar o estágio Tessellator.

O estágio Tessellator é o segundo de três estágios que trabalham em conjunto para incluí ou peça uma superfície. O primeiro estágio é o estágio envoltória-Shader; Ele opera uma vez por patch e configura como o próximo estágio (a função fixa Tessellator) se comporta. Um sombreador envoltória também gera saídas definidas pelo usuário, como pontos de controle de saída e constantes de patch que são enviadas após o Tessellator diretamente para o terceiro estágio, o estágio Domain-Shader. Um sombreador de domínio é invocado uma vez por ponto de Tessellator e avalia as posições da superfície.

O estágio Tessellator é um estágio de função fixo, não há nenhum sombreador a ser gerado e nenhum estado a ser definido. Ele recebe todo o seu estado de configuração do estágio envoltória-Shader; Depois que o estágio envoltória-Shader tiver sido inicializado, o estágio Tessellator será inicializado automaticamente.

**Para inicializar o estágio Tessellator**

-   Inicialize o estágio envoltória-Shader usando [**ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppClassInstances* é um ponteiro para uma matriz de interfaces de sombreador, representado por ponteiros [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) e o número de interfaces, representado por *NumClassInstances*. Se não for usado, esses parâmetros poderão ser definidos como **NULL** e 0, respectivamente.

Depois que o estágio envoltória-Shader for inicializado, você também deverá inicializar o estágio Domain-Shader.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Visão geral do mosaico](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




