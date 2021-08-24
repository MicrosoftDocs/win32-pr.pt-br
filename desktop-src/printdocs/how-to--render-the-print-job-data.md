---
description: Este tópico descreve como renderizar os dados do programa a serem impressos.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Como: renderizar dados de trabalho de impressão'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70724cc9dee6b7d3bb0434f08e3db959acfecfc54bc4ebafac5f5a3c6bd4b014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825126"
---
# <a name="how-to-render-print-job-data"></a>Como: renderizar dados de trabalho de impressão

Este tópico descreve como renderizar os dados do programa a serem impressos. Este tópico não explica em detalhes como renderizar imagens de texto ou gráficos específicos. Em vez disso, ele descreve como gerenciar os dados do programa e renderizá-los como um documento XPS, que ele envia para uma impressora usando a [API de impressão XPS](xps-printing.md).

## <a name="overview"></a>Visão geral

Renderizar dados de trabalho de impressão para impressão envolve pegar os dados específicos do programa, como texto, imagens e formatação, e convertê-los em um formato compatível com a impressora de destino. O programa que envia os dados para a impressora deve enviá-lo no formato que o driver de impressora requer.

Use a [API de impressão XPS](xps-printing.md) para enviar os dados para a impressora e ela exige que os dados sejam formatados como um documento XPS. Para produzir o conteúdo do documento XPS que a API de impressão XPS precisa, o programa de exemplo usa a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).

Se o conteúdo do programa estiver em um formato que não seja compatível com uma impressora, ele precisará ser renderizado antes de ser enviado para a impressora. Se o programa usar a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para gerenciar o conteúdo do programa, o conteúdo do programa estará em um formato que pode ser enviado diretamente para a [API de impressão do XPS](xps-printing.md) e não exigirá nenhuma renderização adicional antes de enviá-lo para a impressora.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API de impressão XPS](xps-printing.md)
</dt> </dl>

 

 
