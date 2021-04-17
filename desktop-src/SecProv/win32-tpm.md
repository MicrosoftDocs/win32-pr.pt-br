---
description: Representa o Trusted Platform Module (TPM), um chip de segurança de hardware que fornece uma raiz de confiança para um sistema de computador.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756146"
---
# <a name="win32_tpm-class"></a><span data-ttu-id="e5161-103">\_Classe TPM do Win32</span><span class="sxs-lookup"><span data-stu-id="e5161-103">Win32\_Tpm class</span></span>

<span data-ttu-id="e5161-104">A classe **Win32 \_ TPM** representa o Trusted Platform Module (TPM), um chip de segurança de hardware que fornece uma raiz de confiança para um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="e5161-104">The **Win32\_Tpm** class represents the Trusted Platform Module (TPM), a hardware security chip that provides a root of trust for a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5161-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5161-105">Syntax</span></span>

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a><span data-ttu-id="e5161-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e5161-106">Members</span></span>

<span data-ttu-id="e5161-107">A classe **Win32 \_ TPM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e5161-107">The **Win32\_Tpm** class has these types of members:</span></span>

-   [<span data-ttu-id="e5161-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e5161-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5161-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5161-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5161-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e5161-110">Methods</span></span>

<span data-ttu-id="e5161-111">A classe **Win32 \_ TPM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e5161-111">The **Win32\_Tpm** class has these methods.</span></span>



| <span data-ttu-id="e5161-112">Método</span><span class="sxs-lookup"><span data-stu-id="e5161-112">Method</span></span>                                                                                   | <span data-ttu-id="e5161-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5161-113">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5161-114">**AddBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="e5161-114">**AddBlockedCommand**</span></span>](addblockedcommand-win32-tpm.md)                                 | <span data-ttu-id="e5161-115">Adiciona um comando TPM à lista local de comandos bloqueados no Windows.</span><span class="sxs-lookup"><span data-stu-id="e5161-115">Adds a TPM command to the local list of commands blocked on Windows.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="e5161-116">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="e5161-116">**ChangeOwnerAuth**</span></span>](changeownerauth-win32-tpm.md)                                     | <span data-ttu-id="e5161-117">Altera o valor de autorização do proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-117">Changes the TPM owner authorization value.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="e5161-118">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="e5161-118">**Clear**</span></span>](clear-win32-tpm.md)                                                         | <span data-ttu-id="e5161-119">Redefine o TPM para seu estado de fábrica-padrão.</span><span class="sxs-lookup"><span data-stu-id="e5161-119">Resets the TPM to its factory-default state.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="e5161-120">**ConvertToOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="e5161-120">**ConvertToOwnerAuth**</span></span>](converttoownerauth-win32-tpm.md)                               | <span data-ttu-id="e5161-121">Converte uma frase secreta fornecida pelo usuário em um valor de autorização de proprietário de 20 bytes que pode ser usado para interagir com o TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-121">Converts a user-provided passphrase to a 20-byte owner authorization value that can be used to interact with the TPM.</span></span><br/>                                                            |
| [<span data-ttu-id="e5161-122">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="e5161-122">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)                   | <span data-ttu-id="e5161-123">Cria um par de chaves de endosso de 2048 bits no TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-123">Creates a 2048-bit endorsement key pair on the TPM.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="e5161-124">**Desabilitar**</span><span class="sxs-lookup"><span data-stu-id="e5161-124">**Disable**</span></span>](disable-win32-tpm.md)                                                     | <span data-ttu-id="e5161-125">Permite que o proprietário do TPM desabilite o TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-125">Allows the TPM owner to disable the TPM.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="e5161-126">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="e5161-126">**Enable**</span></span>](enable-win32-tpm.md)                                                       | <span data-ttu-id="e5161-127">Permite que o proprietário do TPM habilite o TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-127">Allows the TPM owner to enable the TPM.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="e5161-128">**GetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="e5161-128">**GetPhysicalPresenceRequest**</span></span>](getphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="e5161-129">Obtém e retorna a operação de presença física de TPM pendente.</span><span class="sxs-lookup"><span data-stu-id="e5161-129">Gets and returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="e5161-130">Use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação.</span><span class="sxs-lookup"><span data-stu-id="e5161-130">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span><br/> |
| [<span data-ttu-id="e5161-131">**GetPhysicalPresenceResponse**</span><span class="sxs-lookup"><span data-stu-id="e5161-131">**GetPhysicalPresenceResponse**</span></span>](getphysicalpresenceresponse-win32-tpm.md)             | <span data-ttu-id="e5161-132">Obtém e retorna os resultados de uma operação de presença física de TPM que foi executada.</span><span class="sxs-lookup"><span data-stu-id="e5161-132">Gets and returns the results from a TPM physical presence operation that was performed.</span></span><br/>                                                                                          |
| [<span data-ttu-id="e5161-133">**GetPhysicalPresenceTransition**</span><span class="sxs-lookup"><span data-stu-id="e5161-133">**GetPhysicalPresenceTransition**</span></span>](getphysicalpresencetransition-win32-tpm.md)         | <span data-ttu-id="e5161-134">Indica a ação do usuário necessária para executar uma operação de presença física do TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-134">Indicates the user action that is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e5161-135">**Isactivad**</span><span class="sxs-lookup"><span data-stu-id="e5161-135">**IsActivated**</span></span>](isactivated-win32-tpm.md)                                             | <span data-ttu-id="e5161-136">Indica se o TPM está ativado.</span><span class="sxs-lookup"><span data-stu-id="e5161-136">Indicates whether the TPM is activated.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="e5161-137">**IsCommandBlocked**</span><span class="sxs-lookup"><span data-stu-id="e5161-137">**IsCommandBlocked**</span></span>](iscommandblocked-win32-tpm.md)                                   | <span data-ttu-id="e5161-138">Indica se o comando TPM pode ser executado neste sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e5161-138">Indicates whether the TPM command can run on this operating system.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e5161-139">**IsCommandPresent**</span><span class="sxs-lookup"><span data-stu-id="e5161-139">**IsCommandPresent**</span></span>](iscommandpresent-win32-tpm.md)                                   | <span data-ttu-id="e5161-140">Indica se há suporte para um comando TPM neste computador.</span><span class="sxs-lookup"><span data-stu-id="e5161-140">Indicates whether a TPM command is supported by this computer.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="e5161-141">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e5161-141">**IsEnabled**</span></span>](isenabled-win32-tpm.md)                                                 | <span data-ttu-id="e5161-142">Indica se o TPM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e5161-142">Indicates whether the TPM is enabled.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="e5161-143">**IsEndorsementKeyPairPresent**</span><span class="sxs-lookup"><span data-stu-id="e5161-143">**IsEndorsementKeyPairPresent**</span></span>](isendorsementkeypairpresent-win32-tpm.md)             | <span data-ttu-id="e5161-144">Indica se o TPM tem um par de chaves de endosso.</span><span class="sxs-lookup"><span data-stu-id="e5161-144">Indicates whether the TPM has an endorsement key pair.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="e5161-145">**Isdele**</span><span class="sxs-lookup"><span data-stu-id="e5161-145">**IsOwned**</span></span>](isowned-win32-tpm.md)                                                     | <span data-ttu-id="e5161-146">Indica se o TPM tem um proprietário.</span><span class="sxs-lookup"><span data-stu-id="e5161-146">Indicates whether the TPM has an owner.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="e5161-147">**IsOwnerClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="e5161-147">**IsOwnerClearDisabled**</span></span>](isownercleardisabled-win32-tpm.md)                           | <span data-ttu-id="e5161-148">Indica se o proprietário do TPM pode limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-148">Indicates whether the TPM owner can clear the TPM.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="e5161-149">**IsOwnershipAllowed**</span><span class="sxs-lookup"><span data-stu-id="e5161-149">**IsOwnershipAllowed**</span></span>](isownershipallowed-win32-tpm.md)                               | <span data-ttu-id="e5161-150">Indica se um proprietário do TPM pode ser instalado.</span><span class="sxs-lookup"><span data-stu-id="e5161-150">Indicates whether a TPM owner can be installed.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="e5161-151">**IsPhysicalClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="e5161-151">**IsPhysicalClearDisabled**</span></span>](isphysicalcleardisabled-win32-tpm.md)                     | <span data-ttu-id="e5161-152">Indica se uma operação de presença física de TPM pode limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-152">Indicates whether a TPM physical presence operation can clear the TPM.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="e5161-153">**IsPhysicalPresenceHardwareEnabled**</span><span class="sxs-lookup"><span data-stu-id="e5161-153">**IsPhysicalPresenceHardwareEnabled**</span></span>](isphysicalpresencehardwareenabled-win32-tpm.md) | <span data-ttu-id="e5161-154">Indica se este computador dá suporte a um caminho de hardware dedicado para sinalizar a presença física.</span><span class="sxs-lookup"><span data-stu-id="e5161-154">Indicates whether this computer supports a dedicated hardware path to signal physical presence.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e5161-155">**IsSrkAuthCompatible**</span><span class="sxs-lookup"><span data-stu-id="e5161-155">**IsSrkAuthCompatible**</span></span>](issrkauthcompatible-win32-tpm.md)                             | <span data-ttu-id="e5161-156">Indica se a autorização da chave de raiz de armazenamento (SRK) é compatível com o Windows.</span><span class="sxs-lookup"><span data-stu-id="e5161-156">Indicates whether the Storage Root Key (SRK) authorization is compatible with Windows.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e5161-157">**RemoveBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="e5161-157">**RemoveBlockedCommand**</span></span>](removeblockedcommand-win32-tpm.md)                           | <span data-ttu-id="e5161-158">Remove um comando TPM da lista local de comandos bloqueados pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="e5161-158">Removes a TPM command from the local list of commands blocked by Windows.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="e5161-159">**ResetAuthLockOut**</span><span class="sxs-lookup"><span data-stu-id="e5161-159">**ResetAuthLockOut**</span></span>](resetauthlockout-win32-tpm.md)                                   | <span data-ttu-id="e5161-160">Redefine o período de tempo limite ou outro mecanismo que os fabricantes de TPM implementam para proteger contra ataques de dicionário no TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-160">Resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on the TPM.</span></span><br/>                                                 |
| [<span data-ttu-id="e5161-161">**ResetSrkAuth**</span><span class="sxs-lookup"><span data-stu-id="e5161-161">**ResetSrkAuth**</span></span>](resetsrkauth-win32-tpm.md)                                           | <span data-ttu-id="e5161-162">Redefine o valor de autorização da chave raiz de armazenamento (SRK) para ser compatível com o Windows.</span><span class="sxs-lookup"><span data-stu-id="e5161-162">Resets the Storage Root Key (SRK) authorization value to be compatible with Windows.</span></span><br/>                                                                                             |
| [<span data-ttu-id="e5161-163">**SelfTest**</span><span class="sxs-lookup"><span data-stu-id="e5161-163">**SelfTest**</span></span>](selftest-win32-tpm.md)                                                   | <span data-ttu-id="e5161-164">Executa um teste automático do TPM e retorna o resultado.</span><span class="sxs-lookup"><span data-stu-id="e5161-164">Performs a self-test of the TPM and returns the result.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="e5161-165">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="e5161-165">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="e5161-166">Solicita a execução de uma operação de presença física do TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-166">Requests a TPM physical presence operation to run.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="e5161-167">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="e5161-167">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)                                         | <span data-ttu-id="e5161-168">Instala um proprietário para o TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-168">Installs an owner for the TPM.</span></span><br/>                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="e5161-169">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5161-169">Properties</span></span>

