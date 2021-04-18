---
description: A forma mais simples de e/s no Windows Sockets 2 é o bloqueio de e/s.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Bloqueando entrada/saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796094"
---
# <a name="blocking-inputoutput"></a>Bloqueando entrada/saída

A forma mais simples de e/s no Windows Sockets 2 é o bloqueio de e/s. Conforme mencionado nos [sinalizadores e modos de atributo de soquete](socket-attribute-flags-and-modes-2.md), os soquetes são criados no modo de bloqueio por padrão. Qualquer operação de e/s com um soquete de bloqueio não retornará até que a operação seja totalmente concluída. Assim, qualquer thread só pode executar uma operação de e/s por vez. Por exemplo, se um thread emitir uma operação de recebimento e nenhum dado estiver disponível no momento, o thread será bloqueado até que os dados se tornem disponíveis e sejam colocados no buffer do thread. Embora isso seja simples, não é necessariamente a maneira mais eficiente de executar e/s (Confira [pseudo-bloqueio e bloqueio real](pseudo-vs--true-blocking-2.md) para obter mais informações).

 

 



