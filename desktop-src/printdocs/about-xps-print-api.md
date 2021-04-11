---
description: O XPS&\# 160; Imprimir&\# 160; A API fornece uma interface para o spooler de impressão que os aplicativos podem usar para imprimir trabalhos que enviam documentos XPS para uma impressora.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Sobre a API de impressão do XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091598"
---
# <a name="about-the-xps-print-api"></a>Sobre a API de impressão do XPS

A [API de impressão XPS](xps-printing.md) fornece uma interface para o spooler de impressão que os aplicativos podem usar para imprimir trabalhos que enviam documentos XPS para uma impressora.

Se a impressora de destino usar um driver de impressora XPSDrv, a API de impressão XPS possibilitará que o driver de impressora XPSDrv receba eventos de documento à medida que o spooler de impressão processar um trabalho de impressão. Para obter uma descrição dos eventos de documento que são enviados para o driver de impressora XPSDrv, consulte [eventos de documento do driver XPS](/windows-hardware/drivers/print/xps-driver-document-events).

Se a impressora de destino usar um driver de impressora GDI, a [API de impressão XPS](xps-printing.md) permitirá que o sistema manipule a conversão necessária dos dados de trabalho de impressão do formato XPS para o formato EMF (metarquivo avançado) que o driver de impressora GDI usa. Para obter uma descrição dos eventos de documento do driver de impressora GDI, consulte a [função DocumentEvent](documentevent.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a API de impressão XPS](using-the-xps-print-api.md)
</dt> <dt>

[Referência da API de impressão do XPS](xpsprint-api.md)
</dt> </dl>

 

 
