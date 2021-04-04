---
description: Um manipulador de interface do usuário externo (IU) pode retornar qualquer número de valores para Windows Installer dependendo do tipo de botão fornecido no parâmetro de tipo de mensagem que o instalador passa para o manipulador.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Retornando valores de um manipulador de interface do usuário externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661557"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a><span data-ttu-id="24193-103">Retornando valores de um manipulador de interface do usuário externo</span><span class="sxs-lookup"><span data-stu-id="24193-103">Returning Values from an External User Interface Handler</span></span>

<span data-ttu-id="24193-104">Um manipulador de interface do usuário externo (IU) pode retornar qualquer número de valores para Windows Installer dependendo do tipo de botão fornecido no parâmetro de tipo de mensagem que o instalador passa para o manipulador.</span><span class="sxs-lookup"><span data-stu-id="24193-104">An external user interface (UI) handler can return any number of values to Windows Installer depending on the button type provided in the message type parameter the installer passes to the handler.</span></span>

<span data-ttu-id="24193-105">O manipulador de interface do usuário externa pode retornar os valores – 1 e 0 a qualquer momento, pois eles não estão relacionados aos tipos de botão.</span><span class="sxs-lookup"><span data-stu-id="24193-105">The external UI handler can return the values –1 and 0 at any time because these are not related to the button types.</span></span> <span data-ttu-id="24193-106">Um valor de retorno de – 1 indica que ocorreu um erro interno no manipulador de interface do usuário externa.</span><span class="sxs-lookup"><span data-stu-id="24193-106">A return value of –1 indicates that an internal error occurred in the external UI handler.</span></span> <span data-ttu-id="24193-107">Um valor de retorno de 0 indica que o manipulador de interface do usuário externo não tratou a mensagem do instalador e o instalador deve manipular a mensagem em vez disso.</span><span class="sxs-lookup"><span data-stu-id="24193-107">A return value of 0 indicates that the external UI handler has not handled the installer message and the installer must handle the message instead.</span></span>

<span data-ttu-id="24193-108">Para mensagens que não incluem um tipo de botão, como INSTALLMESSAGE \_ ACTIONDATA e INSTALLMESSAGE \_ Progress, retornar IDCANCEL cancela a instalação.</span><span class="sxs-lookup"><span data-stu-id="24193-108">For messages that do not include a button type, such as INSTALLMESSAGE\_ACTIONDATA and INSTALLMESSAGE\_PROGRESS, returning IDCANCEL cancels the installation.</span></span> <span data-ttu-id="24193-109">Retornar IDOK notifica o instalador de que a mensagem foi tratada pelo manipulador de interface do usuário externa.</span><span class="sxs-lookup"><span data-stu-id="24193-109">Returning IDOK notifies the installer that the message was handled by the external UI handler.</span></span>

<span data-ttu-id="24193-110">Os valores de retorno restantes, conforme descrito abaixo, estão diretamente relacionados aos tipos de botão que são incluídos com o tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="24193-110">The remaining return values, as described below, are directly related to the button types that are included with the message type.</span></span>



