---
description: Obtém o uso do disco atual do usuário como uma cadeia de texto.
title: Propriedade DIDiskQuotaUser. QuotaUsedText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 1091d7f2d75b264b085c09af1873ac7c8ebd1617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967314"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="f0517-103">Propriedade DIDiskQuotaUser. QuotaUsedText</span><span class="sxs-lookup"><span data-stu-id="f0517-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="f0517-104">Obtém o uso do disco atual do usuário como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="f0517-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="f0517-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f0517-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0517-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0517-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="f0517-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f0517-107">Property value</span></span>

<span data-ttu-id="f0517-108">Um valor de cadeia de caracteres que é definido como a quantidade de espaço em disco em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="f0517-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="f0517-109">Se a compactação de arquivo NTFS estiver habilitada, essa propriedade refletirá a quantidade de espaço em disco que os dados precisariam em um estado descompactado.</span><span class="sxs-lookup"><span data-stu-id="f0517-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0517-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0517-110">Requirements</span></span>



| <span data-ttu-id="f0517-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0517-111">Requirement</span></span> | <span data-ttu-id="f0517-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f0517-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0517-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0517-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f0517-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0517-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0517-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0517-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f0517-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0517-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f0517-117">DLL</span><span class="sxs-lookup"><span data-stu-id="f0517-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0517-118"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f0517-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0517-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0517-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0517-120">**Objeto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="f0517-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="f0517-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="f0517-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="f0517-122">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="f0517-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="f0517-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="f0517-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




