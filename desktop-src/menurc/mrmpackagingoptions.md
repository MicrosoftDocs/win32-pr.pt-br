---
title: Enumeração MrmPackagingOptions (MrmResourceIndexer. h)
description: Define constantes que especificam opções para o arquivo PRI criado por MrmCreateResourceFile e MrmCreateResourceFileInMemory.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- Menus de enumeração MrmPackagingOptions e outros recursos
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a8b2bee733fe17e91501fe295e5f80be159ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105793888"
---
# <a name="mrmpackagingoptions-enumeration"></a><span data-ttu-id="314a3-104">Enumeração MrmPackagingOptions</span><span class="sxs-lookup"><span data-stu-id="314a3-104">MrmPackagingOptions enumeration</span></span>

<span data-ttu-id="314a3-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="314a3-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="314a3-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="314a3-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="314a3-107">Define constantes que especificam opções para o arquivo PRI criado por [**MrmCreateResourceFile**](mrmcreateresourcefile.md) e [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="314a3-107">Defines constants that specify options for the PRI file created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="314a3-108">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="314a3-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="314a3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="314a3-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a><span data-ttu-id="314a3-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="314a3-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="314a3-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span><span class="sxs-lookup"><span data-stu-id="314a3-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span></span>
</dt> <dd>

<span data-ttu-id="314a3-112">Especifica nenhuma opção de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="314a3-112">Specifies no packaging options.</span></span>

</dd> <dt>

<span data-ttu-id="314a3-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span><span class="sxs-lookup"><span data-stu-id="314a3-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span></span>
</dt> <dd>

<span data-ttu-id="314a3-114">Especifica que um pacote de recursos sem esquema deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="314a3-114">Specifies that a schema-free resource pack should be created.</span></span>

</dd> <dt>

<span data-ttu-id="314a3-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span><span class="sxs-lookup"><span data-stu-id="314a3-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span></span>
</dt> <dd>

<span data-ttu-id="314a3-116">Especifica que o arquivo PRI deve ser dividido automaticamente por todos os qualificadores com suporte (especificamente, idioma e escala).</span><span class="sxs-lookup"><span data-stu-id="314a3-116">Specifies that the PRI file should be automatically split by all supported qualifiers (specifically, language and scale).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="314a3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="314a3-117">Requirements</span></span>



| <span data-ttu-id="314a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="314a3-118">Requirement</span></span> | <span data-ttu-id="314a3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="314a3-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314a3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="314a3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="314a3-121">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="314a3-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="314a3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="314a3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="314a3-123">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="314a3-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="314a3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="314a3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="314a3-125"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="314a3-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314a3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="314a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314a3-127">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="314a3-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

