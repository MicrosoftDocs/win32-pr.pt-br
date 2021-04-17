---
description: Retorna os resultados de uma operação de presença física de TPM que foi executada.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Método GetPhysicalPresenceResponse da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 47dfad1491b398b035e40867d10d2d3e46327dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780153"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a><span data-ttu-id="f5ad0-103">Método GetPhysicalPresenceResponse da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="f5ad0-103">GetPhysicalPresenceResponse method of the Win32\_Tpm class</span></span>

<span data-ttu-id="f5ad0-104">O método **GetPhysicalPresenceResponse** da classe [**Win32 \_ TPM**](win32-tpm.md) retorna os resultados de uma operação de presença física de TPM que foi executada.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-104">The **GetPhysicalPresenceResponse** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the results from a TPM physical presence operation that was performed.</span></span> <span data-ttu-id="f5ad0-105">Use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-105">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ad0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5ad0-106">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a><span data-ttu-id="f5ad0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5ad0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ad0-108">*Solicitação* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f5ad0-108">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ad0-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5ad0-109">Type: **uint32**</span></span>

<span data-ttu-id="f5ad0-110">Um valor inteiro que especifica a operação de presença física do TPM que foi executada.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-110">An integer value that specifies the TPM physical presence operation that was performed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f5ad0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f5ad0-111">Value</span></span></th>
<th><span data-ttu-id="f5ad0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="f5ad0-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-113"><dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-113"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-114">Nenhuma solicitação.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-114">No request.</span></span><br/> <span data-ttu-id="f5ad0-115">Nenhuma operação de presença física foi executada.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-115">No physical presence operation was performed.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-117">Habilite o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-117">Enable the TPM.</span></span><br/> <span data-ttu-id="f5ad0-118">Esta operação é revertida pela operação 2.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="f5ad0-119">Para obter mais informações, consulte estes métodos relacionados que não envolvem a presença física:</span><span class="sxs-lookup"><span data-stu-id="f5ad0-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="f5ad0-120"><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5ad0-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="f5ad0-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="f5ad0-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-123">Desabilite o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-123">Disable the TPM.</span></span><br/> <span data-ttu-id="f5ad0-124">Esta operação é revertida pela operação 1.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="f5ad0-125">Para obter mais informações, consulte este método relacionado que não envolve a presença física: <a href="disable-win32-tpm.md"><strong>desabilitar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-126"><dt>Beta</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-127">Ative o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-127">Activate the TPM.</span></span><br/> <span data-ttu-id="f5ad0-128">Esta operação é revertida pela operação 4.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-129"><dt>quatro</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-130">Desativar o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="f5ad0-131">Esta operação é revertida pela operação 3.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-132"><dt>05</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-133">Limpe o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-133">Clear the TPM.</span></span><br/> <span data-ttu-id="f5ad0-134">Esta operação não pode ser revertida.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-134">This operation cannot be reversed.</span></span> <br/> <span data-ttu-id="f5ad0-135">Para obter mais informações, consulte este método relacionado que não envolve a presença física: <a href="clear-win32-tpm.md"><strong>claro</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-136"><dt>152</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-137">Habilitar e ativar o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-137">Enable and activate the TPM.</span></span><br/> <span data-ttu-id="f5ad0-138">Esta operação é revertida pela operação 7.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-140">Desativar e desabilitar o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="f5ad0-141">Esta operação é revertida pela operação 6.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-142"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-143">Permitir a instalação de um proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-143">Allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="f5ad0-144">Esta operação é revertida pela operação 9.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-145"><dt>99</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-146">Impedir a instalação de um proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="f5ad0-147">Esta operação é revertida pela operação 8.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-148"><dt>254</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-149">Habilite, ative e permita a instalação de um proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="f5ad0-150">Esta operação é revertida pela operação 11.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-151"><dt>11</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-152">Desativar, desabilitar e impedir a instalação de um proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="f5ad0-153">Esta operação é revertida pela operação 10.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="f5ad0-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-155">PresenceunownedFieldUpgrade físico adiado</span><span class="sxs-lookup"><span data-stu-id="f5ad0-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="f5ad0-156">A configuração de presença física foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="f5ad0-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-158"><dt>140</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-159">Limpar, habilitar e ativar o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="f5ad0-160">Esta operação não pode ser revertida.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-161"><dt>15</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="f5ad0-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="f5ad0-163">Define o provisionamento que você deve estar fisicamente presente para definir o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="f5ad0-164">Esta operação é revertida pela operação 16.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="f5ad0-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-166"><dt>16</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="f5ad0-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="f5ad0-168">Define o provisionamento de que você não precisa estar fisicamente presente para definir o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="f5ad0-169">Esta operação é revertida pela operação 15.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="f5ad0-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-171"><dt>16</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="f5ad0-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="f5ad0-173">Define o provisionamento que você deve estar fisicamente presente para limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="f5ad0-174">Esta operação é revertida pela operação 18.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="f5ad0-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-176"><dt>anos</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="f5ad0-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="f5ad0-178">Define o provisionamento que você não precisa estar fisicamente presente para limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="f5ad0-179">Esta operação é revertida pela operação 17.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="f5ad0-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-181"><dt>aprimora</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="f5ad0-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="f5ad0-183">Define o provisionamento que você deve estar fisicamente presente para manter o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="f5ad0-184">Esta operação é revertida pela operação 20.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="f5ad0-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-186"><dt>20,00</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="f5ad0-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="f5ad0-188">Define o provisionamento que você deve estar fisicamente presente para manter o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="f5ad0-189">Esta operação é revertida pela operação 19.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="f5ad0-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f5ad0-191"><dt>Abril</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-192">Habilitar + ativar + limpar</span><span class="sxs-lookup"><span data-stu-id="f5ad0-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="f5ad0-193">Habilitar, ativar e limpar o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="f5ad0-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f5ad0-195"><dt>22</dt> </span><span class="sxs-lookup"><span data-stu-id="f5ad0-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="f5ad0-196">Habilitar + ativar + limpar + habilitar + ativar</span><span class="sxs-lookup"><span data-stu-id="f5ad0-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="f5ad0-197">Habilite, ative e limpe o TPM e, em seguida, habilite e reative o TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="f5ad0-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="f5ad0-199">*Resposta* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f5ad0-199">*Response* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ad0-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5ad0-200">Type: **uint32**</span></span>

