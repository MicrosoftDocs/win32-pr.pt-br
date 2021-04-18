---
description: Redefine o período de tempo limite ou outro mecanismo que os fabricantes do TPM implementam para proteger contra ataques de dicionário em valores de autorização do TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Método ResetAuthLockOut da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756556"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a><span data-ttu-id="af6a4-103">Método ResetAuthLockOut da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="af6a4-103">ResetAuthLockOut method of the Win32\_Tpm class</span></span>

<span data-ttu-id="af6a4-104">O método **ResetAuthLockOut** da classe [**do \_ TPM do Win32**](win32-tpm.md) redefine o período de tempo limite ou outro mecanismo que os fabricantes do TPM implementam para proteger contra ataques de dicionário em valores de autorização do TPM.</span><span class="sxs-lookup"><span data-stu-id="af6a4-104">The **ResetAuthLockOut** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on TPM authorization values.</span></span> <span data-ttu-id="af6a4-105">Em um ataque de dicionário, um invasor tenta adivinhar um valor de autorização do TPM correto, tentando exaustivamente todos os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="af6a4-105">In a dictionary attack, an attacker tries to guess a correct TPM authorization value by exhaustively attempting all possible values.</span></span>

<span data-ttu-id="af6a4-106">Use esse método se o TPM estiver bloqueado devido a muitas tentativas incorretas na inserção da autorização do proprietário ou de outros valores de autorização.</span><span class="sxs-lookup"><span data-stu-id="af6a4-106">Use this method if the TPM is locked out due to too many incorrect attempts at entering the owner authorization or other authorization values.</span></span> <span data-ttu-id="af6a4-107">Quando o TPM estiver bloqueado, alguns ou todos os comandos emitidos para o TPM retornarão um erro, o TPM \_ E \_ defenderão o \_ bloqueio \_ em execução (0x80280803).</span><span class="sxs-lookup"><span data-stu-id="af6a4-107">When the TPM is locked out, some or all commands issued to the TPM will return an error, TPM\_E\_DEFEND\_LOCK\_RUNNING (0x80280803).</span></span>

> [!Note]  
> <span data-ttu-id="af6a4-108">Esse método só pode ser usado exatamente uma vez quando o TPM é bloqueado. Se a autorização de proprietário fornecida para esse método estiver incorreta, o TPM será bloqueado durante todo o período de tempo limite e as tentativas adicionais na redefinição do bloqueio falharão.</span><span class="sxs-lookup"><span data-stu-id="af6a4-108">This method can only be used exactly once when the TPM is locked out. If the owner authorization provided to this method is incorrect, the TPM will lock out for the entire time-out period and additional attempts at resetting the lock will fail.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="af6a4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af6a4-109">Syntax</span></span>


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="af6a4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af6a4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af6a4-111">*OwnerAuth* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="af6a4-111">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="af6a4-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="af6a4-112">Type: **string**</span></span>

<span data-ttu-id="af6a4-113">Uma cadeia de caracteres que identifica o proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="af6a4-113">A string that identifies the TPM owner.</span></span>

<span data-ttu-id="af6a4-114">Essa cadeia de caracteres deve ser uma cadeia de caracteres terminada em NULL codificada em base64 que contenha exatamente 20 bytes de dados binários.</span><span class="sxs-lookup"><span data-stu-id="af6a4-114">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="af6a4-115">Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma frase secreta nesse formato esperado.</span><span class="sxs-lookup"><span data-stu-id="af6a4-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="af6a4-116">O parâmetro *OwnerAuth* será lido no registro se nenhum for fornecido.</span><span class="sxs-lookup"><span data-stu-id="af6a4-116">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af6a4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af6a4-117">Return value</span></span>

<span data-ttu-id="af6a4-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af6a4-118">Type: **uint32**</span></span>

<span data-ttu-id="af6a4-119">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="af6a4-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span> <span data-ttu-id="af6a4-120">A tabela a seguir lista alguns dos valores de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="af6a4-120">The following table lists some of the common return values.</span></span>



