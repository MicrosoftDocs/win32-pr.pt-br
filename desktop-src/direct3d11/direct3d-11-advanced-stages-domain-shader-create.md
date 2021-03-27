---
title: Como criar um sombreador de domínio
description: Este tópico mostra como criar um sombreador de domínio.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005043"
---
# <a name="how-to-create-a-domain-shader"></a>Como: criar um sombreador de domínio

Um sombreador de domínio é o terceiro de três estágios que trabalham em conjunto para implementar o [mosaico](direct3d-11-advanced-stages-tessellation.md). As entradas para o estágio de sombreador de domínio vêm de um sombreador envoltória. Este tópico mostra como criar um sombreador de domínio.

Um sombreador de domínio transforma a geometria da superfície (criada pelo estágio de Tessellator da função fixa) usando pontos de controle de saída do sombreador envoltória, patch de saída do sombreador envoltória-dados constantes e um único conjunto de coordenadas Tessellator UV.

**Para criar um sombreador de domínio**

1.  Criar um sombreador de domínio. Consulte [como: criar um sombreador de domínio](direct3d-11-advanced-stages-domain-shader-design.md).
2.  Compile o código do sombreador.
3.  Crie um objeto de sombreador de domínio usando [**ID3D11Device:: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  Inicialize o estágio do pipeline usando [**ID3D11DeviceContext::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
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

 

 




