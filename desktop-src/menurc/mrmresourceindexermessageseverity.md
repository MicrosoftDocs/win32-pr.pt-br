---
title: Enumeração MrmResourceIndexerMessageSeverity (MrmResourceIndexer. h)
description: Define constantes que especificam a severidade de uma mensagem do indexador de recursos. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: A4734256-94BD-43BE-B93C-55B98DF8A9BF
keywords:
- Menus de enumeração MrmResourceIndexerMessageSeverity e outros recursos
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessageSeverity
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdcbb42291ab88e91eca6c16c0a6c95c3e89fd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756327"
---
# <a name="mrmresourceindexermessageseverity-enumeration"></a><span data-ttu-id="b9c22-105">Enumeração MrmResourceIndexerMessageSeverity</span><span class="sxs-lookup"><span data-stu-id="b9c22-105">MrmResourceIndexerMessageSeverity enumeration</span></span>

<span data-ttu-id="b9c22-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b9c22-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b9c22-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b9c22-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b9c22-108">Define constantes que especificam a severidade de uma mensagem do indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9c22-108">Defines constants that specify the severity of an resource indexer message.</span></span> <span data-ttu-id="b9c22-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b9c22-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c22-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9c22-110">Syntax</span></span>


```C++
typedef enum _MrmResourceIndexerMessageSeverity { 
  MrmResourceIndexerMessageSeverityVerbose  = 1,
  MrmResourceIndexerMessageSeverityInfo     = 2,
  MrmResourceIndexerMessageSeverityWarning  = 3,
  MrmResourceIndexerMessageSeverityError    = 4
} MrmResourceIndexerMessageSeverity;
```



## <a name="constants"></a><span data-ttu-id="b9c22-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="b9c22-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b9c22-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span><span class="sxs-lookup"><span data-stu-id="b9c22-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span></span>
</dt> <dd>

<span data-ttu-id="b9c22-113">Indica que a mensagem é detalhada.</span><span class="sxs-lookup"><span data-stu-id="b9c22-113">Indicates that the message is verbose.</span></span>

</dd> <dt>

<span data-ttu-id="b9c22-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span><span class="sxs-lookup"><span data-stu-id="b9c22-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="b9c22-115">Indica que a mensagem é informativa.</span><span class="sxs-lookup"><span data-stu-id="b9c22-115">Indicates that the message is informational.</span></span>

</dd> <dt>

<span data-ttu-id="b9c22-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span><span class="sxs-lookup"><span data-stu-id="b9c22-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span></span>
</dt> <dd>

<span data-ttu-id="b9c22-117">Indica que a mensagem é um aviso.</span><span class="sxs-lookup"><span data-stu-id="b9c22-117">Indicates that the message is a warning.</span></span>

</dd> <dt>

<span data-ttu-id="b9c22-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span><span class="sxs-lookup"><span data-stu-id="b9c22-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span></span>
</dt> <dd>

<span data-ttu-id="b9c22-119">Indica que a mensagem é um erro.</span><span class="sxs-lookup"><span data-stu-id="b9c22-119">Indicates that the message is an error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9c22-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9c22-120">Requirements</span></span>



| <span data-ttu-id="b9c22-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9c22-121">Requirement</span></span> | <span data-ttu-id="b9c22-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b9c22-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c22-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9c22-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c22-124">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="b9c22-124">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b9c22-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9c22-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c22-126">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="b9c22-126">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b9c22-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9c22-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9c22-128"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9c22-128"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9c22-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9c22-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c22-130">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="b9c22-130">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

