---
description: Funções de depuração de espera
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funções de depuração de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8f1de3d19ce7408625a5ab42f230d23ce401728e9fa7cf060edae62e19fcfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049196"
---
# <a name="wait-debugging-functions"></a>Funções de depuração de espera

O Microsoft DirectShow fornece várias funções para depurar esperas infinitas.

Em builds de varejo, as funções [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funcionam como suas contrapartes de API do Windows, **WaitForMultipleObjects** **e WaitForSingleObject,** com intervalos de tempo-out infinitos.

Em builds de depuração, essas funções usam um valor de tempo-out global. Se o tempo-expirar, a função disparará uma declaração. A seguinte chave do Registro especifica o valor de tempo-máximo, em milissegundos:

**HKEY \_ LOCAL \_ MACHINE \\ <DebugRoot> \\ <Module Name> \\ TIMEOUT**

em *<DebugRoot>* que é o caminho do Registro descrito no tópico Funções de Saída de [Depuração](debug-output-functions.md).

Se a chave não existir, o valor de tempo-out será padrão como INFINITE. Você pode usar a [**função DbgSetWaitTimeout**](dbgsetwaittimeout.md) para substituir a entrada do Registro.



| Função                                                       | Descrição                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Define o valor de tempo-máximo de depuração.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Aguarda que qualquer (ou todos) dos objetos especificados seja sinalizado. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Aguarda até que um objeto seja sinalizado.                         |



 

 

 



