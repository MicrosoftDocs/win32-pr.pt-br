---
description: Obtém o uso do disco atual do usuário, em bytes.
title: Propriedade DIDiskQuotaUser. QuotaUsed
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: 7d5068e6f80fd2b0b435d04583e99da929e17fce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090020"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="4817b-103">Propriedade DIDiskQuotaUser. QuotaUsed</span><span class="sxs-lookup"><span data-stu-id="4817b-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="4817b-104">Obtém o uso do disco atual do usuário, em bytes.</span><span class="sxs-lookup"><span data-stu-id="4817b-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="4817b-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4817b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4817b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4817b-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="4817b-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4817b-107">Property value</span></span>

<span data-ttu-id="4817b-108">O valor **inteiro** que é definido como a quantidade de espaço em disco em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="4817b-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="4817b-109">Se a compactação de arquivo NTFS estiver habilitada, **QuotaUsed** refletirá a quantidade de espaço em disco que os dados precisariam em um estado descompactado.</span><span class="sxs-lookup"><span data-stu-id="4817b-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4817b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4817b-110">Requirements</span></span>



| <span data-ttu-id="4817b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4817b-111">Requirement</span></span> | <span data-ttu-id="4817b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="4817b-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4817b-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4817b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4817b-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4817b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4817b-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4817b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4817b-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4817b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4817b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="4817b-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4817b-118"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4817b-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4817b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="4817b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4817b-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="4817b-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="4817b-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="4817b-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="4817b-122">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="4817b-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="4817b-123">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="4817b-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




