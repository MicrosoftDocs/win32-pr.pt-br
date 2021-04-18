---
description: Para criar extensões personalizadas ou para codificar uma extensão complexa, você pode escrever seus próprios manipuladores de extensão que exportam interfaces personalizadas.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Gravando manipuladores de extensão personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796365"
---
# <a name="writing-custom-extension-handlers"></a><span data-ttu-id="28147-103">Gravando manipuladores de extensão personalizados</span><span class="sxs-lookup"><span data-stu-id="28147-103">Writing Custom Extension Handlers</span></span>

<span data-ttu-id="28147-104">Para criar extensões personalizadas ou para codificar uma extensão complexa, você pode escrever seus próprios manipuladores de extensão que exportam interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="28147-104">To create custom extensions or to encode a complex extension, you can write your own extension handlers that export custom interfaces.</span></span> <span data-ttu-id="28147-105">Os serviços de certificados da Microsoft são fornecidos com as seguintes interfaces que podem ser usadas para codificar vários tipos de dados de extensão: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)e [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span><span class="sxs-lookup"><span data-stu-id="28147-105">Microsoft Certificate Services ships with the following interfaces which can be used to encode various types of extension data: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray), and [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span></span> <span data-ttu-id="28147-106">Essas interfaces estão contidas em Certenc.dll.</span><span class="sxs-lookup"><span data-stu-id="28147-106">These interfaces are contained in Certenc.dll.</span></span> <span data-ttu-id="28147-107">Além disso, as informações de tipo para essas interfaces estão contidas no Certencl.dll, que está contido no SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="28147-107">Additionally, the type information for these interfaces is contained in Certencl.dll, which is contained in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="28147-108">Para obter mais informações sobre manipuladores de extensão, consulte [manipuladores de extensão](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="28147-108">For more information about extension handlers, see [Extension Handlers](extension-handlers.md).</span></span>

 

 



