---
description: Define ou recupera um valor booliano que especifica se os prompts de interface do usuário para uma identidade de signatário ou remetente podem ser usados.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Propriedade Settings. EnablePromptForCertificateUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758157"
---
# <a name="settingsenablepromptforcertificateui-property"></a><span data-ttu-id="7c9d5-103">Propriedade Settings. EnablePromptForCertificateUI</span><span class="sxs-lookup"><span data-stu-id="7c9d5-103">Settings.EnablePromptForCertificateUI property</span></span>

<span data-ttu-id="7c9d5-104">\[A propriedade **EnablePromptForCertificateUI** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="7c9d5-104">\[The **EnablePromptForCertificateUI** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="7c9d5-105">A propriedade **EnablePromptForCertificateUI** define ou recupera um valor booliano que especifica se os prompts de interface do usuário para a identidade de um signatário ou remetente podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="7c9d5-105">The **EnablePromptForCertificateUI** property sets or retrieves a Boolean value that specifies whether user interface prompts for a signer or sender's identity can be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c9d5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c9d5-106">Syntax</span></span>


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7c9d5-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7c9d5-107">Property value</span></span>

<span data-ttu-id="7c9d5-108">Se **for true**, os prompts da interface do usuário para o assinante ou a identidade do remetente poderão ser usados.</span><span class="sxs-lookup"><span data-stu-id="7c9d5-108">If **true**, user interface prompts for a signer or sender's identity can be used.</span></span> <span data-ttu-id="7c9d5-109">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="7c9d5-109">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="7c9d5-110">Definir essa propriedade não desabilita os avisos gerados antes de qualquer uso de chave privada ser feito de um aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="7c9d5-110">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c9d5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c9d5-111">Requirements</span></span>



| <span data-ttu-id="7c9d5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c9d5-112">Requirement</span></span> | <span data-ttu-id="7c9d5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7c9d5-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9d5-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7c9d5-114">Redistributable</span></span><br/> | <span data-ttu-id="7c9d5-115">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c9d5-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7c9d5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7c9d5-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="7c9d5-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c9d5-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c9d5-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c9d5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c9d5-119">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="7c9d5-119">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




