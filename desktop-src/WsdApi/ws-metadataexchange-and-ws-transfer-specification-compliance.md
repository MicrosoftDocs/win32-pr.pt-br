---
description: Antes de agosto de 2006, WS-MetadataExchange definiu seu próprio método de troca de metadados, que foi usado pelo perfil de dispositivos para serviços Web (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Conformidade de especificação de WS-MetadataExchange e WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091274"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a><span data-ttu-id="da787-103">Conformidade de especificação de WS-MetadataExchange e WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="da787-103">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>

<span data-ttu-id="da787-104">Antes de agosto de 2006, o [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) definiu seu próprio método de troca de metadados [Get](get--metadata-exchange--http-request-and-message.md) , que foi usado pelo [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="da787-104">Before August 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) defined its own [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange method, which was used by [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="da787-105">A especificação de WS-MetadataExchange versão 1,1 substituiu esse método pelo método Get definido na especificação WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="da787-105">The WS-MetadataExchange specification version 1.1 replaced this method with the Get method defined in the WS-Transfer specification.</span></span>

<span data-ttu-id="da787-106">No modelo atual, WS-Transfer fornece o método [Get](get--metadata-exchange--http-request-and-message.md) e não faz nenhuma referência ao tipo do corpo.</span><span class="sxs-lookup"><span data-stu-id="da787-106">In the current model, WS-Transfer provides the [Get](get--metadata-exchange--http-request-and-message.md) method and makes no reference to the type of the body.</span></span> <span data-ttu-id="da787-107">WS-MetadataExchange descreve o formato do corpo e um mecanismo para empacotar várias partes de metadados em uma única resposta, e DPWS descreve partes específicas de metadados que um serviço deve incluir em uma resposta de metadados.</span><span class="sxs-lookup"><span data-stu-id="da787-107">WS-MetadataExchange describes the format of the body and a mechanism for packaging multiple pieces of metadata in a single response, and DPWS describes specific pieces of metadata that a service should include in a metadata response.</span></span>

<span data-ttu-id="da787-108">O WSDAPI não dá suporte completo à especificação de WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="da787-108">WSDAPI does not fully support the WS-Transfer specification.</span></span> <span data-ttu-id="da787-109">Como apenas o método [Get](get--metadata-exchange--http-request-and-message.md) é necessário para dispositivos, nenhuma outra parte do WS-Transfer foi implementada.</span><span class="sxs-lookup"><span data-stu-id="da787-109">Because only the [Get](get--metadata-exchange--http-request-and-message.md) method is required for devices, no other portions of WS-Transfer have been implemented.</span></span> <span data-ttu-id="da787-110">Além disso, o WSDAPI não implementa o método GetMetadata opcional descrito em WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="da787-110">Also, WSDAPI does not implement the optional GetMetadata method described in WS-MetadataExchange.</span></span>

 

 



