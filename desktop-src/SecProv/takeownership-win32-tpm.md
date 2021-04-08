---
description: Instala um proprietário para o TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Método TakeOwnership da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011668"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a><span data-ttu-id="83c6e-103">Método TakeOwnership da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="83c6e-103">TakeOwnership method of the Win32\_Tpm class</span></span>

<span data-ttu-id="83c6e-104">O método **TakeOwnership** da classe [**Win32 \_ TPM**](win32-tpm.md) instala um proprietário para o TPM.</span><span class="sxs-lookup"><span data-stu-id="83c6e-104">The **TakeOwnership** method of the [**Win32\_Tpm**](win32-tpm.md) class installs an owner for the TPM.</span></span> <span data-ttu-id="83c6e-105">O proprietário do TPM pode fazer uso total dos recursos do TPM.</span><span class="sxs-lookup"><span data-stu-id="83c6e-105">The owner of the TPM can make full use of TPM capabilities.</span></span> <span data-ttu-id="83c6e-106">Depois que um proprietário é definido, nenhum outro usuário ou software pode reivindicar a propriedade do TPM.</span><span class="sxs-lookup"><span data-stu-id="83c6e-106">After an owner is set, no other user or software can claim ownership of the TPM.</span></span>

<span data-ttu-id="83c6e-107">Os métodos [**IsEnabled**](isenabled-win32-tpm.md), [**isActivated**](isactivated-win32-tpm.md)e [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) devem ser verdadeiros para que o método **TakeOwnership** possa ser bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="83c6e-107">The [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) methods must all be true before the **TakeOwnership** method can succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c6e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83c6e-108">Syntax</span></span>


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="83c6e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83c6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c6e-110">*OwnerAuth* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="83c6e-110">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83c6e-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83c6e-111">Type: **string**</span></span>

<span data-ttu-id="83c6e-112">Uma cadeia de caracteres que identifica o proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="83c6e-112">A string that identifies the TPM owner.</span></span> <span data-ttu-id="83c6e-113">Essa cadeia de caracteres deve ser uma cadeia de caracteres terminada em NULL codificada em base64 que contenha exatamente 20 bytes de dados binários.</span><span class="sxs-lookup"><span data-stu-id="83c6e-113">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="83c6e-114">Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma frase secreta nesse formato esperado.</span><span class="sxs-lookup"><span data-stu-id="83c6e-114">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="83c6e-115">O parâmetro *OwnerAuth* será lido no registro se nenhum for fornecido.</span><span class="sxs-lookup"><span data-stu-id="83c6e-115">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c6e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83c6e-116">Return value</span></span>

<span data-ttu-id="83c6e-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83c6e-117">Type: **uint32**</span></span>

