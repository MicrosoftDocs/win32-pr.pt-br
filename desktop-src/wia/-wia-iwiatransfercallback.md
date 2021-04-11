---
description: A interface IWiaTransferCallback recebe retornos de chamada durante uma transferência de dados.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interface IWiaTransferCallback (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090501"
---
# <a name="iwiatransfercallback-interface"></a><span data-ttu-id="3ae62-103">Interface IWiaTransferCallback</span><span class="sxs-lookup"><span data-stu-id="3ae62-103">IWiaTransferCallback interface</span></span>

<span data-ttu-id="3ae62-104">A interface **IWiaTransferCallback** recebe retornos de chamada durante uma transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="3ae62-104">The **IWiaTransferCallback** interface receives callbacks during a data transfer.</span></span>

## <a name="members"></a><span data-ttu-id="3ae62-105">Membros</span><span class="sxs-lookup"><span data-stu-id="3ae62-105">Members</span></span>

<span data-ttu-id="3ae62-106">A interface **IWiaTransferCallback** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3ae62-106">The **IWiaTransferCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3ae62-107">**IWiaTransferCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3ae62-107">**IWiaTransferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="3ae62-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ae62-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3ae62-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ae62-109">Methods</span></span>

<span data-ttu-id="3ae62-110">A interface **IWiaTransferCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3ae62-110">The **IWiaTransferCallback** interface has these methods.</span></span>



| <span data-ttu-id="3ae62-111">Método</span><span class="sxs-lookup"><span data-stu-id="3ae62-111">Method</span></span>                                                                 | <span data-ttu-id="3ae62-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ae62-112">Description</span></span>                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="3ae62-113">**GetNextStream**</span><span class="sxs-lookup"><span data-stu-id="3ae62-113">**GetNextStream**</span></span>](-wia-iwiatransfercallback-getnextstream.md)       | <span data-ttu-id="3ae62-114">Obtém um novo fluxo para o item especificado.</span><span class="sxs-lookup"><span data-stu-id="3ae62-114">Gets a new stream for the specified item.</span></span> <br/>                    |
| [<span data-ttu-id="3ae62-115">**TransferCallback**</span><span class="sxs-lookup"><span data-stu-id="3ae62-115">**TransferCallback**</span></span>](-wia-iwiatransfercallback-transfercallback.md) | <span data-ttu-id="3ae62-116">Fornece o progresso e outras notificações durante uma transferência.</span><span class="sxs-lookup"><span data-stu-id="3ae62-116">Provides progress and other notifications during a transfer.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ae62-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ae62-117">Remarks</span></span>

<span data-ttu-id="3ae62-118">Os desenvolvedores de filtro de processamento de imagens devem implementar essa interface e a interface [**IWiaImageFilter**](-wia-iwiaimagefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="3ae62-118">Image processing filter developers should implement this interface and the [**IWiaImageFilter**](-wia-iwiaimagefilter.md) interface.</span></span>

<span data-ttu-id="3ae62-119">A interface **IWiaTransferCallback** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3ae62-119">The **IWiaTransferCallback** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="3ae62-120">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ae62-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="3ae62-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ae62-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3ae62-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="3ae62-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="3ae62-123">Retorna ponteiros para interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="3ae62-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="3ae62-124">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="3ae62-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="3ae62-125">Incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="3ae62-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="3ae62-126">IUnknown:: versão</span><span class="sxs-lookup"><span data-stu-id="3ae62-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="3ae62-127">Decrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="3ae62-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="3ae62-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ae62-128">Requirements</span></span>



| <span data-ttu-id="3ae62-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae62-129">Requirement</span></span> | <span data-ttu-id="3ae62-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3ae62-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae62-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ae62-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae62-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-132">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3ae62-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ae62-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae62-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ae62-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3ae62-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ae62-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ae62-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-136"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="3ae62-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="3ae62-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ae62-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-138"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="3ae62-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ae62-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ae62-140"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ae62-140"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
