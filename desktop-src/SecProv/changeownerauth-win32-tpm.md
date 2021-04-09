---
description: Altera o valor de autorização do proprietário do TPM.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Método ChangeOwnerAuth da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090176"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="5da43-103">Método ChangeOwnerAuth da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="5da43-103">ChangeOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="5da43-104">O método **ChangeOwnerAuth** da classe [**Win32 \_ TPM**](win32-tpm.md) altera o valor de autorização do proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="5da43-104">The **ChangeOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class changes the TPM owner authorization value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5da43-105">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="5da43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5da43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da43-107">*OldOwnerAuth* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5da43-107">*OldOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5da43-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5da43-108">Type: **string**</span></span>

<span data-ttu-id="5da43-109">Uma cadeia de caracteres que nomeia o valor atual de autorização do proprietário do TPM do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5da43-109">A string that names the current TPM owner authorization value of the device.</span></span> <span data-ttu-id="5da43-110">Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma senha para esse valor de autorização.</span><span class="sxs-lookup"><span data-stu-id="5da43-110">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="5da43-111">O parâmetro *OldOwnerAuth* não é fornecido ou uma cadeia de caracteres vazia é fornecida, esse método obtém o valor do registro, se presente.</span><span class="sxs-lookup"><span data-stu-id="5da43-111">The *OldOwnerAuth* parameter is not supplied or an empty string is provided, this method gets the value from the registry if present.</span></span>

</dd> <dt>

<span data-ttu-id="5da43-112">*NewOwnerAuth* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5da43-112">*NewOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5da43-113">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5da43-113">Type: **string**</span></span>

<span data-ttu-id="5da43-114">Uma cadeia de caracteres que nomeia o novo valor de autorização de proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="5da43-114">A string that names the new TPM owner authorization value.</span></span> <span data-ttu-id="5da43-115">Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma senha para esse valor de autorização.</span><span class="sxs-lookup"><span data-stu-id="5da43-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="5da43-116">O parâmetro *NewOwnerAuth* não pode ser vazio ou **nulo.**</span><span class="sxs-lookup"><span data-stu-id="5da43-116">The *NewOwnerAuth* parameter cannot be empty or **NULL.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da43-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5da43-117">Return value</span></span>

<span data-ttu-id="5da43-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5da43-118">Type: **uint32**</span></span>

<span data-ttu-id="5da43-119">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="5da43-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="5da43-120">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="5da43-120">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="5da43-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5da43-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="5da43-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="5da43-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5da43-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5da43-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                              | <span data-ttu-id="5da43-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5da43-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="5da43-125"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="5da43-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>                   | <span data-ttu-id="5da43-126">O valor de autorização do proprietário do TPM atual está incorreto.</span><span class="sxs-lookup"><span data-stu-id="5da43-126">The current TPM owner authorization value is incorrect.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="5da43-127"><dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="5da43-127"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl>      | <span data-ttu-id="5da43-128">O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="5da43-128">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="5da43-129">Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="5da43-129">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="5da43-130"><dt>**FVE \_ E \_ ad \_ Schema \_ não \_ instalado**</dt> <dt>2150694922 (0x8031000A)</dt></span><span class="sxs-lookup"><span data-stu-id="5da43-130"><dt>**FVE\_E\_AD\_SCHEMA\_NOT\_INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt></span></span> </dl> | <span data-ttu-id="5da43-131">Não é possível salvar informações de recuperação na rede.</span><span class="sxs-lookup"><span data-stu-id="5da43-131">Cannot save recovery information to the network.</span></span> <span data-ttu-id="5da43-132">O computador foi configurado para armazenar informações de recuperação para Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="5da43-132">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="5da43-133">Para obter instruções sobre como configurar Active Directory, consulte [criptografia de unidade de disco BitLocker guia de configuração: fazendo backup de informações de recuperação do TPM e do BitLocker para Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="5da43-133">For instructions on how to set up Active Directory, see [BitLocker Drive Encryption Configuration Guide: Backing Up BitLocker and TPM Recovery Information to Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span></span><br/> |
| <dl> <span data-ttu-id="5da43-134"><dt>**Falha na conexão**</dt> <dt>2147943755 (0x8007054B)</dt></span><span class="sxs-lookup"><span data-stu-id="5da43-134"><dt>**Connection Failed**</dt> <dt>2147943755 (0x8007054B)</dt></span></span> </dl>                  | <span data-ttu-id="5da43-135">Não é possível salvar informações de recuperação na rede.</span><span class="sxs-lookup"><span data-stu-id="5da43-135">Cannot save recovery information to the network.</span></span> <span data-ttu-id="5da43-136">O computador foi configurado para armazenar informações de recuperação para Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="5da43-136">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="5da43-137">Uma conexão de rede é necessária para continuar.</span><span class="sxs-lookup"><span data-stu-id="5da43-137">A network connection is required to continue.</span></span><br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="5da43-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="5da43-138">Remarks</span></span>

<span data-ttu-id="5da43-139">O método **ChangeOwnerAuth** faz backup da nova autorização de proprietário do TPM para Active Directory Domain Services se as configurações de política de grupo apropriadas foram configuradas.</span><span class="sxs-lookup"><span data-stu-id="5da43-139">The **ChangeOwnerAuth** method backs up the new TPM owner authorization to Active Directory Domain Services if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="5da43-140">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5da43-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5da43-141">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="5da43-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5da43-142">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5da43-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5da43-143">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5da43-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5da43-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5da43-144">Requirements</span></span>



| <span data-ttu-id="5da43-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5da43-145">Requirement</span></span> | <span data-ttu-id="5da43-146">Valor</span><span class="sxs-lookup"><span data-stu-id="5da43-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da43-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5da43-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5da43-148">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5da43-148">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5da43-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5da43-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5da43-150">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5da43-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5da43-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="5da43-151">Namespace</span></span><br/>                | <span data-ttu-id="5da43-152">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5da43-152">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="5da43-153">MOF</span><span class="sxs-lookup"><span data-stu-id="5da43-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5da43-154"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="5da43-154"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5da43-155">DLL</span><span class="sxs-lookup"><span data-stu-id="5da43-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5da43-156"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="5da43-156"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da43-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="5da43-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da43-158">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="5da43-158">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
