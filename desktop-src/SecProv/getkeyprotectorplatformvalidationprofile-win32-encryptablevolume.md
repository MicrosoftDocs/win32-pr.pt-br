---
description: Recupera o perfil de validação de plataforma para um protetor de chave específico do tipo apropriado.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Método GetKeyProtectorPlatformValidationProfile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760192"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="527b0-103">Método GetKeyProtectorPlatformValidationProfile da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="527b0-103">GetKeyProtectorPlatformValidationProfile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="527b0-104">O método **GetKeyProtectorPlatformValidationProfile** recupera o perfil de validação de plataforma para um determinado protetor de chave do tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="527b0-104">The **GetKeyProtectorPlatformValidationProfile** method retrieves the platform validation profile for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="527b0-105">O identificador de protetor de chave deve se referir a um protetor de chave do tipo "TPM", "TPM e PIN", "TPM e PIN e chave de inicialização", ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="527b0-105">The key protector identifier must refer to a key protector of type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="527b0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="527b0-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a><span data-ttu-id="527b0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="527b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="527b0-108">*VolumeKeyProtectorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="527b0-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="527b0-109">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="527b0-109">Type: **string**</span></span>

<span data-ttu-id="527b0-110">Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="527b0-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="527b0-111">*PlatformValidationProfile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="527b0-111">*PlatformValidationProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="527b0-112">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="527b0-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="527b0-113">Uma matriz de inteiros que especifica como o hardware de segurança do Trusted Platform Module (TPM) do computador protege a chave de criptografia do volume do disco.</span><span class="sxs-lookup"><span data-stu-id="527b0-113">An array of integers that specifies how the Trusted Platform Module (TPM) Security Hardware of the computer secures the encryption key of the disk volume.</span></span>



| <span data-ttu-id="527b0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="527b0-114">Value</span></span>                                                                         | <span data-ttu-id="527b0-115">Significado</span><span class="sxs-lookup"><span data-stu-id="527b0-115">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="527b0-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-116"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="527b0-117">Principal raiz de CRTM (relação de confiança de medida), BIOS e extensões de plataforma</span><span class="sxs-lookup"><span data-stu-id="527b0-117">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="527b0-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-118"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="527b0-119">Configuração e dados da plataforma e da placa-mãe</span><span class="sxs-lookup"><span data-stu-id="527b0-119">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="527b0-120"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-120"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="527b0-121">Código da ROM de opção</span><span class="sxs-lookup"><span data-stu-id="527b0-121">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="527b0-122"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-122"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="527b0-123">Configuração de ROM de opção e dados</span><span class="sxs-lookup"><span data-stu-id="527b0-123">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="527b0-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-124"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="527b0-125">Código de registro mestre de inicialização (MBR)</span><span class="sxs-lookup"><span data-stu-id="527b0-125">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="527b0-126"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-126"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="527b0-127">Tabela de partição MBR (registro mestre de inicialização)</span><span class="sxs-lookup"><span data-stu-id="527b0-127">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="527b0-128"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-128"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="527b0-129">Transição de estado e eventos de ativação</span><span class="sxs-lookup"><span data-stu-id="527b0-129">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="527b0-130"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-130"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="527b0-131">Manufacturer-Specific do computador</span><span class="sxs-lookup"><span data-stu-id="527b0-131">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="527b0-132"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-132"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="527b0-133">Setor de inicialização NTFS</span><span class="sxs-lookup"><span data-stu-id="527b0-133">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="527b0-134"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-134"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="527b0-135">Bloco de inicialização NTFS</span><span class="sxs-lookup"><span data-stu-id="527b0-135">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="527b0-136"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-136"><dt>10</dt></span></span> </dl> | <span data-ttu-id="527b0-137">Gerenciador de inicialização</span><span class="sxs-lookup"><span data-stu-id="527b0-137">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="527b0-138"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-138"><dt>11</dt></span></span> </dl> | <span data-ttu-id="527b0-139">Controle de acesso do BitLocker</span><span class="sxs-lookup"><span data-stu-id="527b0-139">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="527b0-140"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-140"><dt>12</dt></span></span> </dl> | <span data-ttu-id="527b0-141">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="527b0-141">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="527b0-142"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-142"><dt>13</dt></span></span> </dl> | <span data-ttu-id="527b0-143">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="527b0-143">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="527b0-144"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-144"><dt>14</dt></span></span> </dl> | <span data-ttu-id="527b0-145">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="527b0-145">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="527b0-146"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-146"><dt>15</dt></span></span> </dl> | <span data-ttu-id="527b0-147">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="527b0-147">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="527b0-148"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-148"><dt>16</dt></span></span> </dl> | <span data-ttu-id="527b0-149">Usado para depuração</span><span class="sxs-lookup"><span data-stu-id="527b0-149">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="527b0-150"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-150"><dt>17</dt></span></span> </dl> | <span data-ttu-id="527b0-151">CRTM dinâmico</span><span class="sxs-lookup"><span data-stu-id="527b0-151">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="527b0-152"><dt>anos</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-152"><dt>18</dt></span></span> </dl> | <span data-ttu-id="527b0-153">Definido pela plataforma</span><span class="sxs-lookup"><span data-stu-id="527b0-153">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="527b0-154"><dt>aprimora</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-154"><dt>19</dt></span></span> </dl> | <span data-ttu-id="527b0-155">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="527b0-155">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="527b0-156"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-156"><dt>20</dt></span></span> </dl> | <span data-ttu-id="527b0-157">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="527b0-157">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="527b0-158"><dt>Abril</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-158"><dt>21</dt></span></span> </dl> | <span data-ttu-id="527b0-159">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="527b0-159">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="527b0-160"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-160"><dt>22</dt></span></span> </dl> | <span data-ttu-id="527b0-161">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="527b0-161">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="527b0-162"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-162"><dt>23</dt></span></span> </dl> | <span data-ttu-id="527b0-163">Suporte a aplicativos</span><span class="sxs-lookup"><span data-stu-id="527b0-163">Application support</span></span><br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="527b0-164">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="527b0-164">Return value</span></span>

