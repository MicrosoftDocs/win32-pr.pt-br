---
description: Limpa as informações de usuário em cache do objeto.
title: Método DIDiskQuotaUser. Invalidate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 9f8ad77c9697ed5d284cf782f431ec59b38ca415
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843267"
---
# <a name="didiskquotauserinvalidate-method"></a><span data-ttu-id="cfe2f-103">Método DIDiskQuotaUser. Invalidate</span><span class="sxs-lookup"><span data-stu-id="cfe2f-103">DIDiskQuotaUser.Invalidate method</span></span>

<span data-ttu-id="cfe2f-104">Limpa as informações de usuário em cache do objeto.</span><span class="sxs-lookup"><span data-stu-id="cfe2f-104">Clears the object's cached user information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfe2f-105">Syntax</span></span>


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a><span data-ttu-id="cfe2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfe2f-106">Parameters</span></span>

<span data-ttu-id="cfe2f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cfe2f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cfe2f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfe2f-108">Return value</span></span>

<span data-ttu-id="cfe2f-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cfe2f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe2f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfe2f-110">Remarks</span></span>

<span data-ttu-id="cfe2f-111">Esse método limpa as informações do usuário armazenadas no cache do objeto.</span><span class="sxs-lookup"><span data-stu-id="cfe2f-111">This method clears the user information stored in the object's cache.</span></span> <span data-ttu-id="cfe2f-112">Na próxima vez que uma solicitação for feita para informações relacionadas à cota, o objeto recuperará as informações do volume NTFS e atualizará o cache.</span><span class="sxs-lookup"><span data-stu-id="cfe2f-112">The next time a request is made for quota-related information, the object retrieves the information from the NTFS volume and refreshes the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe2f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfe2f-113">Requirements</span></span>



| <span data-ttu-id="cfe2f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe2f-114">Requirement</span></span> | <span data-ttu-id="cfe2f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cfe2f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe2f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfe2f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe2f-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cfe2f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cfe2f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfe2f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe2f-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cfe2f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cfe2f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="cfe2f-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfe2f-121"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cfe2f-121"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe2f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfe2f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe2f-123">**Objeto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="cfe2f-123">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




