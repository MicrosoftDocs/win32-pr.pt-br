---
description: Se o Trusted Platform Module (TPM) estiver disponível, esse método protegerá a chave de criptografia do volume aprimorada por uma chave externa.
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Método ProtectKeyWithTPMAndStartupKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754947"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="07c80-103">Método ProtectKeyWithTPMAndStartupKey da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="07c80-103">ProtectKeyWithTPMAndStartupKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="07c80-104">O método **ProtectKeyWithTPMAndStartupKey** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protege a chave de criptografia do volume usando o hardware de segurança Trusted Platform Module (TPM) no computador, se disponível, aprimorado por uma chave externa que deve ser apresentada ao computador na inicialização.</span><span class="sxs-lookup"><span data-stu-id="07c80-104">The **ProtectKeyWithTPMAndStartupKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by an external key that must be presented to the computer at startup.</span></span>

<span data-ttu-id="07c80-105">A validação pelo TPM e a entrada de um dispositivo de memória USB que contém a chave externa são necessárias para acessar a chave de criptografia do volume e desbloquear o conteúdo do volume.</span><span class="sxs-lookup"><span data-stu-id="07c80-105">Both validation by the TPM and input of a USB memory device that contains the external key are necessary to access the volume's encryption key and unlock the volume contents.</span></span> <span data-ttu-id="07c80-106">Use o método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) para salvar essa chave externa em um arquivo em um dispositivo de memória USB para uso como uma chave de inicialização.</span><span class="sxs-lookup"><span data-stu-id="07c80-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file on a USB memory device for usage as a startup key.</span></span>

<span data-ttu-id="07c80-107">Esse método só é aplicável ao volume que contém o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="07c80-107">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="07c80-108">Um protetor de chave do tipo "TPM e chave de inicialização" será criado para o volume, se ainda não existir um.</span><span class="sxs-lookup"><span data-stu-id="07c80-108">A key protector of type "TPM And Startup Key" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c80-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07c80-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="07c80-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07c80-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c80-111">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="07c80-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07c80-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07c80-112">Type: **string**</span></span>

<span data-ttu-id="07c80-113">Um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="07c80-113">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="07c80-114">Se esse parâmetro não for especificado, um valor em branco será usado.</span><span class="sxs-lookup"><span data-stu-id="07c80-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="07c80-115">*PlatformValidationProfile* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="07c80-115">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07c80-116">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="07c80-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="07c80-117">Uma matriz de inteiros que especifica como o hardware de segurança do Trusted Platform Module do computador (TPM) protege a chave de criptografia do volume do disco.</span><span class="sxs-lookup"><span data-stu-id="07c80-117">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the encryption key of the disk volume.</span></span>

