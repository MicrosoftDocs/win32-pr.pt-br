---
description: Esta seção descreve as extensões do Winsock específicas para intercâmbio de pacotes de Internet/Intercâmbio de pacotes sequenciados (IPX/SPX). Ele também descreve aspectos de funções Winsock base que exigem uma consideração especial ou que podem apresentar comportamento exclusivo.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Anexo de IPX/SPX do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773009"
---
# <a name="winsock-ipxspx-annex"></a>Anexo de IPX/SPX do Winsock

Esta seção descreve as extensões do Winsock específicas para intercâmbio de pacotes de Internet/Intercâmbio de pacotes sequenciados (IPX/SPX). Ele também descreve aspectos de funções Winsock base que exigem uma consideração especial ou que podem apresentar comportamento exclusivo.



| Elemento          | Descrição                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome (s) de protocolo | IPX, SPX                                                                                                                                        |
| Description      | Fornece serviços de transporte pela camada de rede IPX: IPX para datagramas não confiáveis, SPX para fluxos de mensagens confiáveis e orientados a conexão. |
| Família de endereços   | \_IPX AF                                                                                                                                         |
| Arquivo de cabeçalho      | Wsipx. h                                                                                                                                         |



 

Esta seção discute como usar o Winsock com a família de protocolos IPX, permitindo que os aplicativos IPX tradicionais sejam portados para o Winsock. As redes IPX operam de maneira fundamentalmente diferente das redes IP, portanto, essas diferenças devem ser consideradas ao usar o IPX/SPX.

 

 



