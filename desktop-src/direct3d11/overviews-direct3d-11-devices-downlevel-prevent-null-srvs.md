---
title: Impedindo SRVs de sombreador de pixel nulo indesejado
description: Este tópico discute como contornar o driver recebendo exibições de recurso de sombreador nulo (SRVs) mesmo quando SRVs não nulo estão associados ao estágio de sombreador de pixel.
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bacacf7704cffe12df44b9b0be667632307adb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988529"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a>Impedindo SRVs de sombreador de pixel nulo indesejado

Os aplicativos do Direct3D 11 executados em hardware de gráficos do Direct3D 9 podem, inadvertidamente, fazer com que o driver receba exibições de recurso de sombreador **nulo** (SRVs) mesmo quando os aplicativos associam SRVs não **nulo** ao estágio do sombreador de pixel. Essa situação pode ocorrer somente se os aplicativos destruirem o SRVs enquanto eles são executados. Este tópico discute como contornar o driver recebendo exibições de recurso de sombreador **nulo** (SRVs) mesmo quando SRVs não **nulo** estão associados ao estágio de sombreador de pixel.

Para impedir que o driver receba SRVs **nulos** indesejados, os aplicativos devem chamar [**ID3D11DeviceContext::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) para remover todos os SRVs antes de cada chamada para [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader). No entanto, se os aplicativos não destruirem o SRVs até o final da execução do código, eles não precisarão remover a SRVs.

A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct3D 11 em hardware de nível inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




