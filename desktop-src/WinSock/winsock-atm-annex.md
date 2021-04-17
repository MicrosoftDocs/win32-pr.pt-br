---
description: O ATM é aplicável a ambientes de LAN e WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Anexo ATM do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811727"
---
# <a name="winsock-atm-annex"></a>Anexo ATM do Winsock

O ATM é aplicável a ambientes de LAN e WAN. Uma rede ATM transporta simultaneamente uma ampla variedade de tráfego de rede: voz, dados, imagem e vídeo. Ele fornece aos usuários uma qualidade de serviço garantida em uma base de VC (por canal virtual).



| Elemento          | Descrição                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome (s) de protocolo | ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER                                                                                                                           |
| Description      | O ATM AAL5 fornece um serviço de transporte orientado por conexão, limite de mensagens preservado e QOS garantido. ATMPROTO \_ AALUSER é uma AAL definida pelo usuário. |
| Família de endereços   | \_ATM AF                                                                                                                                                     |
| Arquivo de cabeçalho      | Ws2atm. h                                                                                                                                                    |



 

Esta seção descreve as extensões específicas do modo de transferência assíncrona (ATM) necessárias para dar suporte aos serviços ATM nativos como expostos e especificados na especificação de UNI (interface de rede do usuário) do fórum do ATM versão 3. x (3,0 e 3,1). Este documento dá suporte a AAL tipo 5 (modo de mensagem) e AAL definida pelo usuário. As versões futuras deste documento irão dar suporte a outros tipos de AAL, bem como a UNI 4,0.

 

 



