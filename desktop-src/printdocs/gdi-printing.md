---
description: A API de Impressão GDI fornece aos aplicativos uma interface de impressão independente do dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API de Impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc2a872b3a310ea44ddfc84103ddbd11cff61998d4884dca5f490e88c3d73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949187"
---
# <a name="gdi-print-api"></a>API de Impressão GDI

A API de Impressão GDI fornece aos aplicativos uma interface de impressão independente do dispositivo. Use essa interface se o aplicativo usar GDI para renderizar texto e elementos gráficos.

Se você escrever aplicativos para o Windows Vista ou versões posteriores do Windows, considere usar a API de Documento [XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e a API de Impressão [XPS](xps-printing.md) para usar as interfaces gráficas de alto desempenho com suporte dos drivers de impressão XPSDrv.

Esta seção fornece informações sobre os tópicos a seguir.



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre a API de Impressão GDI](about-the-gdi-print-api.md)<br/>                                 | Uma visão geral da funcionalidade de impressão GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Usando a API de Impressão GDI](using-the-printing-functions.md)<br/>                            | Informações sobre como usar a API de Impressão GDI em um aplicativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Referência da API de Impressão GDI](gdi-print-api-reference.md)<br/>                                 | Descrições detalhadas das funções, estruturas e outros elementos da API de Impressão GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md)<br/> | O [MXDC (Microsoft XPS Document Converter)](microsoft-xps-document-converter--mxdc-.md) é um componente que permite que os aplicativos usem a API de Impressão GDI com impressoras que têm um Driver de Impressão XPSDrv.<br/>                                                                                                                                                                                                                                                                                               |
| [MXDW (Microsoft XPS Document Writer)](microsoft-xps-document-writer.md)<br/>              | O [MXDW (Microsoft XPS Document Writer)](microsoft-xps-document-writer.md) fornece aplicativos com a funcionalidade "salvar como XPS" ou "exportar para XPS". Aplicativos que não criam conteúdo de documento XPS de forma nativa podem usar o MXDW para criar arquivos de documento XPS sem usar a [API de Documento XPS.](/previous-versions/windows/desktop/dd316976(v=vs.85)) No entanto, a API de Documento XPS fornece um aplicativo com a capacidade de usar as interfaces gráficas de alto desempenho com suporte dos drivers de impressão XPSDrv.<br/> |



 

O diagrama a seguir mostra a relação da API de Impressão GDI com as outras APIs de impressão que um aplicativo pode usar.

![um diagrama que mostra a relação da API de impressão gdi com as outras APIs de impressão que um aplicativo win32 pode usar](images/print-apis-gdi.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[API de Documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API de Impressão XPS](xps-printing.md)
</dt> <dt>

[API do Spooler de Impressão](print-spooler-api.md)
</dt> <dt>

[API de Tíquete de Impressão](print-ticket-api.md)
</dt> </dl>

 

