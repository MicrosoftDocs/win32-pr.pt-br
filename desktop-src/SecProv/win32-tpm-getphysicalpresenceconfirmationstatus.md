---
description: Indica se a confirmação de um usuário fisicamente presente é necessária para uma determinada operação de presença física.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Método Win32_Tpm:: GetPhysicalPresenceConfirmationStatus'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922103"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a><span data-ttu-id="40866-103">\_Método TPM:: GetPhysicalPresenceConfirmationStatus do Win32</span><span class="sxs-lookup"><span data-stu-id="40866-103">Win32\_Tpm::GetPhysicalPresenceConfirmationStatus method</span></span>

<span data-ttu-id="40866-104">Indica se a confirmação de um usuário fisicamente presente é necessária para uma determinada operação de presença física.</span><span class="sxs-lookup"><span data-stu-id="40866-104">Indicates if confirmation from a physically present user is required for a given physical presence operation.</span></span>

<span data-ttu-id="40866-105">Esse método só pode ser acessado por administradores locais.</span><span class="sxs-lookup"><span data-stu-id="40866-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="40866-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40866-106">Syntax</span></span>


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="40866-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40866-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40866-108">*Operação* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="40866-108">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40866-109">Um valor inteiro que especifica a operação de TPM solicitada que requer a presença física.</span><span class="sxs-lookup"><span data-stu-id="40866-109">An integer value that specifies the requested TPM operation that requires physical presence.</span></span> <span data-ttu-id="40866-110">Também há suporte para comandos específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="40866-110">Vendor specific commands are supported as well.</span></span>

<span data-ttu-id="40866-111">O parâmetro *Operation* pode consistir nos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="40866-111">The *Operation* parameter may consist of the following values.</span></span>



| <span data-ttu-id="40866-112">Valor</span><span class="sxs-lookup"><span data-stu-id="40866-112">Value</span></span>                                                                                                                               | <span data-ttu-id="40866-113">Significado</span><span class="sxs-lookup"><span data-stu-id="40866-113">Meaning</span></span>                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="40866-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="40866-114"><dt>1</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-115">Habilitar</span><span class="sxs-lookup"><span data-stu-id="40866-115">Enable</span></span><br/>                                        |
| <dl> <span data-ttu-id="40866-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="40866-116"><dt>2</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-117">Desabilitar</span><span class="sxs-lookup"><span data-stu-id="40866-117">Disable</span></span><br/>                                       |
| <dl> <span data-ttu-id="40866-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="40866-118"><dt>3</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-119">Ativar</span><span class="sxs-lookup"><span data-stu-id="40866-119">Activate</span></span><br/>                                      |
| <dl> <span data-ttu-id="40866-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="40866-120"><dt>4</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-121">Desativar</span><span class="sxs-lookup"><span data-stu-id="40866-121">Deactivate</span></span><br/>                                    |
| <dl> <span data-ttu-id="40866-122"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="40866-122"><dt>5</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-123">Limpar</span><span class="sxs-lookup"><span data-stu-id="40866-123">Clear</span></span><br/>                                         |
| <dl> <span data-ttu-id="40866-124"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="40866-124"><dt>6</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-125">Habilitar + ativar</span><span class="sxs-lookup"><span data-stu-id="40866-125">Enable + Activate</span></span><br/>                             |
| <dl> <span data-ttu-id="40866-126"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="40866-126"><dt>7</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-127">Desativar + desabilitar</span><span class="sxs-lookup"><span data-stu-id="40866-127">Deactivate + Disable</span></span><br/>                          |
| <dl> <span data-ttu-id="40866-128"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="40866-128"><dt>8</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-129">SetOwnerInstall \_ true</span><span class="sxs-lookup"><span data-stu-id="40866-129">SetOwnerInstall\_True</span></span><br/>                         |
| <dl> <span data-ttu-id="40866-130"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="40866-130"><dt>9</dt></span></span> </dl>                                                        | <span data-ttu-id="40866-131">SetOwnerInstall \_ false</span><span class="sxs-lookup"><span data-stu-id="40866-131">SetOwnerInstall\_False</span></span><br/>                        |
| <dl> <span data-ttu-id="40866-132"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="40866-132"><dt>10</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-133">Habilitar + ativar + SetOwnerInstall \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="40866-133">Enable + Activate + SetOwnerInstall\_True</span></span><br/>     |
| <dl> <span data-ttu-id="40866-134"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="40866-134"><dt>11</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-135">SetOwnerInstall \_ false + desativar + desabilitar</span><span class="sxs-lookup"><span data-stu-id="40866-135">SetOwnerInstall\_False + Deactivate + Disable</span></span><br/> |
| <dl> <span data-ttu-id="40866-136"><dt></dt><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="40866-136"><dt></dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="40866-137">PresenceunownedFieldUpgrade físico adiado</span><span class="sxs-lookup"><span data-stu-id="40866-137">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> |
| <dl> <span data-ttu-id="40866-138"><dt></dt><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="40866-138"><dt></dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="40866-139">Limpar + habilitar + ativar</span><span class="sxs-lookup"><span data-stu-id="40866-139">Clear + Enable + Activate</span></span><br/>                     |
| <dl> <span data-ttu-id="40866-140"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="40866-140"><dt>15</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-141">SetNoPPIProvision \_ false</span><span class="sxs-lookup"><span data-stu-id="40866-141">SetNoPPIProvision\_False</span></span><br/>                      |
| <dl> <span data-ttu-id="40866-142"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="40866-142"><dt>16</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-143">SetNoPPIProvision \_ true</span><span class="sxs-lookup"><span data-stu-id="40866-143">SetNoPPIProvision\_True</span></span><br/>                       |
| <dl> <span data-ttu-id="40866-144"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="40866-144"><dt>17</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-145">SetNoPPIClear \_ false</span><span class="sxs-lookup"><span data-stu-id="40866-145">SetNoPPIClear\_False</span></span><br/>                          |
| <dl> <span data-ttu-id="40866-146"><dt>anos</dt></span><span class="sxs-lookup"><span data-stu-id="40866-146"><dt>18</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-147">SetNoPPIClear \_ true</span><span class="sxs-lookup"><span data-stu-id="40866-147">SetNoPPIClear\_True</span></span><br/>                           |
| <dl> <span data-ttu-id="40866-148"><dt>aprimora</dt></span><span class="sxs-lookup"><span data-stu-id="40866-148"><dt>19</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-149">SetNoPPIMaintenance \_ false</span><span class="sxs-lookup"><span data-stu-id="40866-149">SetNoPPIMaintenance\_False</span></span><br/>                    |
| <dl> <span data-ttu-id="40866-150"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="40866-150"><dt>20</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-151">SetNoPPIMaintenance \_ true</span><span class="sxs-lookup"><span data-stu-id="40866-151">SetNoPPIMaintenance\_True</span></span><br/>                     |
| <dl> <span data-ttu-id="40866-152"><dt>Abril</dt></span><span class="sxs-lookup"><span data-stu-id="40866-152"><dt>21</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-153">Habilitar + ativar + limpar</span><span class="sxs-lookup"><span data-stu-id="40866-153">Enable + Activate + Clear</span></span><br/>                     |
| <dl> <span data-ttu-id="40866-154"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="40866-154"><dt>22</dt></span></span> </dl>                                                       | <span data-ttu-id="40866-155">Habilitar + ativar + limpar + habilitar + ativar</span><span class="sxs-lookup"><span data-stu-id="40866-155">Enable + Activate + Clear + Enable + Activate</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="40866-156">*ConfirmationStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="40866-156">*ConfirmationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40866-157">Retorna o status de confirmação para o comando de presença física.</span><span class="sxs-lookup"><span data-stu-id="40866-157">Returns the confirmation status for physical presence command.</span></span>

