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
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a><span data-ttu-id="a0f2d-103">Impedindo SRVs de sombreador de pixel nulo indesejado</span><span class="sxs-lookup"><span data-stu-id="a0f2d-103">Preventing Unwanted NULL Pixel Shader SRVs</span></span>

<span data-ttu-id="a0f2d-104">Os aplicativos do Direct3D 11 executados em hardware de gráficos do Direct3D 9 podem, inadvertidamente, fazer com que o driver receba exibições de recurso de sombreador **nulo** (SRVs) mesmo quando os aplicativos associam SRVs não **nulo** ao estágio do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-104">Direct3D 11 applications that run on Direct3D 9 graphics hardware could inadvertently cause the driver to receive **NULL** shader-resource views (SRVs) even when the applications bind non-**NULL** SRVs to the pixel shader stage.</span></span> <span data-ttu-id="a0f2d-105">Essa situação pode ocorrer somente se os aplicativos destruirem o SRVs enquanto eles são executados.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-105">This situation can occur only if the applications destroy SRVs while they execute.</span></span> <span data-ttu-id="a0f2d-106">Este tópico discute como contornar o driver recebendo exibições de recurso de sombreador **nulo** (SRVs) mesmo quando SRVs não **nulo** estão associados ao estágio de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-106">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span>

<span data-ttu-id="a0f2d-107">Para impedir que o driver receba SRVs **nulos** indesejados, os aplicativos devem chamar [**ID3D11DeviceContext::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) para remover todos os SRVs antes de cada chamada para [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="a0f2d-107">To prevent the driver from receiving unwanted **NULL** SRVs, the applications must call [**ID3D11DeviceContext::PSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) to unset all SRVs before each call to [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span></span> <span data-ttu-id="a0f2d-108">No entanto, se os aplicativos não destruirem o SRVs até o final da execução do código, eles não precisarão remover a SRVs.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-108">However, if the applications do not destroy SRVs until the end of their code execution, they do not need to unset the SRVs.</span></span>

<span data-ttu-id="a0f2d-109">A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.</span><span class="sxs-lookup"><span data-stu-id="a0f2d-109">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0f2d-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0f2d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f2d-111">Direct3D 11 em hardware de nível inferior</span><span class="sxs-lookup"><span data-stu-id="a0f2d-111">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




