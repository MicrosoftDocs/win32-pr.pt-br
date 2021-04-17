---
description: Retorna a operação de presença física de TPM pendente. Use o método SetPhysicalPresenceRequest para solicitar uma operação.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Método GetPhysicalPresenceRequest da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761996"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a><span data-ttu-id="d6fb2-104">Método GetPhysicalPresenceRequest da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="d6fb2-104">GetPhysicalPresenceRequest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="d6fb2-105">O método **GetPhysicalPresenceRequest** da classe [**Win32 \_ TPM**](win32-tpm.md) retorna a operação de presença física de TPM pendente.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-105">The **GetPhysicalPresenceRequest** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="d6fb2-106">Use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6fb2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6fb2-107">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a><span data-ttu-id="d6fb2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6fb2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6fb2-109">*Solicitação* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d6fb2-109">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6fb2-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6fb2-110">Type: **uint32**</span></span>

<span data-ttu-id="d6fb2-111">Um valor que especifica a operação de presença física de TPM pendente.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-111">A value that specifies the pending TPM physical presence operation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6fb2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d6fb2-112">Value</span></span></th>
<th><span data-ttu-id="d6fb2-113">Significado</span><span class="sxs-lookup"><span data-stu-id="d6fb2-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-114"><dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-114"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-115">Nenhuma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-115">No request.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-117">Habilite o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-117">Enable the TPM.</span></span><br/> <span data-ttu-id="d6fb2-118">Esta operação é revertida pela operação 2.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="d6fb2-119">Para obter mais informações, consulte estes métodos relacionados que não envolvem a presença física:</span><span class="sxs-lookup"><span data-stu-id="d6fb2-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="d6fb2-120"><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6fb2-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="d6fb2-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6fb2-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-123">Desabilite o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-123">Disable the TPM.</span></span><br/> <span data-ttu-id="d6fb2-124">Esta operação é revertida pela operação 1.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="d6fb2-125">Para obter mais informações, consulte este método relacionado que não envolve a presença física: <a href="disable-win32-tpm.md"><strong>desabilitar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-126"><dt>Beta</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-127">Ative o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-127">Activate the TPM.</span></span><br/> <span data-ttu-id="d6fb2-128">Esta operação é revertida pela operação 4.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-129"><dt>quatro</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-130">Desativar o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="d6fb2-131">Esta operação é revertida pela operação 3.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-132"><dt>05</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-133">Limpe o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-133">Clear the TPM.</span></span><br/> <span data-ttu-id="d6fb2-134">Esta operação não pode ser revertida.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-134">This operation cannot be reversed.</span></span><br/> <span data-ttu-id="d6fb2-135">Para obter mais informações, consulte este método relacionado que não envolve a presença física: <a href="clear-win32-tpm.md"><strong>claro</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-136"><dt>152</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-137">Habilitar e ativar o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-137">Enable and activate the TPM.</span></span> <br/> <span data-ttu-id="d6fb2-138">Esta operação é revertida pela operação 7.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-140">Desativar e desabilitar o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="d6fb2-141">Esta operação é revertida pela operação 6.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-142"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-143">Permitir a instalação de um proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-143">Allow the installation of a TPM owner.</span></span> <br/> <span data-ttu-id="d6fb2-144">Esta operação é revertida pela operação 9.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-145"><dt>99</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-146">Impedir a instalação de um proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="d6fb2-147">Esta operação é revertida pela operação 8.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-148"><dt>254</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-149">Habilite, ative e permita a instalação de um proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="d6fb2-150">Esta operação é revertida pela operação 11.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-151"><dt>11</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-152">Desativar, desabilitar e impedir a instalação de um proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="d6fb2-153">Esta operação é revertida pela operação 10.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="d6fb2-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-155">PresenceunownedFieldUpgrade físico adiado</span><span class="sxs-lookup"><span data-stu-id="d6fb2-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="d6fb2-156">A configuração de presença física foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="d6fb2-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-158"><dt>140</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-159">Limpar, habilitar e ativar o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="d6fb2-160">Esta operação não pode ser revertida.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-161"><dt>15</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="d6fb2-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="d6fb2-163">Define o provisionamento que você deve estar fisicamente presente para definir o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="d6fb2-164">Esta operação é revertida pela operação 16.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="d6fb2-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-166"><dt>16</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="d6fb2-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="d6fb2-168">Define o provisionamento de que você não precisa estar fisicamente presente para definir o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="d6fb2-169">Esta operação é revertida pela operação 15.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="d6fb2-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-171"><dt>16</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="d6fb2-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="d6fb2-173">Define o provisionamento que você deve estar fisicamente presente para limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="d6fb2-174">Esta operação é revertida pela operação 18.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="d6fb2-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-176"><dt>anos</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="d6fb2-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="d6fb2-178">Define o provisionamento que você não precisa estar fisicamente presente para limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="d6fb2-179">Esta operação é revertida pela operação 17.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="d6fb2-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-181"><dt>aprimora</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="d6fb2-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="d6fb2-183">Define o provisionamento que você deve estar fisicamente presente para manter o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="d6fb2-184">Esta operação é revertida pela operação 20.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="d6fb2-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-186"><dt>20,00</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="d6fb2-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="d6fb2-188">Define o provisionamento que você deve estar fisicamente presente para manter o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="d6fb2-189">Esta operação é revertida pela operação 19.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="d6fb2-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d6fb2-191"><dt>Abril</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-192">Habilitar + ativar + limpar</span><span class="sxs-lookup"><span data-stu-id="d6fb2-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="d6fb2-193">Habilitar, ativar e limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="d6fb2-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d6fb2-195"><dt>22</dt> </span><span class="sxs-lookup"><span data-stu-id="d6fb2-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="d6fb2-196">Habilitar + ativar + limpar + habilitar + ativar</span><span class="sxs-lookup"><span data-stu-id="d6fb2-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="d6fb2-197">Habilite, ative e limpe o TPM e, em seguida, habilite e reative o TPM.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="d6fb2-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6fb2-199">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6fb2-199">Return value</span></span>

