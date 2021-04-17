---
description: O spooler de impressão monitora os trabalhos de impressão atuais e a impressora de destino para determinar um horário apropriado para imprimir um trabalho.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Processador de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752814"
---
# <a name="print-processor"></a>Processador de impressão

O spooler de impressão monitora os trabalhos de impressão atuais e a impressora de destino para determinar um horário apropriado para imprimir um trabalho. Depois que o spooler determina que um trabalho deve ser impresso, ele chama o processador de impressão. O processador de impressão é um plug-in que processa os dados do trabalho de impressão.

Use as funções a seguir para trabalhar com processadores de impressão.



| Função                                                           | Descrição                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [**AddPrintProcessor**](addprintprocessor.md)                     | Instala um processador de impressão em um servidor especificado.                    |
| [**DeletePrintProcessor**](deleteprintprocessor.md)               | Remove um processador de impressora de um servidor especificado.                 |
| [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) | Enumera os tipos de dados aos quais um processador de impressão especificado dá suporte. |
| [**EnumPrintProcessors**](enumprintprocessors.md)                 | Enumera os processadores de impressão instalados em um servidor especificado.     |
| [**GetPrintProcessorDirectory**](getprintprocessordirectory.md)   | Recupera o caminho para o processador de impressão no servidor especificado.  |



 

 

 