<span data-ttu-id="07c80-118">Um perfil de validação de plataforma consiste em um conjunto de índices de PCR (registro de configuração de plataforma) que variam de 0 a 23, inclusive.</span><span class="sxs-lookup"><span data-stu-id="07c80-118">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="07c80-119">Os valores de repetição no parâmetro são ignorados.</span><span class="sxs-lookup"><span data-stu-id="07c80-119">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="07c80-120">Cada índice de PCR é associado a serviços que são executados quando o sistema operacional é iniciado.</span><span class="sxs-lookup"><span data-stu-id="07c80-120">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="07c80-121">Cada vez que o computador for iniciado, o TPM verificará se os serviços especificados no perfil de validação de plataforma não foram alterados.</span><span class="sxs-lookup"><span data-stu-id="07c80-121">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="07c80-122">Se qualquer um desses serviços for alterado enquanto a proteção Criptografia de Unidade de Disco BitLocker (BDE) permanecer ativada, o TPM não liberará a chave de criptografia para desbloquear o volume do disco e o computador entrará no modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="07c80-122">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="07c80-123">Se esse parâmetro for especificado enquanto a configuração de Política de Grupo correspondente tiver sido habilitada, ela deverá corresponder à configuração de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="07c80-123">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="07c80-124">Se esse parâmetro não for especificado, o padrão 0, 2, 4, 5, 8, 9, 10 e 11 será usado.</span><span class="sxs-lookup"><span data-stu-id="07c80-124">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="07c80-125">O perfil de validação de plataforma padrão protege a chave de criptografia contra alterações nos seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="07c80-125">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="07c80-126">Principal raiz de confiança de medida (CRTM)</span><span class="sxs-lookup"><span data-stu-id="07c80-126">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="07c80-127">BIOS</span><span class="sxs-lookup"><span data-stu-id="07c80-127">BIOS</span></span>
-   <span data-ttu-id="07c80-128">Extensões de plataforma (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="07c80-128">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="07c80-129">Código ROM de opção (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="07c80-129">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="07c80-130">Código de MBR (registro mestre de inicialização) (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="07c80-130">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="07c80-131">Tabela de partição MBR (registro mestre de inicialização) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="07c80-131">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="07c80-132">Setor de inicialização NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="07c80-132">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="07c80-133">Bloco de inicialização NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="07c80-133">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="07c80-134">Gerenciador de inicialização (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="07c80-134">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="07c80-135">Controle de acesso do BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="07c80-135">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="07c80-136">Para a segurança do seu computador, recomendamos o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="07c80-136">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="07c80-137">Para proteção adicional contra alterações de configuração de inicialização antecipada, use um perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="07c80-137">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="07c80-138">Os computadores baseados em Unified Extensible Firmware Interface (UEFI) não usam a PCR 5 por padrão.</span><span class="sxs-lookup"><span data-stu-id="07c80-138">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="07c80-139">A alteração do perfil padrão afeta a segurança e a capacidade de gerenciamento do seu computador.</span><span class="sxs-lookup"><span data-stu-id="07c80-139">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="07c80-140">A sensibilidade do BitLocker com as modificações de plataforma (maliciosas ou autorizadas) é aumentada ou reduzida, dependendo da inclusão ou exclusão, respectivamente, do PCRs.</span><span class="sxs-lookup"><span data-stu-id="07c80-140">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="07c80-141">Para que a proteção do BitLocker seja habilitada, o perfil de validação de plataforma deve incluir o PCR 11.</span><span class="sxs-lookup"><span data-stu-id="07c80-141">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="07c80-142">Valor</span><span class="sxs-lookup"><span data-stu-id="07c80-142">Value</span></span>                                                                         | <span data-ttu-id="07c80-143">Significado</span><span class="sxs-lookup"><span data-stu-id="07c80-143">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07c80-144"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-144"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="07c80-145">Principal raiz de CRTM (relação de confiança de medida), BIOS e extensões de plataforma</span><span class="sxs-lookup"><span data-stu-id="07c80-145">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="07c80-146"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-146"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="07c80-147">Configuração e dados da plataforma e da placa-mãe</span><span class="sxs-lookup"><span data-stu-id="07c80-147">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="07c80-148"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-148"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="07c80-149">Código da ROM de opção</span><span class="sxs-lookup"><span data-stu-id="07c80-149">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="07c80-150"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-150"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="07c80-151">Configuração de ROM de opção e dados</span><span class="sxs-lookup"><span data-stu-id="07c80-151">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="07c80-152"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-152"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="07c80-153">Código de registro mestre de inicialização (MBR)</span><span class="sxs-lookup"><span data-stu-id="07c80-153">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="07c80-154"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-154"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="07c80-155">Tabela de partição MBR (registro mestre de inicialização)</span><span class="sxs-lookup"><span data-stu-id="07c80-155">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="07c80-156"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-156"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="07c80-157">Transição de estado e eventos de ativação</span><span class="sxs-lookup"><span data-stu-id="07c80-157">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="07c80-158"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-158"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="07c80-159">Manufacturer-Specific do computador</span><span class="sxs-lookup"><span data-stu-id="07c80-159">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="07c80-160"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-160"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="07c80-161">Setor de inicialização NTFS</span><span class="sxs-lookup"><span data-stu-id="07c80-161">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="07c80-162"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-162"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="07c80-163">Bloco de inicialização NTFS</span><span class="sxs-lookup"><span data-stu-id="07c80-163">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="07c80-164"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-164"><dt>10</dt></span></span> </dl> | <span data-ttu-id="07c80-165">Gerenciador de inicialização</span><span class="sxs-lookup"><span data-stu-id="07c80-165">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="07c80-166"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-166"><dt>11</dt></span></span> </dl> | <span data-ttu-id="07c80-167">Controle de acesso do BitLocker</span><span class="sxs-lookup"><span data-stu-id="07c80-167">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="07c80-168"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-168"><dt>12</dt></span></span> </dl> | <span data-ttu-id="07c80-169">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="07c80-169">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="07c80-170"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-170"><dt>13</dt></span></span> </dl> | <span data-ttu-id="07c80-171">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="07c80-171">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="07c80-172"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-172"><dt>14</dt></span></span> </dl> | <span data-ttu-id="07c80-173">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="07c80-173">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="07c80-174"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-174"><dt>15</dt></span></span> </dl> | <span data-ttu-id="07c80-175">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="07c80-175">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="07c80-176"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-176"><dt>16</dt></span></span> </dl> | <span data-ttu-id="07c80-177">Usado para depuração</span><span class="sxs-lookup"><span data-stu-id="07c80-177">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="07c80-178"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-178"><dt>17</dt></span></span> </dl> | <span data-ttu-id="07c80-179">CRTM dinâmico</span><span class="sxs-lookup"><span data-stu-id="07c80-179">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="07c80-180"><dt>anos</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-180"><dt>18</dt></span></span> </dl> | <span data-ttu-id="07c80-181">Definido pela plataforma</span><span class="sxs-lookup"><span data-stu-id="07c80-181">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="07c80-182"><dt>aprimora</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-182"><dt>19</dt></span></span> </dl> | <span data-ttu-id="07c80-183">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="07c80-183">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="07c80-184"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-184"><dt>20</dt></span></span> </dl> | <span data-ttu-id="07c80-185">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="07c80-185">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="07c80-186"><dt>Abril</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-186"><dt>21</dt></span></span> </dl> | <span data-ttu-id="07c80-187">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="07c80-187">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="07c80-188"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-188"><dt>22</dt></span></span> </dl> | <span data-ttu-id="07c80-189">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="07c80-189">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="07c80-190"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-190"><dt>23</dt></span></span> </dl> | <span data-ttu-id="07c80-191">Suporte a aplicativos</span><span class="sxs-lookup"><span data-stu-id="07c80-191">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="07c80-192">*ExternalKey* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="07c80-192">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07c80-193">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="07c80-193">Type: **uint8\[\]**</span></span>

<span data-ttu-id="07c80-194">Uma matriz de bytes que especifica a chave externa de 256 bits usada para desbloquear o volume quando o computador é iniciado.</span><span class="sxs-lookup"><span data-stu-id="07c80-194">An array of bytes that specifies the 256-bit external key used to unlock the volume when the computer starts.</span></span>

<span data-ttu-id="07c80-195">Se nenhuma chave externa for especificada, uma será gerada aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="07c80-195">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="07c80-196">Use o método [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) para obter a chave gerada aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="07c80-196">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="07c80-197">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07c80-197">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c80-198">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07c80-198">Type: **string**</span></span>

<span data-ttu-id="07c80-199">Uma cadeia de caracteres que é o identificador exclusivo associado ao protetor de chave criado que pode ser usado para gerenciar o protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="07c80-199">A string that is the unique identifier associated with the created key protector that can be used to manage the key protector.</span></span>

<span data-ttu-id="07c80-200">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="07c80-200">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c80-201">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07c80-201">Return value</span></span>

<span data-ttu-id="07c80-202">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07c80-202">Type: **uint32**</span></span>

<span data-ttu-id="07c80-203">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="07c80-203">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="07c80-204">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="07c80-204">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="07c80-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="07c80-205">Description</span></span>                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07c80-206"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-206"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="07c80-207">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="07c80-207">The method was successful.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="07c80-208"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-208"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="07c80-209">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="07c80-209">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="07c80-210"><dt>**TBS \_ O \_ serviço E \_ não \_ está executando**</dt> o <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-210"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="07c80-211">Nenhum TPM compatível foi encontrado neste computador.</span><span class="sxs-lookup"><span data-stu-id="07c80-211">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="07c80-212"><dt>**FVE \_ E \_ o \_ VOLUME externo**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-212"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="07c80-213">O TPM não pode proteger a chave de criptografia do volume porque o volume não contém o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="07c80-213">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                                                                                                               |
| <dl> <span data-ttu-id="07c80-214"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-214"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="07c80-215">O parâmetro *PlatformValidationProfile* é fornecido, mas seus valores não estão dentro do intervalo conhecido ou não correspondem à configuração de política de grupo atualmente em vigor.</span><span class="sxs-lookup"><span data-stu-id="07c80-215">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> <span data-ttu-id="07c80-216">O parâmetro *ExternalKey* é fornecido, mas não é uma matriz de tamanho de 32.</span><span class="sxs-lookup"><span data-stu-id="07c80-216">The *ExternalKey* parameter is provided but is not an array of size 32.</span></span><br/> |
| <dl> <span data-ttu-id="07c80-217"><dt>**FVE \_ E \_ inicializável \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-217"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>       | <span data-ttu-id="07c80-218">Um CD/DVD inicializável foi encontrado neste computador.</span><span class="sxs-lookup"><span data-stu-id="07c80-218">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="07c80-219">Remova o CD/DVD e reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="07c80-219">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="07c80-220"><dt>**FVE \_ O \_ protetor E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>     | <span data-ttu-id="07c80-221">Já existe um protetor de chave deste tipo.</span><span class="sxs-lookup"><span data-stu-id="07c80-221">A key protector of this type already exists.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a><span data-ttu-id="07c80-222">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="07c80-222">Security Considerations</span></span>

<span data-ttu-id="07c80-223">Para a segurança do seu computador, recomendamos o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="07c80-223">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="07c80-224">Para proteção adicional contra alterações de código de inicialização antecipada, use um perfil de PCRs 0, 2, 4, 5, 8, 9, 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="07c80-224">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="07c80-225">Para proteção adicional contra alterações de configuração de inicialização antecipada, use um perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="07c80-225">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="07c80-226">A alteração do perfil padrão afeta a segurança ou a usabilidade do seu computador.</span><span class="sxs-lookup"><span data-stu-id="07c80-226">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="07c80-227">Comentários</span><span class="sxs-lookup"><span data-stu-id="07c80-227">Remarks</span></span>

<span data-ttu-id="07c80-228">No máximo um protetor de chave do tipo "TPM e chave de inicialização" pode existir para um volume a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="07c80-228">At most one key protector of type "TPM And Startup Key" can exist for a volume at any time.</span></span> <span data-ttu-id="07c80-229">Se você quiser alterar o nome de exibição ou o perfil de validação de plataforma usado por um protetor de chave "TPM Plus Startup Key" existente, primeiro deverá remover o protetor de chave existente e, em seguida, chamar **ProtectKeyWithTPMAndStartupKey** para criar um novo.</span><span class="sxs-lookup"><span data-stu-id="07c80-229">If you want to change the display name or the platform validation profile used by an existing "TPM plus Startup Key" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndStartupKey** to create a new one.</span></span> <span data-ttu-id="07c80-230">Protetores de chave adicionais devem ser especificados para desbloquear o volume em cenários de recuperação em que o acesso à chave de criptografia do volume não pode ser obtido; por exemplo, quando o TPM não pode validar com êxito no perfil de validação de plataforma ou quando a memória USB que contém a chave externa é perdida.</span><span class="sxs-lookup"><span data-stu-id="07c80-230">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when USB memory that contains the external key is lost.</span></span>

<span data-ttu-id="07c80-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para criar um ou mais protetores de chave para recuperar um volume bloqueado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="07c80-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="07c80-232">Embora seja possível ter tanto um protetor de chave do tipo "TPM" quanto outro do tipo "TPM e chave de inicialização", a presença do tipo de protetor de chave "TPM" nega os efeitos de outros protetores de chave baseados em TPM.</span><span class="sxs-lookup"><span data-stu-id="07c80-232">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And Startup Key", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="07c80-233">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="07c80-233">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="07c80-234">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="07c80-234">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="07c80-235">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="07c80-235">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="07c80-236">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="07c80-236">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07c80-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c80-237">Requirements</span></span>



| <span data-ttu-id="07c80-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c80-238">Requirement</span></span> | <span data-ttu-id="07c80-239">Valor</span><span class="sxs-lookup"><span data-stu-id="07c80-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c80-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07c80-240">Minimum supported client</span></span><br/> | <span data-ttu-id="07c80-241">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="07c80-241">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="07c80-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07c80-242">Minimum supported server</span></span><br/> | <span data-ttu-id="07c80-243">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07c80-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07c80-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="07c80-244">Namespace</span></span><br/>                | <span data-ttu-id="07c80-245">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="07c80-245">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="07c80-246">MOF</span><span class="sxs-lookup"><span data-stu-id="07c80-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07c80-247"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07c80-247"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c80-248">Confira também</span><span class="sxs-lookup"><span data-stu-id="07c80-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c80-249">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="07c80-249">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="07c80-250">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="07c80-250">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
