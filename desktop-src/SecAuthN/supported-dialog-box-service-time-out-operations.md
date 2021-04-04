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
# <a name="supported-dialog-box-service-time-out-operations"></a><span data-ttu-id="bf623-103">Caixa de diálogo com suporte Tempo de Serviço operações de saída</span><span class="sxs-lookup"><span data-stu-id="bf623-103">Supported Dialog Box Service Time-out Operations</span></span>

<span data-ttu-id="bf623-104">O [*Winlogon*](../secgloss/w-gly.md) implementa duas operações de tempo limite, uma para caixas de diálogo seguras e a outra para ativação e encerramento de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="bf623-104">[*Winlogon*](../secgloss/w-gly.md) implements two time-out operations, one for secure dialog boxes and the other for screen saver activation and termination.</span></span>

<span data-ttu-id="bf623-105">Ao exibir uma caixa de diálogo segura, como logon ou desbloqueio de uma estação de trabalho, o Winlogon pode cronometrar as caixas de diálogo e retornar um código de resultado apropriado para o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bf623-105">While displaying a secure dialog box, such as logon or unlocking a workstation, Winlogon can time-out the dialog boxes and return an appropriate result code to the dialog box procedure.</span></span> <span data-ttu-id="bf623-106">O Winlogon fornece um conjunto de funções de suporte de caixa de diálogo para a [*Gina*](../secgloss/g-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bf623-106">Winlogon provides a set of dialog box support functions for the [*GINA*](../secgloss/g-gly.md).</span></span> <span data-ttu-id="bf623-107">A GINA deve usar essas funções em vez de suas contrapartes do Windows para garantir que a GINA e o Winlogon mantenham o controle apropriado nas caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bf623-107">The GINA must use these functions instead of their Windows counterparts to ensure that the GINA and Winlogon maintain appropriate control over the dialog boxes.</span></span> <span data-ttu-id="bf623-108">A falha ao usar as versões do Winlogon dessas funções pode fazer com que usuários não autorizados obtenham acesso ao sistema.</span><span class="sxs-lookup"><span data-stu-id="bf623-108">Failure to use the Winlogon versions of these functions could result in unauthorized users gaining access to the system.</span></span>

<span data-ttu-id="bf623-109">Os serviços da caixa de diálogo Winlogon são fornecidos pelas seguintes funções de suporte.</span><span class="sxs-lookup"><span data-stu-id="bf623-109">Winlogon dialog box services are provided by the following support functions.</span></span>



