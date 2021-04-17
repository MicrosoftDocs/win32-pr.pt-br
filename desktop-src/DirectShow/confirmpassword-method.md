---
description: O método DVDAdm. ConfirmPassword testa se a senha especificada corresponde à senha salva anteriormente.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Método ConfirmPassword (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755587"
---
# <a name="confirmpassword-method"></a><span data-ttu-id="0304b-103">Método ConfirmPassword</span><span class="sxs-lookup"><span data-stu-id="0304b-103">ConfirmPassword Method</span></span>

> [!Note]  
> <span data-ttu-id="0304b-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0304b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0304b-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0304b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0304b-106">O `DVDAdm.ConfirmPassword` método testa se a senha especificada corresponde à senha salva anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0304b-106">The `DVDAdm.ConfirmPassword` method tests whether the specified password matches the previously saved password.</span></span>

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="0304b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0304b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0304b-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="0304b-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="0304b-109">Especifica o nome do usuário como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0304b-109">Specifies the user's name as a String.</span></span>

</dd> <dt>

<span data-ttu-id="0304b-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="0304b-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="0304b-111">Especifica a nova senha como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0304b-111">Specifies the new password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0304b-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0304b-112">Return Value</span></span>

<span data-ttu-id="0304b-113">Retornará true se a senha especificada corresponder à senha existente; caso contrário, retorna false.</span><span class="sxs-lookup"><span data-stu-id="0304b-113">Returns true if the specified password matches the existing password, false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0304b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0304b-114">Remarks</span></span>

<span data-ttu-id="0304b-115">Atualmente, o parâmetro *sUserName* é ignorado neste e em todos os métodos relacionados.</span><span class="sxs-lookup"><span data-stu-id="0304b-115">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="0304b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0304b-116">Requirements</span></span>



| <span data-ttu-id="0304b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0304b-117">Requirement</span></span> | <span data-ttu-id="0304b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0304b-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0304b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0304b-119">Header</span></span><br/> | <dl> <span data-ttu-id="0304b-120"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="0304b-120"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0304b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0304b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0304b-122">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="0304b-122">**ChangePassword**</span></span>](changepassword-method.md)
</dt> <dt>

[<span data-ttu-id="0304b-123">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="0304b-123">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




