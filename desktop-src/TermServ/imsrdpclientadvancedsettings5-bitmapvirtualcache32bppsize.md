---
title: Propriedade IMsRdpClientAdvancedSettings5 BitmapVirtualCache32BppSize
description: Define ou recupera o tamanho do arquivo de cache virtual para bitmaps de 32 bits por pixel (BPP).
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BitmapVirtualCache32BppSize
- Propriedade BitmapVirtualCache32BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade BitmapVirtualCache32BppSize
- Propriedade BitmapVirtualCache32BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade BitmapVirtualCache32BppSize
- Propriedade BitmapVirtualCache32BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade BitmapVirtualCache32BppSize
- Propriedade BitmapVirtualCache32BppSize Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade BitmapVirtualCache32BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d43de82b97e16fa36f83a5edde43712b2a9cbbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369436"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a><span data-ttu-id="1d5ca-112">Propriedade IMsRdpClientAdvancedSettings5:: BitmapVirtualCache32BppSize</span><span class="sxs-lookup"><span data-stu-id="1d5ca-112">IMsRdpClientAdvancedSettings5::BitmapVirtualCache32BppSize property</span></span>

<span data-ttu-id="1d5ca-113">Define ou recupera o tamanho do arquivo de cache virtual para bitmaps de 32 bits por pixel (BPP).</span><span class="sxs-lookup"><span data-stu-id="1d5ca-113">Sets or retrieves the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span>

<span data-ttu-id="1d5ca-114">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5ca-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d5ca-115">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="1d5ca-116">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1d5ca-116">Property value</span></span>

<span data-ttu-id="1d5ca-117">Define o tamanho do arquivo de cache virtual para bitmaps de 32 bpp, em megabytes (MB).</span><span class="sxs-lookup"><span data-stu-id="1d5ca-117">Sets the size of the virtual cache file for 32 bpp bitmaps, in megabytes (MB).</span></span> <span data-ttu-id="1d5ca-118">O valor máximo é 48 MB.</span><span class="sxs-lookup"><span data-stu-id="1d5ca-118">The maximum value is 48 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d5ca-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d5ca-119">Requirements</span></span>



| <span data-ttu-id="1d5ca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d5ca-120">Requirement</span></span> | <span data-ttu-id="1d5ca-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1d5ca-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5ca-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d5ca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1d5ca-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d5ca-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1d5ca-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d5ca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1d5ca-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d5ca-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1d5ca-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1d5ca-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d5ca-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d5ca-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1d5ca-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1d5ca-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d5ca-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d5ca-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1d5ca-130">IID</span><span class="sxs-lookup"><span data-stu-id="1d5ca-130">IID</span></span><br/>                      | <span data-ttu-id="1d5ca-131">IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="1d5ca-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d5ca-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d5ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5ca-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1d5ca-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1d5ca-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1d5ca-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1d5ca-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1d5ca-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1d5ca-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1d5ca-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





