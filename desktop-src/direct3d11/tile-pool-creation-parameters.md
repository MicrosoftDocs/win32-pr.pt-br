---
title: Parâmetros de criação de pool de blocos
description: Use os parâmetros nesta seção para definir pools de blocos por meio da API CreateBuffer ID3D11Device.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005039"
---
# <a name="tile-pool-creation-parameters"></a><span data-ttu-id="b4c81-103">Parâmetros de criação de pool de blocos</span><span class="sxs-lookup"><span data-stu-id="b4c81-103">Tile pool creation parameters</span></span>

<span data-ttu-id="b4c81-104">Use os parâmetros nesta seção para definir pools de blocos por meio da API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) .</span><span class="sxs-lookup"><span data-stu-id="b4c81-104">Use the parameters in this section to define tile pools via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API.</span></span>

<dl> <dt>

<span data-ttu-id="b4c81-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="b4c81-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="b4c81-106">Tamanho da alocação, como um múltiplo de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="b4c81-106">Allocation size, as a multiple of 64KB.</span></span> <span data-ttu-id="b4c81-107">0 é válido porque você pode usar posteriormente uma operação [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) .</span><span class="sxs-lookup"><span data-stu-id="b4c81-107">0 is valid because you can later use a [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation.</span></span>

</dd> <dt>

<span data-ttu-id="b4c81-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Sinalizadores diversos de recurso com suporte**</span><span class="sxs-lookup"><span data-stu-id="b4c81-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b4c81-109">\_ \_ \_ Pool de blocos diversos \_ do recurso D3D11 (identifica o recurso como um pool de blocos), D3D11 \_ \_ de recursos diversos \_ compartilhado, \_ \_ KEYEDMUTEX compartilhados ou \_ \_ NTHANDLE compartilhados.</span><span class="sxs-lookup"><span data-stu-id="b4c81-109">D3D11\_RESOURCE\_MISC\_TILE\_POOL (identifies the resource as a tile pool), D3D11\_RESOURCE\_MISC\_SHARED, \_SHARED\_KEYEDMUTEX, or \_SHARED\_NTHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="b4c81-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos com suporte**</span><span class="sxs-lookup"><span data-stu-id="b4c81-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="b4c81-111">\_Somente padrão de uso D3D11 \_ .</span><span class="sxs-lookup"><span data-stu-id="b4c81-111">D3D11\_USAGE\_DEFAULT only.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b4c81-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4c81-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4c81-113">Criando recursos em ladrilhos</span><span class="sxs-lookup"><span data-stu-id="b4c81-113">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




