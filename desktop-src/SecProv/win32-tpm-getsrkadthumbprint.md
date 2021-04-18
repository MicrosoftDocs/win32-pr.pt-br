---
description: Obtém a impressão digital da chave raiz de armazenamento para um determinado módulo da parte pública da chave raiz de armazenamento do TPM.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Método Win32_Tpm:: GetSrkADThumbprint'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762902"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a><span data-ttu-id="17f08-103">\_Método TPM:: GetSrkADThumbprint do Win32</span><span class="sxs-lookup"><span data-stu-id="17f08-103">Win32\_Tpm::GetSrkADThumbprint method</span></span>

<span data-ttu-id="17f08-104">Obtém a impressão digital da chave raiz de armazenamento para um determinado módulo da parte pública da chave raiz de armazenamento do TPM.</span><span class="sxs-lookup"><span data-stu-id="17f08-104">Gets the Storage root key thumbprint for a given modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="17f08-105">A impressão digital é usada para indexar as chaves raiz de armazenamento no servidor de Active Directory se o Active Directory backup das informações de autorização do proprietário do TPM for habilitado por meio da configuração Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="17f08-105">The thumbprint is used to index the Storage Root Keys on the Active Directory server if the Active Directory backup of TPM owner authorization information is enabled through Group Policy setting.</span></span>

> [!Note]  
> <span data-ttu-id="17f08-106">A partir do Windows 10, versão 1607, a autorização do proprietário do TPM nunca é submetida a backup em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="17f08-106">Beginning with Windows 10, version 1607, the TPM owner authorization is never backed up to Active Directory.</span></span>

 

<span data-ttu-id="17f08-107">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="17f08-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f08-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17f08-108">Syntax</span></span>


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a><span data-ttu-id="17f08-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17f08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f08-110">*SrkPublicKeyModulus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17f08-110">*SrkPublicKeyModulus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17f08-111">O módulo da parte pública da chave raiz de armazenamento do TPM.</span><span class="sxs-lookup"><span data-stu-id="17f08-111">The modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="17f08-112">Ele também pode ser obtido usando o método [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) da classe [Win32 \_ TPM](win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="17f08-112">It can also be obtained using the [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) method of the [Win32\_TPM](win32-tpm.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="17f08-113">*SrkADThumbprint* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="17f08-113">*SrkADThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17f08-114">Retorna uma matriz de 20 bytes que contém a impressão digital da chave raiz de armazenamento para o módulo fornecido.</span><span class="sxs-lookup"><span data-stu-id="17f08-114">Returns a 20-byte array containing the storage root key thumbprint for the given modulus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17f08-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17f08-115">Return value</span></span>

<span data-ttu-id="17f08-116">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="17f08-116">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="17f08-117">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="17f08-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="17f08-118">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="17f08-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="17f08-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="17f08-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="17f08-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="17f08-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="17f08-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="17f08-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17f08-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="17f08-122">Remarks</span></span>

<span data-ttu-id="17f08-123">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="17f08-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="17f08-124">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="17f08-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="17f08-125">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="17f08-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="17f08-126">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="17f08-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17f08-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17f08-127">Requirements</span></span>



| <span data-ttu-id="17f08-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="17f08-128">Requirement</span></span> | <span data-ttu-id="17f08-129">Valor</span><span class="sxs-lookup"><span data-stu-id="17f08-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f08-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17f08-130">Minimum supported client</span></span><br/> | <span data-ttu-id="17f08-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="17f08-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="17f08-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17f08-132">Minimum supported server</span></span><br/> | <span data-ttu-id="17f08-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="17f08-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="17f08-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="17f08-134">Namespace</span></span><br/>                | <span data-ttu-id="17f08-135">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="17f08-135">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="17f08-136">MOF</span><span class="sxs-lookup"><span data-stu-id="17f08-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17f08-137"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="17f08-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="17f08-138">DLL</span><span class="sxs-lookup"><span data-stu-id="17f08-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17f08-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="17f08-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f08-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="17f08-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f08-141">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="17f08-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
