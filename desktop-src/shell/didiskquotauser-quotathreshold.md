---
description: Define ou Obtém o limite de aviso do usuário, em bytes.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Propriedade DIDiskQuotaUser. QuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826887"
---
# <a name="didiskquotauserquotathreshold-property"></a><span data-ttu-id="3955c-103">Propriedade DIDiskQuotaUser. QuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="3955c-103">DIDiskQuotaUser.QuotaThreshold property</span></span>

<span data-ttu-id="3955c-104">Define ou Obtém o limite de aviso do usuário, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3955c-104">Sets or gets the user's warning threshold, in bytes.</span></span>

<span data-ttu-id="3955c-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3955c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3955c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3955c-106">Syntax</span></span>


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="3955c-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3955c-107">Property value</span></span>

<span data-ttu-id="3955c-108">Um valor **inteiro** que especifica ou recebe o limite de aviso do usuário.</span><span class="sxs-lookup"><span data-stu-id="3955c-108">An **Integer** value that specifies or receives the user's warning threshold.</span></span> <span data-ttu-id="3955c-109">Se o uso do disco de um usuário exceder esse valor e a propriedade [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) for definida como **true**, o sistema gerará uma entrada de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="3955c-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="3955c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3955c-110">Requirements</span></span>



| <span data-ttu-id="3955c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3955c-111">Requirement</span></span> | <span data-ttu-id="3955c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3955c-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3955c-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3955c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3955c-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3955c-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3955c-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3955c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3955c-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3955c-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3955c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3955c-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3955c-118"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3955c-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3955c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3955c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3955c-120">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="3955c-120">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="3955c-121">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="3955c-121">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="3955c-122">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="3955c-122">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="3955c-123">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="3955c-123">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




