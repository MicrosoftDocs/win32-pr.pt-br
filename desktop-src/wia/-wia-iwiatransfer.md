---
description: A interface IWiaTransfer fornece transferência de dados baseada em fluxo.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interface IWiaTransfer (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164528"
---
# <a name="iwiatransfer-interface"></a><span data-ttu-id="c734a-103">Interface IWiaTransfer</span><span class="sxs-lookup"><span data-stu-id="c734a-103">IWiaTransfer interface</span></span>

<span data-ttu-id="c734a-104">A interface **IWiaTransfer** fornece transferência de dados baseada em fluxo.</span><span class="sxs-lookup"><span data-stu-id="c734a-104">The **IWiaTransfer** interface provides stream-based transfer of data.</span></span>

## <a name="members"></a><span data-ttu-id="c734a-105">Membros</span><span class="sxs-lookup"><span data-stu-id="c734a-105">Members</span></span>

<span data-ttu-id="c734a-106">A interface **IWiaTransfer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c734a-106">The **IWiaTransfer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c734a-107">**IWiaTransfer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c734a-107">**IWiaTransfer** also has these types of members:</span></span>

-   [<span data-ttu-id="c734a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c734a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c734a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c734a-109">Methods</span></span>

<span data-ttu-id="c734a-110">A interface **IWiaTransfer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c734a-110">The **IWiaTransfer** interface has these methods.</span></span>



| <span data-ttu-id="c734a-111">Método</span><span class="sxs-lookup"><span data-stu-id="c734a-111">Method</span></span>                                                                 | <span data-ttu-id="c734a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c734a-112">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c734a-113">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="c734a-113">**Cancel**</span></span>](-wia-iwiatransfer-cancel.md)                             | <span data-ttu-id="c734a-114">Cancela a operação de transferência atual.</span><span class="sxs-lookup"><span data-stu-id="c734a-114">Cancels the current transfer operation.</span></span> <br/>                                         |
| [<span data-ttu-id="c734a-115">**Baixar**</span><span class="sxs-lookup"><span data-stu-id="c734a-115">**Download**</span></span>](-wia-iwiatransfer-download.md)                         | <span data-ttu-id="c734a-116">Inicia um download de dados para o chamador.</span><span class="sxs-lookup"><span data-stu-id="c734a-116">Initiates a data download to the caller.</span></span> <br/>                                        |
| [<span data-ttu-id="c734a-117">**\_Informações do formato EnumWIA \_**</span><span class="sxs-lookup"><span data-stu-id="c734a-117">**EnumWIA\_FORMAT\_INFO**</span></span>](-wia-iwiatransfer-enumwia-format-info.md) | <span data-ttu-id="c734a-118">Cria um enumerador para os formatos de transferência aos quais o dispositivo WIA 2,0 dá suporte.</span><span class="sxs-lookup"><span data-stu-id="c734a-118">Creates an enumerator for the transfer formats that the WIA 2.0 device supports.</span></span><br/> |
| [<span data-ttu-id="c734a-119">**Carregar**</span><span class="sxs-lookup"><span data-stu-id="c734a-119">**Upload**</span></span>](-wia-iwiatransfer-upload.md)                             | <span data-ttu-id="c734a-120">Inicia um carregamento de dados de um único item do chamador.</span><span class="sxs-lookup"><span data-stu-id="c734a-120">Initiates a data upload of a single item from the caller.</span></span> <br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="c734a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c734a-121">Remarks</span></span>

<span data-ttu-id="c734a-122">A interface **IWiaTransfer** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c734a-122">The **IWiaTransfer** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="c734a-123">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="c734a-123">IUnknown Methods</span></span>                                        | <span data-ttu-id="c734a-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="c734a-124">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c734a-125">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="c734a-125">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="c734a-126">Retorna ponteiros para interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="c734a-126">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="c734a-127">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="c734a-127">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="c734a-128">Incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="c734a-128">Increments reference count.</span></span>               |
| [<span data-ttu-id="c734a-129">IUnknown:: versão</span><span class="sxs-lookup"><span data-stu-id="c734a-129">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="c734a-130">Decrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="c734a-130">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="c734a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c734a-131">Requirements</span></span>



| <span data-ttu-id="c734a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c734a-132">Requirement</span></span> | <span data-ttu-id="c734a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c734a-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c734a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c734a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c734a-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c734a-135">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c734a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c734a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c734a-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c734a-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c734a-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c734a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c734a-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c734a-139"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="c734a-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="c734a-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c734a-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c734a-141"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="c734a-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c734a-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="c734a-143"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c734a-143"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
