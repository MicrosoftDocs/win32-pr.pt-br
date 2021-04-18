---
description: Indica a ação do usuário necessária para executar a operação de presença física do Trusted Platform Module (TPM). Use o método SetPhysicalPresenceRequest para solicitar uma operação.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Método GetPhysicalPresenceTransition da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758152"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a><span data-ttu-id="f6ef0-104">Método GetPhysicalPresenceTransition da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="f6ef0-104">GetPhysicalPresenceTransition method of the Win32\_Tpm class</span></span>

<span data-ttu-id="f6ef0-105">O método **GetPhysicalPresenceTransition** da classe [**Win32 \_ TPM**](win32-tpm.md) indica a ação do usuário necessária para executar a operação de presença física do Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="f6ef0-105">The **GetPhysicalPresenceTransition** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates the user action that is needed to perform the Trusted Platform Module (TPM) physical presence operation.</span></span> <span data-ttu-id="f6ef0-106">Use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span> <span data-ttu-id="f6ef0-107">A ação do usuário necessária está definida para seu computador no momento da fabricação.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-107">The required user action is set for your computer at the time of manufacture.</span></span> <span data-ttu-id="f6ef0-108">Normalmente, é necessária uma reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-108">Usually a computer restart is needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ef0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6ef0-109">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a><span data-ttu-id="f6ef0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6ef0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6ef0-111">*Transição* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f6ef0-111">*Transition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ef0-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6ef0-112">Type: **uint32**</span></span>

<span data-ttu-id="f6ef0-113">Um valor inteiro que especifica a transição necessária para executar uma operação de presença física de TPM.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-113">An integer value that specifies the transition needed to perform a TPM physical presence operation.</span></span>



| <span data-ttu-id="f6ef0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f6ef0-114">Value</span></span>                                                                        | <span data-ttu-id="f6ef0-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f6ef0-115">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6ef0-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6ef0-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="f6ef0-117">Nenhuma ação do usuário é necessária para executar uma operação de presença física do TPM.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-117">No user action is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="f6ef0-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f6ef0-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="f6ef0-119">Para executar uma operação de presença física do TPM, o usuário deve desligar o computador e ligá-lo novamente usando o botão de energia.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-119">To perform a TPM physical presence operation, the user must shutdown the computer and then turn it back on by using the power button.</span></span> <span data-ttu-id="f6ef0-120">O usuário deve estar fisicamente presente no computador para aceitar ou rejeitar a alteração quando solicitado pelo BIOS.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-120">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/> |
| <dl> <span data-ttu-id="f6ef0-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6ef0-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f6ef0-122">Para executar uma operação de presença física de TPM, o usuário deve reiniciar o computador usando uma reinicialização a quente.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-122">To perform a TPM physical presence operation, the user must restart the computer by using a warm reboot.</span></span> <span data-ttu-id="f6ef0-123">O usuário deve estar fisicamente presente no computador para aceitar ou rejeitar a alteração quando solicitado pelo BIOS.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-123">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/>                              |
| <dl> <span data-ttu-id="f6ef0-124"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f6ef0-124"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f6ef0-125">A ação do usuário necessária é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-125">The required user action is unknown.</span></span><br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6ef0-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6ef0-126">Return value</span></span>

<span data-ttu-id="f6ef0-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6ef0-127">Type: **uint32**</span></span>

<span data-ttu-id="f6ef0-128">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-128">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="f6ef0-129">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-129">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="f6ef0-130">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f6ef0-130">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="f6ef0-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6ef0-131">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6ef0-132"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f6ef0-132"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="f6ef0-133">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-133">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="f6ef0-134"><dt>**TPM \_ \_Falha de \_ ACPI \_ PPI**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="f6ef0-134"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="f6ef0-135">Ocorreu uma falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-135">A hardware failure occurred.</span></span> <span data-ttu-id="f6ef0-136">Consulte o fabricante do seu computador para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-136">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6ef0-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6ef0-137">Remarks</span></span>

<span data-ttu-id="f6ef0-138">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f6ef0-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f6ef0-139">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f6ef0-140">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f6ef0-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f6ef0-141">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f6ef0-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6ef0-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6ef0-142">Requirements</span></span>



| <span data-ttu-id="f6ef0-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6ef0-143">Requirement</span></span> | <span data-ttu-id="f6ef0-144">Valor</span><span class="sxs-lookup"><span data-stu-id="f6ef0-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ef0-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6ef0-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ef0-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6ef0-146">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f6ef0-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6ef0-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ef0-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6ef0-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f6ef0-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6ef0-149">Namespace</span></span><br/>                | <span data-ttu-id="f6ef0-150">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f6ef0-150">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="f6ef0-151">MOF</span><span class="sxs-lookup"><span data-stu-id="f6ef0-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6ef0-152"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="f6ef0-152"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6ef0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f6ef0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6ef0-154"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="f6ef0-154"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6ef0-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6ef0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ef0-156">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f6ef0-156">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="f6ef0-157">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="f6ef0-157">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
