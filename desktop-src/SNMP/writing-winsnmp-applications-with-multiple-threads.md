---
title: Escrevendo aplicativos WinSNMP com vários threads
description: A implementação do Microsoft WinSNMP garante que as operações de WinSNMP de um processo não modifiquem as configurações de WinSNMP de outro processo.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6b7991968c5c5efafa898758c3c60cad1abb2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366320"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a><span data-ttu-id="8efd7-103">Escrevendo aplicativos WinSNMP com vários threads</span><span class="sxs-lookup"><span data-stu-id="8efd7-103">Writing WinSNMP Applications with Multiple Threads</span></span>

<span data-ttu-id="8efd7-104">A implementação do Microsoft WinSNMP garante que as operações de WinSNMP de um processo não modifiquem as configurações de WinSNMP de outro processo.</span><span class="sxs-lookup"><span data-stu-id="8efd7-104">The Microsoft WinSNMP implementation ensures that the WinSNMP operations of one process do not modify the WinSNMP settings of another process.</span></span>

<span data-ttu-id="8efd7-105">Um aplicativo WinSNMP com vários threads deve garantir que operações de WinSNMP que definem parâmetros de nível de aplicativo sejam thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8efd7-105">A WinSNMP application with multiple threads must ensure that WinSNMP operations that set application-level parameters are thread-safe.</span></span> <span data-ttu-id="8efd7-106">As funções que definem os parâmetros de nível de aplicativo são [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) e [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span><span class="sxs-lookup"><span data-stu-id="8efd7-106">The functions that set application-level parameters are [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) and [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span></span> <span data-ttu-id="8efd7-107">Essas funções modificam as configurações para o modo de tradução de contexto e entidade e o modo de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="8efd7-107">These functions modify settings for the entity and context translation mode and the retransmission mode.</span></span>

<span data-ttu-id="8efd7-108">Para obter mais informações, consulte [vários threads](/windows/desktop/ProcThread/multiple-threads) e [direitos de acesso e segurança de thread](/windows/desktop/ProcThread/thread-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="8efd7-108">For more information, see [Multiple Threads](/windows/desktop/ProcThread/multiple-threads) and [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).</span></span>

 

 