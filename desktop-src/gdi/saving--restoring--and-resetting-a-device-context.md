---
description: 'As funções a seguir permitem que um aplicativo Salve, restaure e Redefina um contexto de dispositivo: SaveDC, RestoreDC e ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Salvando, restaurando e redefinindo um contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967960"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a><span data-ttu-id="e7dc4-103">Salvando, restaurando e redefinindo um contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e7dc4-103">Saving, Restoring, and Resetting a Device Context</span></span>

<span data-ttu-id="e7dc4-104">As funções a seguir permitem que um aplicativo Salve, restaure e Redefina um contexto de dispositivo: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)e [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span><span class="sxs-lookup"><span data-stu-id="e7dc4-104">The following functions enable an application to save, restore, and reset a device context: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc), and [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span></span> <span data-ttu-id="e7dc4-105">A função SaveDC registra em uma pilha GDI especial os objetos gráficos atuais do DC e seus atributos e modos gráficos.</span><span class="sxs-lookup"><span data-stu-id="e7dc4-105">The SaveDC function records on a special GDI stack the current DC's graphic objects and their attributes, and graphic modes.</span></span> <span data-ttu-id="e7dc4-106">Um aplicativo de desenho pode chamar essa função antes que um usuário comece a desenhar e salve o estado original do aplicativo fornecendo um Tablet limpo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e7dc4-106">A drawing application can call this function before a user begins drawing and save the application's original state providing a clean slate for the user.</span></span> <span data-ttu-id="e7dc4-107">Para retornar a esse estado original, o aplicativo chama a função RestoreDC.</span><span class="sxs-lookup"><span data-stu-id="e7dc4-107">To return to this original state, the application calls the RestoreDC function.</span></span>

<span data-ttu-id="e7dc4-108">O [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) é fornecido para redefinir os dados do DC da impressora.</span><span class="sxs-lookup"><span data-stu-id="e7dc4-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) is provided to reset printer DC data.</span></span> <span data-ttu-id="e7dc4-109">Um aplicativo chama essa função para redefinir a orientação do papel, o tamanho do papel, o fator de dimensionamento de saída, o número de cópias a serem impressadas, a origem do papel (ou o compartimento), o modo duplex e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e7dc4-109">An application calls this function to reset the paper orientation, paper size, output scaling factor, number of copies to be printed, paper source (or bin), duplex mode, and so on.</span></span> <span data-ttu-id="e7dc4-110">Normalmente, um aplicativo chama essa função depois que um usuário altera uma das opções de impressora e o sistema emitiu uma mensagem de [**\_ DEVMODECHANGE do WM**](wm-devmodechange.md) .</span><span class="sxs-lookup"><span data-stu-id="e7dc4-110">Typically, an application calls this function after a user has changed one of the printer options and the system has issued a [**WM\_DEVMODECHANGE**](wm-devmodechange.md) message.</span></span>

 

 



