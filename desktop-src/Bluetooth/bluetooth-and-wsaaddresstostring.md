---
title: Bluetooth e WSAAddressToString
description: A função WSAAddressToString do Windows Sockets é usada para converter um endereço de dispositivo Bluetooth em uma cadeia de caracteres, que, por sua vez, é fornecida para a função WSALookupServiceBegin por meio da estrutura WSAQUERYSET ao recuperar informações do serviço de dispositivo.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007628"
---
# <a name="bluetooth-and-wsaaddresstostring"></a><span data-ttu-id="eb95f-103">Bluetooth e WSAAddressToString</span><span class="sxs-lookup"><span data-stu-id="eb95f-103">Bluetooth and WSAAddressToString</span></span>

<span data-ttu-id="eb95f-104">A função [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) do Windows Sockets é usada para converter um endereço de dispositivo Bluetooth em uma cadeia de caracteres, que, por sua vez, é fornecida para a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) por meio da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) ao recuperar informações do serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb95f-104">The [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets function is used to convert a Bluetooth Device Address to a string, which is in turn provided to the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function via the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure when retrieving device service information.</span></span>

<span data-ttu-id="eb95f-105">Embora um endereço de dispositivo Bluetooth caiba em um buffer de 20 caracteres, a função [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) atualmente retorna **WSAEFAULT** para endereços de dispositivo Bluetooth, a menos que o buffer e o valor de *lpdwAddressStringLength* especificado sejam definidos como um comprimento de caractere de 40.</span><span class="sxs-lookup"><span data-stu-id="eb95f-105">While a Bluetooth Device Address fits within a 20 character buffer, the [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) function currently returns **WSAEFAULT** for Bluetooth Device Addresses unless the buffer and the specified *lpdwAddressStringLength* value are set to a character length of 40.</span></span>

> [!Note]  
> <span data-ttu-id="eb95f-106">Quando **WSAEFAULT** é retornado por [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) como resultado de um buffer insuficiente, o parâmetro *lpdwAddressStringLength* não é atualizado com o tamanho do buffer necessário para a operação.</span><span class="sxs-lookup"><span data-stu-id="eb95f-106">When **WSAEFAULT** is returned by [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) as the result of an insufficient buffer, the *lpdwAddressStringLength* parameter is not updated with the buffer size required for the operation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eb95f-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb95f-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb95f-108">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="eb95f-108">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="eb95f-109">Bluetooth e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="eb95f-109">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="eb95f-110">Bluetooth e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="eb95f-110">Bluetooth and WSAQUERYSET</span></span>](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 