<span data-ttu-id="f5ad0-201">Um valor inteiro que especifica os resultados da execução da operação de presença física do TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-201">An integer value that specifies the results of performing the TPM physical presence operation.</span></span>

<span data-ttu-id="f5ad0-202">Uma operação de presença física será bem-sucedida se um usuário presente fisicamente confirmar a operação e se a operação for executada sem erros.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-202">A physical presence operation is successful if a physically present user confirms the operation and if the operation runs without errors.</span></span>

<span data-ttu-id="f5ad0-203">Esse valor pode conter qualquer erro de TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-203">This value may contain any TPM error.</span></span> <span data-ttu-id="f5ad0-204">A tabela a seguir lista algumas das respostas de erro comuns.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-204">The following table lists some of the common error responses.</span></span>



| <span data-ttu-id="f5ad0-205">Valor</span><span class="sxs-lookup"><span data-stu-id="f5ad0-205">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="f5ad0-206">Significado</span><span class="sxs-lookup"><span data-stu-id="f5ad0-206">Meaning</span></span>                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5ad0-207"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5ad0-207"><dt>0</dt></span></span> </dl>                                                                                                                                                                                             | <span data-ttu-id="f5ad0-208">A operação do TPM solicitada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-208">The requested TPM operation was successful.</span></span><br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <span data-ttu-id="f5ad0-209"><dt>**TPM \_ E/ \_ PPI \_ usuário \_ anular**</dt> <dt>2150171393 (0x80290301)</dt></span><span class="sxs-lookup"><span data-stu-id="f5ad0-209"><dt>**TPM\_E\_PPI\_USER\_ABORT**</dt> <dt>2150171393 (0x80290301)</dt></span></span> </dl>       | <span data-ttu-id="f5ad0-210">O usuário rejeitou a operação de TPM solicitada.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-210">The user rejected the requested TPM operation.</span></span><br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <span data-ttu-id="f5ad0-211"><dt>**TPM \_ \_Falha de \_ BIOS \_ E PPI**</dt> <dt>2150171394 (0x80290302)</dt></span><span class="sxs-lookup"><span data-stu-id="f5ad0-211"><dt>**TPM\_E\_PPI\_BIOS\_FAILURE**</dt> <dt>2150171394 (0x80290302)</dt></span></span> </dl> | <span data-ttu-id="f5ad0-212">Ocorreu uma falha do BIOS ao executar a operação do TPM.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-212">A BIOS failure occurred while running the TPM operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ad0-213">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5ad0-213">Return value</span></span>

<span data-ttu-id="f5ad0-214">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5ad0-214">Type: **uint32**</span></span>

<span data-ttu-id="f5ad0-215">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-215">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="f5ad0-216">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-216">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="f5ad0-217">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f5ad0-217">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="f5ad0-218">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5ad0-218">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5ad0-219"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f5ad0-219"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="f5ad0-220">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-220">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="f5ad0-221"><dt>**TPM \_ \_Falha de \_ ACPI \_ PPI**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="f5ad0-221"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="f5ad0-222">Ocorreu uma falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-222">A hardware failure occurred.</span></span> <span data-ttu-id="f5ad0-223">Consulte o fabricante do seu computador para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-223">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5ad0-224">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5ad0-224">Remarks</span></span>

<span data-ttu-id="f5ad0-225">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f5ad0-225">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5ad0-226">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-226">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f5ad0-227">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f5ad0-227">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5ad0-228">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f5ad0-228">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ad0-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5ad0-229">Requirements</span></span>



| <span data-ttu-id="f5ad0-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ad0-230">Requirement</span></span> | <span data-ttu-id="f5ad0-231">Valor</span><span class="sxs-lookup"><span data-stu-id="f5ad0-231">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ad0-232">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5ad0-232">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ad0-233">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5ad0-233">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f5ad0-234">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5ad0-234">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ad0-235">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5ad0-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f5ad0-236">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5ad0-236">Namespace</span></span><br/>                | <span data-ttu-id="f5ad0-237">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f5ad0-237">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="f5ad0-238">MOF</span><span class="sxs-lookup"><span data-stu-id="f5ad0-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5ad0-239"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="f5ad0-239"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5ad0-240">DLL</span><span class="sxs-lookup"><span data-stu-id="f5ad0-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5ad0-241"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="f5ad0-241"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ad0-242">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5ad0-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ad0-243">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f5ad0-243">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="f5ad0-244">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="f5ad0-244">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="f5ad0-245">**Desabilitar**</span><span class="sxs-lookup"><span data-stu-id="f5ad0-245">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="f5ad0-246">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="f5ad0-246">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="f5ad0-247">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f5ad0-247">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> </dl>

 

 
