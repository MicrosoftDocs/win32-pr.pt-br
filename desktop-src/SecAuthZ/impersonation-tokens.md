---
description: Explica o uso de tokens de representação no controle de acesso.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Tokens de representação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755967"
---
# <a name="impersonation-tokens"></a><span data-ttu-id="f150c-103">Tokens de representação</span><span class="sxs-lookup"><span data-stu-id="f150c-103">Impersonation Tokens</span></span>

<span data-ttu-id="f150c-104">Um thread de representação tem dois [*tokens de acesso*](/windows/desktop/SecGloss/a-gly):</span><span class="sxs-lookup"><span data-stu-id="f150c-104">An impersonating thread has two [*access tokens*](/windows/desktop/SecGloss/a-gly):</span></span>

-   <span data-ttu-id="f150c-105">Um [*token de acesso primário*](/windows/desktop/SecGloss/p-gly) que descreve o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) do servidor.</span><span class="sxs-lookup"><span data-stu-id="f150c-105">A [*primary access token*](/windows/desktop/SecGloss/p-gly) that describes the [*security context*](/windows/desktop/SecGloss/s-gly) of the server.</span></span> <span data-ttu-id="f150c-106">Para obter um identificador para esse token, chame a função [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .</span><span class="sxs-lookup"><span data-stu-id="f150c-106">To get a handle to this token, call the [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function.</span></span>
-   <span data-ttu-id="f150c-107">Um token de acesso de representação que descreve o contexto de segurança do cliente que está sendo representado.</span><span class="sxs-lookup"><span data-stu-id="f150c-107">An impersonation access token that describes the security context of the client being impersonated.</span></span> <span data-ttu-id="f150c-108">Para obter um identificador para esse token, chame a função [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .</span><span class="sxs-lookup"><span data-stu-id="f150c-108">To get a handle to this token, call the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function.</span></span>

<span data-ttu-id="f150c-109">Um servidor pode usar o [*token de representação*](/windows/desktop/SecGloss/i-gly) nas seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="f150c-109">A server can use the [*impersonation token*](/windows/desktop/SecGloss/i-gly) in the following functions:</span></span>

-   <span data-ttu-id="f150c-110">Nas funções [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)e [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para determinar se um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) permite ao cliente um conjunto de direitos de acesso.</span><span class="sxs-lookup"><span data-stu-id="f150c-110">In the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype), and [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) functions to determine whether a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows the client a set of access rights.</span></span>
-   <span data-ttu-id="f150c-111">Na função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar ou desabilitar os privilégios do cliente.</span><span class="sxs-lookup"><span data-stu-id="f150c-111">In the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable or disable the client's privileges.</span></span>
-   <span data-ttu-id="f150c-112">Na função [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar se um conjunto de privilégios está habilitado no token do cliente.</span><span class="sxs-lookup"><span data-stu-id="f150c-112">In the [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) function to determine whether a set of privileges are enabled in the client's token.</span></span>
-   <span data-ttu-id="f150c-113">Em funções que geram entradas no log de eventos de segurança, como [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) ou [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span><span class="sxs-lookup"><span data-stu-id="f150c-113">In functions that generate entries in the security event log, such as [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) or [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span></span> <span data-ttu-id="f150c-114">Essas funções usam um token de representação para obter informações sobre o cliente para a entrada de log.</span><span class="sxs-lookup"><span data-stu-id="f150c-114">These functions use an impersonation token to get information about the client for the log entry.</span></span>

 

 
