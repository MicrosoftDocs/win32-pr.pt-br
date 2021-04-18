---
description: Fornece um método para invocar objetos ISearchItem.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Interface ISearchProtocolUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764447"
---
# <a name="isearchprotocolui-interface"></a><span data-ttu-id="22fd7-103">Interface ISearchProtocolUI</span><span class="sxs-lookup"><span data-stu-id="22fd7-103">ISearchProtocolUI interface</span></span>

<span data-ttu-id="22fd7-104">Fornece um método para invocar objetos [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="22fd7-104">Provides a method for invoking [**ISearchItem**](-search-isearchitem.md) objects.</span></span> <span data-ttu-id="22fd7-105">Os métodos nessa interface são chamados pelo host de protocolo ao processar URLs do gatherer.</span><span class="sxs-lookup"><span data-stu-id="22fd7-105">Methods in this interface are called by the protocol host when processing URLs from the gatherer.</span></span> <span data-ttu-id="22fd7-106">O manipulador de protocolo implementa o protocolo para acessar uma fonte de conteúdo em seu formato nativo, e essa interface implementa um manipulador de protocolo personalizado para expandir as fontes de dados que podem ser indexadas.</span><span class="sxs-lookup"><span data-stu-id="22fd7-106">The protocol handler implements the protocol for accessing a content source in its native format, and this interface implements a custom protocol handler to expand the data sources that can be indexed.</span></span>

## <a name="members"></a><span data-ttu-id="22fd7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="22fd7-107">Members</span></span>

<span data-ttu-id="22fd7-108">A interface **ISearchProtocolUI** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="22fd7-108">The **ISearchProtocolUI** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="22fd7-109">**ISearchProtocolUI** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="22fd7-109">**ISearchProtocolUI** also has these types of members:</span></span>

-   [<span data-ttu-id="22fd7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="22fd7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="22fd7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="22fd7-111">Methods</span></span>

<span data-ttu-id="22fd7-112">A interface **ISearchProtocolUI** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="22fd7-112">The **ISearchProtocolUI** interface has these methods.</span></span>



| <span data-ttu-id="22fd7-113">Método</span><span class="sxs-lookup"><span data-stu-id="22fd7-113">Method</span></span>                                                                       | <span data-ttu-id="22fd7-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="22fd7-114">Description</span></span>                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22fd7-115">**GetSearchItemForUrl**</span><span class="sxs-lookup"><span data-stu-id="22fd7-115">**GetSearchItemForUrl**</span></span>](-search-isearchprotocolui-getsearchitemforurl.md) | <span data-ttu-id="22fd7-116">Obtém o item de pesquisa para os dados especificados.</span><span class="sxs-lookup"><span data-stu-id="22fd7-116">Gets the search item for the data specified.</span></span> <span data-ttu-id="22fd7-117">Esse método é chamado uma vez para cada URL processada pelo gatherer e recupera um ponteiro para o objeto [**ISearchItem**](-search-isearchitem.md) .</span><span class="sxs-lookup"><span data-stu-id="22fd7-117">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="22fd7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="22fd7-118">Remarks</span></span>

<span data-ttu-id="22fd7-119">A interface **ISearchProtocolUI** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="22fd7-119">The **ISearchProtocolUI** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="22fd7-120">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **ISearchProtocolUI** e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="22fd7-120">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchProtocolUI** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="22fd7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22fd7-121">Requirements</span></span>



| <span data-ttu-id="22fd7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="22fd7-122">Requirement</span></span> | <span data-ttu-id="22fd7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="22fd7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22fd7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22fd7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="22fd7-125">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="22fd7-125">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="22fd7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22fd7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="22fd7-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22fd7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="22fd7-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="22fd7-128">Redistributable</span></span><br/>          | <span data-ttu-id="22fd7-129">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="22fd7-129">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
