---
description: O ATM é aplicável a ambientes de LAN e WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Anexo do WINSOCK ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f55c71b830fa8a5f27f083af0263c62766e7b037e433c04b73bfea5ba12960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822442"
---
# <a name="winsock-atm-annex"></a>Anexo do WINSOCK ATM

O ATM é aplicável a ambientes de LAN e WAN. Uma rede de ATM transporta simultaneamente uma ampla variedade de tráfego de rede – voz, dados, imagem e vídeo. Ele fornece aos usuários uma qualidade de serviço garantida em uma base de VC (canal por virtual).



| Elemento          | Descrição                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nomes de protocolo | ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER                                                                                                                           |
| Descrição      | O ATM AAL5 fornece um serviço de transporte orientado a conexão, limite de mensagem preservado e QOS garantido. ATMPROTO \_ AALUSER é uma AAL definida pelo usuário. |
| Família de endereços   | AF \_ ATM                                                                                                                                                     |
| Arquivo de cabeçalho      | Ws2atm.h                                                                                                                                                    |



 

Esta seção descreve as extensões específicas do ATM (Modo de Transferência Assíncrona) necessárias para dar suporte aos serviços nativos do ATM conforme expostos e especificados na especificação UNI (Interface de Rede de Usuário) do Fórum do ATM versão 3.x (3.0 e 3.1). Este documento dá suporte ao tipo AAL 5 (modo de mensagem) e à AAL definida pelo usuário. Versões futuras deste documento darão suporte a outros tipos de AAL, bem como AO UNI 4.0.

 

 



