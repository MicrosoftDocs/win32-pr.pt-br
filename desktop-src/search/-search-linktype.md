---
description: Especifica o tipo de link ao rastrear ou indexar.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Enumeração de LINKID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782465"
---
# <a name="linktype-enumeration"></a><span data-ttu-id="1a1ac-103">Enumeração de LINKID</span><span class="sxs-lookup"><span data-stu-id="1a1ac-103">LINKTYPE enumeration</span></span>

<span data-ttu-id="1a1ac-104">\[A enumeração **LinkId** só tem suporte no Windows XP e no windows Server 2003 e não deve mais ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="1a1ac-104">\[The **LINKTYPE** enumeration is supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="1a1ac-105">Especifica o tipo de link ao rastrear ou indexar.</span><span class="sxs-lookup"><span data-stu-id="1a1ac-105">Specifies the type of link when crawling or indexing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a1ac-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a1ac-106">Syntax</span></span>


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a><span data-ttu-id="1a1ac-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="1a1ac-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1a1ac-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**URL de LINKID \_**</span><span class="sxs-lookup"><span data-stu-id="1a1ac-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="1a1ac-109">Especifica se o tipo de link de URLs deve ser indexado.</span><span class="sxs-lookup"><span data-stu-id="1a1ac-109">Specifies whether the URLs link type should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="1a1ac-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**conteúdo de LINKtype \_**</span><span class="sxs-lookup"><span data-stu-id="1a1ac-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE\_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="1a1ac-111">Especifica se o conteúdo do link deve ser indexado.</span><span class="sxs-lookup"><span data-stu-id="1a1ac-111">Specifies whether the link content should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="1a1ac-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKtype \_ relacionado**</span><span class="sxs-lookup"><span data-stu-id="1a1ac-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE\_RELATED**</span></span>
</dt> <dd>

<span data-ttu-id="1a1ac-113">Especifica um link relacionado.</span><span class="sxs-lookup"><span data-stu-id="1a1ac-113">Specifies a related link.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a1ac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a1ac-114">Remarks</span></span>

<span data-ttu-id="1a1ac-115">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar os sinalizadores **LinkId** e as outras APIs a seguir: os métodos [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e a estrutura [**LINKINFO**](-search-linkinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1a1ac-115">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKTYPE** flags, and the following other APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKINFO**](-search-linkinfo.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a1ac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a1ac-116">Requirements</span></span>



| <span data-ttu-id="1a1ac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a1ac-117">Requirement</span></span> | <span data-ttu-id="1a1ac-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1a1ac-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a1ac-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a1ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1a1ac-120">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="1a1ac-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1a1ac-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a1ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1a1ac-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a1ac-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




