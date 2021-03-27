---
description: Obtém o limite de aviso do usuário como uma cadeia de texto.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: Propriedade DIDiskQuotaUser. QuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 511829233b93dbe164ce2feccd1247ccebf3ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967317"
---
# <a name="didiskquotauserquotathresholdtext-property"></a><span data-ttu-id="70428-103">Propriedade DIDiskQuotaUser. QuotaThresholdText</span><span class="sxs-lookup"><span data-stu-id="70428-103">DIDiskQuotaUser.QuotaThresholdText property</span></span>

<span data-ttu-id="70428-104">Obtém o limite de aviso do usuário como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="70428-104">Gets the user's warning threshold as a text string.</span></span>

<span data-ttu-id="70428-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="70428-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="70428-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70428-106">Syntax</span></span>


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="70428-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="70428-107">Property value</span></span>

<span data-ttu-id="70428-108">O valor da cadeia de caracteres que contém o limite de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="70428-108">The string value that contains the user's warning threshold.</span></span> <span data-ttu-id="70428-109">Se o uso do disco de um usuário exceder esse valor e a propriedade [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) for definida como **true**, o sistema gerará uma entrada de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="70428-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="70428-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70428-110">Requirements</span></span>



| <span data-ttu-id="70428-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="70428-111">Requirement</span></span> | <span data-ttu-id="70428-112">Valor</span><span class="sxs-lookup"><span data-stu-id="70428-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70428-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70428-113">Minimum supported client</span></span><br/> | <span data-ttu-id="70428-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="70428-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70428-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70428-115">Minimum supported server</span></span><br/> | <span data-ttu-id="70428-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="70428-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="70428-117">DLL</span><span class="sxs-lookup"><span data-stu-id="70428-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70428-118"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="70428-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70428-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="70428-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70428-120">**Objeto IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="70428-120">**IDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="70428-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="70428-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="70428-122">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="70428-122">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="70428-123">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="70428-123">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




