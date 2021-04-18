---
description: As operações de conclusão permitem que um aplicativo especifique como ele deseja tratar uma sessão quando fatores como um destino ocupado impedem uma conexão normal.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Concluir uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788071"
---
# <a name="complete-a-session"></a><span data-ttu-id="f65b5-103">Concluir uma sessão</span><span class="sxs-lookup"><span data-stu-id="f65b5-103">Complete a Session</span></span>

<span data-ttu-id="f65b5-104">As operações de conclusão permitem que um aplicativo especifique como ele deseja tratar uma sessão quando fatores como um destino ocupado impedem uma conexão normal.</span><span class="sxs-lookup"><span data-stu-id="f65b5-104">Completion operations allow an application to specify how it wants to handle a session when factors such as a busy destination prevent normal connection.</span></span>

<span data-ttu-id="f65b5-105">As [ \_ constantes LINECALLCOMPLMODE](./linecallcomplmode--constants.md) definem as possíveis opções que um aplicativo pode ter, dependendo dos recursos do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="f65b5-105">The [LINECALLCOMPLMODE\_ Constants](./linecallcomplmode--constants.md) define the possible options an application might have, depending on service provider capabilities.</span></span>

<span data-ttu-id="f65b5-106">Várias solicitações de conclusão de chamada podem estar pendentes para um determinado endereço a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="f65b5-106">Multiple call completion requests might be outstanding for a given address at any one time.</span></span> <span data-ttu-id="f65b5-107">Para identificar solicitações individuais, a implementação retorna um [identificador de conclusão](completion-id-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="f65b5-107">To identify individual requests, the implementation returns a [completion identifier](completion-id-ovr.md).</span></span> <span data-ttu-id="f65b5-108">Cancelar uma solicitação de conclusão de chamada em andamento também usa esse identificador de conclusão de chamada.</span><span class="sxs-lookup"><span data-stu-id="f65b5-108">Canceling a call completion request in progress also uses this call completion identifier.</span></span>

<span data-ttu-id="f65b5-109">**TAPI 2. x:** Consulte [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span><span class="sxs-lookup"><span data-stu-id="f65b5-109">**TAPI 2.x:** See [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).</span></span>

<span data-ttu-id="f65b5-110">**TAPI 3. x:** Consulte [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="f65b5-110">**TAPI 3.x:** See [**ITBasicCallControl::Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