<span data-ttu-id="40866-158">O parâmetro *ConfirmationStatus* pode consistir nos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="40866-158">The *ConfirmationStatus* parameter may consist of the following values.</span></span>



| <span data-ttu-id="40866-159">Valor</span><span class="sxs-lookup"><span data-stu-id="40866-159">Value</span></span>                                                                        | <span data-ttu-id="40866-160">Significado</span><span class="sxs-lookup"><span data-stu-id="40866-160">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40866-161"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40866-161"><dt>0</dt></span></span> </dl> | <span data-ttu-id="40866-162">Não implementado</span><span class="sxs-lookup"><span data-stu-id="40866-162">Not implemented</span></span><br/>                                             |
| <dl> <span data-ttu-id="40866-163"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="40866-163"><dt>1</dt></span></span> </dl> | <span data-ttu-id="40866-164">Somente BIOS.</span><span class="sxs-lookup"><span data-stu-id="40866-164">BIOS only.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="40866-165"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="40866-165"><dt>2</dt></span></span> </dl> | <span data-ttu-id="40866-166">Bloqueado para o sistema operacional pela configuração do BIOS.</span><span class="sxs-lookup"><span data-stu-id="40866-166">Blocked for the operating system by the BIOS configuration.</span></span><br/> |
| <dl> <span data-ttu-id="40866-167"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="40866-167"><dt>3</dt></span></span> </dl> | <span data-ttu-id="40866-168">Usuário permitido e fisicamente presente necessário.</span><span class="sxs-lookup"><span data-stu-id="40866-168">Allowed and physically present user required.</span></span><br/>               |
| <dl> <span data-ttu-id="40866-169"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="40866-169"><dt>4</dt></span></span> </dl> | <span data-ttu-id="40866-170">Usuário permitido e fisicamente presente não é necessário</span><span class="sxs-lookup"><span data-stu-id="40866-170">Allowed and physically present user not required</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40866-171">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40866-171">Return value</span></span>

<span data-ttu-id="40866-172">Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="40866-172">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="40866-173">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="40866-173">Common return codes are listed below.</span></span>



| <span data-ttu-id="40866-174">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="40866-174">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="40866-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="40866-175">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="40866-176"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="40866-176"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="40866-177">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="40866-177">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40866-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="40866-178">Remarks</span></span>

<span data-ttu-id="40866-179">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="40866-179">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="40866-180">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="40866-180">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="40866-181">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="40866-181">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="40866-182">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="40866-182">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40866-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40866-183">Requirements</span></span>



| <span data-ttu-id="40866-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="40866-184">Requirement</span></span> | <span data-ttu-id="40866-185">Valor</span><span class="sxs-lookup"><span data-stu-id="40866-185">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="40866-186">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40866-186">Minimum supported client</span></span><br/> | <span data-ttu-id="40866-187">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="40866-187">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="40866-188">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40866-188">Minimum supported server</span></span><br/> | <span data-ttu-id="40866-189">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="40866-189">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="40866-190">Namespace</span><span class="sxs-lookup"><span data-stu-id="40866-190">Namespace</span></span><br/>                | <span data-ttu-id="40866-191">\\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="40866-191">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="40866-192">MOF</span><span class="sxs-lookup"><span data-stu-id="40866-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40866-193"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="40866-193"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="40866-194">DLL</span><span class="sxs-lookup"><span data-stu-id="40866-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40866-195"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="40866-195"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40866-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="40866-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40866-197">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="40866-197">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