<span data-ttu-id="527b0-165">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="527b0-165">Type: **uint32**</span></span>

<span data-ttu-id="527b0-166">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="527b0-166">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="527b0-167">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="527b0-167">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="527b0-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="527b0-168">Description</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="527b0-169"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-169"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="527b0-170">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="527b0-170">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="527b0-171"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-171"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="527b0-172">O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "TPM", "TPM e PIN", "TPM e PIN e chave de inicialização", ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="527b0-172">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="527b0-173"><dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-173"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="527b0-174">O BitLocker não está habilitado no volume.</span><span class="sxs-lookup"><span data-stu-id="527b0-174">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="527b0-175">Adicione um protetor de chave para habilitar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="527b0-175">Add a key protector to enable BitLocker.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="527b0-176">Comentários</span><span class="sxs-lookup"><span data-stu-id="527b0-176">Remarks</span></span>

<span data-ttu-id="527b0-177">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="527b0-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="527b0-178">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="527b0-178">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="527b0-179">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="527b0-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="527b0-180">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="527b0-180">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="527b0-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="527b0-181">Requirements</span></span>



| <span data-ttu-id="527b0-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="527b0-182">Requirement</span></span> | <span data-ttu-id="527b0-183">Valor</span><span class="sxs-lookup"><span data-stu-id="527b0-183">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="527b0-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="527b0-184">Minimum supported client</span></span><br/> | <span data-ttu-id="527b0-185">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="527b0-185">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="527b0-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="527b0-186">Minimum supported server</span></span><br/> | <span data-ttu-id="527b0-187">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="527b0-187">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="527b0-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="527b0-188">Namespace</span></span><br/>                | <span data-ttu-id="527b0-189">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="527b0-189">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="527b0-190">MOF</span><span class="sxs-lookup"><span data-stu-id="527b0-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="527b0-191"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="527b0-191"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="527b0-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="527b0-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527b0-193">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="527b0-193">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
