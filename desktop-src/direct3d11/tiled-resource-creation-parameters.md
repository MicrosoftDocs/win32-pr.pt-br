---
title: Parâmetros de criação de recursos por lado
description: Há algumas restrições sobre o tipo de recursos do Direct3D que você pode criar com o sinalizador diD3D11 de \_ recursos diversos do recurso \_ \_ . Esta seção fornece os parâmetros válidos para a criação de recursos em ladrilho.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/13/2019
ms.locfileid: "103638845"
---
# <a name="tiled-resource-creation-parameters"></a><span data-ttu-id="4a3a1-104">Parâmetros de criação de recursos por lado</span><span class="sxs-lookup"><span data-stu-id="4a3a1-104">Tiled resource creation parameters</span></span>

<span data-ttu-id="4a3a1-105">Há algumas restrições sobre o tipo de recursos do Direct3D que você pode criar com o sinalizador [**diD3D11 de \_ recursos \_ diversos \_ do recurso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="4a3a1-105">There are some constraints on the type of Direct3D resources that you can create with the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> <span data-ttu-id="4a3a1-106">Esta seção fornece os parâmetros válidos para a criação de recursos em ladrilho.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-106">This section provides the valid parameters for creating tiled resources.</span></span>

<dl> <dt>

<span data-ttu-id="4a3a1-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo de recurso com suporte**</span><span class="sxs-lookup"><span data-stu-id="4a3a1-107"><span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Supported Resource Type**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a1-108">\[Matriz Texture2D \] (incluindo \[ matriz TextureCube \] , que é uma variante da \[ matriz Texture2D \] ) ou buffer.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-108">Texture2D\[Array\] (including TextureCube\[Array\], which is a variant of Texture2D\[Array\]) or Buffer.</span></span>

<span data-ttu-id="4a3a1-109">**Sem suporte:** Texture1D \[ array \] ou Texture3D, mas o Texture3D pode ter suporte no futuro.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-109">**NOT supported:** Texture1D\[Array\] or Texture3D, but Texture3D might be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a1-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos com suporte**</span><span class="sxs-lookup"><span data-stu-id="4a3a1-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a1-111">Padrão de uso de D3D11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4a3a1-111">D3D11\_USAGE\_DEFAULT.</span></span>

<span data-ttu-id="4a3a1-112">**Sem suporte:** Uso \_ \_ dinâmico de D3D11, \_ preparo de uso de D3D11 \_ ou \_ uso \_ inalterável de D3D11.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-112">**NOT supported:** D3D11\_USAGE\_DYNAMIC, D3D11\_USAGE\_STAGING, or D3D11\_USAGE\_IMMUTABLE.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a1-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Sinalizadores diversos de recurso com suporte**</span><span class="sxs-lookup"><span data-stu-id="4a3a1-113"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a1-114">\_Recurso D3D11 \_ misc. \_ lado a lado (por definição), \_ misc \_ TEXTURECUBE, \_ DRAWINDIRECT \_ args, \_ buffer \_ permite \_ \_ exibições brutas, \_ buffer \_ estruturado, \_ Resource \_ fixe ou \_ gerar \_ MIPS.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-114">D3D11\_RESOURCE\_MISC\_TILED (by definition), \_MISC\_TEXTURECUBE, \_DRAWINDIRECT\_ARGS, \_BUFFER\_ALLOW\_RAW\_VIEWS, \_BUFFER\_STRUCTURED, \_RESOURCE\_CLAMP, or \_GENERATE\_MIPS.</span></span>

<span data-ttu-id="4a3a1-115">**Sem suporte:** \_ COMPARTILHAMENTO compartilhado \_ , \_ KEYEDMUTEX compartilhado \_ , \_ compatível com GDI, \_ \_ NTHANDLE compartilhados, \_ \_ conteúdo restrito, \_ restringir \_ \_ recurso compartilhado, \_ restringir \_ \_ \_ Driver de recurso compartilhado, \_ protegido ou \_ pool de blocos \_ .</span><span class="sxs-lookup"><span data-stu-id="4a3a1-115">**NOT supported:** \_SHARED, \_SHARED\_KEYEDMUTEX, \_GDI\_COMPATIBLE, \_SHARED\_NTHANDLE, \_RESTRICTED\_CONTENT, \_RESTRICT\_SHARED\_RESOURCE, \_RESTRICT\_SHARED\_RESOURCE\_DRIVER, \_GUARDED, or \_TILE\_POOL.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a1-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Sinalizadores de associação com suporte**</span><span class="sxs-lookup"><span data-stu-id="4a3a1-116"><span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Supported Bind Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a1-117">\_Recurso D3D11 BIND \_ Shader \_ , \_ destino de renderização \_ , \_ \_ estêncil de profundidade ou \_ acesso não ordenado \_ .</span><span class="sxs-lookup"><span data-stu-id="4a3a1-117">D3D11\_BIND\_SHADER\_RESOURCE, \_RENDER\_TARGET, \_DEPTH\_STENCIL, or \_UNORDERED\_ACCESS.</span></span>

<span data-ttu-id="4a3a1-118">**Sem suporte:** \_ Buffer de constantes \_ , o \_ buffer de vértice \_ \[ Observe que a associação de um buffer de ladrilhos como SRV/UAV/RTV ainda é ok \] , \_ \_ buffer de índice, \_ \_ saída de fluxo, \_ \_ decodificador de associação ou \_ \_ codificador de vídeo de ligação \_ .</span><span class="sxs-lookup"><span data-stu-id="4a3a1-118">**NOT supported:** \_CONSTANT\_BUFFER, \_VERTEX\_BUFFER \[note that binding a tiled Buffer as an SRV/UAV/RTV is still ok\], \_INDEX\_BUFFER, \_STREAM\_OUTPUT, \_BIND\_DECODER, or \_BIND\_VIDEO\_ENCODER.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a1-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formatos com suporte**</span><span class="sxs-lookup"><span data-stu-id="4a3a1-119"><span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Supported Formats**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a1-120">Todos os formatos que devem estar disponíveis para determinada configuração, independentemente dela ser lado a lado, com algumas exceções.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-120">All formats that would be available for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a1-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc com suporte (contagem de multiamostras, qualidade)**</span><span class="sxs-lookup"><span data-stu-id="4a3a1-121"><span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Supported SampleDesc (Multisample count, quality)**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a1-122">Tudo o que seria suportado para a configuração fornecida, independentemente dela ser lado a lado, com algumas exceções.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-122">Whatever would be supported for the given configuration regardless of it being tiled, with some exceptions.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a1-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Largura/altura/MipLevels/matrizes com suporte**</span><span class="sxs-lookup"><span data-stu-id="4a3a1-123"><span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Supported Width/Height/MipLevels/ArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a1-124">Extensões completas com suporte do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-124">Full extents supported by Direct3D 11.</span></span> <span data-ttu-id="4a3a1-125">Os recursos em ladrilho não têm a restrição sobre o tamanho total da memória imposta em recursos que não são de lado do ladrilho.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-125">Tiled resources don't have the restriction on total memory size imposed on non-tiled resources.</span></span> <span data-ttu-id="4a3a1-126">Os recursos em ladrilhos são restritos pelos limites gerais de espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-126">Tiled resources are only constrained by overall virtual address space limits.</span></span> <span data-ttu-id="4a3a1-127">Para obter informações, consulte [espaço de endereço disponível para recursos em ladrilho](address-space-available-for-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="4a3a1-127">For info, see [Address space available for tiled resources](address-space-available-for-tiled-resources.md).</span></span>

</dd> </dl>

<span data-ttu-id="4a3a1-128">O conteúdo inicial da memória do pool de bloco é indefinido.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-128">The initial contents of tile pool memory are undefined.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a3a1-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a3a1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a3a1-130">Criando recursos em ladrilhos</span><span class="sxs-lookup"><span data-stu-id="4a3a1-130">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




