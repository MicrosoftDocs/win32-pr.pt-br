---
description: Define métodos para obter informações sobre as propriedades de um item de pesquisa. Essa interface tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Interface IItemPropertyBag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090048"
---
# <a name="iitempropertybag-interface"></a><span data-ttu-id="80173-104">Interface IItemPropertyBag</span><span class="sxs-lookup"><span data-stu-id="80173-104">IItemPropertyBag interface</span></span>

<span data-ttu-id="80173-105">Define métodos para obter informações sobre as propriedades de um item de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="80173-105">Defines methods to obtain information about the properties of a search item.</span></span> <span data-ttu-id="80173-106">Essa interface tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="80173-106">This interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="80173-107">Membros</span><span class="sxs-lookup"><span data-stu-id="80173-107">Members</span></span>

<span data-ttu-id="80173-108">A interface **IItemPropertyBag** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="80173-108">The **IItemPropertyBag** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="80173-109">**IItemPropertyBag** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="80173-109">**IItemPropertyBag** also has these types of members:</span></span>

-   [<span data-ttu-id="80173-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="80173-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="80173-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="80173-111">Methods</span></span>

<span data-ttu-id="80173-112">A interface **IItemPropertyBag** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="80173-112">The **IItemPropertyBag** interface has these methods.</span></span>



| <span data-ttu-id="80173-113">Método</span><span class="sxs-lookup"><span data-stu-id="80173-113">Method</span></span>                                                      | <span data-ttu-id="80173-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="80173-114">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="80173-115">[**Contarproperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80173-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span></span> | <span data-ttu-id="80173-116">Obtém uma contagem do número de propriedades no recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="80173-116">Gets a count of the number of properties in the property bag.</span></span><br/>                     |
| [<span data-ttu-id="80173-117">**GetPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="80173-117">**GetPropertyInfo**</span></span>](iitempropertybag-getpropertyinfo.md) | <span data-ttu-id="80173-118">Obtém as informações necessárias para ler ou salvar as propriedades no recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="80173-118">Gets the information required to read or save the properties in the property bag.</span></span><br/> |
| [<span data-ttu-id="80173-119">**Ler**</span><span class="sxs-lookup"><span data-stu-id="80173-119">**Read**</span></span>](iitempropertybag-read.md)                       | <span data-ttu-id="80173-120">Faz com que uma ou mais propriedades sejam lidas do recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="80173-120">Causes one or more properties to be read from the property bag.</span></span><br/>                   |
| [<span data-ttu-id="80173-121">**Gravar**</span><span class="sxs-lookup"><span data-stu-id="80173-121">**Write**</span></span>](iitempropertybag-write.md)                     | <span data-ttu-id="80173-122">Faz com que uma ou mais propriedades sejam salvas no recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="80173-122">Causes one or more properties to be saved into the property bag.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="80173-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="80173-123">Remarks</span></span>

<span data-ttu-id="80173-124">A interface **IItemPropertyBag** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="80173-124">The **IItemPropertyBag** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="80173-125">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **IItemPropertyBag** e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISEARCHITEM**](-search-isearchitem.md) , as estruturas [**LINKINFO**](-search-linkinfo.md) e [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="80173-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPropertyBag** interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="80173-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80173-126">Requirements</span></span>



| <span data-ttu-id="80173-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="80173-127">Requirement</span></span> | <span data-ttu-id="80173-128">Valor</span><span class="sxs-lookup"><span data-stu-id="80173-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80173-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80173-129">Minimum supported client</span></span><br/> | <span data-ttu-id="80173-130">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="80173-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="80173-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80173-131">Minimum supported server</span></span><br/> | <span data-ttu-id="80173-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="80173-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="80173-133">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="80173-133">Redistributable</span></span><br/>          | <span data-ttu-id="80173-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="80173-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
