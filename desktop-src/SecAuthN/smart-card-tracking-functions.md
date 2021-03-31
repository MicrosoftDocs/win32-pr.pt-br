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
# <a name="smart-card-tracking-functions"></a><span data-ttu-id="da156-104">Funções de controle de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="da156-104">Smart Card Tracking Functions</span></span>

<span data-ttu-id="da156-105">As funções a seguir permitem acompanhar os cartões dentro dos leitores.</span><span class="sxs-lookup"><span data-stu-id="da156-105">The following functions let you track cards within readers.</span></span> <span data-ttu-id="da156-106">Essas rotinas normalmente usam a estrutura do [**scartar \_ ReaderState**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) dentro de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="da156-106">These routines typically use the [**SCARD\_READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) structure within an array.</span></span>



| <span data-ttu-id="da156-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="da156-107">Topic</span></span>                                                | <span data-ttu-id="da156-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="da156-108">Description</span></span>                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da156-109">**SCardLocateCards**</span><span class="sxs-lookup"><span data-stu-id="da156-109">**SCardLocateCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | <span data-ttu-id="da156-110">Pesquise um cartão cuja [*cadeia de caracteres ATR*](../secgloss/a-gly.md) corresponda a um nome de cartão fornecido.</span><span class="sxs-lookup"><span data-stu-id="da156-110">Search for a card whose [*ATR string*](../secgloss/a-gly.md) matches a supplied card name.</span></span> |
| [<span data-ttu-id="da156-111">**SCardGetStatusChange**</span><span class="sxs-lookup"><span data-stu-id="da156-111">**SCardGetStatusChange**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | <span data-ttu-id="da156-112">Bloquear a execução até que a disponibilidade atual dos cartões seja alterada.</span><span class="sxs-lookup"><span data-stu-id="da156-112">Block execution until the current availability of cards changes.</span></span>                                                                       |
| [<span data-ttu-id="da156-113">**SCardCancel**</span><span class="sxs-lookup"><span data-stu-id="da156-113">**SCardCancel**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | <span data-ttu-id="da156-114">Encerrar ações pendentes.</span><span class="sxs-lookup"><span data-stu-id="da156-114">Terminate outstanding actions.</span></span>                                                                                                         |



 

 

 
