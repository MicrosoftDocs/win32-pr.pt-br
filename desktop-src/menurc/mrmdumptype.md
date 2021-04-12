---
title: Enumeração MrmDumpType (MrmResourceIndexer. h)
description: Define constantes que especificam o tipo de despejo de arquivo PRI a ser produzido. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: 71E49F35-4B79-478A-A26A-C0D9A9FC2D11
keywords:
- Menus de enumeração MrmDumpType e outros recursos
topic_type:
- apiref
api_name:
- MrmDumpType
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff693f933af299d042b97de319fb221ac133a5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455291"
---
# <a name="mrmdumptype-enumeration"></a><span data-ttu-id="60522-105">Enumeração MrmDumpType</span><span class="sxs-lookup"><span data-stu-id="60522-105">MrmDumpType enumeration</span></span>

<span data-ttu-id="60522-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="60522-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="60522-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="60522-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="60522-108">Define constantes que especificam o tipo de despejo de arquivo PRI a ser produzido.</span><span class="sxs-lookup"><span data-stu-id="60522-108">Defines constants that specify the type of PRI file dump to produce.</span></span> <span data-ttu-id="60522-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="60522-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="60522-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="60522-110">Syntax</span></span>


```C++
typedef enum _MrmDumpType { 
  MrmDumpType_Basic     = 0,
  MrmDumpType_Detailed  = 1,
  MrmDumpType_Schema    = 2
} MrmDumpType;
```



## <a name="constants"></a><span data-ttu-id="60522-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="60522-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="60522-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType \_ básico**</span><span class="sxs-lookup"><span data-stu-id="60522-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType\_Basic**</span></span>
</dt> <dd>

<span data-ttu-id="60522-113">Especifica que o despejo deve ser básico.</span><span class="sxs-lookup"><span data-stu-id="60522-113">Specifies that the dump should be basic.</span></span>

</dd> <dt>

<span data-ttu-id="60522-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType \_ detalhado**</span><span class="sxs-lookup"><span data-stu-id="60522-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType\_Detailed**</span></span>
</dt> <dd>

<span data-ttu-id="60522-115">Especifica que o despejo deve ser detalhado.</span><span class="sxs-lookup"><span data-stu-id="60522-115">Specifies that the dump should be detailed.</span></span>

</dd> <dt>

<span data-ttu-id="60522-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**\_Esquema MrmDumpType**</span><span class="sxs-lookup"><span data-stu-id="60522-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**MrmDumpType\_Schema**</span></span>
</dt> <dd>

<span data-ttu-id="60522-117">Especifica que o despejo deve ser um esquema.</span><span class="sxs-lookup"><span data-stu-id="60522-117">Specifies that the dump should be a schema.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60522-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60522-118">Requirements</span></span>



| <span data-ttu-id="60522-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="60522-119">Requirement</span></span> | <span data-ttu-id="60522-120">Valor</span><span class="sxs-lookup"><span data-stu-id="60522-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60522-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60522-121">Minimum supported client</span></span><br/> | <span data-ttu-id="60522-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="60522-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="60522-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60522-123">Minimum supported server</span></span><br/> | <span data-ttu-id="60522-124">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="60522-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="60522-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60522-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="60522-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="60522-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60522-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="60522-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60522-128">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="60522-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