<span data-ttu-id="d6fb2-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6fb2-200">Type: **uint32**</span></span>

<span data-ttu-id="d6fb2-201">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-201">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="d6fb2-202">A tabela a seguir lista os códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-202">The following table lists the common return codes.</span></span>



| <span data-ttu-id="d6fb2-203">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d6fb2-203">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="d6fb2-204">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6fb2-204">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6fb2-205"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d6fb2-205"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="d6fb2-206">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-206">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="d6fb2-207"><dt>**TPM \_ \_Falha de \_ ACPI \_ PPI**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="d6fb2-207"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="d6fb2-208">Ocorreu uma falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-208">A hardware failure occurred.</span></span> <span data-ttu-id="d6fb2-209">Consulte o fabricante do seu computador para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-209">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d6fb2-210">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6fb2-210">Remarks</span></span>

<span data-ttu-id="d6fb2-211">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d6fb2-211">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d6fb2-212">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-212">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d6fb2-213">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="d6fb2-213">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d6fb2-214">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d6fb2-214">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6fb2-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6fb2-215">Requirements</span></span>



| <span data-ttu-id="d6fb2-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6fb2-216">Requirement</span></span> | <span data-ttu-id="d6fb2-217">Valor</span><span class="sxs-lookup"><span data-stu-id="d6fb2-217">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fb2-218">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6fb2-218">Minimum supported client</span></span><br/> | <span data-ttu-id="d6fb2-219">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6fb2-219">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d6fb2-220">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6fb2-220">Minimum supported server</span></span><br/> | <span data-ttu-id="d6fb2-221">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6fb2-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d6fb2-222">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6fb2-222">Namespace</span></span><br/>                | <span data-ttu-id="d6fb2-223">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d6fb2-223">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="d6fb2-224">MOF</span><span class="sxs-lookup"><span data-stu-id="d6fb2-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6fb2-225"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="d6fb2-225"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6fb2-226">DLL</span><span class="sxs-lookup"><span data-stu-id="d6fb2-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6fb2-227"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="d6fb2-227"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6fb2-228">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6fb2-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fb2-229">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d6fb2-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="d6fb2-230">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="d6fb2-230">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="d6fb2-231">**Desabilitar**</span><span class="sxs-lookup"><span data-stu-id="d6fb2-231">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="d6fb2-232">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="d6fb2-232">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="d6fb2-233">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d6fb2-233">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="d6fb2-234">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="d6fb2-234">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