<span data-ttu-id="e5161-170">A classe **Win32 \_ TPM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e5161-170">The **Win32\_Tpm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5161-171">**Inicial de isActivated \_**</span><span class="sxs-lookup"><span data-stu-id="e5161-171">**IsActivated\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5161-172">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e5161-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5161-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5161-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5161-174">Indica se o TPM está ativado.</span><span class="sxs-lookup"><span data-stu-id="e5161-174">Indicates whether the TPM is activated.</span></span>

<span data-ttu-id="e5161-175">**true** se o dispositivo estiver ativado (ou seja, se **isActivated \_ InitialValue** for true); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e5161-175">**true** if the device is activated (that is, if **IsActivated\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="e5161-176">Esse valor é armazenado quando a classe é instanciada.</span><span class="sxs-lookup"><span data-stu-id="e5161-176">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="e5161-177">É possível que o TPM altere o estado entre a instanciação e quando você marca esse valor.</span><span class="sxs-lookup"><span data-stu-id="e5161-177">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="e5161-178">Para verificar se o TPM está ativado em tempo real, use o método [**isActivated**](isactivated-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="e5161-178">To check whether the TPM is activated in real time, use the [**IsActivated**](isactivated-win32-tpm.md) method.</span></span>

<span data-ttu-id="e5161-179">**Windows Server 2008 e Windows Vista:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="e5161-179">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e5161-180">**Inicial de IsEnabled \_**</span><span class="sxs-lookup"><span data-stu-id="e5161-180">**IsEnabled\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5161-181">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e5161-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5161-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5161-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5161-183">Indica se o TPM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e5161-183">Indicates whether the TPM is enabled.</span></span>

