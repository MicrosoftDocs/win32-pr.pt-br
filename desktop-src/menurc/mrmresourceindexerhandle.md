---
title: Estrutura MrmResourceIndexerHandle (MrmResourceIndexer. h)
description: Representa um identificador opaco para um objeto indexador de recursos. O identificador é gerenciado pelo sistema operacional. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Menus de estrutura MrmResourceIndexerHandle e outros recursos
- Menus de ponteiro de estrutura PMrmResourceIndexerHandle e outros recursos
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5786585597b5d23a6f6c0cd6842b655727c3ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369912"
---
# <a name="mrmresourceindexerhandle-structure"></a><span data-ttu-id="0b293-107">Estrutura MrmResourceIndexerHandle</span><span class="sxs-lookup"><span data-stu-id="0b293-107">MrmResourceIndexerHandle structure</span></span>

<span data-ttu-id="0b293-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0b293-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b293-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0b293-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b293-110">Representa um identificador opaco para um objeto indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b293-110">Represents an opaque handle to a resource indexer object.</span></span> <span data-ttu-id="0b293-111">O identificador é gerenciado pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0b293-111">The handle is managed by the operating system.</span></span> <span data-ttu-id="0b293-112">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="0b293-112">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b293-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b293-113">Syntax</span></span>


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a><span data-ttu-id="0b293-114">Membros</span><span class="sxs-lookup"><span data-stu-id="0b293-114">Members</span></span>

<dl> <dt>

<span data-ttu-id="0b293-115">**processamento**</span><span class="sxs-lookup"><span data-stu-id="0b293-115">**handle**</span></span>
</dt> <dd>

<span data-ttu-id="0b293-116">Tipo: **pVoid**</span><span class="sxs-lookup"><span data-stu-id="0b293-116">Type: **PVOID**</span></span>

</dd> <dd>

<span data-ttu-id="0b293-117">Um identificador opaco para um objeto de indexador de recurso.</span><span class="sxs-lookup"><span data-stu-id="0b293-117">An opaque handle to a resource indexer object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b293-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b293-118">Requirements</span></span>



| <span data-ttu-id="0b293-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b293-119">Requirement</span></span> | <span data-ttu-id="0b293-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0b293-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b293-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b293-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0b293-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="0b293-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0b293-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b293-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0b293-124">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="0b293-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0b293-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b293-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b293-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b293-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b293-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b293-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b293-128">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="0b293-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

