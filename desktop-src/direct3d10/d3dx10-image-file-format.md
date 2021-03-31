---
description: Formatos de arquivo de imagem com suporte pelas funções D3DXCreatexxx e D3DX10Savexxx.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: Enumeração de D3DX10_IMAGE_FILE_FORMAT (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664076"
---
# <a name="d3dx10_image_file_format-enumeration"></a><span data-ttu-id="b5f0c-103">\_Enumeração de \_ formato de arquivo de imagem D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="b5f0c-103">D3DX10\_IMAGE\_FILE\_FORMAT enumeration</span></span>

<span data-ttu-id="b5f0c-104">Formatos de arquivo de imagem com suporte pelas funções D3DXCreatexxx e D3DX10Savexxx.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-104">Image file formats supported by D3DXCreatexxx and D3DX10Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f0c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5f0c-105">Syntax</span></span>


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="b5f0c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b5f0c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b5f0c-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="b5f0c-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="b5f0c-108">Formato de arquivo de bitmap do Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="b5f0c-108">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="b5f0c-109">Contém um cabeçalho que descreve a resolução do dispositivo no qual o retângulo de pixels foi criado, as dimensões do retângulo, o tamanho da matriz de bits, uma paleta lógica e uma matriz de bits que define a relação entre os pixels na imagem de bitmap e as entradas na paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-109">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="b5f0c-110">A extensão de arquivo para esse formato é. bmp.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-110">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0c-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ IFF \_ jpg**</span><span class="sxs-lookup"><span data-stu-id="b5f0c-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="b5f0c-112">Formato de arquivo compactado JPEG (Joint Experts Group).</span><span class="sxs-lookup"><span data-stu-id="b5f0c-112">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="b5f0c-113">Especifica a compactação de variável de cores RGB de 24 bits e arquivos de documento de imagem TIFF de escala cinza de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-113">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="b5f0c-114">A extensão de arquivo para esse formato é. jpg.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-114">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0c-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ IFF \_ png**</span><span class="sxs-lookup"><span data-stu-id="b5f0c-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="b5f0c-116">Formato de arquivo PNG (Portable Network Graphics).</span><span class="sxs-lookup"><span data-stu-id="b5f0c-116">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="b5f0c-117">Um formato de bitmap não proprietário usando compactação sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-117">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="b5f0c-118">A extensão de arquivo para esse formato é. png.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-118">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0c-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="b5f0c-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="b5f0c-120">Formato de arquivo da superfície do DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="b5f0c-120">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="b5f0c-121">Armazena texturas, texturas de volume e mapas de ambiente cúbico, com ou sem os níveis de mipmap, e com ou sem a compactação de pixel.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-121">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="b5f0c-122">A extensão de arquivo para esse formato é. DDS.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-122">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0c-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10 \_ IFF \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="b5f0c-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="b5f0c-124">Formato TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="b5f0c-124">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="b5f0c-125">As extensões de arquivo para esse formato são. tif e. TIFF.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-125">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0c-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10 \_ IFF \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="b5f0c-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="b5f0c-127">Graphics Interchange Format (GIF). A extensão de arquivo para esse formato é. gif.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-127">Graphics Interchange Format (GIF).The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0c-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ IFF \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="b5f0c-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="b5f0c-129">Windows Media Photo Format (WMP).</span><span class="sxs-lookup"><span data-stu-id="b5f0c-129">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="b5f0c-130">Esse formato também é conhecido como HD Photo e JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-130">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="b5f0c-131">As extensões de arquivo para esse formato são. HDP,. jxr e. WDP.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-131">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="b5f0c-132">Para funcionar corretamente, o **D3DX10 \_ IFF \_ WMP** exige que você Inicialize com.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-132">To work properly, **D3DX10\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="b5f0c-133">Portanto, chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) em seu aplicativo antes de chamar D3DX.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-133">Therefore, call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="b5f0c-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b5f0c-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b5f0c-135">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-135">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b5f0c-136">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-136">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b5f0c-137">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-137">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5f0c-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5f0c-138">Remarks</span></span>

<span data-ttu-id="b5f0c-139">Consulte [tipos de bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obter mais informações sobre alguns desses formatos.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-139">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

<span data-ttu-id="b5f0c-140">O D3DX10 usa o Windows Imaging Component para implementar a maioria dos tipos de arquivo de bitmap com suporte.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-140">D3DX10 makes use of the Windows Imaging Component to implement the majority of the supported bitmap file types.</span></span> <span data-ttu-id="b5f0c-141">Consulte [visão geral do Windows Imaging Component](https://msdn.microsoft.com/library/ms737408.aspx) para obter informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="b5f0c-141">See [Windows Imaging Component Overview](https://msdn.microsoft.com/library/ms737408.aspx) for additional information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f0c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5f0c-142">Requirements</span></span>



| <span data-ttu-id="b5f0c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f0c-143">Requirement</span></span> | <span data-ttu-id="b5f0c-144">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f0c-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f0c-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5f0c-145">Header</span></span><br/> | <dl> <span data-ttu-id="b5f0c-146"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f0c-146"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f0c-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5f0c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f0c-148">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="b5f0c-148">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
