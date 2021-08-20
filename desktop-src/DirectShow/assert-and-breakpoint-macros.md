---
description: Macros assert e breakpoint
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macros assert e breakpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f4f9782c96b62cad185899642e55760ac130cbbcd6515ac4cea0a5ec665821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001368"
---
# <a name="assert-and-breakpoint-macros"></a>Macros assert e breakpoint

As [DirectShow base fornecem](directshow-base-classes.md) várias macros que executam declarações ou causam pontos de interrupção.



| Macro                                        | Descrição                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Assert**](assert.md)                     | Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for **FALSE.**                                         |
| [**DbgAssertAligned**](dbgassertaligned.md) | Testa se um ponteiro está alinhado a um limite especificado.                                                                        |
| [**Dbgbreak**](dbgbreak.md)                 | Exibe uma caixa de mensagem com a cadeia de caracteres especificada, o nome do arquivo de origem e o número de linha especificados.                                |
| [**EXECUTE \_ ASSERT**](execute-assert.md)    | Avalia uma expressão em builds de depuração e varejo. Em builds de depuração, exibe uma mensagem de diagnóstico se a expressão for **FALSE.** |
| [**KASSERT**](kassert.md)                   | Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for **FALSE.**                                         |
| [**KDbgBreak**](kdbgbreak.md)               | Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada.                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Utilitários de depuração](debugging-utilities.md)
</dt> </dl>

 

 



