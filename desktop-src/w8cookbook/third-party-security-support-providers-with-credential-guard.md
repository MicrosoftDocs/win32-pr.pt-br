---
title: Credential Guard e aplicativos de terceiros
description: O Credential Guard não permite que SSPs terceirizados solicitem hashes de senha da LSA.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454070"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a><span data-ttu-id="223b5-103">Provedores de suporte de segurança de terceiros com o Credential Guard</span><span class="sxs-lookup"><span data-stu-id="223b5-103">Third party Security Support Providers with Credential Guard</span></span>

<span data-ttu-id="223b5-104">O Credential Guard não permite que SSPs terceirizados solicitem hashes de senha da LSA.</span><span class="sxs-lookup"><span data-stu-id="223b5-104">Credential Guard does not allow 3rd party SSPs to ask for password hashes from LSA.</span></span> <span data-ttu-id="223b5-105">No entanto, SSPs e PAs ainda são notificados sobre a senha quando um usuário faz logon e/ou altera sua senha.</span><span class="sxs-lookup"><span data-stu-id="223b5-105">However, SSPs and APs still get notified of the password when a user logs on and/or changes their password.</span></span> <span data-ttu-id="223b5-106">Qualquer uso de APIs não documentadas dentro de SSPs e PAs personalizados não é permitido.</span><span class="sxs-lookup"><span data-stu-id="223b5-106">Any use of undocumented APIs within custom SSPs and APs are not supported.</span></span>

<span data-ttu-id="223b5-107">À medida que a profundidade e a abrangência de proteções fornecidas pelo Credential Guard aumentam, as versões posteriores do Windows 10 com o Credential Guard podem ter impacto em cenários que funcionavam no passado.</span><span class="sxs-lookup"><span data-stu-id="223b5-107">As the depth and breadth of protections provided by Credential Guard are increased, subsequent releases of Windows 10 with Credential Guard running may impact scenarios that were working in the past.</span></span> <span data-ttu-id="223b5-108">Por exemplo, o Credential Guard pode bloquear o uso de um determinado tipo de credencial ou componente para impedir que malwares tirem proveito das vulnerabilidades.</span><span class="sxs-lookup"><span data-stu-id="223b5-108">For example, Credential Guard may block the use of a particular type of credential or a particular component to prevent malware from taking advantage of vulnerabilities.</span></span> <span data-ttu-id="223b5-109">Portanto, recomendamos que os cenários necessários para as operações em uma organização sejam testados antes da atualização de um dispositivo que tenha o Credential Guard em execução.</span><span class="sxs-lookup"><span data-stu-id="223b5-109">Therefore, we recommend that scenarios required for operations in an organization are tested before upgrading a device that has Credential Guard running.</span></span>

<span data-ttu-id="223b5-110">Veja [Este artigo](/windows/security/identity-protection/credential-guard/credential-guard) para obter a descrição completa e as atenuações recomendadas.</span><span class="sxs-lookup"><span data-stu-id="223b5-110">Please refer to [this article](/windows/security/identity-protection/credential-guard/credential-guard) for the full description and recommended mitigations.</span></span>

 

 