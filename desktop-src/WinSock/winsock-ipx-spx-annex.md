---
description: esta seção descreve as extensões do Winsock específicas ao pacote de rede Exchange pacote/Sequenced Exchange (IPX/SPX). Ele também descreve aspectos de funções Winsock base que exigem uma consideração especial ou que podem apresentar comportamento exclusivo.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Anexo de IPX/SPX do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e5a97b90dc29f577bf2335b93a15fb3fb2c87c8362e0585151e1ac8b1e3393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051344"
---
# <a name="winsock-ipxspx-annex"></a>Anexo de IPX/SPX do Winsock

esta seção descreve as extensões do Winsock específicas ao pacote de rede Exchange pacote/Sequenced Exchange (IPX/SPX). Ele também descreve aspectos de funções Winsock base que exigem uma consideração especial ou que podem apresentar comportamento exclusivo.



| Elemento          | Descrição                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome (s) de protocolo | IPX, SPX                                                                                                                                        |
| Descrição      | Fornece serviços de transporte pela camada de rede IPX: IPX para datagramas não confiáveis, SPX para fluxos de mensagens confiáveis e orientados a conexão. |
| Família de endereços   | \_IPX AF                                                                                                                                         |
| Arquivo de cabeçalho      | Wsipx. h                                                                                                                                         |



 

Esta seção discute como usar o Winsock com a família de protocolos IPX, permitindo que os aplicativos IPX tradicionais sejam portados para o Winsock. As redes IPX operam de maneira fundamentalmente diferente das redes IP, portanto, essas diferenças devem ser consideradas ao usar o IPX/SPX.

 

 



