---
description: Macros Assert e Breakpoint
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macros Assert e Breakpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087882"
---
# <a name="assert-and-breakpoint-macros"></a>Macros Assert e Breakpoint

As [classes base do DirectShow](directshow-base-classes.md) fornecem várias macros que executam asserções ou causam pontos de interrupção.



| Macro                                        | Descrição                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**DECLARAR**](assert.md)                     | Avalia uma expressão e exibe uma mensagem de diagnóstico se a expressão for **falsa**.                                         |
| [**DbgAssertAligned**](dbgassertaligned.md) | Testa se um ponteiro está alinhado a um limite especificado.                                                                        |
| [**DbgBreak**](dbgbreak.md)                 | Exibe uma caixa de mensagem com a cadeia de caracteres especificada, o nome do arquivo de origem e o número da linha.                                |
| [**EXECUTAR \_ declaração**](execute-assert.md)    | Avalia uma expressão em compilações de depuração e de varejo. Em builds de depuração, exibe uma mensagem de diagnóstico se a expressão for **false**. |
| [**KASSERT**](kassert.md)                   | Avalia uma expressão e causa uma exceção de ponto de interrupção se a expressão for **falsa**.                                         |
| [**KDbgBreak**](kdbgbreak.md)               | Causa uma exceção de ponto de interrupção e registra a cadeia de caracteres especificada.                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Utilitários de depuração](debugging-utilities.md)
</dt> </dl>

 

 



