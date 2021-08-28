---
description: As funções a seguir são usadas com o tratamento de erros.
ms.assetid: ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5
title: Funções de tratamento de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60fdc25327bed4966336571c20580b0bfdc22b38858d3edad560359eaf0710e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912756"
---
# <a name="error-handling-functions"></a>Funções de tratamento de erros

As funções a seguir são usadas com o tratamento de erros.



| Função                                                 | Descrição                                                                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Emita**](/windows/win32/api/utilapiset/nf-utilapiset-beep)                                     | Gera tons simples no palestrante.                                                                                        |
| [**CaptureStackbackTrace**](/previous-versions/windows/desktop/legacy/bb204633(v=vs.85))   | Captura um rastreamento regressivo de pilha percorrendo a pilha e registrando as informações de cada quadro.                             |
| [**FatalAppExit**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-fatalappexita)                     | Exibe uma caixa de mensagem e encerra o aplicativo quando a caixa de mensagem é fechada.                                         |
| [**FlashWindow**](/windows/desktop/api/Winuser/nf-winuser-flashwindow)                       | Pisca a janela especificada uma vez.                                                                                        |
| [**FlashWindowEx**](/windows/desktop/api/Winuser/nf-winuser-flashwindowex)                   | Pisca a janela especificada.                                                                                                 |
| [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)                   | Formata uma cadeia de caracteres de mensagem.                                                                                                     |
| [**GetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode)                     | Recupera o modo de erro para o processo atual.                                                                             |
| [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)                     | Recupera o valor do código do último erro do thread de chamada.                                                                         |
| [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode)         | Recupera o modo de erro para o thread de chamada.                                                                              |
| [**MessageBeep**](/windows/desktop/api/WinUser/nf-winuser-messagebeep)                       | Reproduz um som de formato de onda.                                                                                                       |
| [**RtlLookupFunctionEntry**](/windows/desktop/api/WinNT/nf-winnt-rtllookupfunctionentry) | Pesquisa as tabelas de funções ativas em busca de uma entrada que corresponda ao valor de PC especificado.                                  |
| [**RtlNtStatusToDosError**](/windows/desktop/api/Winternl/nf-winternl-rtlntstatustodoserror)   | Recupera o código de erro do sistema que corresponde ao código de erro NT especificado.                                              |
| [**RtlPcToFileHeader**](/windows/desktop/api/WinNT/nf-winnt-rtlpctofileheader)           | Recupera o endereço base da imagem que contém o valor de PC especificado.                                                 |
| [**RtlUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind)                           | Inicia um desenrolamento de quadros de chamada de procedimento.                                                                                 |
| [**RtlUnwind2**](/windows/desktop/api/WinNT/nf-winnt-rtlunwind2)                         | Inicia um desenrolamento de quadros de chamada de procedimento.                                                                                 |
| [**RtlUnwindEx**](/windows/desktop/api/WinNT/nf-winnt-rtlunwindex)                       | Inicia um desenrolamento de quadros de chamada de procedimento.                                                                                 |
| [**RtlVirtualUnwind**](/windows/desktop/api/WinNT/nf-winnt-rtlvirtualunwind)             | Recupera o contexto de invocação da função que precede o contexto de função especificado.                                |
| [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)                     | Controla se o sistema tratará os tipos de erros graves especificados ou se o processo os tratará.       |
| [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror)                     | Define o último código de erro para o thread de chamada.                                                                              |
| [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex)                 | Define o último código de erro para o thread de chamada.                                                                              |
| [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)         | Controla se o sistema tratará os tipos especificados de erros graves ou se o thread de chamada irá tratá-los. |



 

 

 
