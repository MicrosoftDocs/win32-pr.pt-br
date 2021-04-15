---
description: SACL para um novo objeto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL para um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747504"
---
# <a name="sacl-for-a-new-object"></a><span data-ttu-id="4e713-103">SACL para um novo objeto</span><span class="sxs-lookup"><span data-stu-id="4e713-103">SACL for a New Object</span></span>

<span data-ttu-id="4e713-104">O sistema usa o seguinte algoritmo para criar uma SACL para a maioria dos tipos de novos objetos protegíveis:</span><span class="sxs-lookup"><span data-stu-id="4e713-104">The system uses the following algorithm to build a SACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="4e713-105">A SACL do objeto é a SACL do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) especificado pelo criador do objeto.</span><span class="sxs-lookup"><span data-stu-id="4e713-105">The object's SACL is the SACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="4e713-106">O sistema mescla quaisquer ACEs herdáveis na SACL especificada, a menos que o \_ \_ bit se protegido por SACL seja definido nos bits de controle do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="4e713-106">The system merges any inheritable ACEs into the specified SACL unless the SE\_SACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span> <span data-ttu-id="4e713-107">\_As ACEs \_ \_ de atributo de recurso do sistema e \_ \_ \_ \_ a ID da política no escopo do sistema ACEs de um objeto pai serão mescladas a um novo objeto, mesmo se o \_ bit protegido da SACL \_ estiver definido.</span><span class="sxs-lookup"><span data-stu-id="4e713-107">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs and SYSTEM\_SCOPED\_POLICY\_ID\_ACEs from a parent object will be merged to a new object even if the SE\_SACL\_PROTECTED bit is set.</span></span>
2.  <span data-ttu-id="4e713-108">Se o criador não especificar um descritor de segurança, o sistema criará a SACL do objeto de ACEs herdáveis.</span><span class="sxs-lookup"><span data-stu-id="4e713-108">If the creator does not specify a security descriptor, the system builds the object's SACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="4e713-109">Se não houver nenhuma SACL especificada ou herdada, o objeto não terá nenhuma SACL.</span><span class="sxs-lookup"><span data-stu-id="4e713-109">If there is no specified or inherited SACL, the object has no SACL.</span></span>

<span data-ttu-id="4e713-110">Para especificar uma SACL para um novo objeto, o criador do objeto deve ter o \_ \_ [privilégio](privileges.md) nome de segurança se habilitado.</span><span class="sxs-lookup"><span data-stu-id="4e713-110">To specify a SACL for a new object, the object's creator must have the SE\_SECURITY\_NAME [privilege](privileges.md) enabled.</span></span> <span data-ttu-id="4e713-111">Se a SACL especificada para um novo objeto contiver somente \_ ACEs de atributo de recurso \_ \_ do sistema, o \_ privilégio de nome de segurança se \_ não será necessário.</span><span class="sxs-lookup"><span data-stu-id="4e713-111">If the specified SACL for a new object contain only SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs, then the SE\_SECURITY\_NAME privilege is not required.</span></span> <span data-ttu-id="4e713-112">O criador não precisará desse privilégio se a SACL do objeto for criada a partir de ACEs herdadas.</span><span class="sxs-lookup"><span data-stu-id="4e713-112">The creator does not need this privilege if the object's SACL is built from inherited ACEs.</span></span>

<span data-ttu-id="4e713-113">O sistema usa um algoritmo diferente para criar uma SACL para um novo objeto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e713-113">The system uses a different algorithm to build a SACL for a new Active Directory object.</span></span> <span data-ttu-id="4e713-114">Para obter mais informações, consulte [como descritores de segurança são definidos em novos objetos de diretório](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="4e713-114">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
