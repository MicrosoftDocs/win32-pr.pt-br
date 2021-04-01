---
title: Método REVOKE da classe Win32_TSIssuedLicense
description: Revoga a Serviços de Área de Trabalho Remota licenças de acesso para cliente por dispositivo (RDS \ 160; CALs por dispositivo) que são representadas pelo \_ objeto TSIssuedLicense do Win32. Essa não é uma função estática.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método REVOKE
- Método REVOKE Serviços de Área de Trabalho Remota, classe Win32_TSIssuedLicense
- Classe Win32_TSIssuedLicense Serviços de Área de Trabalho Remota, método REVOKE
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645180"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a><span data-ttu-id="f804f-107">Método REVOKE da classe Win32 \_ TSIssuedLicense</span><span class="sxs-lookup"><span data-stu-id="f804f-107">Revoke method of the Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="f804f-108">Revoga a Serviços de Área de Trabalho Remota licenças de acesso para cliente por dispositivo (RDS CALs por dispositivo) que são representadas pelo objeto [**\_ TSIssuedLicense do Win32**](win32-tsissuedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="f804f-108">Revokes the Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are represented by the [**Win32\_TSIssuedLicense**](win32-tsissuedlicense.md) object.</span></span> <span data-ttu-id="f804f-109">Essa não é uma função estática.</span><span class="sxs-lookup"><span data-stu-id="f804f-109">This is not a static function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f804f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f804f-110">Syntax</span></span>


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a><span data-ttu-id="f804f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f804f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f804f-112">*RevokableCals* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f804f-112">*RevokableCals* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f804f-113">Número de RDS CALs do mesmo tipo que o objeto atual que pode ser revogado.</span><span class="sxs-lookup"><span data-stu-id="f804f-113">Number of RDS CALs of the same type as the current object that can be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="f804f-114">*NextRevokeAllowedOn* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f804f-114">*NextRevokeAllowedOn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f804f-115">Data em que o administrador pode tentar revogar licenças novamente.</span><span class="sxs-lookup"><span data-stu-id="f804f-115">Date that the administrator can next try to revoke licenses.</span></span> <span data-ttu-id="f804f-116">Esse parâmetro contém apenas dados válidos quando a chamada do método **REVOKE** falhou porque a contagem máxima de revogação foi atingida.</span><span class="sxs-lookup"><span data-stu-id="f804f-116">This parameter only contains valid data when the **Revoke** method call has failed because the maximum revoke count has been reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f804f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f804f-117">Remarks</span></span>

<span data-ttu-id="f804f-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="f804f-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f804f-119">Somente CALs por dispositivo RDS podem ser revogadas.</span><span class="sxs-lookup"><span data-stu-id="f804f-119">Only RDS Per Device CALs can be revoked.</span></span>

<span data-ttu-id="f804f-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f804f-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f804f-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f804f-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f804f-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f804f-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f804f-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f804f-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f804f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f804f-124">Requirements</span></span>



| <span data-ttu-id="f804f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f804f-125">Requirement</span></span> | <span data-ttu-id="f804f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f804f-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f804f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f804f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f804f-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f804f-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f804f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f804f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f804f-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f804f-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f804f-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="f804f-131">Namespace</span></span><br/>                | <span data-ttu-id="f804f-132">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f804f-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f804f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f804f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f804f-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f804f-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f804f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f804f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f804f-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f804f-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f804f-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f804f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f804f-138">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="f804f-138">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> </dl>

 

