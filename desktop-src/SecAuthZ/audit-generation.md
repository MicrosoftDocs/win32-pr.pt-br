---
description: Os requisitos de segurança no nível de C2 especificam que os administradores de sistema devem ser capazes de auditar eventos relacionados à segurança e que o acesso a esses dados de auditoria deve ser limitado a administradores autorizados.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Geração de auditoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748121"
---
# <a name="audit-generation"></a><span data-ttu-id="63ecc-103">Geração de auditoria</span><span class="sxs-lookup"><span data-stu-id="63ecc-103">Audit Generation</span></span>

<span data-ttu-id="63ecc-104">Os requisitos de segurança no nível de C2 especificam que os administradores de sistema devem ser capazes de auditar eventos relacionados à segurança e que o acesso a esses dados de auditoria deve ser limitado a administradores autorizados.</span><span class="sxs-lookup"><span data-stu-id="63ecc-104">C2-level security requirements specify that system administrators must be able to audit security-related events and that access to this audit data must be limited to authorized administrators.</span></span> <span data-ttu-id="63ecc-105">A API do Windows fornece funções que permitem que um administrador monitore eventos relacionados à segurança.</span><span class="sxs-lookup"><span data-stu-id="63ecc-105">The Windows API provides functions enabling an administrator to monitor security-related events.</span></span>

<span data-ttu-id="63ecc-106">O descritor de segurança para um objeto protegível pode ter uma SACL ( [*lista de controle de acesso do sistema*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="63ecc-106">The security descriptor for a securable object can have a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="63ecc-107">Uma SACL contém ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) que especificam os tipos de tentativas de acesso que geram relatórios de auditoria.</span><span class="sxs-lookup"><span data-stu-id="63ecc-107">A SACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) that specify the types of access attempts that generate audit reports.</span></span> <span data-ttu-id="63ecc-108">Cada ACE identifica um grupo de confiança, um conjunto de direitos de acesso e um conjunto de sinalizadores que indicam se o sistema gera mensagens de auditoria para tentativas de acesso com falha, tentativas de acesso bem-sucedidas ou ambos.</span><span class="sxs-lookup"><span data-stu-id="63ecc-108">Each ACE identifies a trustee, a set of access rights, and a set of flags that indicate whether the system generates audit messages for failed access attempts, successful access attempts, or both.</span></span>

<span data-ttu-id="63ecc-109">O sistema grava as mensagens de auditoria no log de eventos de segurança.</span><span class="sxs-lookup"><span data-stu-id="63ecc-109">The system writes audit messages to the security event log.</span></span> <span data-ttu-id="63ecc-110">Para obter informações sobre como acessar os registros em um log de eventos de segurança, consulte [log de eventos](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="63ecc-110">For information about accessing the records in a security event log, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

<span data-ttu-id="63ecc-111">Para ler ou gravar a SACL de um objeto, um thread deve primeiro habilitar o \_ privilégio nome de segurança se \_ .</span><span class="sxs-lookup"><span data-stu-id="63ecc-111">To read or write an object's SACL, a thread must first enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="63ecc-112">Para obter mais informações, consulte [direitos de acesso à SACL](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="63ecc-112">For more information, see [SACL Access Right](sacl-access-right.md).</span></span>

<span data-ttu-id="63ecc-113">A API do Windows também fornece suporte para aplicativos de servidor para gerar mensagens de auditoria quando um cliente tenta acessar um objeto particular.</span><span class="sxs-lookup"><span data-stu-id="63ecc-113">The Windows API also provides support for server applications to generate audit messages when a client tries to access a private object.</span></span> <span data-ttu-id="63ecc-114">Para obter mais informações, consulte [auditando o acesso a objetos privados](auditing-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="63ecc-114">For more information, see [Auditing Access To Private Objects](auditing-access-to-private-objects.md).</span></span>

 

 
