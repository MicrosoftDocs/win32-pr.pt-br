---
description: O spooler de impressão monitora os trabalhos de impressão atuais e a impressora de destino para determinar um tempo apropriado para imprimir um trabalho.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Processador de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1250c617706b8e11309ffaf151fb09820ba1acbdb9f09d5cf44086e2153f8c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718616"
---
# <a name="print-processor"></a>Processador de impressão

O spooler de impressão monitora os trabalhos de impressão atuais e a impressora de destino para determinar um tempo apropriado para imprimir um trabalho. Depois que o spooler determina que um trabalho deve ser impresso, ele chama o processador de impressão. O processador de impressão é um plug-in que processa dados de trabalho de impressão.

Use as funções a seguir para trabalhar com processadores de impressão.



| Função                                                           | Descrição                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [**AddPrintProcessor**](addprintprocessor.md)                     | Instala um processador de impressão em um servidor especificado.                    |
| [**DeletePrintProcessor**](deleteprintprocessor.md)               | Remove um processador de impressora de um servidor especificado.                 |
| [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) | Enumera os tipos de dados aos quais um processador de impressão especificado dá suporte. |
| [**EnumPrintProcessors**](enumprintprocessors.md)                 | Enumera os processadores de impressão instalados em um servidor especificado.     |
| [**GetPrintProcessorDirectory**](getprintprocessordirectory.md)   | Recupera o caminho para o processador de impressão no servidor especificado.  |



 

 

 



