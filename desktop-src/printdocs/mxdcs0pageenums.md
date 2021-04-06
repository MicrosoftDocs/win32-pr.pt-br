---
description: A \_ enumeração de \_ enumerações de página MXDC S0 \_ é usada para especificar tipos de recursos que podem ser associados a páginas em documentos XPS e que podem ser processados, ou passados não processados pelo conversor de documento XPS da Microsoft (MXDC) para sua saída.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Enumeração de MXDC_S0_PAGE_ENUMS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828309"
---
# <a name="mxdc_s0_page_enums-enumeration"></a><span data-ttu-id="a6ee2-103">\_Enumeração de \_ enumerações de página MXDC S0 \_</span><span class="sxs-lookup"><span data-stu-id="a6ee2-103">MXDC\_S0\_PAGE\_ENUMS enumeration</span></span>

<span data-ttu-id="a6ee2-104">A enumeração de **\_ \_ \_ enumerações de página MXDC S0** é usada para especificar tipos de recursos que podem ser associados a páginas em documentos XPS e que podem ser processados, ou passados não processados pelo conversor de documento XPS da Microsoft (MXDC) para sua saída.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-104">The **MXDC\_S0\_PAGE\_ENUMS** enumeration is used to specify types of resources that can be associated with pages in XPS documents and that can be processed, or passed unprocessed, by Microsoft XPS Document Converter (MXDC) to its output.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ee2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6ee2-105">Syntax</span></span>


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a><span data-ttu-id="a6ee2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a6ee2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a6ee2-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC do \_ recurso \_ ttf**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC\_RESOURCE\_TTF**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-108">Fonte TrueType ou OpenType.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-108">TrueType or OpenType font.</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ recurso \_ JPEG**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC\_RESOURCE\_JPEG**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-110">Imagem JPEG</span><span class="sxs-lookup"><span data-stu-id="a6ee2-110">JPEG image</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ png de recursos \_**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC\_RESOURCE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-112">Imagem PNG.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-112">PNG image.</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**\_recurso \_ TIFF do MXDC**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC\_RESOURCE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-114">Imagem TIFF.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-114">TIFF image.</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC de \_ recursos \_ WDP**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC\_RESOURCE\_WDP**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-116">Imagem de foto do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-116">Windows Media Photo image.</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_dicionário de recursos MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC\_RESOURCE\_DICTIONARY**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-118">Dicionário de recursos remotos que deve ser passado para a saída do MXDC não processado.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-118">Remote resource dictionary that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ perfil ICC do recurso MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC\_RESOURCE\_ICC\_PROFILE**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-120">Perfil ICC que deve ser passado para a saída do MXDC não processada.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-120">ICC profile that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**\_miniatura de \_ JPEG do recurso MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC\_RESOURCE\_JPEG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-122">Miniatura JPEG que deve ser passada para a saída do MXDC não processada.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-122">JPEG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**\_miniatura do \_ png do recurso MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC\_RESOURCE\_PNG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-124">Miniatura PNG que deve ser passada para a saída do MXDC não processada.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-124">PNG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="a6ee2-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ máximo do recurso \_**</span><span class="sxs-lookup"><span data-stu-id="a6ee2-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC\_RESOURCE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="a6ee2-126">A contagem máxima de recursos para validação.</span><span class="sxs-lookup"><span data-stu-id="a6ee2-126">The maximum resource count for validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6ee2-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6ee2-127">Remarks</span></span>

<span data-ttu-id="a6ee2-128">Essa enumeração é usada principalmente como o membro **dwResourceType** da estrutura [**MXDC \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="a6ee2-128">This enumeration is primarily used as the **dwResourceType** member of the [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ee2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6ee2-129">Requirements</span></span>



| <span data-ttu-id="a6ee2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ee2-130">Requirement</span></span> | <span data-ttu-id="a6ee2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a6ee2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ee2-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6ee2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ee2-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6ee2-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a6ee2-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6ee2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ee2-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6ee2-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a6ee2-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6ee2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ee2-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ee2-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




