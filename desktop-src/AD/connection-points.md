---
title: Pontos de conexão
description: Um objeto de ponto de conexão contém dados sobre uma ou mais instâncias de um serviço disponível na rede.
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- pontos de conexão AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc61c4c5b7dd74626ab1f3884ad403cfa20b843
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007349"
---
# <a name="connection-points"></a>Pontos de conexão

Um objeto de ponto de conexão contém dados sobre uma ou mais instâncias de um serviço disponível na rede. A classe de objeto [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) é a classe base abstrata da qual os objetos que representam recursos conectáveis no Active Directory Domain Services são derivados. A ilustração a seguir mostra algumas das classes de objeto derivadas da classe de objeto **ConnectionPoint** .

![classes de objeto derivadas da classe de objeto ConnectionPoint](images/connection-points.png)

A tabela a seguir lista as subclasses imediatas da classe [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) .



| Classe de objeto                                                    | Descrição                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | Objetos de ponto de conexão de serviço (SCP) para publicar dados que os aplicativos cliente usam para associar a um serviço. Para obter mais informações, consulte [publicação com pontos de conexão de serviço (SCPs)](publishing-with-service-connection-points.md).                                                                               |
| [**rpcEntry**](/windows/desktop/ADSchema/c-rpcentry)                             | Uma classe abstrata cujas subclasses são usadas pelo NS (serviço de nomes RPC) acessado por meio das funções **RpcNs \*** na API do Win32. Para obter mais informações, consulte [publicando com o serviço de nomes RPC (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md).                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | Objeto de ponto de conexão usado pelo serviço de nome de RnR (registro e resolução do Windows Sockets), acessado por meio das APIs do **WSA \*** do Windows Sockets. Para obter mais informações, consulte [publicação com RNR (registro e resolução do Windows Sockets)](publishing-with-windows-sockets-registration-and-resolution.md). |
| [**printQueue**](/windows/desktop/ADSchema/c-printqueue)                         | Objeto de ponto de conexão usado para publicar impressoras de rede. Para obter mais informações, consulte [**IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue).                                                                                                                                                                                           |
| [**volume**](/windows/desktop/ADSchema/c-volume)                                 | Objeto de ponto de conexão usado para publicar serviços de arquivo.                                                                                                                                                                                                                                                                   |



 

Lembre-se de que os serviços baseados em COM não usam objetos de ponto de conexão para se anunciar. Esses serviços são publicados no repositório de classe. O armazenamento de classe do Windows 2000 é um repositório baseado em diretório para todos os aplicativos, interfaces e APIs baseados em COM, que fornecem publicação e atribuição de aplicativos. Para obter mais informações, consulte [publicando serviços com+](publishing-com-services.md).

 

 