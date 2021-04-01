---
description: Um descritor de segurança funcional válido contém informações de segurança em formato binário.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Cadeia de caracteres do descritor de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb875bee4d35267b578193ca7cd08420722400a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090747"
---
# <a name="security-descriptor-strings"></a><span data-ttu-id="6acfc-103">Cadeia de caracteres do descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="6acfc-103">Security Descriptor Strings</span></span>

<span data-ttu-id="6acfc-104">Um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) funcional válido contém informações de segurança em formato binário.</span><span class="sxs-lookup"><span data-stu-id="6acfc-104">A valid functional [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains security information in binary format.</span></span> <span data-ttu-id="6acfc-105">A API do Windows fornece funções para converter descritores de segurança binários de e para cadeias de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="6acfc-105">The Windows API provides functions for converting binary security descriptors to and from text strings.</span></span> <span data-ttu-id="6acfc-106">Os descritores de segurança no formato de cadeia de caracteres não são funcionais, mas podem ser úteis para armazenar ou transportar informações de descrição de segurança.</span><span class="sxs-lookup"><span data-stu-id="6acfc-106">Security descriptors in string format are not functional, but they can be useful for storing or transporting security descriptor information.</span></span>

<span data-ttu-id="6acfc-107">Para converter um descritor de segurança em um formato de cadeia de caracteres, chame a função [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="6acfc-107">To convert a security descriptor to a string format, call the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) function.</span></span> <span data-ttu-id="6acfc-108">Para converter um descritor de segurança de formato de cadeia de caracteres de volta para um descritor de segurança funcional válido, chame a função [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="6acfc-108">To convert a string-format security descriptor back to a valid functional security descriptor, call the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function.</span></span>

<span data-ttu-id="6acfc-109">Para obter mais informações, consulte [linguagem de definição do descritor de segurança](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="6acfc-109">For more information, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

 

 
