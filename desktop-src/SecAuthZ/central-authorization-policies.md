---
description: Uma CAP (política de autorização central) coleta as regras de autorização específicas (CAPRs) em uma única política.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Políticas de autorização central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751523"
---
# <a name="central-authorization-policies"></a><span data-ttu-id="f76e7-103">Políticas de autorização central</span><span class="sxs-lookup"><span data-stu-id="f76e7-103">Central Authorization Policies</span></span>

<span data-ttu-id="f76e7-104">Uma CAP (política de autorização central) coleta as regras de autorização específicas (CAPRs) em uma única política.</span><span class="sxs-lookup"><span data-stu-id="f76e7-104">A Central Authorization Policy (CAP) collects the specific authorization rules (CAPRs) into a single policy.</span></span> <span data-ttu-id="f76e7-105">Para permitir que as regras de autorização específicas (CAPRs) sejam combinadas na política de autorização holística da organização, o CAPRs pode ser referenciado em conjunto e aplicado a um conjunto de recursos.</span><span class="sxs-lookup"><span data-stu-id="f76e7-105">To allow the specific authorization rules (CAPRs) to be combined into the holistic authorization policy of the organization, CAPRs can be referenced together and applied to a set of resources.</span></span> <span data-ttu-id="f76e7-106">Isso é feito pela coleta de vários (por referência) em um limite.</span><span class="sxs-lookup"><span data-stu-id="f76e7-106">This is done by collecting multiple (by reference) into a CAP.</span></span> <span data-ttu-id="f76e7-107">Depois que um limite é definido, ele pode ser distribuído consumido pelos gerenciadores de recursos para aplicar a política de autorização de organizações aos recursos.</span><span class="sxs-lookup"><span data-stu-id="f76e7-107">Once a CAP is defined it can be distributed consumed by resource managers to apply the organizations authorization policy to resources.</span></span>

<span data-ttu-id="f76e7-108">Um CAP tem os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="f76e7-108">A CAP has the following attributes:</span></span>

-   <span data-ttu-id="f76e7-109">Coleção de CAPRs – uma lista de referências a objetos CAPR existentes</span><span class="sxs-lookup"><span data-stu-id="f76e7-109">Collection of CAPRs – a list of references to existing CAPR objects</span></span>
-   <span data-ttu-id="f76e7-110">Um identificador (SID)</span><span class="sxs-lookup"><span data-stu-id="f76e7-110">An identifier (Sid)</span></span>
-   <span data-ttu-id="f76e7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f76e7-111">Description</span></span>
-   <span data-ttu-id="f76e7-112">Nome</span><span class="sxs-lookup"><span data-stu-id="f76e7-112">Name</span></span>

<span data-ttu-id="f76e7-113">Um limite é avaliado durante a avaliação de acesso para arquivos e pastas nos quais um administrador o habilita.</span><span class="sxs-lookup"><span data-stu-id="f76e7-113">A CAP is evaluated during access evaluation for files and folders on which an administrator enables it.</span></span> <span data-ttu-id="f76e7-114">Durante uma chamada [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , a verificação de Cap é logicamente combinada com a verificação de ACL condicional; Isso significa que, para obter acesso a um arquivo ao qual a CAP se aplica, um usuário precisa ter acesso de acordo com o limite (seu CAPRs associado) e a ACL condicional no arquivo.</span><span class="sxs-lookup"><span data-stu-id="f76e7-114">During an [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) call, the CAP check is logically combined with the discretionary ACL check; this means that in order to obtain access to a file to which the CAP applies, a user needs to have access both according to the CAP (its associated CAPRs) and the discretionary ACL on the file.</span></span>

<span data-ttu-id="f76e7-115">Exemplo de CAP:</span><span class="sxs-lookup"><span data-stu-id="f76e7-115">Example CAP:</span></span>

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a><span data-ttu-id="f76e7-116">Definição de CAP</span><span class="sxs-lookup"><span data-stu-id="f76e7-116">CAP Definition</span></span>

<span data-ttu-id="f76e7-117">Um limite é criado e editado no Active Directory usando um novo UX no ADAC (ou PowerShell) que permite ao administrador criar um limite e especificar um conjunto de CAPRs que compõem o limite.</span><span class="sxs-lookup"><span data-stu-id="f76e7-117">A CAP is created and edited in Active Directory using a new UX in ADAC (or PowerShell) that allows the administrator to create a CAP and specify a set of CAPRs that make up the CAP.</span></span>

 

 
