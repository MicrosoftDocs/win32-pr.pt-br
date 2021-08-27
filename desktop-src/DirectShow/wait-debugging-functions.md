---
description: Aguardar funções de depuração
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Aguardar funções de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2aabec60a14ff36d74298a21d31c91b4bc6d94
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884025"
---
# <a name="wait-debugging-functions"></a>Aguardar funções de depuração

o Microsoft DirectShow fornece várias funções para depurar esperas infinitas.

em compilações de varejo, as funções [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionam como suas contrapartes de API Windows, **WaitForMultipleObjects** e **WaitForSingleObject**, com intervalos de tempo limite infinitos.

Em compilações de depuração, essas funções usam um valor de tempo limite global. Se o tempo limite expirar, a função acionará uma declaração. A chave do registro a seguir especifica o valor de tempo limite, em milissegundos:

**HKey \_ local \_ Machine \\ &lt; DebugRoot &gt; \\ <Module Name> \\ Timeout**

em que *&lt; DebugRoot &gt;* é o caminho do registro descrito no tópico [depurar funções de saída](debug-output-functions.md).

Se a chave não existir, o valor de tempo limite padrão será infinito. Você pode usar a função [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) para substituir a entrada do registro.



| Função                                                       | Descrição                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Define o valor de tempo limite de depuração.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Aguarda que qualquer (ou todos) os objetos especificados sejam sinalizados. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Aguarda a um objeto ser sinalizado.                         |



 

 

 



