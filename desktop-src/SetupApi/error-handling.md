---
description: 'Há três funções que geram caixas de diálogo para manipular erros: SetupCopyError, SetupDeleteError e SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Tratamento de erro (API de instalação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755787"
---
# <a name="error-handling-setup-api"></a><span data-ttu-id="8cf38-103">Tratamento de erro (API de instalação)</span><span class="sxs-lookup"><span data-stu-id="8cf38-103">Error Handling (Setup API)</span></span>

<span data-ttu-id="8cf38-104">Há três funções que geram caixas de diálogo para manipular erros: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)e [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span><span class="sxs-lookup"><span data-stu-id="8cf38-104">There are three functions that generate dialog boxes to handle errors: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), and [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).</span></span>

<span data-ttu-id="8cf38-105">As rotinas de retorno de chamada podem usar essas funções para gerar uma interface do usuário para lidar com notificações [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)e [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf38-105">Callback routines can use these functions to generate a user interface to handle [**SPFILENOTIFY\_COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md), and [**SPFILENOTIFY\_RENAMEERROR**](spfilenotify-renameerror.md) notifications.</span></span>

<span data-ttu-id="8cf38-106">Cada uma dessas funções de tratamento de erros gera uma caixa de diálogo que solicita ao usuário informações sobre como proceder.</span><span class="sxs-lookup"><span data-stu-id="8cf38-106">Each of these error-handling functions generates a dialog box that asks the user for information on how to proceed.</span></span> <span data-ttu-id="8cf38-107">Assim como com o [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), você pode modificar o layout e o comportamento da caixa de diálogo especificando sinalizadores durante a chamada de função.</span><span class="sxs-lookup"><span data-stu-id="8cf38-107">As with [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), you can modify the dialog box's layout and behavior by specifying flags during the function call.</span></span>

 

 