<span data-ttu-id="e5161-184">**true** se o dispositivo estiver habilitado (ou seja, se **IsEnabled \_ inicialvalue** for true); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e5161-184">**true** if the device is enabled (that is, if **IsEnabled\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="e5161-185">Esse valor é armazenado quando a classe é instanciada.</span><span class="sxs-lookup"><span data-stu-id="e5161-185">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="e5161-186">É possível que o TPM altere o estado entre a instanciação e quando você marca esse valor.</span><span class="sxs-lookup"><span data-stu-id="e5161-186">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="e5161-187">Para verificar se o TPM está habilitado em tempo real, use o método [**IsEnabled**](isenabled-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="e5161-187">To check whether the TPM is enabled in real time, use the [**IsEnabled**](isenabled-win32-tpm.md) method.</span></span>

<span data-ttu-id="e5161-188">**Windows Server 2008 e Windows Vista:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="e5161-188">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e5161-189">**\_Inicialvalue de propriedade**</span><span class="sxs-lookup"><span data-stu-id="e5161-189">**IsOwned\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5161-190">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e5161-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5161-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5161-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5161-192">Indica se o TPM tem um proprietário.</span><span class="sxs-lookup"><span data-stu-id="e5161-192">Indicates whether the TPM has an owner.</span></span>

