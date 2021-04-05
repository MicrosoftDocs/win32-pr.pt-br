---
description: Fornece métodos que definem a interação entre uma interface do usuário e os objetos de namespace de pesquisa criados pelo indexador.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Interface ISearchItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370622"
---
# <a name="isearchitem-interface"></a><span data-ttu-id="a703c-103">Interface ISearchItem</span><span class="sxs-lookup"><span data-stu-id="a703c-103">ISearchItem interface</span></span>

<span data-ttu-id="a703c-104">Fornece métodos que definem a interação entre uma interface do usuário e os objetos de namespace de pesquisa criados pelo indexador.</span><span class="sxs-lookup"><span data-stu-id="a703c-104">Provides methods that define interaction between a user interface (UI) and the Search namespace objects created by the indexer.</span></span>

## <a name="members"></a><span data-ttu-id="a703c-105">Membros</span><span class="sxs-lookup"><span data-stu-id="a703c-105">Members</span></span>

<span data-ttu-id="a703c-106">A interface **ISearchItem** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a703c-106">The **ISearchItem** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a703c-107">**ISearchItem** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a703c-107">**ISearchItem** also has these types of members:</span></span>

-   [<span data-ttu-id="a703c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a703c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a703c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a703c-109">Methods</span></span>

<span data-ttu-id="a703c-110">A interface **ISearchItem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a703c-110">The **ISearchItem** interface has these methods.</span></span>



| <span data-ttu-id="a703c-111">Método</span><span class="sxs-lookup"><span data-stu-id="a703c-111">Method</span></span>                                                         | <span data-ttu-id="a703c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a703c-112">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a703c-113">**GetParentFolder**</span><span class="sxs-lookup"><span data-stu-id="a703c-113">**GetParentFolder**</span></span>](-search-isearchitem-getparentfolder.md) | <span data-ttu-id="a703c-114">Obtém o objeto **ISearchItem** se a URL representa uma fonte de dados do Shell real (também conhecida como extensão de namespace do Shell).</span><span class="sxs-lookup"><span data-stu-id="a703c-114">Gets the **ISearchItem** object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span><br/> |
| <span data-ttu-id="a703c-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a703c-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span></span>     | <span data-ttu-id="a703c-116">Obtém o objeto da interface do usuário (UI) de **ISearchItem**.</span><span class="sxs-lookup"><span data-stu-id="a703c-116">Gets the user interface (UI) object of **ISearchItem**.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="a703c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a703c-117">Remarks</span></span>

<span data-ttu-id="a703c-118">O [**ISearchItem:: GetParentFolder**](-search-isearchitem-getparentfolder.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="a703c-118">The [**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="a703c-119">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **ISearchItem** e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI**](-search-isearchprotocolui.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="a703c-119">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchItem** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a703c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a703c-120">Requirements</span></span>



| <span data-ttu-id="a703c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a703c-121">Requirement</span></span> | <span data-ttu-id="a703c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a703c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a703c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a703c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a703c-124">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="a703c-124">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a703c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a703c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a703c-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a703c-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a703c-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a703c-127">Redistributable</span></span><br/>          | <span data-ttu-id="a703c-128">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="a703c-128">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
