---
description: O Winlogon implementa duas operações de tempo limite, uma para caixas de diálogo seguras e a outra para ativação e encerramento de proteção de tela.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Caixa de diálogo com suporte Tempo de Serviço operações de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647191"
---
# <a name="supported-dialog-box-service-time-out-operations"></a>Caixa de diálogo com suporte Tempo de Serviço operações de saída

O [*Winlogon*](../secgloss/w-gly.md) implementa duas operações de tempo limite, uma para caixas de diálogo seguras e a outra para ativação e encerramento de proteção de tela.

Ao exibir uma caixa de diálogo segura, como logon ou desbloqueio de uma estação de trabalho, o Winlogon pode cronometrar as caixas de diálogo e retornar um código de resultado apropriado para o procedimento da caixa de diálogo. O Winlogon fornece um conjunto de funções de suporte de caixa de diálogo para a [*Gina*](../secgloss/g-gly.md). A GINA deve usar essas funções em vez de suas contrapartes do Windows para garantir que a GINA e o Winlogon mantenham o controle apropriado nas caixas de diálogo. A falha ao usar as versões do Winlogon dessas funções pode fazer com que usuários não autorizados obtenham acesso ao sistema.

Os serviços da caixa de diálogo Winlogon são fornecidos pelas seguintes funções de suporte.



| Função de suporte                                               | Descrição                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**WlxMessageBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | Semelhante à função [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) do Windows.                         |
| [**WlxDialogBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | Semelhante à função [**caixa**](/windows/win32/api/winuser/nf-winuser-dialogboxa) do Windows.                           |
| [**WlxDialogBoxIndirect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | Semelhante à função [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) do Windows.           |
| [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | Semelhante à função [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) do Windows.                 |
| [**WlxDialogBoxIndirectParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | Semelhante à função [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) do Windows. |



 

As DLLs GINAs também podem \_ receber \_ mensagens SAS do WLX WM do Winlogon. Essas mensagens serão enviadas para caixas de diálogo ativas se uma SAS ( [*sequência de atenção segura*](../secgloss/s-gly.md) ) for recebida. Isso será útil se a GINA estiver no processo de solicitar o PIN correspondente para um [*cartão inteligente*](../secgloss/s-gly.md)e o cartão for removido do [*leitor*](../secgloss/r-gly.md)de cartão inteligente. O Winlogon usa \_ \_ a SAS WLX DLG como o código de resultado do EndDialog quando ocorre um evento SAS durante uma operação da caixa de diálogo.

Os tempos limite também são fornecidos dessa maneira. Uma mensagem SAS do WLX do \_ WM \_ é enviada com WLX \_ SAS \_ tipo \_ SCRNSVR \_ Timeout ou WLX \_ SAS \_ tipo \_ Timeout. A caixa de diálogo terminará com um código de saída apropriado para permitir que os desenvolvedores de GINA vinculem as notificações de tempo limite.

As caixas de diálogo GINA podem ser encerradas pelo Winlogon usando o logoff do usuário do Code WLX \_ DLG \_ \_ . Isso indica que o usuário fez logoff durante a execução da caixa de diálogo (por exemplo, chamando a função [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) de outro thread).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicializando Winlogon](initializing-winlogon.md)
</dt> <dt>

[Estados do Winlogon](winlogon-states.md)
</dt> <dt>

[Enviando mensagens para a GINA](sending-messages-to-the-gina.md)
</dt> <dt>

[Funções de suporte do Winlogon](authentication-functions.md)
</dt> </dl>

 

 
