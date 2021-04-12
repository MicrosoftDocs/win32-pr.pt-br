---
description: Redefine o valor de autorização da chave raiz de armazenamento (SRK) como compatível com o sistema operacional.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Método ResetSrkAuth da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d838ded7051511b6a8f9117327ee7cdb1a00d7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297431"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="8c5d2-103">Método ResetSrkAuth da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="8c5d2-103">ResetSrkAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="8c5d2-104">O método **ResetSrkAuth** da classe [**Win32 \_ TPM**](win32-tpm.md) redefine o valor de autorização da chave de raiz de armazenamento (SRK) para ser compatível com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-104">The **ResetSrkAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the Storage Root Key (SRK) authorization value to be compatible with the operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c5d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c5d2-105">Syntax</span></span>


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="8c5d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c5d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c5d2-107">*OwnerAuth* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c5d2-107">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c5d2-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8c5d2-108">Type: **string**</span></span>

<span data-ttu-id="8c5d2-109">Uma cadeia de caracteres que identifica o proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-109">A string that identifies the TPM owner.</span></span> <span data-ttu-id="8c5d2-110">Essa cadeia de caracteres deve ser uma cadeia de caracteres terminada em NULL codificada em base64 que contenha exatamente 20 bytes de dados binários.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-110">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="8c5d2-111">Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma frase secreta nesse formato esperado.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-111">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="8c5d2-112">O parâmetro *OwnerAuth* será lido no registro se nenhum for fornecido.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-112">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c5d2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c5d2-113">Return value</span></span>

<span data-ttu-id="8c5d2-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c5d2-114">Type: **uint32**</span></span>

<span data-ttu-id="8c5d2-115">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="8c5d2-116">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-116">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="8c5d2-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8c5d2-117">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="8c5d2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c5d2-118">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c5d2-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8c5d2-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="8c5d2-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-120">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="8c5d2-121"><dt> **TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="8c5d2-121"><dt>**TPM\_E\_AUTHFAIL** </dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>             | <span data-ttu-id="8c5d2-122">O valor de autorização do proprietário fornecido não pode atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-122">The provided owner authorization value cannot fulfill the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="8c5d2-123"><dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="8c5d2-123"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="8c5d2-124">O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-124">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="8c5d2-125">Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="8c5d2-125">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8c5d2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c5d2-126">Remarks</span></span>

<span data-ttu-id="8c5d2-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8c5d2-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8c5d2-128">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8c5d2-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8c5d2-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8c5d2-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8c5d2-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c5d2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c5d2-131">Requirements</span></span>



| <span data-ttu-id="8c5d2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c5d2-132">Requirement</span></span> | <span data-ttu-id="8c5d2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8c5d2-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c5d2-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c5d2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8c5d2-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c5d2-135">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8c5d2-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c5d2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8c5d2-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c5d2-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8c5d2-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c5d2-138">Namespace</span></span><br/>                | <span data-ttu-id="8c5d2-139">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="8c5d2-139">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="8c5d2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8c5d2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c5d2-141"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="8c5d2-141"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c5d2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8c5d2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c5d2-143"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="8c5d2-143"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c5d2-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c5d2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c5d2-145">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="8c5d2-145">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
