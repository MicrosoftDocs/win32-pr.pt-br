---
description: Componentes de SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Componentes de SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010591"
---
# <a name="sid-components"></a><span data-ttu-id="6af3c-103">Componentes de SID</span><span class="sxs-lookup"><span data-stu-id="6af3c-103">SID Components</span></span>

<span data-ttu-id="6af3c-104">Um valor de SID inclui componentes que fornecem informações sobre a estrutura e os componentes de [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid) que identificam exclusivamente um confiável.</span><span class="sxs-lookup"><span data-stu-id="6af3c-104">A SID value includes components that provide information about the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure and components that uniquely identify a trustee.</span></span> <span data-ttu-id="6af3c-105">Um SID consiste nos seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="6af3c-105">A SID consists of the following components:</span></span>

-   <span data-ttu-id="6af3c-106">O nível de revisão da estrutura de [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid)</span><span class="sxs-lookup"><span data-stu-id="6af3c-106">The revision level of the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure</span></span>
-   <span data-ttu-id="6af3c-107">Um valor de autoridade de identificador de 48 bits que identifica a autoridade que emitiu o SID</span><span class="sxs-lookup"><span data-stu-id="6af3c-107">A 48-bit identifier authority value that identifies the authority that issued the SID</span></span>
-   <span data-ttu-id="6af3c-108">Um número variável de subautoridade ou valores de RID ( [*identificador relativo*](/windows/desktop/SecGloss/r-gly) ) que identificam exclusivamente o Trustee relativo à autoridade que emitiu o Sid</span><span class="sxs-lookup"><span data-stu-id="6af3c-108">A variable number of subauthority or [*relative identifier*](/windows/desktop/SecGloss/r-gly) (RID) values that uniquely identify the trustee relative to the authority that issued the SID</span></span>

<span data-ttu-id="6af3c-109">A combinação do valor de autoridade de identificador e os valores de subautoridade garante que nenhum Sid seja o mesmo, mesmo que duas autoridades de emissão de SID diferentes emitam a mesma combinação de valores de RID.</span><span class="sxs-lookup"><span data-stu-id="6af3c-109">The combination of the identifier authority value and the subauthority values ensures that no two SIDs will be the same, even if two different SID-issuing authorities issue the same combination of RID values.</span></span> <span data-ttu-id="6af3c-110">Cada autoridade emissora de SID emite um determinado RID apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="6af3c-110">Each SID-issuing authority issues a given RID only once.</span></span>

<span data-ttu-id="6af3c-111">Os SIDs são armazenados em formato binário em uma estrutura de [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid) .</span><span class="sxs-lookup"><span data-stu-id="6af3c-111">SIDs are stored in binary format in a [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure.</span></span> <span data-ttu-id="6af3c-112">Para exibir um SID, você pode chamar a função [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) para converter um SID binário em formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6af3c-112">To display a SID, you can call the [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) function to convert a binary SID to string format.</span></span> <span data-ttu-id="6af3c-113">Para converter uma cadeia de caracteres de SID de volta para um SID válido e funcional, chame a função [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .</span><span class="sxs-lookup"><span data-stu-id="6af3c-113">To convert a SID string back to a valid, functional SID, call the [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) function.</span></span>

<span data-ttu-id="6af3c-114">Essas funções usam a seguinte notação de cadeia de caracteres padronizada para SIDs, o que torna mais simples Visualizar seus componentes:</span><span class="sxs-lookup"><span data-stu-id="6af3c-114">These functions use the following standardized string notation for SIDs, which makes it simpler to visualize their components:</span></span>

<span data-ttu-id="6af3c-115">s-*R* - *I* - *s*...</span><span class="sxs-lookup"><span data-stu-id="6af3c-115">S-*R*-*I*-*S*…</span></span>

<span data-ttu-id="6af3c-116">Nessa notação, o caractere literal "S" identifica a série de dígitos como um SID, *R* é o nível de revisão, *I* é o valor da autoridade de identificação e *S*...</span><span class="sxs-lookup"><span data-stu-id="6af3c-116">In this notation, the literal character "S" identifies the series of digits as a SID, *R* is the revision level, *I* is the identifier-authority value, and *S*…</span></span> <span data-ttu-id="6af3c-117">é um ou mais valores de subautoridade.</span><span class="sxs-lookup"><span data-stu-id="6af3c-117">is one or more subauthority values.</span></span>

<span data-ttu-id="6af3c-118">O exemplo a seguir usa essa notação para exibir o SID relativo do domínio conhecido do grupo local de administradores:</span><span class="sxs-lookup"><span data-stu-id="6af3c-118">The following example uses this notation to display the well-known domain-relative SID of the local Administrators group:</span></span>

<span data-ttu-id="6af3c-119">S-1-5-32-544</span><span class="sxs-lookup"><span data-stu-id="6af3c-119">S-1-5-32-544</span></span>

<span data-ttu-id="6af3c-120">Neste exemplo, o SID tem os seguintes componentes.</span><span class="sxs-lookup"><span data-stu-id="6af3c-120">In this example, the SID has the following components.</span></span> <span data-ttu-id="6af3c-121">As constantes entre parênteses são uma autoridade de identificador bem conhecida e valores de [*RID*](/windows/desktop/SecGloss/r-gly) definidos em Winnt. h:</span><span class="sxs-lookup"><span data-stu-id="6af3c-121">The constants in parentheses are well-known identifier authority and [*RID*](/windows/desktop/SecGloss/r-gly) values defined in Winnt.h:</span></span>

-   <span data-ttu-id="6af3c-122">Um nível de revisão de 1</span><span class="sxs-lookup"><span data-stu-id="6af3c-122">A revision level of 1</span></span>
-   <span data-ttu-id="6af3c-123">Um valor de autoridade de identificação de 5 ( \_ autoridade de segurança NT \_ )</span><span class="sxs-lookup"><span data-stu-id="6af3c-123">An identifier-authority value of 5 (SECURITY\_NT\_AUTHORITY)</span></span>
-   <span data-ttu-id="6af3c-124">Um primeiro valor de subautoridade de 32 (segurança \_ interna do \_ RID do domínio \_ )</span><span class="sxs-lookup"><span data-stu-id="6af3c-124">A first subauthority value of 32 (SECURITY\_BUILTIN\_DOMAIN\_RID)</span></span>
-   <span data-ttu-id="6af3c-125">Um segundo valor de subautoridade de 544 ( \_ Administradores RID de alias de domínio \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="6af3c-125">A second subauthority value of 544 (DOMAIN\_ALIAS\_RID\_ADMINS)</span></span>

 

 
