---
description: Fornece métodos para fornecer configurações do navegador. A interface IItemPreviewerExt tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Interface IItemPreviewerExt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920763"
---
# <a name="iitempreviewerext-interface"></a><span data-ttu-id="d834c-104">Interface IItemPreviewerExt</span><span class="sxs-lookup"><span data-stu-id="d834c-104">IItemPreviewerExt interface</span></span>

<span data-ttu-id="d834c-105">Fornece métodos para fornecer configurações do navegador.</span><span class="sxs-lookup"><span data-stu-id="d834c-105">Provides methods for supplying browser settings.</span></span> <span data-ttu-id="d834c-106">A interface **IItemPreviewerExt** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="d834c-106">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="d834c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d834c-107">Members</span></span>

<span data-ttu-id="d834c-108">A interface **IItemPreviewerExt** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d834c-108">The **IItemPreviewerExt** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d834c-109">**IItemPreviewerExt** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d834c-109">**IItemPreviewerExt** also has these types of members:</span></span>

-   [<span data-ttu-id="d834c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d834c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d834c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d834c-111">Methods</span></span>

<span data-ttu-id="d834c-112">A interface **IItemPreviewerExt** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d834c-112">The **IItemPreviewerExt** interface has these methods.</span></span>



| <span data-ttu-id="d834c-113">Método</span><span class="sxs-lookup"><span data-stu-id="d834c-113">Method</span></span>                                                                               | <span data-ttu-id="d834c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d834c-114">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d834c-115">**GetLinkedContent**</span><span class="sxs-lookup"><span data-stu-id="d834c-115">**GetLinkedContent**</span></span>](-search-iitempreviewerext-getlinkedcontent.md)               | <span data-ttu-id="d834c-116">Permite a extensão para o conteúdo avançado de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="d834c-116">Permits the extension to rich content for a property.</span></span> <br/>                            |
| [<span data-ttu-id="d834c-117">**GetRelatedPart**</span><span class="sxs-lookup"><span data-stu-id="d834c-117">**GetRelatedPart**</span></span>](-search-iitempreviewerext-getrelatedpart.md)                   | <span data-ttu-id="d834c-118">Obtém uma parte do corpo relacionado para inserir no fluxo de saída de MHTML.</span><span class="sxs-lookup"><span data-stu-id="d834c-118">Gets a related body part for embedding into the output MHTML stream.</span></span><br/>              |
| [<span data-ttu-id="d834c-119">**ProcessTransformCommand**</span><span class="sxs-lookup"><span data-stu-id="d834c-119">**ProcessTransformCommand**</span></span>](-search-iitempreviewerext-processtransformcommand.md) | <span data-ttu-id="d834c-120">Permite o processamento de um comando de transformação encontrado em um modelo de visualização.</span><span class="sxs-lookup"><span data-stu-id="d834c-120">Permits processing of a transformation command encountered in a preview template.</span></span><br/> |
| [<span data-ttu-id="d834c-121">**SuggestBrowserPolicy**</span><span class="sxs-lookup"><span data-stu-id="d834c-121">**SuggestBrowserPolicy**</span></span>](-search-iitempreviewerext-suggestbrowserpolicy.md)       | <span data-ttu-id="d834c-122">Sugere a política de segurança a ser aplicada ao navegador.</span><span class="sxs-lookup"><span data-stu-id="d834c-122">Suggests the security policy to be applied to the browser.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d834c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d834c-123">Remarks</span></span>

<span data-ttu-id="d834c-124">A interface **IItemPreviewerExt** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="d834c-124">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="d834c-125">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface **IItemPreviewerExt** e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="d834c-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPreviewerExt** interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d834c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d834c-126">Requirements</span></span>



| <span data-ttu-id="d834c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d834c-127">Requirement</span></span> | <span data-ttu-id="d834c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d834c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d834c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d834c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d834c-130">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="d834c-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d834c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d834c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d834c-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d834c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d834c-133">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d834c-133">Redistributable</span></span><br/>          | <span data-ttu-id="d834c-134">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d834c-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