| <span data-ttu-id="af6a4-121">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="af6a4-121">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="af6a4-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="af6a4-122">Description</span></span>                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af6a4-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="af6a4-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                            | <span data-ttu-id="af6a4-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="af6a4-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="af6a4-125"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="af6a4-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl> | <span data-ttu-id="af6a4-126">O valor de autorização do proprietário fornecido está incorreto.</span><span class="sxs-lookup"><span data-stu-id="af6a4-126">The provided owner authorization value is incorrect.</span></span> <span data-ttu-id="af6a4-127">Tentativas adicionais na redefinição do bloqueio falharão com esse mesmo erro.</span><span class="sxs-lookup"><span data-stu-id="af6a4-127">Additional attempts at resetting the lock will fail with this same error.</span></span> <span data-ttu-id="af6a4-128">Aguarde até que o período de tempo limite ou outro mecanismo específico do fabricante tenha expirado antes de tentar novamente os comandos bloqueados do TPM.</span><span class="sxs-lookup"><span data-stu-id="af6a4-128">Please wait until the time-out period or other manufacturer-specific mechanism has expired before retrying locked TPM commands.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af6a4-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="af6a4-129">Remarks</span></span>

<span data-ttu-id="af6a4-130">Esse método chama o \_ comando ResetLockValue do TPM no TPM.</span><span class="sxs-lookup"><span data-stu-id="af6a4-130">This method calls the TPM\_ResetLockValue command on the TPM.</span></span> <span data-ttu-id="af6a4-131">O comportamento exato desse método varia entre os fabricantes do TPM.</span><span class="sxs-lookup"><span data-stu-id="af6a4-131">The exact behavior of this method varies among TPM manufacturers.</span></span> <span data-ttu-id="af6a4-132">A documentação do fabricante do computador ou TPM pode fornecer informações adicionais sobre a implementação do mecanismo de ataque do anti-dicionário.</span><span class="sxs-lookup"><span data-stu-id="af6a4-132">Documentation from the computer or TPM manufacturer may provide additional information on the implementation of the anti-dictionary attack mechanism.</span></span>

<span data-ttu-id="af6a4-133">Em geral, os fabricantes podem detectar ataques de dicionário mantendo o controle das autenticações com falha.</span><span class="sxs-lookup"><span data-stu-id="af6a4-133">In general, manufacturers can detect dictionary attacks by keeping track of failed authentications.</span></span> <span data-ttu-id="af6a4-134">Se o número ou a frequência de falhas se tornarem alta o suficiente, o TPM bloqueará outros comandos por um determinado tempo.</span><span class="sxs-lookup"><span data-stu-id="af6a4-134">If the number or frequency of failures become high enough, the TPM will lock out further commands for a certain time.</span></span> <span data-ttu-id="af6a4-135">Em geral, o período de tempo limite inicial será curto, para permitir que um usuário legítimo a oportunidade de corrigir a situação.</span><span class="sxs-lookup"><span data-stu-id="af6a4-135">Generally, the initial time-out period will be short, to allow a legitimate user a chance to correct the situation.</span></span> <span data-ttu-id="af6a4-136">Se as falhas continuarem, a duração de cada período de tempo limite subsequente pode aumentar rapidamente.</span><span class="sxs-lookup"><span data-stu-id="af6a4-136">If failures continue, the duration of each subsequent time-out period may increase rapidly.</span></span>

<span data-ttu-id="af6a4-137">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="af6a4-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="af6a4-138">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="af6a4-138">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="af6a4-139">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="af6a4-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="af6a4-140">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="af6a4-140">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af6a4-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af6a4-141">Requirements</span></span>



| <span data-ttu-id="af6a4-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="af6a4-142">Requirement</span></span> | <span data-ttu-id="af6a4-143">Valor</span><span class="sxs-lookup"><span data-stu-id="af6a4-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="af6a4-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af6a4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="af6a4-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af6a4-145">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="af6a4-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af6a4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="af6a4-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af6a4-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="af6a4-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="af6a4-148">Namespace</span></span><br/>                | <span data-ttu-id="af6a4-149">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="af6a4-149">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="af6a4-150">MOF</span><span class="sxs-lookup"><span data-stu-id="af6a4-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af6a4-151"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="af6a4-151"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="af6a4-152">DLL</span><span class="sxs-lookup"><span data-stu-id="af6a4-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af6a4-153"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="af6a4-153"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af6a4-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="af6a4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af6a4-155">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="af6a4-155">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
