---
description: Armazena informações sobre tipos de link e é usada pela interface IItemPreviewerExt.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Estrutura LINKINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164338"
---
# <a name="linkinfo-structure"></a><span data-ttu-id="ebd73-103">Estrutura LINKINFO</span><span class="sxs-lookup"><span data-stu-id="ebd73-103">LINKINFO structure</span></span>

<span data-ttu-id="ebd73-104">\[Só há suporte para **LINKINFO** e [**IITEMPREVIEWEREXT**](-search-iitempreviewerext.md) no Windows XP e no Windows Server 2003 e não deve mais ser usado.\]</span><span class="sxs-lookup"><span data-stu-id="ebd73-104">\[**LINKINFO** and [**IItemPreviewerExt**](-search-iitempreviewerext.md) are supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="ebd73-105">Armazena informações sobre tipos de link e é usada pela interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd73-105">Stores information about link types, and is used by the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd73-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebd73-106">Syntax</span></span>


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a><span data-ttu-id="ebd73-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ebd73-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ebd73-108">**tipo**</span><span class="sxs-lookup"><span data-stu-id="ebd73-108">**type**</span></span>
</dt> <dd>

<span data-ttu-id="ebd73-109">Tipo: **[ **LinkId**](-search-linktype.md)**</span><span class="sxs-lookup"><span data-stu-id="ebd73-109">Type: **[**LINKTYPE**](-search-linktype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ebd73-110">O tipo de link especificado ao rastrear ou indexar indicado por uma constante de [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd73-110">The type of link specified when crawling or indexing indicated by a [**LINKTYPE**](-search-linktype.md) constant.</span></span>

</dd> <dt>

<span data-ttu-id="ebd73-111">**bstrContentType**</span><span class="sxs-lookup"><span data-stu-id="ebd73-111">**bstrContentType**</span></span>
</dt> <dd>

<span data-ttu-id="ebd73-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ebd73-112">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ebd73-113">Um valor **BSTR** que especifica o tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ebd73-113">A **BSTR** value that specifies the content type.</span></span>

</dd> <dt>

<span data-ttu-id="ebd73-114">**bstrEncoding**</span><span class="sxs-lookup"><span data-stu-id="ebd73-114">**bstrEncoding**</span></span>
</dt> <dd>

<span data-ttu-id="ebd73-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ebd73-115">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ebd73-116">Um atributo encodingStyle especificado no arquivo WSDL (Web Services Description Language).</span><span class="sxs-lookup"><span data-stu-id="ebd73-116">An EncodingStyle attribute specified in the Web Services Description Language (WSDL) file.</span></span>

</dd> <dt>

<span data-ttu-id="ebd73-117">**bstrFileExt**</span><span class="sxs-lookup"><span data-stu-id="ebd73-117">**bstrFileExt**</span></span>
</dt> <dd>

<span data-ttu-id="ebd73-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ebd73-118">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ebd73-119">Um valor **BSTR** que especifica a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ebd73-119">A **BSTR** value that specifies the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="ebd73-120">**varData**</span><span class="sxs-lookup"><span data-stu-id="ebd73-120">**varData**</span></span>
</dt> <dd>

<span data-ttu-id="ebd73-121">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="ebd73-121">Type: **VARIANT**</span></span>

</dd> <dd>

<span data-ttu-id="ebd73-122">Uma variante que especifica o valor da variável.</span><span class="sxs-lookup"><span data-stu-id="ebd73-122">A variant that specifies the variable value.</span></span>

</dd> <dt>

<span data-ttu-id="ebd73-123">**dwRelatedParts**</span><span class="sxs-lookup"><span data-stu-id="ebd73-123">**dwRelatedParts**</span></span>
</dt> <dd>

<span data-ttu-id="ebd73-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ebd73-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ebd73-125">Um **DWORD** que especifica as partes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ebd73-125">A **DWORD** that specifies the related parts.</span></span>

</dd> <dt>

<span data-ttu-id="ebd73-126">**bstrRelatedCid**</span><span class="sxs-lookup"><span data-stu-id="ebd73-126">**bstrRelatedCid**</span></span>
</dt> <dd>

<span data-ttu-id="ebd73-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ebd73-127">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ebd73-128">Um valor **BSTR** que especifica uma propriedade CID, uma cadeia de caracteres decimal assinada não preenchida.</span><span class="sxs-lookup"><span data-stu-id="ebd73-128">A **BSTR** value that specifies a Cid property, a non-padded, signed decimal string.</span></span>

</dd> <dt>

<span data-ttu-id="ebd73-129">**lCodePage**</span><span class="sxs-lookup"><span data-stu-id="ebd73-129">**lCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="ebd73-130">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="ebd73-130">Type: **Long**</span></span>

</dd> <dd>

<span data-ttu-id="ebd73-131">A página de código a ser usada para codificar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ebd73-131">The code page to use for encoding the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebd73-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebd73-132">Remarks</span></span>

<span data-ttu-id="ebd73-133">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a estrutura **LINKINFO** e as seguintes APIs: os métodos [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd73-133">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKINFO** structure, and the following APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd73-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebd73-134">Requirements</span></span>



| <span data-ttu-id="ebd73-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd73-135">Requirement</span></span> | <span data-ttu-id="ebd73-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ebd73-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ebd73-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebd73-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd73-138">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="ebd73-138">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ebd73-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebd73-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd73-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ebd73-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ebd73-141">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ebd73-141">Redistributable</span></span><br/>          | <span data-ttu-id="ebd73-142">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="ebd73-142">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 