<span data-ttu-id="83c6e-118">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="83c6e-118">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="83c6e-119">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="83c6e-119">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="83c6e-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="83c6e-120">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="83c6e-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="83c6e-121">Description</span></span>                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83c6e-122"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="83c6e-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="83c6e-123">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="83c6e-123">The method was successful.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="83c6e-124"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="83c6e-124"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="83c6e-125">O parâmetro *OwnerAuth* não é válido.</span><span class="sxs-lookup"><span data-stu-id="83c6e-125">The *OwnerAuth* parameter is not valid.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="83c6e-126"><dt>**TPM \_ \_ \_ Conjunto de proprietário E**</dt> <dt>2150105108 (0x80280014)</dt></span><span class="sxs-lookup"><span data-stu-id="83c6e-126"><dt>**TPM\_E\_OWNER\_SET**</dt> <dt>2150105108 (0x80280014)</dt></span></span> </dl>            | <span data-ttu-id="83c6e-127">Já existe um proprietário no TPM.</span><span class="sxs-lookup"><span data-stu-id="83c6e-127">An owner already exists on the TPM.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="83c6e-128"><dt>**TPM \_ E \_ sem \_ endosso**</dt> <dt>2150105123 (0x80280023)</dt></span><span class="sxs-lookup"><span data-stu-id="83c6e-128"><dt>**TPM\_E\_NO\_ENDORSEMENT**</dt> <dt>2150105123 (0x80280023)</dt></span></span> </dl>       | <span data-ttu-id="83c6e-129">Nenhuma chave de endosso pode ser encontrada no TPM.</span><span class="sxs-lookup"><span data-stu-id="83c6e-129">No endorsement key can be found on the TPM.</span></span><br/> <span data-ttu-id="83c6e-130">Para criar um par de chaves de endosso no TPM, consulte o método [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="83c6e-130">To create an endorsement key pair on the TPM, see the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="83c6e-131"><dt>**TPM \_ E \_ instalação \_ desabilitada**</dt> <dt>2150105099 (0x8028000B)</dt></span><span class="sxs-lookup"><span data-stu-id="83c6e-131"><dt>**TPM\_E\_INSTALL\_DISABLED**</dt> <dt>2150105099 (0x8028000B)</dt></span></span> </dl>     | <span data-ttu-id="83c6e-132">Não é possível instalar um proprietário neste TPM.</span><span class="sxs-lookup"><span data-stu-id="83c6e-132">An owner cannot be installed on this TPM.</span></span><br/> <span data-ttu-id="83c6e-133">Para obter informações sobre como permitir a instalação de um proprietário de dispositivo, consulte [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="83c6e-133">For information about how to allow installation of a device owner, see [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span></span><br/> |
| <dl> <span data-ttu-id="83c6e-134"><dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="83c6e-134"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="83c6e-135">O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="83c6e-135">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="83c6e-136">Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="83c6e-136">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="83c6e-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="83c6e-137">Remarks</span></span>

<span data-ttu-id="83c6e-138">Os métodos [**IsEnabled**](isenabled-win32-tpm.md), [**isActivated**](isactivated-win32-tpm.md)e [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) devem ser verdadeiros para que **TakeOwnership** possa ter sucesso.</span><span class="sxs-lookup"><span data-stu-id="83c6e-138">The methods [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) must all be true before **TakeOwnership** can succeed.</span></span>

<span data-ttu-id="83c6e-139">Você deve usar o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para alterar uma frase secreta no valor de entrada usado para o parâmetro *OwnerAuth* .</span><span class="sxs-lookup"><span data-stu-id="83c6e-139">You should use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to change a passphrase into the input value used for the *OwnerAuth* parameter.</span></span>

<span data-ttu-id="83c6e-140">O método **TakeOwnership** faz backup do valor de autorização do proprietário para Active Directory se as configurações de política de grupo apropriadas foram configuradas.</span><span class="sxs-lookup"><span data-stu-id="83c6e-140">The **TakeOwnership** method backs up the owner authorization value to Active Directory if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="83c6e-141">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="83c6e-141">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="83c6e-142">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="83c6e-142">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="83c6e-143">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="83c6e-143">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="83c6e-144">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="83c6e-144">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83c6e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83c6e-145">Requirements</span></span>



| <span data-ttu-id="83c6e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="83c6e-146">Requirement</span></span> | <span data-ttu-id="83c6e-147">Valor</span><span class="sxs-lookup"><span data-stu-id="83c6e-147">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c6e-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83c6e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="83c6e-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83c6e-149">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="83c6e-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83c6e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="83c6e-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83c6e-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="83c6e-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="83c6e-152">Namespace</span></span><br/>                | <span data-ttu-id="83c6e-153">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="83c6e-153">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="83c6e-154">MOF</span><span class="sxs-lookup"><span data-stu-id="83c6e-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83c6e-155"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="83c6e-155"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="83c6e-156">DLL</span><span class="sxs-lookup"><span data-stu-id="83c6e-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83c6e-157"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="83c6e-157"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83c6e-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="83c6e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c6e-159">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="83c6e-159">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
