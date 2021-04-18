---
description: A interface IWiaUIExtension fornece métodos que substituem a interface do usuário do sistema padrão, fornecem um logotipo de bitmap de dispositivo personalizado e fornecem um ícone de dispositivo personalizado.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Interface IWiaUIExtension (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105795456"
---
# <a name="iwiauiextension-interface"></a><span data-ttu-id="d2dbd-103">Interface IWiaUIExtension</span><span class="sxs-lookup"><span data-stu-id="d2dbd-103">IWiaUIExtension interface</span></span>

<span data-ttu-id="d2dbd-104">A interface **IWiaUIExtension** fornece métodos que substituem a interface do usuário do sistema padrão, fornecem um logotipo de bitmap de dispositivo personalizado e fornecem um ícone de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="d2dbd-104">The **IWiaUIExtension** interface provides methods that replace the default system user interface, provide a custom device bitmap logo, and provide a custom device icon.</span></span>

## <a name="members"></a><span data-ttu-id="d2dbd-105">Membros</span><span class="sxs-lookup"><span data-stu-id="d2dbd-105">Members</span></span>

<span data-ttu-id="d2dbd-106">A interface **IWiaUIExtension** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d2dbd-106">The **IWiaUIExtension** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d2dbd-107">**IWiaUIExtension** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d2dbd-107">**IWiaUIExtension** also has these types of members:</span></span>

-   [<span data-ttu-id="d2dbd-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2dbd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d2dbd-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2dbd-109">Methods</span></span>

<span data-ttu-id="d2dbd-110">A interface **IWiaUIExtension** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d2dbd-110">The **IWiaUIExtension** interface has these methods.</span></span>



| <span data-ttu-id="d2dbd-111">Método</span><span class="sxs-lookup"><span data-stu-id="d2dbd-111">Method</span></span>                                                                  | <span data-ttu-id="d2dbd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2dbd-112">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2dbd-113">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="d2dbd-113">**DeviceDialog**</span></span>](-wia-iwiauiextension-devicedialog.md)               | <span data-ttu-id="d2dbd-114">Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="d2dbd-114">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="d2dbd-115">**GetDeviceBitmapLogo**</span><span class="sxs-lookup"><span data-stu-id="d2dbd-115">**GetDeviceBitmapLogo**</span></span>](-wia-iwiauiextension-getdevicebitmaplogo.md) | <span data-ttu-id="d2dbd-116">Obtém um logotipo de bitmap personalizado para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2dbd-116">Gets a custom bitmap logo for the device.</span></span><br/>                                         |
| [<span data-ttu-id="d2dbd-117">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="d2dbd-117">**GetDeviceIcon**</span></span>](-wia-iwiauiextension-getdeviceicon.md)             | <span data-ttu-id="d2dbd-118">Obtém um ícone de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="d2dbd-118">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="d2dbd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2dbd-119">Remarks</span></span>



| <span data-ttu-id="d2dbd-120">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2dbd-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="d2dbd-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2dbd-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="d2dbd-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="d2dbd-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="d2dbd-123">Retorna ponteiros para interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="d2dbd-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="d2dbd-124">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="d2dbd-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="d2dbd-125">Incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="d2dbd-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="d2dbd-126">IUnknown:: versão</span><span class="sxs-lookup"><span data-stu-id="d2dbd-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="d2dbd-127">Decrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="d2dbd-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="d2dbd-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2dbd-128">Requirements</span></span>



| <span data-ttu-id="d2dbd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2dbd-129">Requirement</span></span> | <span data-ttu-id="d2dbd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d2dbd-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2dbd-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2dbd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d2dbd-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d2dbd-132">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d2dbd-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2dbd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d2dbd-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2dbd-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d2dbd-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2dbd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2dbd-136"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2dbd-136"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
