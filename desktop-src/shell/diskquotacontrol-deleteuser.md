---
description: Exclui um usuário do volume.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Método DiskQuotaControl. DeleteUser (Dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164303"
---
# <a name="diskquotacontroldeleteuser-method"></a><span data-ttu-id="6cd4d-103">Método DiskQuotaControl. DeleteUser</span><span class="sxs-lookup"><span data-stu-id="6cd4d-103">DiskQuotaControl.DeleteUser method</span></span>

<span data-ttu-id="6cd4d-104">Exclui um usuário do volume.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-104">Deletes a user from the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd4d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cd4d-105">Syntax</span></span>


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="6cd4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cd4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd4d-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="6cd4d-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="6cd4d-108">Tipo: **objeto**</span><span class="sxs-lookup"><span data-stu-id="6cd4d-108">Type: **Object**</span></span>

<span data-ttu-id="6cd4d-109">Uma expressão de objeto que é avaliada como o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) do usuário.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd4d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cd4d-110">Return value</span></span>

<span data-ttu-id="6cd4d-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cd4d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cd4d-112">Remarks</span></span>

<span data-ttu-id="6cd4d-113">Esse método falhará se o usuário possuir qualquer armazenamento no volume.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-113">This method fails if the user owns any storage on the volume.</span></span> <span data-ttu-id="6cd4d-114">Antes de excluir um usuário de um volume, todo o armazenamento desse usuário deve ser excluído, ser movido para outro volume ou ter sua propriedade transferida para outro usuário.</span><span class="sxs-lookup"><span data-stu-id="6cd4d-114">Before you delete a user from a volume, all storage for that user must be deleted, be moved to another volume, or have its ownership transferred to another user.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd4d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cd4d-115">Requirements</span></span>



| <span data-ttu-id="6cd4d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cd4d-116">Requirement</span></span> | <span data-ttu-id="6cd4d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6cd4d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd4d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cd4d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd4d-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6cd4d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6cd4d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cd4d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd4d-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6cd4d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6cd4d-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6cd4d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cd4d-123"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd4d-123"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="6cd4d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6cd4d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cd4d-125"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6cd4d-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cd4d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cd4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd4d-127">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="6cd4d-127">**AddUser**</span></span>](diskquotacontrol-adduser.md)
</dt> <dt>

[<span data-ttu-id="6cd4d-128">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="6cd4d-128">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




