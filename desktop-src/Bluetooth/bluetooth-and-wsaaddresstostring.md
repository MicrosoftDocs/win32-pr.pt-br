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
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth e WSAAddressToString

A função [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) do Windows Sockets é usada para converter um endereço de dispositivo Bluetooth em uma cadeia de caracteres, que, por sua vez, é fornecida para a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) por meio da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) ao recuperar informações do serviço de dispositivo.

Embora um endereço de dispositivo Bluetooth caiba em um buffer de 20 caracteres, a função [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) atualmente retorna **WSAEFAULT** para endereços de dispositivo Bluetooth, a menos que o buffer e o valor de *lpdwAddressStringLength* especificado sejam definidos como um comprimento de caractere de 40.

> [!Note]  
> Quando **WSAEFAULT** é retornado por [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) como resultado de um buffer insuficiente, o parâmetro *lpdwAddressStringLength* não é atualizado com o tamanho do buffer necessário para a operação.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 