| <span data-ttu-id="bf623-110">Função de suporte</span><span class="sxs-lookup"><span data-stu-id="bf623-110">Support function</span></span>                                               | <span data-ttu-id="bf623-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf623-111">Description</span></span>                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf623-112">**WlxMessageBox**</span><span class="sxs-lookup"><span data-stu-id="bf623-112">**WlxMessageBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | <span data-ttu-id="bf623-113">Semelhante à função [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) do Windows.</span><span class="sxs-lookup"><span data-stu-id="bf623-113">Similar to the Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>                         |
| [<span data-ttu-id="bf623-114">**WlxDialogBox**</span><span class="sxs-lookup"><span data-stu-id="bf623-114">**WlxDialogBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | <span data-ttu-id="bf623-115">Semelhante à função [**caixa**](/windows/win32/api/winuser/nf-winuser-dialogboxa) do Windows.</span><span class="sxs-lookup"><span data-stu-id="bf623-115">Similar to the Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function.</span></span>                           |
| [<span data-ttu-id="bf623-116">**WlxDialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="bf623-116">**WlxDialogBoxIndirect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | <span data-ttu-id="bf623-117">Semelhante à função [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) do Windows.</span><span class="sxs-lookup"><span data-stu-id="bf623-117">Similar to the Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) function.</span></span>           |
| [<span data-ttu-id="bf623-118">**WlxDialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="bf623-118">**WlxDialogBoxParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | <span data-ttu-id="bf623-119">Semelhante à função [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) do Windows.</span><span class="sxs-lookup"><span data-stu-id="bf623-119">Similar to the Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) function.</span></span>                 |
| [<span data-ttu-id="bf623-120">**WlxDialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="bf623-120">**WlxDialogBoxIndirectParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | <span data-ttu-id="bf623-121">Semelhante à função [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) do Windows.</span><span class="sxs-lookup"><span data-stu-id="bf623-121">Similar to the Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) function.</span></span> |



 

<span data-ttu-id="bf623-122">As DLLs GINAs também podem \_ receber \_ mensagens SAS do WLX WM do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="bf623-122">GINA DLLs can also receive WLX\_WM\_SAS messages from Winlogon.</span></span> <span data-ttu-id="bf623-123">Essas mensagens serão enviadas para caixas de diálogo ativas se uma SAS ( [*sequência de atenção segura*](../secgloss/s-gly.md) ) for recebida.</span><span class="sxs-lookup"><span data-stu-id="bf623-123">These messages are sent to active dialog boxes if an [*secure attention sequence*](../secgloss/s-gly.md) (SAS) is received.</span></span> <span data-ttu-id="bf623-124">Isso será útil se a GINA estiver no processo de solicitar o PIN correspondente para um [*cartão inteligente*](../secgloss/s-gly.md)e o cartão for removido do [*leitor*](../secgloss/r-gly.md)de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="bf623-124">This is useful if the GINA is in the process of prompting for the matching PIN for a [*smart card*](../secgloss/s-gly.md), and the card is removed from the smart card [*reader*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="bf623-125">O Winlogon usa \_ \_ a SAS WLX DLG como o código de resultado do EndDialog quando ocorre um evento SAS durante uma operação da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bf623-125">Winlogon uses WLX\_DLG\_SAS as the EndDialog result code when an SAS event occurs during a dialog box operation.</span></span>

<span data-ttu-id="bf623-126">Os tempos limite também são fornecidos dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="bf623-126">Time-outs are also delivered in this manner.</span></span> <span data-ttu-id="bf623-127">Uma mensagem SAS do WLX do \_ WM \_ é enviada com WLX \_ SAS \_ tipo \_ SCRNSVR \_ Timeout ou WLX \_ SAS \_ tipo \_ Timeout.</span><span class="sxs-lookup"><span data-stu-id="bf623-127">A WLX\_WM\_SAS message is sent with WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT or WLX\_SAS\_TYPE\_TIMEOUT.</span></span> <span data-ttu-id="bf623-128">A caixa de diálogo terminará com um código de saída apropriado para permitir que os desenvolvedores de GINA vinculem as notificações de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="bf623-128">The dialog box will end with an appropriate exit code to allow GINA developers to hook the time-out notifications.</span></span>

<span data-ttu-id="bf623-129">As caixas de diálogo GINA podem ser encerradas pelo Winlogon usando o logoff do usuário do Code WLX \_ DLG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bf623-129">GINA dialog boxes can be terminated by Winlogon by using the code WLX\_DLG\_USER\_LOGOFF.</span></span> <span data-ttu-id="bf623-130">Isso indica que o usuário fez logoff durante a execução da caixa de diálogo (por exemplo, chamando a função [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) de outro thread).</span><span class="sxs-lookup"><span data-stu-id="bf623-130">This indicates that the user has logged off during the running of the dialog box (for example, by calling the [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) function from another thread).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf623-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf623-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf623-132">Inicializando Winlogon</span><span class="sxs-lookup"><span data-stu-id="bf623-132">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="bf623-133">Estados do Winlogon</span><span class="sxs-lookup"><span data-stu-id="bf623-133">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="bf623-134">Enviando mensagens para a GINA</span><span class="sxs-lookup"><span data-stu-id="bf623-134">Sending Messages to the GINA</span></span>](sending-messages-to-the-gina.md)
</dt> <dt>

[<span data-ttu-id="bf623-135">Funções de suporte do Winlogon</span><span class="sxs-lookup"><span data-stu-id="bf623-135">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
