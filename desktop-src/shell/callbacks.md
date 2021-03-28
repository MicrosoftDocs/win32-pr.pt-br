---
description: Esta seção descreve as funções de retorno de chamada do shell do Windows.
title: Funções de retorno de chamada do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370616"
---
# <a name="shell-callback-functions"></a><span data-ttu-id="2f313-103">Funções de retorno de chamada do Shell</span><span class="sxs-lookup"><span data-stu-id="2f313-103">Shell Callback Functions</span></span>

<span data-ttu-id="2f313-104">Esta seção descreve as funções de retorno de chamada do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="2f313-104">This section describes the Windows Shell callback functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f313-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2f313-105">In this section</span></span>



| <span data-ttu-id="2f313-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="2f313-106">Topic</span></span>                                                                     | <span data-ttu-id="2f313-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f313-107">Description</span></span>                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f313-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f313-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span></span><br/>                      | <span data-ttu-id="2f313-109">Especifica uma função de retorno de chamada definida pelo aplicativo usada para enviar mensagens e processar mensagens de, uma caixa de diálogo de **procura** exibida em resposta a uma chamada para [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="2f313-109">Specifies an application-defined callback function used to send messages to, and process messages from, a **Browse** dialog box displayed in response to a call to [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span><br/> |
| [<span data-ttu-id="2f313-110">*FMExtensionProc*</span><span class="sxs-lookup"><span data-stu-id="2f313-110">*FMExtensionProc*</span></span>](fmextensionproc.md)<br/>                       | <span data-ttu-id="2f313-111">Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos para se comunicar com uma extensão do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2f313-111">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span><br/>                                                                                            |
| [<span data-ttu-id="2f313-112">*MRUCMPPROC*</span><span class="sxs-lookup"><span data-stu-id="2f313-112">*MRUCMPPROC*</span></span>](mrucmpproc.md)<br/>                                 | <span data-ttu-id="2f313-113">Usado para determinar se um item está presente em uma lista de MRU (usado mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="2f313-113">Used to determine whether an item is present in a most recently used (MRU) list.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="2f313-114">**\_rotina de alteração de PAPPSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="2f313-114">**PAPPSTATE\_CHANGE\_ROUTINE**</span></span>](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | <span data-ttu-id="2f313-115">Especifica uma função de retorno de chamada definida pelo aplicativo que notifica o aplicativo quando o aplicativo está entrando ou saindo de um estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="2f313-115">Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.</span></span><br/>                                                                                            |
| [<span data-ttu-id="2f313-116">**SUBCLASSPROC**</span><span class="sxs-lookup"><span data-stu-id="2f313-116">**SUBCLASSPROC**</span></span>](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | <span data-ttu-id="2f313-117">Define o protótipo para a função de retorno de chamada usada por [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) e [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span><span class="sxs-lookup"><span data-stu-id="2f313-117">Defines the prototype for the callback function used by [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) and [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span></span><br/>                                                   |
| [<span data-ttu-id="2f313-118">**\_proc de DESexclusão de FM \_**</span><span class="sxs-lookup"><span data-stu-id="2f313-118">**FM\_UNDELETE\_PROC**</span></span>](undeletefile.md)<br/>                     | <span data-ttu-id="2f313-119">Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos quando o usuário escolhe o comando **restaurar** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="2f313-119">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span><br/>                                                                   |



 

 

 
