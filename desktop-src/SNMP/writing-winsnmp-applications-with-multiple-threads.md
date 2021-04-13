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
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Escrevendo aplicativos WinSNMP com vários threads

A implementação do Microsoft WinSNMP garante que as operações de WinSNMP de um processo não modifiquem as configurações de WinSNMP de outro processo.

Um aplicativo WinSNMP com vários threads deve garantir que operações de WinSNMP que definem parâmetros de nível de aplicativo sejam thread-safe. As funções que definem os parâmetros de nível de aplicativo são [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) e [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Essas funções modificam as configurações para o modo de tradução de contexto e entidade e o modo de retransmissão.

Para obter mais informações, consulte [vários threads](/windows/desktop/ProcThread/multiple-threads) e [direitos de acesso e segurança de thread](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 