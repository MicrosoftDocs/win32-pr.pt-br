---
title: Bluetooth e WSASetService
description: Bluetooth usa a função WSASetService para registrar ou remover uma instância de serviço no namespace Bluetooth (NS \_ BTH) do Registro.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- WSASetService Bluetooth
- Bluetooth e WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671e43636de67cee1e1c3c945a3647b5db59e7b0dd22b6eefd70b51f4977c31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004166"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth e WSASetService

Bluetooth usa a [**função WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar ou remover uma instância de serviço no namespace Bluetooth (NS \_ BTH) do Registro. O handle retornado por essa operação só pode ser usado para excluir o serviço.

Bluetooth tem dois meios de anunciar serviços usando a [**função WSASetService:**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)

-   O aplicativo pode fazer o sistema anunciar um registro de serviço SDP Bluetooth simples, construído de membros padrão na estrutura [**WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
-   O aplicativo pode fazer com que o sistema anunha seu próprio registro SDP Bluetooth passando uma estrutura [**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) no membro **lpBlob** da estrutura [**WSAQUERYSET.**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) Essa é uma abordagem mais complexa.

> [!Note]  
> Os registros SDP anunciados [**pelo WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) não persistem depois que o processo que os publicou foi encerrar.

 

O uso [**de WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) com Bluetooth tem os seguintes requisitos:

-   O *parâmetro lpqsRegInfo* é o endereço da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) a ser registrada.
-   O *parâmetro essOperation* é uma enumeração que contém uma das operações mostradas na tabela a seguir.



| Valor                  | Descrição                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| RNRSERVICE \_ REGISTER   | Começa a anunciar o serviço para consultas remotas usando o protocolo Bluetooth SDP. |
| RNRSERVICE \_ DEREGISTER | Não válido. Retorna um erro.                                                               |
| RNRSERVICE \_ DELETE     | Interrompe a publicidade do serviço.                                                             |



 

> [!Note]  
> Os alças de serviço descobertos durante uma [**chamada WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ou [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) são incompatíveis com a operação RNRSERVICE \_ DELETE.

 

-   O *parâmetro dwControlFlags* é reservado e deve ser zero.

Para obter mais informações e uma lista de Bluetooth de soquete, consulte [Bluetooth opções de soquete.](bluetooth-and-socket-options.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 