---
title: Enumeração MrmPlatformVersion (MrmResourceIndexer. h)
description: Define constantes que especificam uma versão de plataforma. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: 7BA30B8F-FB23-4DCA-930D-099C7F8476E9
keywords:
- Menus de enumeração MrmPlatformVersion e outros recursos
topic_type:
- apiref
api_name:
- MrmPlatformVersion
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8127d3e6e99d974315327cf89ae9e82add7bc628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919092"
---
# <a name="mrmplatformversion-enumeration"></a><span data-ttu-id="90f64-105">Enumeração MrmPlatformVersion</span><span class="sxs-lookup"><span data-stu-id="90f64-105">MrmPlatformVersion enumeration</span></span>

<span data-ttu-id="90f64-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="90f64-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90f64-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="90f64-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90f64-108">Define constantes que especificam uma versão de plataforma.</span><span class="sxs-lookup"><span data-stu-id="90f64-108">Defines constants that specify a platform version.</span></span> <span data-ttu-id="90f64-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="90f64-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="90f64-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="90f64-110">Syntax</span></span>


```C++
typedef enum _MrmPlatformVersion { 
  MrmPlatformVersion_Default          = 0,
  MrmPlatformVersion_Windows10_0_0_0  = 0x010A0000,
  MrmPlatformVersion_Windows10_0_0_5  = 0x010A0005
} MrmPlatformVersion;
```



## <a name="constants"></a><span data-ttu-id="90f64-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="90f64-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="90f64-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="90f64-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="90f64-113">Especifica que a versão da plataforma é o padrão.</span><span class="sxs-lookup"><span data-stu-id="90f64-113">Specifies that the platform version is the default.</span></span>

</dd> <dt>

<span data-ttu-id="90f64-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion \_ Windows10 \_ 0 \_ 0 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="90f64-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion\_Windows10\_0\_0\_0**</span></span>
</dt> <dd>

<span data-ttu-id="90f64-115">Especifica uma versão de plataforma do Windows 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="90f64-115">Specifies a platform version of Windows 10.0.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="90f64-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion \_ Windows10 \_ 0 \_ 0 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="90f64-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion\_Windows10\_0\_0\_5**</span></span>
</dt> <dd>

<span data-ttu-id="90f64-117">Especifica uma versão de plataforma do Windows 10.0.0.5.</span><span class="sxs-lookup"><span data-stu-id="90f64-117">Specifies a platform version of Windows 10.0.0.5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90f64-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90f64-118">Requirements</span></span>



| <span data-ttu-id="90f64-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="90f64-119">Requirement</span></span> | <span data-ttu-id="90f64-120">Valor</span><span class="sxs-lookup"><span data-stu-id="90f64-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90f64-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90f64-121">Minimum supported client</span></span><br/> | <span data-ttu-id="90f64-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="90f64-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="90f64-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90f64-123">Minimum supported server</span></span><br/> | <span data-ttu-id="90f64-124">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="90f64-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="90f64-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90f64-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="90f64-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="90f64-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90f64-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="90f64-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90f64-128">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="90f64-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

