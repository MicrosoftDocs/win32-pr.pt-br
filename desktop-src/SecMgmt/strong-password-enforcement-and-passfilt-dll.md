---
description: Lista os requisitos impostos por ferramentas de administração do sistema de senha forte.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Imposição de senha forte e Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b7be524511d52048e06ae83ab110384c3bf5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501540"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a><span data-ttu-id="bbf3a-103">Imposição de senha forte e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="bbf3a-103">Strong Password Enforcement and Passfilt.dll</span></span>

<span data-ttu-id="bbf3a-104">A imposição de senha forte pode ser habilitada usando as ferramentas de administração do sistema.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-104">Strong password enforcement can be enabled by using the system administration tools.</span></span> <span data-ttu-id="bbf3a-105">Se a política de administração do sistema estiver habilitada, as senhas deverão atender aos seguintes requisitos mínimos quando forem criadas ou alteradas:</span><span class="sxs-lookup"><span data-stu-id="bbf3a-105">If the system administration policy is enabled, passwords must meet the following minimum requirements when they are created or changed:</span></span>

-   <span data-ttu-id="bbf3a-106">As senhas não podem conter o valor samAccountName (nome da conta) do usuário ou o displayName inteiro (valor de nome completo).</span><span class="sxs-lookup"><span data-stu-id="bbf3a-106">Passwords may not contain the user's samAccountName (Account Name) value or entire displayName (Full Name value).</span></span> <span data-ttu-id="bbf3a-107">Ambas as verificações não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-107">Both checks are not case sensitive.</span></span>
-   <span data-ttu-id="bbf3a-108">O samAccountName é verificado em sua totalidade apenas para determinar se ele faz parte da senha.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-108">The samAccountName is checked in its entirety only to determine whether it is part of the password.</span></span> <span data-ttu-id="bbf3a-109">Se samAccountName tiver menos de três caracteres, essa verificação será ignorada.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-109">If the samAccountName is less than three characters long, this check is skipped.</span></span>
-   <span data-ttu-id="bbf3a-110">O displayName é analisado para delimitadores: vírgulas, pontos, traços ou hifens, sublinhados, espaços, sinais de libra e tabulações.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-110">The displayName is parsed for delimiters: commas, periods, dashes or hyphens, underscores, spaces, pound signs, and tabs.</span></span> <span data-ttu-id="bbf3a-111">Se qualquer um desses delimitadores for encontrado, o displayName será dividido e todas as seções analisadas (tokens) serão confirmadas para não serem incluídas na senha.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-111">If any of these delimiters are found, the displayName is split and all parsed sections (tokens) are confirmed to not be included in the password.</span></span> <span data-ttu-id="bbf3a-112">Os tokens com menos de três caracteres são ignorados e as subcadeias dos tokens não são verificadas.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-112">Tokens that are less than three characters are ignored, and substrings of the tokens are not checked.</span></span> <span data-ttu-id="bbf3a-113">Por exemplo, o nome "Erin M. Hagens" é dividido em três tokens: "Erin", "M" e "Hagens".</span><span class="sxs-lookup"><span data-stu-id="bbf3a-113">For example, the name "Erin M. Hagens" is split into three tokens: "Erin", "M", and "Hagens".</span></span> <span data-ttu-id="bbf3a-114">Como o segundo token é apenas um caractere, ele é ignorado.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-114">Because the second token is only one character long, it is ignored.</span></span> <span data-ttu-id="bbf3a-115">Portanto, esse usuário não poderia ter uma senha que incluisse "Erin" ou "Hagens" como uma subcadeia de caracteres em qualquer lugar da senha.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-115">Therefore, this user could not have a password that included either "erin" or "hagens" as a substring anywhere in the password.</span></span>
-   <span data-ttu-id="bbf3a-116">As senhas devem conter caracteres de três das cinco categorias a seguir.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-116">Passwords must contain characters from three of the five following categories.</span></span>



