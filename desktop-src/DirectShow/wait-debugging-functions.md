---
description: Aguardar funções de depuração
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Aguardar funções de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8f1de3d19ce7408625a5ab42f230d23ce401728e9fa7cf060edae62e19fcfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049196"
---
# <a name="wait-debugging-functions"></a>Aguardar funções de depuração

o Microsoft DirectShow fornece várias funções para depurar esperas infinitas.

em compilações de varejo, as funções [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionam como suas contrapartes de API Windows, **WaitForMultipleObjects** e **WaitForSingleObject**, com intervalos de tempo limite infinitos.

Em compilações de depuração, essas funções usam um valor de tempo limite global. Se o tempo limite expirar, a função acionará uma declaração. A chave do registro a seguir especifica o valor de tempo limite, em milissegundos:

**\_ \_ \\ <DebugRoot> \\ <Module Name> \\ tempo limite do computador local hKey**

em que *<DebugRoot>* é o caminho do registro descrito no tópico [depurar funções de saída](debug-output-functions.md).

Se a chave não existir, o valor de tempo limite padrão será infinito. Você pode usar a função [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) para substituir a entrada do registro.



| Função                                                       | Descrição                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Define o valor de tempo limite de depuração.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Aguarda que qualquer (ou todos) os objetos especificados sejam sinalizados. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Aguarda a um objeto ser sinalizado.                         |



 

 

 