| <span data-ttu-id="24193-111">Valor de retorno da interface do usuário externa</span><span class="sxs-lookup"><span data-stu-id="24193-111">External UI return value</span></span> | <span data-ttu-id="24193-112">Significado</span><span class="sxs-lookup"><span data-stu-id="24193-112">Meaning</span></span>                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24193-113">IDOK</span><span class="sxs-lookup"><span data-stu-id="24193-113">IDOK</span></span>                     | <span data-ttu-id="24193-114">O botão **OK** foi pressionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="24193-114">The **OK** button was pressed by the user.</span></span> <span data-ttu-id="24193-115">As informações da mensagem foram compreendidas.</span><span class="sxs-lookup"><span data-stu-id="24193-115">The message information was understood.</span></span>                     |
| <span data-ttu-id="24193-116">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="24193-116">IDCANCEL</span></span>                 | <span data-ttu-id="24193-117">O botão **Cancelar** foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="24193-117">The **CANCEL** button was pressed.</span></span> <span data-ttu-id="24193-118">Cancele a instalação.</span><span class="sxs-lookup"><span data-stu-id="24193-118">Cancel the installation.</span></span>                                            |
| <span data-ttu-id="24193-119">IDABORT</span><span class="sxs-lookup"><span data-stu-id="24193-119">IDABORT</span></span>                  | <span data-ttu-id="24193-120">O botão **anular** foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="24193-120">The **ABORT** button was pressed.</span></span> <span data-ttu-id="24193-121">Anule a instalação.</span><span class="sxs-lookup"><span data-stu-id="24193-121">Abort the installation.</span></span>                                              |
| <span data-ttu-id="24193-122">IDRETRY</span><span class="sxs-lookup"><span data-stu-id="24193-122">IDRETRY</span></span>                  | <span data-ttu-id="24193-123">O botão de **repetição** foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="24193-123">The **RETRY** button was pressed.</span></span> <span data-ttu-id="24193-124">Tente a ação novamente.</span><span class="sxs-lookup"><span data-stu-id="24193-124">Try the action again.</span></span>                                                |
| <span data-ttu-id="24193-125">IDIGNORE</span><span class="sxs-lookup"><span data-stu-id="24193-125">IDIGNORE</span></span>                 | <span data-ttu-id="24193-126">O botão **ignorar** foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="24193-126">The **IGNORE** button was pressed.</span></span> <span data-ttu-id="24193-127">Ignore o erro e continue.</span><span class="sxs-lookup"><span data-stu-id="24193-127">Ignore the error and continue.</span></span>                                      |
| <span data-ttu-id="24193-128">IDYES</span><span class="sxs-lookup"><span data-stu-id="24193-128">IDYES</span></span>                    | <span data-ttu-id="24193-129">O botão **Sim** foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="24193-129">The **YES** button was pressed.</span></span> <span data-ttu-id="24193-130">A resposta afirmativo, continue com a sequência atual de eventos..</span><span class="sxs-lookup"><span data-stu-id="24193-130">The affirmative response, continue with current sequence of events..</span></span>   |
| <span data-ttu-id="24193-131">IDNO</span><span class="sxs-lookup"><span data-stu-id="24193-131">IDNO</span></span>                     | <span data-ttu-id="24193-132">O botão **não** foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="24193-132">The **NO** button was pressed.</span></span> <span data-ttu-id="24193-133">A resposta negativa não continua com a sequência de eventos atual.</span><span class="sxs-lookup"><span data-stu-id="24193-133">The negative response, do not continue with current sequence of events.</span></span> |



 

<span data-ttu-id="24193-134">Por exemplo, se o manipulador da interface do usuário externa for enviado uma mensagem com o \_ sinalizador de estilos da caixa de mensagem MB ABORTRETRYIGNORE, o manipulador de interface do usuário externa poderá retornar um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="24193-134">For example, if the external UI handler is sent a message with the MB\_ABORTRETRYIGNORE message box styles flag, the external UI handler can return one of the following values:</span></span>

-   <span data-ttu-id="24193-135">– 1 (erro no manipulador de interface do usuário externa)</span><span class="sxs-lookup"><span data-stu-id="24193-135">–1 (error in external UI handler)</span></span>
-   <span data-ttu-id="24193-136">0 (nenhuma ação realizada no manipulador de interface do usuário externa, permita que Windows Installer manipule-o)</span><span class="sxs-lookup"><span data-stu-id="24193-136">0 (no action taken in external UI handler, let Windows Installer handle it)</span></span>
-   <span data-ttu-id="24193-137">IDABORT (botão **anular** pressionado)</span><span class="sxs-lookup"><span data-stu-id="24193-137">IDABORT (**ABORT** button pressed)</span></span>
-   <span data-ttu-id="24193-138">IDRETRY (botão de **repetição** pressionado)</span><span class="sxs-lookup"><span data-stu-id="24193-138">IDRETRY (**RETRY** button pressed)</span></span>
-   <span data-ttu-id="24193-139">IDIGNORE (botão **ignorar** pressionado)</span><span class="sxs-lookup"><span data-stu-id="24193-139">IDIGNORE (**IGNORE** button pressed)</span></span>

 

 



