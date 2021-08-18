---
title: Bluetooth e WSAAddressToString
description: a função WSAAddressToString Windows sockets é usada para converter um endereço de dispositivo Bluetooth em uma cadeia de caracteres, que, por sua vez, é fornecida para a função WSALookupServiceBegin por meio da estrutura WSAQUERYSET ao recuperar informações do serviço do dispositivo.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bb49563355b3a85ff64d7168f77e8526ca1679cffaa565e7b9cd7070cf87f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004276"
---
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth e WSAAddressToString

a função [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows sockets é usada para converter um endereço de dispositivo Bluetooth em uma cadeia de caracteres, que, por sua vez, é fornecida para a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) por meio da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) ao recuperar informações do serviço do dispositivo.

embora um endereço de dispositivo Bluetooth caiba em um buffer de 20 caracteres, a função [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) atualmente retorna **WSAEFAULT** para endereços de dispositivo Bluetooth, a menos que o buffer e o valor de *lpdwAddressStringLength* especificado sejam definidos como um comprimento de caractere de 40.

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

 

 