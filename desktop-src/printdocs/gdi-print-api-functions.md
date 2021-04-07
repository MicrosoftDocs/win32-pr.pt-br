---
description: Funções da API de impressão GDI
ms.assetid: cf3f4a61-8858-4c91-a778-d2a65998ef70
title: Funções da API de impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125e5feef16a64433dadd11e830a09241877a453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828208"
---
# <a name="gdi-print-api-functions"></a>Funções da API de impressão GDI

## <a name="in-this-section"></a>Nesta seção



| Função                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                     | A função [**AbortDoc**](/windows/desktop/api/wingdi/nf-wingdi-abortdoc) interrompe o trabalho de impressão atual e apaga tudo desenhado desde a última chamada para a função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                 |
| [*AbortProc*](/windows/desktop/api/Wingdi/nc-wingdi-abortproc)<br/>                                     | A função [**AbortProc**](/windows/desktop/api/wingdi/nc-wingdi-abortproc) é uma função de retorno de chamada definida pelo aplicativo usada com a função [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc) . Ele é chamado quando um trabalho de impressão deve ser cancelado durante o spool. O tipo **AbortProc** define um ponteiro para essa função de retorno de chamada. **AbortProc** é um espaço reservado para o nome da função definida pelo aplicativo.<br/> |
| [**DeviceCapabilities**](/windows/desktop/api/WinGdi/nf-wingdi-devicecapabilitiesa)<br/>                 | A função [**DeviceCapabilities**](/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera os recursos de um driver de impressora.<br/>                                                                                                                                                                                                                                                       |
| [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                         | A função [**EndDoc**](/windows/desktop/api/wingdi/nf-wingdi-enddoc) encerra um trabalho de impressão.<br/>                                                                                                                                                                                                                                                                                                             |
| [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                       | A função **EndPage** notifica o dispositivo que o aplicativo terminou de gravar em uma página. Normalmente, essa função é usada para direcionar o driver de dispositivo a avançar para uma nova página.<br/>                                                                                                                                                                             |
| [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape)<br/>                                         | permite que um aplicativo acesse os recursos de dispositivo definidos pelo sistema que não estão disponíveis por meio do GDI.<br/>                                                                                                                                                                                                                                                         |
| [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                   | A função [**ExtEscape**](/windows/desktop/api/wingdi/nf-wingdi-extescape) permite que um aplicativo acesse recursos do dispositivo que não estão disponíveis por meio do GDI.<br/>                                                                                                                                                                                                                                |
| [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md)<br/> | A função [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md) determina se a janela especificada é redirecionada no momento para impressão.<br/>                                                                                                                                                                                                         |
| [**Janela**](/windows/desktop/api/Winuser/nf-winuser-printwindow)<br/>                               | A [**função de cópia de impressão**](/windows/desktop/api/winuser/nf-winuser-printwindow) copia uma janela Visual para o contexto de dispositivo especificado (DC), normalmente um controlador de domínio de impressora.<br/>                                                                                                                                                                                                                              |
| [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)<br/>                             | A função [**SetAbortProc**](/windows/desktop/api/wingdi/nf-wingdi-setabortproc) define a função de anulação definida pelo aplicativo que permite que um trabalho de impressão seja cancelado durante o spool.<br/>                                                                                                                                                                                                               |
| [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                     | A função [**StartDoc**](/windows/desktop/api/wingdi/nf-wingdi-startdoca) inicia um trabalho de impressão.<br/>                                                                                                                                                                                                                                                                                                       |
| [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                   | A função [**Startpage**](/windows/desktop/api/wingdi/nf-wingdi-startpage) prepara o driver de impressora para aceitar dados.<br/>                                                                                                                                                                                                                                                                             |



 

 

