---
description: O XPS&\# 160; Imprimir&\# 160; A API fornece uma interface para o spooler de impressão que os aplicativos podem usar para imprimir trabalhos que enviam documentos XPS para uma impressora.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Sobre a API de Impressão XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e43c0bde59424c220e3d3ea9eab4b4780ace425cab28882013853a72d422815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950856"
---
# <a name="about-the-xps-print-api"></a>Sobre a API de Impressão XPS

A [API de Impressão XPS](xps-printing.md) fornece uma interface para o spooler de impressão que os aplicativos podem usar para imprimir trabalhos que enviam documentos XPS para uma impressora.

Se a impressora de destino usar um driver de impressora XPSDrv, a API de Impressão XPS possibilita que o driver de impressora XPSDrv receba eventos de documento à medida que o spooler de impressão processa um trabalho de impressão. Para ver uma descrição dos eventos de documento que são enviados para o driver de impressora XPSDrv, consulte [Eventos de documento do driver XPS.](/windows-hardware/drivers/print/xps-driver-document-events)

Se a impressora de destino usar um driver de impressora GDI, a API de Impressão [XPS](xps-printing.md) permitirá que o sistema manipular a conversão necessária dos dados de trabalho de impressão do formato XPS para o formato EMF (Metarquivo Avançado) que o driver de impressora GDI usa. Para ver uma descrição dos eventos de documento do driver de impressora GDI, consulte [Função DocumentEvent](documentevent.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a API de Impressão XPS](using-the-xps-print-api.md)
</dt> <dt>

[Referência da API de Impressão XPS](xpsprint-api.md)
</dt> </dl>

 

 
