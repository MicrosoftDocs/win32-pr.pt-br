---
title: Suporte para IP versão 6
description: A partir do IE7 e superior, o WinINet dá suporte a literais IPv6 no nome do host e ao componente de autoridade do URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Suporte para IP versão 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a024c792995780769a078c84b0493b7abba8647189fa2cee835d93dcb83770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113626"
---
# <a name="ip-version-6-support"></a>Suporte para IP versão 6

A partir do IE7 e superior, o WinINet dá suporte a literais IPv6 no nome do host e ao componente de autoridade do URI. O WinINet também dá suporte ao uso de literais IPv6 em partes relevantes do protocolo HTTP, como no cabeçalho local.

## <a name="hostname-ipv6-literals-and-uri-components"></a>Literais IPv6 do hostname e componentes URI

O WinINet implementa literais IPv6 de acordo com as especificações no RFC 3513. Conforme especificado nesta RFC, os literais IPv6 em um URI devem ser colocados entre colchetes. Por exemplo, https:// \[ :: 1 \] /é um URI IPv6 válido; o formulário sem colchetes ( https://::1/) não é válido. No entanto, os literais IPv6 do nome do host que não fazem parte do URI não precisam estar entre colchetes; ambos os formulários são aceitáveis para o WinINet. Por exemplo, ":: 1" e " \[ :: 1 \] " são formas aceitáveis de literais de nome de host IPv6. Outras APIs, como a API do WinSock, também aceitarão os dois formulários. Portanto, os aplicativos devem estar preparados para lidar com as duas formas de literais de nome de host IPv6.

## <a name="scope-id"></a>ID de escopo

O endereço IPv6 literal no URI pode incluir uma ID de escopo. Uma ID de escopo pode ser uma ID de interface como \[ FE80:: 1% 1 \] . O URI padrão, documentado em RFC 3986, não define a sintaxe para a ID do escopo e o URI é considerado não-uniforme quando a ID do escopo está presente. No entanto, o WinINet aceita uma ID de escopo no componente de autoridade do URI e no literal do nome do host IPv6.

O caractere de porcentagem (%) no endereço literal IPv6 deve ser de porcentagem de escape quando presente no URI. Por exemplo, a ID de escopo FE80:: 2% 3, deve aparecer no URI como "https:// \[ FE80:: 2% 253 \] /", em que %25 é o caractere de porcentagem codificada hexadecimal (%). Se o aplicativo recuperar o URI de uma API Unicode, como a API [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) do Winsock, o aplicativo deverá adicionar a versão de escape do caractere de porcentagem (%) no nome do host do URI. Para criar a versão de escape do URI, os aplicativos chamam [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) com o parâmetro *dwFlags* definido **como \_ \_ autoridade de escape ICU** e o nome de host IPv6 especificado na estrutura de componentes da URL especificada no parâmetro *lpUrlComponents* .

Para todas as operações de soquetes, o WinINet usa a ID de escopo. No entanto, como a ID do escopo tem apenas o significado do host local, ela não é enviada como parte dos cabeçalhos do protocolo HTTP na solicitação. Por exemplo, a chamada para [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) é chamada com a URL a seguir no parâmetro *lpszUrl* .

``` syntax
https://[fec0::2%251]:80/path.htm
```

A parte da ID do escopo da URL é removida pelo WinINet quando a solicitação HTTP é enviada para essa URL. A solicitação contém os seguintes cabeçalhos:

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. para implementações de servidor ou serviços, use [o Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 