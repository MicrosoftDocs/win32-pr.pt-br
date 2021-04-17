---
title: Códigos de erro específicos do WCS
description: Veja a seguir uma lista de códigos de erro que estão especificamente relacionados ao uso do WCS 1,0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3040f462ce226ebd3018070abc818884cee6ad6
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2021
ms.locfileid: "105790673"
---
# <a name="error-codes-specific-to-wcs"></a><span data-ttu-id="45695-103">Códigos de erro específicos do WCS</span><span class="sxs-lookup"><span data-stu-id="45695-103">Error Codes Specific To WCS</span></span>

<span data-ttu-id="45695-104">Veja a seguir uma lista de códigos de erro que estão especificamente relacionados ao uso do WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="45695-104">The following is a list of error codes that are specifically related to the use of WCS 1.0.</span></span> <span data-ttu-id="45695-105">Isso não significa que as funções WCS retornarão apenas esses códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="45695-105">This does not mean that WCS functions will return only these error codes.</span></span> <span data-ttu-id="45695-106">Isso significa que os códigos na tabela a seguir são retornados apenas pelas funções WCS.</span><span class="sxs-lookup"><span data-stu-id="45695-106">It means that the codes in the table below are returned only by WCS functions.</span></span> <span data-ttu-id="45695-107">Eles também podem retornar outros códigos de erro do Win32 que estão documentados em outro lugar na API do Win32 do SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="45695-107">They may also return other Win32 error codes that are documented elsewhere in the Win32 API of the Platform SDK.</span></span>

<dl> <dt>

<span data-ttu-id="45695-108"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERRO ao \_ excluir o \_ XFORM de ICM \_</span><span class="sxs-lookup"><span data-stu-id="45695-108"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERROR\_DELETING\_ICM\_XFORM</span></span>
</dt> <dd>

<span data-ttu-id="45695-109">Não foi possível excluir a transformação de cor especificada.</span><span class="sxs-lookup"><span data-stu-id="45695-109">The specified color transform could not be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="45695-110"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERRO \_ de \_ marca duplicada</span><span class="sxs-lookup"><span data-stu-id="45695-110"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERROR\_DUPLICATE\_TAG</span></span>
</dt> <dd>

<span data-ttu-id="45695-111">A marca do elemento do perfil de cor especificado já está presente no perfil de cores.</span><span class="sxs-lookup"><span data-stu-id="45695-111">The specified color profile element tag is already present in the color profile.</span></span>

</dd> <dt>

<span data-ttu-id="45695-112"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERRO \_ ICM \_ não \_ habilitado</span><span class="sxs-lookup"><span data-stu-id="45695-112"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERROR\_ICM\_NOT\_ENABLED</span></span>
</dt> <dd>

<span data-ttu-id="45695-113">O gerenciamento de cores de imagem não está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="45695-113">Image Color Management is not currently enabled.</span></span>

</dd> <dt>

<span data-ttu-id="45695-114"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERRO \_ \_ CMM inválido</span><span class="sxs-lookup"><span data-stu-id="45695-114"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERROR\_INVALID\_CMM</span></span>
</dt> <dd>

<span data-ttu-id="45695-115">O nome de arquivo especificado não se refere a um módulo de gerenciamento de cores válido.</span><span class="sxs-lookup"><span data-stu-id="45695-115">The specified file name does not refer to a valid color management module.</span></span>

</dd> <dt>

<span data-ttu-id="45695-116"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERRO \_ \_ COLORSPACE inválido</span><span class="sxs-lookup"><span data-stu-id="45695-116"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERROR\_INVALID\_COLORSPACE</span></span>
</dt> <dd>

<span data-ttu-id="45695-117">O espaço de cores especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="45695-117">The specified color space is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="45695-118"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERRO \_ de \_ perfil inválido</span><span class="sxs-lookup"><span data-stu-id="45695-118"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERROR\_INVALID\_PROFILE</span></span>
</dt> <dd>

<span data-ttu-id="45695-119">O nome de arquivo especificado não se refere a um perfil de cor válido.</span><span class="sxs-lookup"><span data-stu-id="45695-119">The specified file name does not refer to a valid color profile.</span></span>

</dd> <dt>

<span data-ttu-id="45695-120"><span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>\_transformação inválida de erro \_</span><span class="sxs-lookup"><span data-stu-id="45695-120"><span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERROR\_INVALID\_TRANSFORM</span></span> 
</dt> <dd>

<span data-ttu-id="45695-121">A transformação de cor especificada não é uma transformação de cor válida.</span><span class="sxs-lookup"><span data-stu-id="45695-121">The color transform that was specified is not a valid color transform.</span></span>

</dd> <dt>

<span data-ttu-id="45695-122"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>\_perfil \_ de erro não \_ associado \_ ao \_ dispositivo</span><span class="sxs-lookup"><span data-stu-id="45695-122"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="45695-123">O perfil de cor especificado não está associado a nenhum dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45695-123">The specified color profile is not associated with any device.</span></span>

</dd> <dt>

<span data-ttu-id="45695-124"><span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>Perfil de erro \_ \_ não \_ encontrado</span><span class="sxs-lookup"><span data-stu-id="45695-124"><span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>ERROR\_PROFILE\_NOT\_FOUND</span></span> 
</dt> <dd>

<span data-ttu-id="45695-125">O nome do arquivo do perfil de cor especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="45695-125">The specified color profile file name was not found.</span></span> <span data-ttu-id="45695-126">O nome do arquivo ou o caminho está incorreto.</span><span class="sxs-lookup"><span data-stu-id="45695-126">The file name or path is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="45695-127"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>marca de erro \_ \_ não \_ encontrada</span><span class="sxs-lookup"><span data-stu-id="45695-127"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>ERROR\_TAG\_NOT\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="45695-128">A marca do elemento de perfil de cor especificado não foi encontrada no perfil de cor.</span><span class="sxs-lookup"><span data-stu-id="45695-128">The specified color profile element tag was not found in the color profile.</span></span>

</dd> <dt>

<span data-ttu-id="45695-129"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>marca de erro \_ \_ não \_ presente</span><span class="sxs-lookup"><span data-stu-id="45695-129"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>ERROR\_TAG\_NOT\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="45695-130">Uma marca de elemento de perfil de cor que é necessária para que a função tenha êxito não foi passada para a função.</span><span class="sxs-lookup"><span data-stu-id="45695-130">A color profile element tag that is required for the function to succeed was not passed to the function.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="45695-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45695-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45695-132">Conceitos básicos de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="45695-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="45695-133">Constantes do WCS</span><span class="sxs-lookup"><span data-stu-id="45695-133">WCS Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




