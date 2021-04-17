---
title: Propriedade IMsRdpClientAdvancedSettings8 BandwidthDetection
description: Especifica se as alterações de largura de banda são detectadas automaticamente.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BandwidthDetection
- Propriedade BandwidthDetection Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade BandwidthDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760128"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a><span data-ttu-id="3f2d1-106">Propriedade IMsRdpClientAdvancedSettings8:: BandwidthDetection</span><span class="sxs-lookup"><span data-stu-id="3f2d1-106">IMsRdpClientAdvancedSettings8::BandwidthDetection property</span></span>

<span data-ttu-id="3f2d1-107">Especifica se as alterações de largura de banda são detectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-107">Specifies if bandwidth changes are automatically detected.</span></span>

<span data-ttu-id="3f2d1-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f2d1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f2d1-109">Syntax</span></span>


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a><span data-ttu-id="3f2d1-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3f2d1-110">Property value</span></span>

<span data-ttu-id="3f2d1-111">**Variante \_ TRUE** se as alterações de largura de banda forem detectadas automaticamente ou **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3f2d1-111">**VARIANT\_TRUE** if bandwidth changes are automatically detected or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f2d1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f2d1-112">Requirements</span></span>



| <span data-ttu-id="3f2d1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f2d1-113">Requirement</span></span> | <span data-ttu-id="3f2d1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3f2d1-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2d1-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f2d1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3f2d1-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3f2d1-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="3f2d1-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f2d1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3f2d1-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f2d1-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="3f2d1-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3f2d1-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f2d1-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f2d1-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f2d1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3f2d1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f2d1-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f2d1-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f2d1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f2d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2d1-124">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3f2d1-124">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





