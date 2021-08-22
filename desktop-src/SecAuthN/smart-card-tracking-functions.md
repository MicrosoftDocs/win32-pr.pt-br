---
description: Permitir que você acompanhe cartões em leitores. Essas rotinas normalmente usam a estrutura SCARD \_ READERSTATE dentro de uma matriz.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Funções de rastreamento de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b81ce357cf683d29c1a86d48993c16b7f363635b8e6e3c7e0f2a6ad0900f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917336"
---
# <a name="smart-card-tracking-functions"></a>Funções de rastreamento de cartão inteligente

As funções a seguir permitem que você acompanhe cartões em leitores. Essas rotinas normalmente usam a estrutura [**SCARD \_ READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) dentro de uma matriz.



| Tópico                                                | Descrição                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Pesquise um cartão cuja [*cadeia de caracteres ATR*](../secgloss/a-gly.md) corresponde a um nome de cartão fornecido. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Bloqueie a execução até que a disponibilidade atual dos cartões seja mudada.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Encerrar ações pendentes.                                                                                                         |



 

 

 
