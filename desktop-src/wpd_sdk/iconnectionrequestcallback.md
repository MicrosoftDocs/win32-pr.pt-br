---
description: Define um único método de retorno de chamada.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interface IConnectionRequestCallback (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922829"
---
# <a name="iconnectionrequestcallback-interface"></a><span data-ttu-id="b522b-103">Interface IConnectionRequestCallback</span><span class="sxs-lookup"><span data-stu-id="b522b-103">IConnectionRequestCallback interface</span></span>

<span data-ttu-id="b522b-104">A interface **IConnectionRequestCallback** define um único método de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b522b-104">The **IConnectionRequestCallback** interface defines a single callback method.</span></span> <span data-ttu-id="b522b-105">Um aplicativo de dispositivos portáteis do Windows (WPD) implementa essa interface opcional de Component Object Model (COM) para receber notificações sobre solicitações concluídas e para cancelar solicitações pendentes.</span><span class="sxs-lookup"><span data-stu-id="b522b-105">A Windows Portable Devices (WPD) application implements this optional Component Object Model (COM) interface to receive notifications about completed requests and to cancel pending requests.</span></span> <span data-ttu-id="b522b-106">As solicitações são enviadas usando os métodos [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="b522b-106">The requests are sent using the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="members"></a><span data-ttu-id="b522b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b522b-107">Members</span></span>

<span data-ttu-id="b522b-108">A interface **IConnectionRequestCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b522b-108">The **IConnectionRequestCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b522b-109">**IConnectionRequestCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b522b-109">**IConnectionRequestCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="b522b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b522b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b522b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b522b-111">Methods</span></span>

<span data-ttu-id="b522b-112">A interface **IConnectionRequestCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b522b-112">The **IConnectionRequestCallback** interface has these methods.</span></span>



| <span data-ttu-id="b522b-113">Método</span><span class="sxs-lookup"><span data-stu-id="b522b-113">Method</span></span>                                                      | <span data-ttu-id="b522b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b522b-114">Description</span></span>                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b522b-115">**Por completo**</span><span class="sxs-lookup"><span data-stu-id="b522b-115">**OnComplete**</span></span>](iconnectionrequestcallback-oncomplete.md) | <span data-ttu-id="b522b-116">Notifica um aplicativo de que uma solicitação agendada anteriormente foi concluída.</span><span class="sxs-lookup"><span data-stu-id="b522b-116">Notifies an application that a previously scheduled request has completed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b522b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b522b-117">Requirements</span></span>



| <span data-ttu-id="b522b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b522b-118">Requirement</span></span> | <span data-ttu-id="b522b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b522b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b522b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b522b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b522b-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b522b-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="b522b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b522b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b522b-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b522b-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="b522b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b522b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b522b-125"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b522b-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="b522b-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="b522b-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b522b-127"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b522b-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="b522b-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b522b-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b522b-129"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b522b-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

