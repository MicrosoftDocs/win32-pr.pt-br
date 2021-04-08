---
description: A interface IWiaUIExtension2 fornece métodos que substituem a interface do usuário padrão fornecida pelo sistema por uma interface do usuário personalizada e que fornecem um ícone de dispositivo personalizado.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interface IWiaUIExtension2 (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920950"
---
# <a name="iwiauiextension2-interface"></a><span data-ttu-id="d4625-103">Interface IWiaUIExtension2</span><span class="sxs-lookup"><span data-stu-id="d4625-103">IWiaUIExtension2 interface</span></span>

<span data-ttu-id="d4625-104">A interface IWiaUIExtension2 fornece métodos que substituem a interface do usuário padrão fornecida pelo sistema por uma interface do usuário personalizada e que fornecem um ícone de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="d4625-104">The IWiaUIExtension2 interface provides methods that replace the default, system-supplied user interface with a custom user interface, and that provide a custom device icon.</span></span> <span data-ttu-id="d4625-105">Os fornecedores de dispositivos podem implementar essa interface para fornecer interfaces de usuário personalizadas para seus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d4625-105">Device vendors can implement this interface to provide custom user interfaces for their devices.</span></span>

## <a name="members"></a><span data-ttu-id="d4625-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d4625-106">Members</span></span>

<span data-ttu-id="d4625-107">A interface **IWiaUIExtension2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d4625-107">The **IWiaUIExtension2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d4625-108">**IWiaUIExtension2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d4625-108">**IWiaUIExtension2** also has these types of members:</span></span>

-   [<span data-ttu-id="d4625-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4625-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d4625-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4625-110">Methods</span></span>

<span data-ttu-id="d4625-111">A interface **IWiaUIExtension2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d4625-111">The **IWiaUIExtension2** interface has these methods.</span></span>



| <span data-ttu-id="d4625-112">Método</span><span class="sxs-lookup"><span data-stu-id="d4625-112">Method</span></span>                                                       | <span data-ttu-id="d4625-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4625-113">Description</span></span>                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4625-114">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="d4625-114">**DeviceDialog**</span></span>](-wia-iwiauiextension2-devicedialog.md)   | <span data-ttu-id="d4625-115">Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="d4625-115">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="d4625-116">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="d4625-116">**GetDeviceIcon**</span></span>](-wia-iwiauiextension2-getdeviceicon.md) | <span data-ttu-id="d4625-117">Obtém um ícone de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="d4625-117">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="d4625-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4625-118">Remarks</span></span>



| <span data-ttu-id="d4625-119">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4625-119">IUnknown Methods</span></span>                                        | <span data-ttu-id="d4625-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4625-120">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="d4625-121">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="d4625-121">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="d4625-122">Retorna ponteiros para interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="d4625-122">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="d4625-123">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="d4625-123">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="d4625-124">Incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="d4625-124">Increments reference count.</span></span>               |
| [<span data-ttu-id="d4625-125">IUnknown:: versão</span><span class="sxs-lookup"><span data-stu-id="d4625-125">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="d4625-126">Decrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="d4625-126">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="d4625-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4625-127">Requirements</span></span>



| <span data-ttu-id="d4625-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4625-128">Requirement</span></span> | <span data-ttu-id="d4625-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d4625-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4625-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4625-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d4625-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4625-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d4625-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4625-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d4625-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d4625-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d4625-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4625-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4625-135"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4625-135"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
