---
title: Escrevendo aplicativos WinSNMP com vários threads
description: A implementação do Microsoft WinSNMP garante que as operações winSNMP de um processo não modifiquem as configurações do WinSNMP de outro processo.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33ee400009204a1117eb54b8166ade2c10f3d1dd3317a8316d70fc8c2d606d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142729"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Escrevendo aplicativos WinSNMP com vários threads

A implementação do Microsoft WinSNMP garante que as operações winSNMP de um processo não modifiquem as configurações do WinSNMP de outro processo.

Um aplicativo WinSNMP com vários threads deve garantir que as operações winSNMP que definiam parâmetros no nível do aplicativo sejam thread-safe. As funções que configuram parâmetros no nível do aplicativo [**são SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) e [**SnmpSetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) Essas funções modificam as configurações para o modo de conversão de entidade e contexto e o modo de retransmissão.

Para obter mais informações, consulte [Multiple Threads](/windows/desktop/ProcThread/multiple-threads) and [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 