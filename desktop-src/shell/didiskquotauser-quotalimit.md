---
description: Define ou obtém o limite de cota atual do usuário.
title: Propriedade DIDiskQuotaUser.QuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: b1971871bdeb18e3c7dd4c7978152bbec276fa8b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841627"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="ec9a5-103">Propriedade DIDiskQuotaUser.QuotaLimit</span><span class="sxs-lookup"><span data-stu-id="ec9a5-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="ec9a5-104">Define ou obtém o limite de cota [**atual do usuário.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="ec9a5-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="ec9a5-105">Essa propriedade é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ec9a5-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec9a5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec9a5-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="ec9a5-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ec9a5-107">Property value</span></span>

<span data-ttu-id="ec9a5-108">Um **valor** inteiro que especifica ou recebe o limite de cota atual do usuário, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ec9a5-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec9a5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec9a5-109">Requirements</span></span>



| <span data-ttu-id="ec9a5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec9a5-110">Requirement</span></span> | <span data-ttu-id="ec9a5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ec9a5-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec9a5-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec9a5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ec9a5-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec9a5-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec9a5-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec9a5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ec9a5-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec9a5-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ec9a5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ec9a5-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec9a5-117"><dt>Shell32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ec9a5-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec9a5-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec9a5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec9a5-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="ec9a5-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="ec9a5-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="ec9a5-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="ec9a5-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="ec9a5-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




