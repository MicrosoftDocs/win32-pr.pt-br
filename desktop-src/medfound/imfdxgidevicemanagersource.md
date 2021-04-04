---
description: Fornece a funcionalidade para obter o IMFDXGIDeviceManager do coletor de renderização de vídeo Microsoft Media Foundation.
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: Interface IMFDXGIDeviceManagerSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647572"
---
# <a name="imfdxgidevicemanagersource-interface"></a><span data-ttu-id="be5de-103">Interface IMFDXGIDeviceManagerSource</span><span class="sxs-lookup"><span data-stu-id="be5de-103">IMFDXGIDeviceManagerSource interface</span></span>

<span data-ttu-id="be5de-104">Fornece a funcionalidade para obter o [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) do coletor de renderização de vídeo Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="be5de-104">Provides functionality for getting the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="members"></a><span data-ttu-id="be5de-105">Membros</span><span class="sxs-lookup"><span data-stu-id="be5de-105">Members</span></span>

<span data-ttu-id="be5de-106">A interface **IMFDXGIDeviceManagerSource** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be5de-106">The **IMFDXGIDeviceManagerSource** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be5de-107">**IMFDXGIDeviceManagerSource** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="be5de-107">**IMFDXGIDeviceManagerSource** also has these types of members:</span></span>

-   [<span data-ttu-id="be5de-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="be5de-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be5de-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="be5de-109">Methods</span></span>

<span data-ttu-id="be5de-110">A interface **IMFDXGIDeviceManagerSource** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="be5de-110">The **IMFDXGIDeviceManagerSource** interface has these methods.</span></span>



| <span data-ttu-id="be5de-111">Método</span><span class="sxs-lookup"><span data-stu-id="be5de-111">Method</span></span>                                                      | <span data-ttu-id="be5de-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="be5de-112">Description</span></span>                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be5de-113">**GetManager**</span><span class="sxs-lookup"><span data-stu-id="be5de-113">**GetManager**</span></span>](imfdxgidevicemanagersource-getmanager.md) | <span data-ttu-id="be5de-114">Obtém o [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) do coletor de renderização de vídeo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="be5de-114">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Media Foundation video rendering sink.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be5de-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be5de-115">Requirements</span></span>



| <span data-ttu-id="be5de-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="be5de-116">Requirement</span></span> | <span data-ttu-id="be5de-117">Valor</span><span class="sxs-lookup"><span data-stu-id="be5de-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be5de-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be5de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="be5de-119">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="be5de-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="be5de-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be5de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="be5de-121">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="be5de-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="be5de-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="be5de-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be5de-123"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be5de-123"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be5de-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="be5de-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5de-125">Interfaces Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be5de-125">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
