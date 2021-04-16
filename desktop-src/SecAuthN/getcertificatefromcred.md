---
description: Obtém o certificado da credencial do usuário.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Função GetCertificateFromCred (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747243"
---
# <a name="getcertificatefromcred-function"></a><span data-ttu-id="55fcc-103">Função GetCertificateFromCred</span><span class="sxs-lookup"><span data-stu-id="55fcc-103">GetCertificateFromCred function</span></span>

<span data-ttu-id="55fcc-104">Obtém o certificado da credencial do usuário.</span><span class="sxs-lookup"><span data-stu-id="55fcc-104">Gets the certificate from the user credential.</span></span>

## <a name="syntax"></a><span data-ttu-id="55fcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55fcc-105">Syntax</span></span>


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a><span data-ttu-id="55fcc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55fcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55fcc-107">*ProviderHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55fcc-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55fcc-108">Identificador do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="55fcc-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="55fcc-109">*ClientToken* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55fcc-109">*ClientToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55fcc-110">Token do chamador que está recuperando o certificado.</span><span class="sxs-lookup"><span data-stu-id="55fcc-110">Token of the caller who is retrieving the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="55fcc-111">*SuppliedCred* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55fcc-111">*SuppliedCred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55fcc-112">Um ponteiro para uma estrutura de [**\_ \_ credencial fornecida pelo SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) que contém a credencial de uma ID online cujo certificado é solicitado.</span><span class="sxs-lookup"><span data-stu-id="55fcc-112">A pointer to a [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure that contains the credential of an online ID whose certificate is requested.</span></span> <span data-ttu-id="55fcc-113">O provedor de identidade deve validar os dados de entrada como se eles esvenham de uma fonte não confiável.</span><span class="sxs-lookup"><span data-stu-id="55fcc-113">The identity provider must validate the input data as if it is coming from an untrusted source.</span></span>

</dd> <dt>

<span data-ttu-id="55fcc-114">*SuppliedCredSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55fcc-114">*SuppliedCredSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55fcc-115">O tamanho, em bytes, do buffer *SuppliedCred* .</span><span class="sxs-lookup"><span data-stu-id="55fcc-115">The size, in bytes, of the *SuppliedCred* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="55fcc-116">*CertContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="55fcc-116">*CertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55fcc-117">Se a função for realizada com sucesso, esse parâmetro será um ponteiro para o \_ ponteiro de contexto CCERT retornado.</span><span class="sxs-lookup"><span data-stu-id="55fcc-117">If the function succeeds, this parameter is a pointer to the returned CCERT\_CONTEXT pointer.</span></span> <span data-ttu-id="55fcc-118">Quando você terminar de usar o contexto do certificado, libere-o chamando a função [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="55fcc-118">When you have finished using the certificate context, release it by calling the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55fcc-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55fcc-119">Return value</span></span>

<span data-ttu-id="55fcc-120">Se a função for bem-sucedida, a função retornará o STATUS \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="55fcc-120">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="55fcc-121">Se a função falhar, a função poderá retornar um dos seguintes códigos de erro de NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="55fcc-121">If the function fails, the function may return one of the following NTSTATUS error codes.</span></span>



| <span data-ttu-id="55fcc-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="55fcc-122">Return value</span></span>                                                                                            | <span data-ttu-id="55fcc-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="55fcc-123">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55fcc-124"><dt>STATUS \_ sem \_ suporte</dt></span><span class="sxs-lookup"><span data-stu-id="55fcc-124"><dt>STATUS\_NOT\_SUPPORTED</dt></span></span> </dl>       | <span data-ttu-id="55fcc-125">O provedor de identidade não reconhece o tipo de credencial da credencial fornecida.</span><span class="sxs-lookup"><span data-stu-id="55fcc-125">The identity provider does not recognize the credential type of the supplied credential.</span></span> <span data-ttu-id="55fcc-126">O LSA tentará o próximo provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="55fcc-126">LSA will try the next identity provider.</span></span><br/>                                           |
| <dl> <span data-ttu-id="55fcc-127"><dt>\_falha de logon de status \_</dt></span><span class="sxs-lookup"><span data-stu-id="55fcc-127"><dt>STATUS\_LOGON\_FAILURE</dt></span></span> </dl>       | <span data-ttu-id="55fcc-128">A credencial está incorreta.</span><span class="sxs-lookup"><span data-stu-id="55fcc-128">The credential is incorrect.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="55fcc-129"><dt>parâmetro de STATUS \_ inválido \_</dt></span><span class="sxs-lookup"><span data-stu-id="55fcc-129"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>   | <span data-ttu-id="55fcc-130">Um parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="55fcc-130">A parameter is not valid.</span></span> <span data-ttu-id="55fcc-131">A credencial pode estar em um formato incorreto e não na estrutura de [**\_ \_ credenciais fornecida pelo SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) definido.</span><span class="sxs-lookup"><span data-stu-id="55fcc-131">The credential may be in an incorrect format and not in the defined [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure.</span></span><br/> |
| <dl> <span data-ttu-id="55fcc-132"><dt>rede de STATUS \_ \_ inacessível</dt></span><span class="sxs-lookup"><span data-stu-id="55fcc-132"><dt>STATUS\_NETWORK\_UNREACHABLE</dt></span></span> </dl> | <span data-ttu-id="55fcc-133">O provedor de identidade não pode entrar em contato com a nuvem para obter o certificado.</span><span class="sxs-lookup"><span data-stu-id="55fcc-133">The identity provider cannot contact the cloud to obtain the certificate.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="55fcc-134"><dt>senha de STATUS \_ \_ expirada</dt></span><span class="sxs-lookup"><span data-stu-id="55fcc-134"><dt>STATUS\_PASSWORD\_EXPIRED</dt></span></span> </dl>    | <span data-ttu-id="55fcc-135">A senha da conta expirou.</span><span class="sxs-lookup"><span data-stu-id="55fcc-135">The account password has expired.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="55fcc-136"><dt>conta de STATUS \_ \_ bloqueada \_</dt></span><span class="sxs-lookup"><span data-stu-id="55fcc-136"><dt>STATUS\_ACCOUNT\_LOCKED\_OUT</dt></span></span> </dl> | <span data-ttu-id="55fcc-137">A conta foi bloqueada.</span><span class="sxs-lookup"><span data-stu-id="55fcc-137">The account has been locked out.</span></span> <br/>                                                                                                                                           |
| <dl> <span data-ttu-id="55fcc-138"><dt>Others</dt></span><span class="sxs-lookup"><span data-stu-id="55fcc-138"><dt>Others</dt></span></span> </dl>                       | <span data-ttu-id="55fcc-139">Outros códigos de erro específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="55fcc-139">Other provider-specific error codes.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="55fcc-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="55fcc-140">Remarks</span></span>

<span data-ttu-id="55fcc-141">Antes de buscar o certificado da nuvem, o provedor de identidade deve verificar se há um certificado válido para esse usuário no repositório de certificados "MY" do usuário.</span><span class="sxs-lookup"><span data-stu-id="55fcc-141">Before fetching the certificate from the cloud, the identity provider should check that there is a valid certificate for this user in the user's "MY" certificate store.</span></span> <span data-ttu-id="55fcc-142">Se houver um certificado válido, o provedor deverá retornar esse certificado para evitar o tráfego de rede desnecessário.</span><span class="sxs-lookup"><span data-stu-id="55fcc-142">If a valid certificate exists, the provider should return this certificate to avoid unnecessary network traffic.</span></span>

<span data-ttu-id="55fcc-143">O provedor de identidade também pode armazenar o certificado em cache localmente, desde que ele seja protegido do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="55fcc-143">The identity provider can also cache the certificate locally as long as it is protected from the current user.</span></span>

## <a name="requirements"></a><span data-ttu-id="55fcc-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55fcc-144">Requirements</span></span>



| <span data-ttu-id="55fcc-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="55fcc-145">Requirement</span></span> | <span data-ttu-id="55fcc-146">Valor</span><span class="sxs-lookup"><span data-stu-id="55fcc-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55fcc-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55fcc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="55fcc-148">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="55fcc-148">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="55fcc-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55fcc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="55fcc-150">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="55fcc-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="55fcc-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55fcc-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="55fcc-152"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="55fcc-152"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

