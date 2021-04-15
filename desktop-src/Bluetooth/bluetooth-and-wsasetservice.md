---
title: Bluetooth e WSASetService
description: O Bluetooth usa a função WSASetService para registrar ou remover uma instância de serviço no namespace do Bluetooth (NS \_ BTH) do registro.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth de Bluetooth
- WSASetService Bluetooth
- Bluetooth e Bluetooth WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454097"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth e WSASetService

O Bluetooth usa a função [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar ou remover uma instância de serviço no namespace do Bluetooth (ns \_ BTH) do registro. O identificador retornado por esta operação só pode ser usado para excluir o serviço.

O Bluetooth tem dois meios de anunciar serviços usando a função [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :

-   O aplicativo pode fazer com que o sistema anuncie um registro de serviço SDP simples de Bluetooth, construído a partir de membros padrão na estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .
-   O aplicativo pode fazer com que o sistema Anuncie seu próprio registro de SDP de Bluetooth passando uma estrutura de [**\_ \_ serviço BTH Set**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) no membro **lpBlob** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Essa é uma abordagem mais complexa.

> [!Note]  
> Os registros SDP anunciados pelo [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) não persistem depois que o processo que o publicou foi encerrado.

 

O uso de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) com Bluetooth tem os seguintes requisitos:

-   O parâmetro *lpqsRegInfo* é o endereço da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) a ser registrada.
-   O parâmetro *essOperation* é uma enumeração que contém uma das operações mostradas na tabela a seguir.



| Valor                  | Descrição                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| registro de RNRSERVICE \_   | Começa a anunciar o serviço para a consulta de rádios remotos usando o protocolo de SDP Bluetooth. |
| RNRSERVICE \_ Cancelar registro | Inválido. Retorna um erro.                                                               |
| RNRSERVICE \_ excluir     | Interrompe o anúncio do serviço.                                                             |



 

> [!Note]  
> Os identificadores de serviço descobertos durante uma chamada de [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ou [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) são incompatíveis com a operação de exclusão de RNRSERVICE \_ .

 

-   O parâmetro *dwControlFlags* é reservado e deve ser zero.

Para obter mais informações e uma lista de opções de soquete Bluetooth, consulte [Opções de soquete e Bluetooth](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 