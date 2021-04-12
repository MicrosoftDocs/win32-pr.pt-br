---
description: Redefine o TPM para seu estado de fábrica-padrão.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Método Clear da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170914"
---
# <a name="clear-method-of-the-win32_tpm-class"></a><span data-ttu-id="b7560-103">Método Clear da classe do \_ TPM do Win32</span><span class="sxs-lookup"><span data-stu-id="b7560-103">Clear method of the Win32\_Tpm class</span></span>

<span data-ttu-id="b7560-104">O método **Clear** da classe [**do \_ TPM do Win32**](win32-tpm.md) redefine o TPM para seu estado de fábrica padrão.</span><span class="sxs-lookup"><span data-stu-id="b7560-104">The **Clear** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the TPM to its factory-default state.</span></span> <span data-ttu-id="b7560-105">Um proprietário do TPM pode usar esse método para cancelar a propriedade do TPM e invalidar materiais criptográficos criados pelo proprietário anterior.</span><span class="sxs-lookup"><span data-stu-id="b7560-105">A TPM owner can use this method to cancel TPM ownership and invalidate cryptographic materials created by the previous owner.</span></span> <span data-ttu-id="b7560-106">Esse método suspende o BitLocker se a chamada puder fazer com que a recuperação do BitLocker seja necessária.</span><span class="sxs-lookup"><span data-stu-id="b7560-106">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="b7560-107">O BitLocker será retomado automaticamente depois que o TPM tiver sido provisionado.</span><span class="sxs-lookup"><span data-stu-id="b7560-107">BitLocker would automatically resume once TPM has been provisioned.</span></span>

> [!Caution]  
> <span data-ttu-id="b7560-108">Ao limpar o TPM, você perderá todas as chaves do TPM criadas e usadas pelos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b7560-108">By clearing the TPM, you will lose all TPM keys created and used by applications.</span></span> <span data-ttu-id="b7560-109">Se essas chaves foram usadas para criptografar dados, verifique se você tem outra maneira de acessar os dados antes de limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="b7560-109">If these keys were used to encrypt data, ensure that you have another way to access the data before clearing the TPM.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b7560-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7560-110">Syntax</span></span>


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="b7560-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7560-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7560-112">*OwnerAuth* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7560-112">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7560-113">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7560-113">Type: **string**</span></span>

<span data-ttu-id="b7560-114">Uma cadeia de caracteres que identifica o proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="b7560-114">A string that identifies the TPM owner.</span></span> <span data-ttu-id="b7560-115">Essa cadeia de caracteres deve ser uma cadeia de caracteres codificada em base64 que contenha exatamente 20 bytes de dados binários.</span><span class="sxs-lookup"><span data-stu-id="b7560-115">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="b7560-116">Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma frase secreta nesse formato esperado.</span><span class="sxs-lookup"><span data-stu-id="b7560-116">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="b7560-117">O parâmetro *OwnerAuth* será lido no registro se nenhum for fornecido.</span><span class="sxs-lookup"><span data-stu-id="b7560-117">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7560-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7560-118">Return value</span></span>

<span data-ttu-id="b7560-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7560-119">Type: **uint32**</span></span>

<span data-ttu-id="b7560-120">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="b7560-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="b7560-121">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="b7560-121">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="b7560-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b7560-122">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="b7560-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7560-123">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7560-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b7560-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="b7560-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b7560-125">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="b7560-126"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="b7560-126"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="b7560-127">O valor de autorização do proprietário fornecido não pode executar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b7560-127">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="b7560-128"><dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="b7560-128"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="b7560-129">O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="b7560-129">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="b7560-130">Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="b7560-130">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7560-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7560-131">Remarks</span></span>

<span data-ttu-id="b7560-132">A execução desse método pode ajudar a preparar um computador equipado com TPM para reciclagem.</span><span class="sxs-lookup"><span data-stu-id="b7560-132">Running this method can help prepare a TPM-equipped computer for recycling.</span></span>

<span data-ttu-id="b7560-133">Para limpar o TPM, mas não tiver mais a autorização de proprietário do TPM, você precisa de acesso físico ao computador.</span><span class="sxs-lookup"><span data-stu-id="b7560-133">To clear the TPM but no longer have the TPM owner authorization, you need physical access to the computer.</span></span> <span data-ttu-id="b7560-134">O método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) inclui funcionalidade para ajudar a limpar o TPM sem autorização de proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="b7560-134">The [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method includes functionality to help clear the TPM without TPM owner authorization.</span></span>

<span data-ttu-id="b7560-135">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b7560-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b7560-136">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b7560-136">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b7560-137">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b7560-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b7560-138">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b7560-138">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7560-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7560-139">Requirements</span></span>



| <span data-ttu-id="b7560-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7560-140">Requirement</span></span> | <span data-ttu-id="b7560-141">Valor</span><span class="sxs-lookup"><span data-stu-id="b7560-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7560-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7560-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b7560-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7560-143">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b7560-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7560-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b7560-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7560-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b7560-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7560-146">Namespace</span></span><br/>                | <span data-ttu-id="b7560-147">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b7560-147">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="b7560-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b7560-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7560-149"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="b7560-149"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7560-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b7560-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7560-151"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="b7560-151"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7560-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7560-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7560-153">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="b7560-153">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
