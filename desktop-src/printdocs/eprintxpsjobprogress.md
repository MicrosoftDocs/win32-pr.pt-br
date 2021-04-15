---
description: Especifica o que o spooler está fazendo atualmente enquanto processa um trabalho de impressão XPS.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: Enumeração EPrintXPSJobProgress (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2a09b55ed72a6276a1a9d224cc08e03546f887d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506024"
---
# <a name="eprintxpsjobprogress-enumeration"></a><span data-ttu-id="0c228-103">Enumeração EPrintXPSJobProgress</span><span class="sxs-lookup"><span data-stu-id="0c228-103">EPrintXPSJobProgress enumeration</span></span>

<span data-ttu-id="0c228-104">Especifica o que o spooler está fazendo atualmente enquanto processa um trabalho de impressão XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-104">Specifies what the spooler is currently doing as it processes an XPS print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c228-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c228-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a><span data-ttu-id="0c228-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0c228-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0c228-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="0c228-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-108">Uma sequência de documento está prestes a ser adicionada ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-108">A document sequence is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span><span class="sxs-lookup"><span data-stu-id="0c228-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-110">Uma sequência de documento foi adicionada ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-110">A document sequence has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span><span class="sxs-lookup"><span data-stu-id="0c228-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-112">Um documento fixo está prestes a ser adicionado ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-112">A fixed document is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span><span class="sxs-lookup"><span data-stu-id="0c228-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-114">Um documento fixo foi adicionado ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-114">A fixed document has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span><span class="sxs-lookup"><span data-stu-id="0c228-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-116">Uma página está prestes a ser adicionada ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-116">A page is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span><span class="sxs-lookup"><span data-stu-id="0c228-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-118">Uma página foi adicionada ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-118">A page has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span><span class="sxs-lookup"><span data-stu-id="0c228-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-120">Um recurso foi adicionado ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-120">A resource had been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span><span class="sxs-lookup"><span data-stu-id="0c228-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-122">Uma fonte foi adicionada ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-122">A font has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span><span class="sxs-lookup"><span data-stu-id="0c228-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-124">Uma imagem foi adicionada ao trabalho XPS.</span><span class="sxs-lookup"><span data-stu-id="0c228-124">An image has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="0c228-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span><span class="sxs-lookup"><span data-stu-id="0c228-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span></span>
</dt> <dd>

<span data-ttu-id="0c228-126">Os dados do trabalho XPS foram confirmados.</span><span class="sxs-lookup"><span data-stu-id="0c228-126">The data for the XPS job has been committed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c228-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c228-127">Remarks</span></span>

<span data-ttu-id="0c228-128">Essa enumeração é usada principalmente como um parâmetro para a função [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="0c228-128">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

<span data-ttu-id="0c228-129">Esses valores podem se referir à fase de processamento ou de spool de um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="0c228-129">These values can refer to either the spooling or the rendering phase of a print job.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c228-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c228-130">Requirements</span></span>



| <span data-ttu-id="0c228-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c228-131">Requirement</span></span> | <span data-ttu-id="0c228-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0c228-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c228-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c228-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0c228-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c228-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0c228-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c228-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0c228-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c228-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0c228-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c228-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c228-138"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c228-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




