---
title: Enumeração MrmPackagingMode (MrmResourceIndexer. h)
description: Define constantes que especificam que tipo de arquivo PRI deve ser criado por MrmCreateResourceFile e MrmCreateResourceFileInMemory.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Menus de enumeração MrmPackagingMode e outros recursos
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295796"
---
# <a name="mrmpackagingmode-enumeration"></a><span data-ttu-id="8466c-104">Enumeração MrmPackagingMode</span><span class="sxs-lookup"><span data-stu-id="8466c-104">MrmPackagingMode enumeration</span></span>

<span data-ttu-id="8466c-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="8466c-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8466c-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="8466c-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8466c-107">Define constantes que especificam que tipo de arquivo PRI deve ser criado por [**MrmCreateResourceFile**](mrmcreateresourcefile.md) e [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="8466c-107">Defines constants that specify what kind of PRI file(s) should be created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="8466c-108">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="8466c-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="8466c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8466c-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a><span data-ttu-id="8466c-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="8466c-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8466c-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span><span class="sxs-lookup"><span data-stu-id="8466c-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span></span>
</dt> <dd>

<span data-ttu-id="8466c-112">Especifica que um único arquivo PRI deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="8466c-112">Specifies that a single PRI file should be created.</span></span>

</dd> <dt>

<span data-ttu-id="8466c-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span><span class="sxs-lookup"><span data-stu-id="8466c-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span></span>
</dt> <dd>

<span data-ttu-id="8466c-114">Especifica que vários arquivos PRI devem ser criados; dividir automaticamente por todos os qualificadores com suporte (especificamente, idioma e escala).</span><span class="sxs-lookup"><span data-stu-id="8466c-114">Specifies that multiple PRI files should be created; split automatically by all supported qualifiers (specifically, language and scale).</span></span>

</dd> <dt>

<span data-ttu-id="8466c-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span><span class="sxs-lookup"><span data-stu-id="8466c-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span></span>
</dt> <dd>

<span data-ttu-id="8466c-116">Especifica que um arquivo PRI satélite de complemento deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="8466c-116">Specifies that an add-on satellite PRI file should be created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8466c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8466c-117">Requirements</span></span>



| <span data-ttu-id="8466c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8466c-118">Requirement</span></span> | <span data-ttu-id="8466c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8466c-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8466c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8466c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8466c-121">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="8466c-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8466c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8466c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8466c-123">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="8466c-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8466c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8466c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8466c-125"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="8466c-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8466c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8466c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8466c-127">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="8466c-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