<span data-ttu-id="e5161-193">**true** se o dispositivo tiver um proprietário (ou seja, se isdelede **\_ inicial** for true); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e5161-193">**true** if the device has an owner (that is, if **IsOwned\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="e5161-194">Esse valor é armazenado quando a classe é instanciada.</span><span class="sxs-lookup"><span data-stu-id="e5161-194">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="e5161-195">É possível que o TPM altere o estado entre a instanciação e quando você marca esse valor.</span><span class="sxs-lookup"><span data-stu-id="e5161-195">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="e5161-196">Para verificar se o TPM pertence ao tempo real, [**use o método**](isowned-win32-tpm.md) IsDeleted.</span><span class="sxs-lookup"><span data-stu-id="e5161-196">To check whether the TPM is owned in real time, use the [**IsOwned**](isowned-win32-tpm.md) method.</span></span>

<span data-ttu-id="e5161-197">**Windows Server 2008 e Windows Vista:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="e5161-197">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e5161-198">**ManufacturerID**</span><span class="sxs-lookup"><span data-stu-id="e5161-198">**ManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5161-199">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5161-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5161-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5161-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5161-201">As informações de identificação que nomeiam exclusivamente o fabricante do TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-201">The identifying information that uniquely names the TPM manufacturer.</span></span>

<span data-ttu-id="e5161-202">Quando os dados estiverem indisponíveis, zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="e5161-202">When the data is unavailable, zero is returned.</span></span>

<span data-ttu-id="e5161-203">Esse valor inteiro pode ser convertido em um valor de cadeia de caracteres interpretando cada byte como um caractere ASCII.</span><span class="sxs-lookup"><span data-stu-id="e5161-203">This integer value can be translated to a string value by interpreting each byte as an ASCII character.</span></span> <span data-ttu-id="e5161-204">Por exemplo, um valor inteiro de 1414548736 pode ser dividido nesses 4 bytes: 0x54, 0x50, 0x4D e 0x00.</span><span class="sxs-lookup"><span data-stu-id="e5161-204">For example, an integer value of 1414548736 can be divided into these 4 bytes: 0x54, 0x50, 0x4D, and 0x00.</span></span> <span data-ttu-id="e5161-205">Supondo que a cadeia de caracteres seja interpretada da esquerda para a direita, esse valor inteiro é convertido em um valor de cadeia de caracteres "TPM".</span><span class="sxs-lookup"><span data-stu-id="e5161-205">Assuming the string is interpreted from left to right, this integer value translated to a string value of "TPM".</span></span>

</dd> <dt>

<span data-ttu-id="e5161-206">**ManufacturerVersion**</span><span class="sxs-lookup"><span data-stu-id="e5161-206">**ManufacturerVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5161-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5161-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5161-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5161-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5161-209">A versão do TPM, conforme especificado pelo fabricante.</span><span class="sxs-lookup"><span data-stu-id="e5161-209">The version of the TPM, as specified by the manufacturer.</span></span>

