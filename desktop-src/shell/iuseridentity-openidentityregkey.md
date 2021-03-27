---
description: Preterido. Recupera a chave no registro que corresponde a essa identidade de usuário.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'Método IUserIdentity:: OpenIdentityRegKey (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967486"
---
# <a name="iuseridentityopenidentityregkey-method"></a><span data-ttu-id="94834-104">Método IUserIdentity:: OpenIdentityRegKey</span><span class="sxs-lookup"><span data-stu-id="94834-104">IUserIdentity::OpenIdentityRegKey method</span></span>

<span data-ttu-id="94834-105">\[O método **IUserIdentity:: OpenIdentityRegKey** está disponível para uso no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="94834-105">\[The **IUserIdentity::OpenIdentityRegKey** method is available for use in Windows 2000.</span></span> <span data-ttu-id="94834-106">No Windows XP, essa funcionalidade foi substituída por [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md)e pode ser alterada ou indisponível nas versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="94834-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="94834-107">Preterido.</span><span class="sxs-lookup"><span data-stu-id="94834-107">Deprecated.</span></span> <span data-ttu-id="94834-108">Recupera a chave no registro que corresponde a essa identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="94834-108">Retrieves the key in the registry that corresponds to this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="94834-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94834-109">Syntax</span></span>


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a><span data-ttu-id="94834-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94834-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94834-111">*dwDesiredAccess* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94834-111">*dwDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94834-112">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94834-112">Type: **DWORD**</span></span>

<span data-ttu-id="94834-113">Um valor que descreve o nível de acesso solicitado da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="94834-113">A value that describes the access level requested of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="94834-114">*phKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="94834-114">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94834-115">Tipo: \**HKEY \** _</span><span class="sxs-lookup"><span data-stu-id="94834-115">Type: \**HKEY\** _</span></span>

<span data-ttu-id="94834-116">Um ponteiro que recebe a chave do registro.</span><span class="sxs-lookup"><span data-stu-id="94834-116">A pointer that receives the registry key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94834-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94834-117">Return value</span></span>

<span data-ttu-id="94834-118">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="94834-118">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="94834-119">O resultado da solicitação do registro.</span><span class="sxs-lookup"><span data-stu-id="94834-119">The result of the registry request.</span></span> <span data-ttu-id="94834-120">Se for bem-sucedido, retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="94834-120">If successful, it returns **S\_OK**.</span></span> <span data-ttu-id="94834-121">Caso contrário, ele retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="94834-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="94834-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="94834-122">Return code</span></span>                                                                                            | <span data-ttu-id="94834-123">Description</span><span class="sxs-lookup"><span data-stu-id="94834-123">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="94834-124"><dt>**\_identidade E \_ não \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="94834-124"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="94834-125">Essa identidade não tem uma chave de registro associada.</span><span class="sxs-lookup"><span data-stu-id="94834-125">This identity does not have an associated registry key.</span></span><br/> |
| <dl> <span data-ttu-id="94834-126"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="94834-126"><dt>**E\_FAIL**</dt></span></span> </dl>                 | <span data-ttu-id="94834-127">A chave do registro não pôde ser acessada.</span><span class="sxs-lookup"><span data-stu-id="94834-127">The registry key was unable to be accessed.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="94834-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="94834-128">Remarks</span></span>

<span data-ttu-id="94834-129">O parâmetro *dwDesiredAccess* é um descritor de segurança de acesso do registro padrão que descreve o acesso que você deseja obter à chave do registro.</span><span class="sxs-lookup"><span data-stu-id="94834-129">The *dwDesiredAccess* parameter is a standard registry access security descriptor that describes the access you want to gain to the registry key.</span></span> <span data-ttu-id="94834-130">Para obter mais informações sobre a segurança do registro, incluindo uma lista de valores aceitáveis para esse parâmetro, consulte [segurança da chave do registro e direitos de acesso](../sysinfo/registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="94834-130">For more information on registry security, including a list of acceptable values for this parameter, see [Registry Key Security and Access Rights](../sysinfo/registry-key-security-and-access-rights.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94834-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94834-131">Requirements</span></span>



| <span data-ttu-id="94834-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="94834-132">Requirement</span></span> | <span data-ttu-id="94834-133">Valor</span><span class="sxs-lookup"><span data-stu-id="94834-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94834-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94834-134">Minimum supported client</span></span><br/> | <span data-ttu-id="94834-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94834-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="94834-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94834-136">Minimum supported server</span></span><br/> | <span data-ttu-id="94834-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94834-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="94834-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94834-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="94834-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="94834-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="94834-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="94834-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94834-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94834-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="94834-142">DLL</span><span class="sxs-lookup"><span data-stu-id="94834-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94834-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94834-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94834-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="94834-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94834-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="94834-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="94834-146">**IUserIdentity::GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="94834-146">**IUserIdentity::GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
