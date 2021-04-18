---
description: Aguardar funções de depuração
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Aguardar funções de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810927"
---
# <a name="wait-debugging-functions"></a>Aguardar funções de depuração

O Microsoft DirectShow fornece várias funções para depurar esperas infinitas.

Em compilações de varejo, as funções [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionam como suas contrapartes da API do Windows, **WaitForMultipleObjects** e **WaitForSingleObject**, com intervalos de tempo limite infinitos.

Em compilações de depuração, essas funções usam um valor de tempo limite global. Se o tempo limite expirar, a função acionará uma declaração. A chave do registro a seguir especifica o valor de tempo limite, em milissegundos:

**\_ \_ \\ <DebugRoot> \\ <Module Name> \\ tempo limite do computador local hKey**

em que *<DebugRoot>* é o caminho do registro descrito no tópico [depurar funções de saída](debug-output-functions.md).

Se a chave não existir, o valor de tempo limite padrão será infinito. Você pode usar a função [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) para substituir a entrada do registro.



| Função                                                       | Descrição                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Define o valor de tempo limite de depuração.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Aguarda que qualquer (ou todos) os objetos especificados sejam sinalizados. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Aguarda a um objeto ser sinalizado.                         |



 

 

 



