---
description: Interfaces de conexão MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de conexão MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011675"
---
# <a name="mtpbluetooth-connection-interfaces"></a><span data-ttu-id="030e9-103">Interfaces de conexão MTP/Bluetooth</span><span class="sxs-lookup"><span data-stu-id="030e9-103">MTP/Bluetooth Connection Interfaces</span></span>

<span data-ttu-id="030e9-104">As interfaces a seguir permitem que os aplicativos enumerem e se conectem somente a dispositivos que dão suporte ao MTP (protocolo de transferência de mídia) via Bluetooth (MTP/Bluetooth).</span><span class="sxs-lookup"><span data-stu-id="030e9-104">The following interfaces allow applications to enumerate and connect only to devices that support the Media Transfer Protocol (MTP) over Bluetooth (MTP/Bluetooth).</span></span> <span data-ttu-id="030e9-105">As interfaces de driver, coleção e cliente WPD não são restritas ao protocolo MTP/Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="030e9-105">The WPD driver-, collection-, and client-interfaces are not restricted to the MTP/ Bluetooth protocol.</span></span>



| <span data-ttu-id="030e9-106">Interface</span><span class="sxs-lookup"><span data-stu-id="030e9-106">Interface</span></span>                                                              | <span data-ttu-id="030e9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="030e9-107">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="030e9-108">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="030e9-108">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)       | <span data-ttu-id="030e9-109">Define um único método de retorno de chamada que os aplicativos usam para receber notificação de solicitações concluídas e canceladas.</span><span class="sxs-lookup"><span data-stu-id="030e9-109">Defines a single callback method that applications use to receive notification of completed and cancelled requests.</span></span> |
| [<span data-ttu-id="030e9-110">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="030e9-110">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md) | <span data-ttu-id="030e9-111">Enumera as interfaces **IPortableDeviceConnector** .</span><span class="sxs-lookup"><span data-stu-id="030e9-111">Enumerates **IPortableDeviceConnector** interfaces.</span></span>                                                                 |
| [<span data-ttu-id="030e9-112">**IPortableDeviceConnector**</span><span class="sxs-lookup"><span data-stu-id="030e9-112">**IPortableDeviceConnector**</span></span>](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | <span data-ttu-id="030e9-113">Dá suporte a métodos que os aplicativos chamam para estabelecer conexões com dispositivos Bluetooth MTP.</span><span class="sxs-lookup"><span data-stu-id="030e9-113">Supports methods that applications call to establish connections to MTP Bluetooth devices.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="030e9-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="030e9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="030e9-115">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="030e9-115">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



