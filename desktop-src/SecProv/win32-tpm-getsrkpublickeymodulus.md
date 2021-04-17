---
description: Obtém o módulo da parte pública da chave raiz de armazenamento do TPM.
ms.assetid: 266AE378-8BF2-4F6E-A055-E15D95E218DC
title: 'Método Win32_Tpm:: GetSrkPublicKeyModulus'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkPublicKeyModulus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6d78abb695f2a9bc9de3887c8128395c2403b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762901"
---
# <a name="win32_tpmgetsrkpublickeymodulus-method"></a><span data-ttu-id="0576e-103">\_Método TPM:: GetSrkPublicKeyModulus do Win32</span><span class="sxs-lookup"><span data-stu-id="0576e-103">Win32\_Tpm::GetSrkPublicKeyModulus method</span></span>

<span data-ttu-id="0576e-104">Obtém o módulo da parte pública da chave raiz de armazenamento do TPM.</span><span class="sxs-lookup"><span data-stu-id="0576e-104">Gets the modulus of the public portion of the TPM Storage Root Key.</span></span>

<span data-ttu-id="0576e-105">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="0576e-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="0576e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0576e-106">Syntax</span></span>


```C++
uint32 GetSrkPublicKeyModulus(
  [out] uint8 SrkPublicKeyModulus
);
```



## <a name="parameters"></a><span data-ttu-id="0576e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0576e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0576e-108">*SrkPublicKeyModulus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0576e-108">*SrkPublicKeyModulus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0576e-109">Retorna uma matriz de 256 bytes que contém o módulo da parte pública da chave de raiz de armazenamento do TPM</span><span class="sxs-lookup"><span data-stu-id="0576e-109">Returns a 256-byte array containing the modulus of the public portion of the TPM Storage Root Key</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0576e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0576e-110">Return value</span></span>

<span data-ttu-id="0576e-111">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="0576e-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="0576e-112">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="0576e-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="0576e-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0576e-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="0576e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0576e-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="0576e-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0576e-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0576e-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0576e-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0576e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0576e-117">Remarks</span></span>

<span data-ttu-id="0576e-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0576e-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0576e-119">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="0576e-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0576e-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="0576e-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0576e-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0576e-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0576e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0576e-122">Requirements</span></span>



| <span data-ttu-id="0576e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0576e-123">Requirement</span></span> | <span data-ttu-id="0576e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0576e-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0576e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0576e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0576e-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0576e-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0576e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0576e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0576e-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0576e-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0576e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="0576e-129">Namespace</span></span><br/>                | <span data-ttu-id="0576e-130">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0576e-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="0576e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0576e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0576e-132"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="0576e-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="0576e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0576e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0576e-134"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="0576e-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0576e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="0576e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0576e-136">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="0576e-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
