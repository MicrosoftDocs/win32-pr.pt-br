---
description: Permitem acompanhar os cartões dentro dos leitores. Essas rotinas normalmente usam a \_ estrutura do scartar ReaderState dentro de uma matriz.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Funções de controle de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829558"
---
# <a name="smart-card-tracking-functions"></a>Funções de controle de cartão inteligente

As funções a seguir permitem acompanhar os cartões dentro dos leitores. Essas rotinas normalmente usam a estrutura do [**scartar \_ ReaderState**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) dentro de uma matriz.



| Tópico                                                | Descrição                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Pesquise um cartão cuja [*cadeia de caracteres ATR*](../secgloss/a-gly.md) corresponda a um nome de cartão fornecido. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Bloquear a execução até que a disponibilidade atual dos cartões seja alterada.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Encerrar ações pendentes.                                                                                                         |



 

 

 