| <span data-ttu-id="bbf3a-117">Categorias de caractere</span><span class="sxs-lookup"><span data-stu-id="bbf3a-117">Character categories</span></span>                                                                                                                                                      | <span data-ttu-id="bbf3a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbf3a-118">Examples</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="bbf3a-119">Letras maiúsculas de idiomas europeus (A a Z, com marcas diacrítico, caracteres gregos e cirílico)</span><span class="sxs-lookup"><span data-stu-id="bbf3a-119">Uppercase letters of European languages (A through Z, with diacritic marks, Greek and Cyrillic characters)</span></span><br/>                                                     | <span data-ttu-id="bbf3a-120">A, B, C, Z</span><span class="sxs-lookup"><span data-stu-id="bbf3a-120">A, B, C,   Z</span></span><br/>                |
| <span data-ttu-id="bbf3a-121">Letras minúsculas de idiomas europeus (a a z, Sharp-s, com marcas de sinais diacríticos, caracteres gregos e cirílico)</span><span class="sxs-lookup"><span data-stu-id="bbf3a-121">Lowercase letters of European languages (a through z, sharp-s, with diacritic marks, Greek and Cyrillic characters)</span></span><br/>                                            | <span data-ttu-id="bbf3a-122">a, b, c, z</span><span class="sxs-lookup"><span data-stu-id="bbf3a-122">a, b, c,   z</span></span><br/>                |
| <span data-ttu-id="bbf3a-123">10 dígitos base (0 a 9)</span><span class="sxs-lookup"><span data-stu-id="bbf3a-123">Base 10 digits (0 through 9)</span></span><br/>                                                                                                                                   | <span data-ttu-id="bbf3a-124">0, 1, 2, 9</span><span class="sxs-lookup"><span data-stu-id="bbf3a-124">0, 1, 2,   9</span></span><br/>                |
| <span data-ttu-id="bbf3a-125">Caracteres não alfanuméricos (caracteres especiais)</span><span class="sxs-lookup"><span data-stu-id="bbf3a-125">Non-alphanumeric characters (special characters)</span></span><br/>                                                                                                               | <span data-ttu-id="bbf3a-126">$,!,%, ^, () {} \[ \] ;: <>?</span><span class="sxs-lookup"><span data-stu-id="bbf3a-126">$,!,%,^,(){}\[\];:<>?</span></span><br/> |
| <span data-ttu-id="bbf3a-127">Qualquer caractere Unicode que é Categorizado como um caractere alfabético, mas não é maiúsculo ou minúsculo.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-127">Any Unicode character that is categorized as an alphabetic character but is not uppercase or lowercase.</span></span> <span data-ttu-id="bbf3a-128">Isso inclui caracteres Unicode de idiomas asiáticos.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-128">This includes Unicode characters from Asian languages.</span></span><br/> |                                        |



 

<span data-ttu-id="bbf3a-129">**Para habilitar a imposição de senha forte**</span><span class="sxs-lookup"><span data-stu-id="bbf3a-129">**To enable strong password enforcement**</span></span>

1.  <span data-ttu-id="bbf3a-130">No console de administração, localize **política de segurança local**.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-130">From the administration console, locate **Local Security Policy**.</span></span>
2.  <span data-ttu-id="bbf3a-131">Selecione **política de conta** e selecione **política de senha**.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-131">Select **Account Policy**, and then select **Password Policy**.</span></span>
3.  <span data-ttu-id="bbf3a-132">Habilite a configuração as **senhas devem atender aos requisitos de complexidade** .</span><span class="sxs-lookup"><span data-stu-id="bbf3a-132">Enable the **Passwords must meet complexity requirements** setting.</span></span>

> [!Note]  
> <span data-ttu-id="bbf3a-133">Um determinado caractere pode satisfazer apenas uma categoria.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-133">A given character can satisfy only one category.</span></span> <span data-ttu-id="bbf3a-134">A função [GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) é usada para testar se cada caractere na senha é maiúsculo, minúsculo ou alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="bbf3a-134">The [GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) function is used to test whether each character in the password is uppercase, lowercase, or alphanumeric.</span></span>

 

 