<span data-ttu-id="e5161-210">Quando os dados não estão disponíveis, "sem suporte" é retornado.</span><span class="sxs-lookup"><span data-stu-id="e5161-210">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="e5161-211">**ManufacturerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="e5161-211">**ManufacturerVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5161-212">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5161-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5161-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5161-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5161-214">Outras informações de versão específicas do fabricante para o TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-214">Other manufacturer-specific version information for the TPM.</span></span>

<span data-ttu-id="e5161-215">Quando os dados não estão disponíveis, "sem suporte" é retornado.</span><span class="sxs-lookup"><span data-stu-id="e5161-215">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="e5161-216">**PhysicalPresenceVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="e5161-216">**PhysicalPresenceVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5161-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5161-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5161-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5161-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5161-219">A versão da interface de presença física, um mecanismo de comunicação usado para executar operações de dispositivo que exigem a presença física, à qual o computador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e5161-219">The version of the Physical Presence Interface, a communication mechanism used to run device operations that require physical presence, that the computer supports.</span></span>

<span data-ttu-id="e5161-220">Essa interface deve estar disponível para executar operações de presença física do TPM.</span><span class="sxs-lookup"><span data-stu-id="e5161-220">This interface must be available to run TPM physical presence operations.</span></span> <span data-ttu-id="e5161-221">Os métodos do **\_ TPM do Win32** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)e [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expõem os recursos da interface de presença física.</span><span class="sxs-lookup"><span data-stu-id="e5161-221">The **Win32\_Tpm** methods [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md), and [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expose the capabilities of the Physical Presence Interface.</span></span>

<span data-ttu-id="e5161-222">Quando os dados não estão disponíveis, "sem suporte" é retornado.</span><span class="sxs-lookup"><span data-stu-id="e5161-222">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="e5161-223">**SpecVersion**</span><span class="sxs-lookup"><span data-stu-id="e5161-223">**SpecVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5161-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e5161-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5161-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5161-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5161-226">A versão da especificação de Trusted Computing Group (TCG) à qual o TPM dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e5161-226">The version of the Trusted Computing Group (TCG) specification that the TPM supports.</span></span> <span data-ttu-id="e5161-227">Esse valor inclui a versão de especificação de TCG principal e secundária, o nível de revisão de especificação e o nível de revisão de errata.</span><span class="sxs-lookup"><span data-stu-id="e5161-227">This value includes the major and minor TCG specification version, the specification revision level, and the errata revision level.</span></span> <span data-ttu-id="e5161-228">Todos os valores estão em hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e5161-228">All values are in hexadecimal.</span></span> <span data-ttu-id="e5161-229">Por exemplo, uma informação de versão de "1,2, 2, 0" indica que o dispositivo foi implementado para a especificação de TCG versão 1,2, nível de revisão 2 e sem errata.</span><span class="sxs-lookup"><span data-stu-id="e5161-229">For example, a version information of "1.2, 2, 0" indicates that the device was implemented to TCG specification version 1.2, revision level 2, and with no errata.</span></span>

<span data-ttu-id="e5161-230">Quando os dados não estão disponíveis, "sem suporte" é retornado.</span><span class="sxs-lookup"><span data-stu-id="e5161-230">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5161-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5161-231">Remarks</span></span>

<span data-ttu-id="e5161-232">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e5161-232">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e5161-233">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="e5161-233">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e5161-234">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e5161-234">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e5161-235">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e5161-235">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5161-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5161-236">Requirements</span></span>



| <span data-ttu-id="e5161-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5161-237">Requirement</span></span> | <span data-ttu-id="e5161-238">Valor</span><span class="sxs-lookup"><span data-stu-id="e5161-238">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5161-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5161-239">Minimum supported client</span></span><br/> | <span data-ttu-id="e5161-240">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5161-240">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e5161-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5161-241">Minimum supported server</span></span><br/> | <span data-ttu-id="e5161-242">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5161-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e5161-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5161-243">Namespace</span></span><br/>                | <span data-ttu-id="e5161-244">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="e5161-244">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="e5161-245">MOF</span><span class="sxs-lookup"><span data-stu-id="e5161-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5161-246"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="e5161-246"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5161-247">DLL</span><span class="sxs-lookup"><span data-stu-id="e5161-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5161-248"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="e5161-248"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



 

 
