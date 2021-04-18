---
description: Permite que o proprietário do TPM desabilite ou suspenda o TPM.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Método Disable da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811041"
---
# <a name="disable-method-of-the-win32_tpm-class"></a><span data-ttu-id="7f072-103">Método Disable da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="7f072-103">Disable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="7f072-104">O método **Disable** da classe [**Win32 \_ TPM**](win32-tpm.md) permite que o proprietário do TPM desabilite ou suspenda o TPM.</span><span class="sxs-lookup"><span data-stu-id="7f072-104">The **Disable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to disable or suspend the TPM.</span></span> <span data-ttu-id="7f072-105">Esse método suspende o BitLocker se a chamada puder fazer com que a recuperação do BitLocker seja necessária.</span><span class="sxs-lookup"><span data-stu-id="7f072-105">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="7f072-106">O BitLocker será retomado automaticamente depois que o TPM tiver sido provisionado.</span><span class="sxs-lookup"><span data-stu-id="7f072-106">BitLocker would automatically resume once TPM has been provisioned.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f072-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f072-107">Syntax</span></span>


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="7f072-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f072-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f072-109">*OwnerAuth* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7f072-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f072-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7f072-110">Type: **string**</span></span>

<span data-ttu-id="7f072-111">Uma cadeia de caracteres que identifica o proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="7f072-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="7f072-112">Essa cadeia de caracteres deve ser uma cadeia de caracteres codificada em base64 que contenha exatamente 20 bytes de dados binários.</span><span class="sxs-lookup"><span data-stu-id="7f072-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="7f072-113">Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma frase secreta nesse formato esperado.</span><span class="sxs-lookup"><span data-stu-id="7f072-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="7f072-114">O parâmetro *OwnerAuth* será lido no registro se nenhum for fornecido.</span><span class="sxs-lookup"><span data-stu-id="7f072-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f072-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f072-115">Return value</span></span>

<span data-ttu-id="7f072-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f072-116">Type: **uint32**</span></span>

<span data-ttu-id="7f072-117">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="7f072-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="7f072-118">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="7f072-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="7f072-119">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7f072-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="7f072-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f072-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f072-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7f072-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="7f072-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7f072-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="7f072-123"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="7f072-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="7f072-124">O valor de autorização do proprietário fornecido não pode executar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7f072-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="7f072-125"><dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="7f072-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="7f072-126">O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="7f072-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="7f072-127">Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="7f072-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f072-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f072-128">Remarks</span></span>

<span data-ttu-id="7f072-129">Para desabilitar o TPM sem ter o valor de autorização de proprietário do TPM, use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="7f072-129">To disable the TPM without having the TPM owner authorization value, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

<span data-ttu-id="7f072-130">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7f072-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7f072-131">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f072-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7f072-132">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7f072-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7f072-133">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7f072-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f072-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f072-134">Requirements</span></span>



| <span data-ttu-id="7f072-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f072-135">Requirement</span></span> | <span data-ttu-id="7f072-136">Valor</span><span class="sxs-lookup"><span data-stu-id="7f072-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f072-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f072-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7f072-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f072-138">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7f072-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f072-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7f072-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f072-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7f072-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f072-141">Namespace</span></span><br/>                | <span data-ttu-id="7f072-142">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7f072-142">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7f072-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7f072-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f072-144"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="7f072-144"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f072-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7f072-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f072-146"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="7f072-146"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f072-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f072-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f072-148">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="7f072-148">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="7f072-149">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="7f072-149">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
