---
description: Obtém o nome do contêiner da conta do usuário.
title: Propriedade DIDiskQuotaUser. AccountContainerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646831"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="5e6c5-103">Propriedade DIDiskQuotaUser. AccountContainerName</span><span class="sxs-lookup"><span data-stu-id="5e6c5-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="5e6c5-104">Obtém o nome do contêiner da conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e6c5-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="5e6c5-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5e6c5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6c5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e6c5-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="5e6c5-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5e6c5-107">Property value</span></span>

<span data-ttu-id="5e6c5-108">Um valor de cadeia de caracteres que é definido como o nome do contêiner da conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e6c5-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e6c5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e6c5-109">Remarks</span></span>

<span data-ttu-id="5e6c5-110">Para contas sem informações de serviços de diretório, essa propriedade contém o nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="5e6c5-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="5e6c5-111">Para contas com informações de serviços de diretório, essa propriedade contém um nome canônico com o nome do objeto de encerramento removido.</span><span class="sxs-lookup"><span data-stu-id="5e6c5-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e6c5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e6c5-112">Requirements</span></span>



| <span data-ttu-id="5e6c5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e6c5-113">Requirement</span></span> | <span data-ttu-id="5e6c5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5e6c5-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e6c5-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e6c5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5e6c5-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e6c5-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e6c5-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e6c5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5e6c5-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e6c5-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5e6c5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5e6c5-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e6c5-120"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5e6c5-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e6c5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e6c5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6c5-122">**Objeto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="5e6c5-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




