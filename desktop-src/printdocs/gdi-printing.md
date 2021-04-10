---
description: A API de impressão GDI fornece aplicativos com uma interface de impressão independente de dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API de impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169462"
---
# <a name="gdi-print-api"></a>API de impressão GDI

A API de impressão GDI fornece aplicativos com uma interface de impressão independente de dispositivo. Use essa interface se o aplicativo usar GDI para renderizar texto e elementos gráficos.

Se você escrever aplicativos para o Windows Vista ou versões posteriores do Windows, considere usar a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e a [API de impressão XPS](xps-printing.md) para usar as interfaces gráficas de alto desempenho com suporte nos drivers de impressão XPSDrv.

Esta seção fornece informações sobre os tópicos a seguir.



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre a API de impressão GDI](about-the-gdi-print-api.md)<br/>                                 | Uma visão geral da funcionalidade de impressão GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Usando a API de impressão GDI](using-the-printing-functions.md)<br/>                            | Informações sobre como usar a API de impressão GDI em um aplicativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Referência da API de impressão GDI](gdi-print-api-reference.md)<br/>                                 | Descrições detalhadas das funções, estruturas e outros elementos da API de impressão do GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Conversor de documento XPS da Microsoft (MXDC)](microsoft-xps-document-converter--mxdc-.md)<br/> | O [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) é um componente que permite que os aplicativos usem a API de impressão GDI com impressoras que têm um driver de impressão XPSDrv.<br/>                                                                                                                                                                                                                                                                                               |
| [Gravador de documento XPS da Microsoft (MXDW)](microsoft-xps-document-writer.md)<br/>              | O [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) fornece aplicativos com a funcionalidade "salvar como XPS" ou "exportar para XPS". Aplicativos que não criam conteúdo de documento XPS de forma nativa podem usar o MXDW para criar arquivos de documento XPS sem usar a [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). No entanto, a API de documento XPS fornece um aplicativo com a capacidade de usar as interfaces gráficas de alto desempenho com suporte nos drivers de impressão XPSDrv.<br/> |



 

O diagrama a seguir mostra a relação da API de impressão GDI com as outras APIs de impressão que um aplicativo pode usar.

![um diagrama que mostra a relação da API de impressão GDI com as outras APIs de impressão que um aplicativo Win32 pode usar](images/print-apis-gdi.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API de impressão XPS](xps-printing.md)
</dt> <dt>

[API do spooler de impressão](print-spooler-api.md)
</dt> <dt>

[API de tíquete de impressão](print-ticket-api.md)
</dt> </dl>

 

