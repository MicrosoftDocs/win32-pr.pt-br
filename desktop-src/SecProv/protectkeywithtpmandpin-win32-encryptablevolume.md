---
description: Se o Trusted Platform Module (TPM) estiver disponível, esse método protegerá a chave de criptografia do volume aprimorada por um número de identificação pessoal especificado pelo usuário.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Método ProtectKeyWithTPMAndPIN da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e5a0a7a253723bec84df7a86fa94ab182bd192dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826969"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="60d21-103">Método ProtectKeyWithTPMAndPIN da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="60d21-103">ProtectKeyWithTPMAndPIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="60d21-104">O método **ProtectKeyWithTPMAndPIN** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protege a chave de criptografia do volume usando o hardware de segurança Trusted Platform Module (TPM) no computador, se disponível, aprimorado por um PIN (número de identificação pessoal) especificado pelo usuário que deve ser fornecido ao computador na inicialização.</span><span class="sxs-lookup"><span data-stu-id="60d21-104">The **ProtectKeyWithTPMAndPIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by a user-specified personal identification number (PIN) that must be provided to the computer at startup.</span></span>

<span data-ttu-id="60d21-105">A validação do TPM e a entrada da cadeia de caracteres de identificação pessoal são necessárias para acessar a chave de criptografia do volume e desbloquear o conteúdo do volume.</span><span class="sxs-lookup"><span data-stu-id="60d21-105">Both validation by the TPM and input of the personal identification string are necessary to access the volume's encryption key and unlock volume contents.</span></span>

<span data-ttu-id="60d21-106">Esse método só é aplicável ao volume que contém o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="60d21-106">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="60d21-107">Um protetor de chave do tipo "TPM e PIN" será criado para o volume, se ainda não existir um.</span><span class="sxs-lookup"><span data-stu-id="60d21-107">A key protector of type "TPM And PIN" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d21-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60d21-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="60d21-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60d21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60d21-110">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="60d21-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60d21-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60d21-111">Type: **string**</span></span>

<span data-ttu-id="60d21-112">Um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="60d21-112">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="60d21-113">Se esse parâmetro não for especificado, um valor em branco será usado.</span><span class="sxs-lookup"><span data-stu-id="60d21-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="60d21-114">*PlatformValidationProfile* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="60d21-114">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60d21-115">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="60d21-115">Type: **uint8\[\]**</span></span>

<span data-ttu-id="60d21-116">Uma matriz de inteiros que especifica como o hardware de segurança do Trusted Platform Module do computador (TPM) protege a chave de criptografia do volume do disco.</span><span class="sxs-lookup"><span data-stu-id="60d21-116">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="60d21-117">Um perfil de validação de plataforma consiste em um conjunto de índices de PCR (registro de configuração de plataforma) que variam de 0 a 23, inclusive.</span><span class="sxs-lookup"><span data-stu-id="60d21-117">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="60d21-118">Os valores de repetição no parâmetro são ignorados.</span><span class="sxs-lookup"><span data-stu-id="60d21-118">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="60d21-119">Cada índice de PCR é associado a serviços que são executados quando o sistema operacional é iniciado.</span><span class="sxs-lookup"><span data-stu-id="60d21-119">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="60d21-120">Cada vez que o computador for iniciado, o TPM verificará se os serviços especificados no perfil de validação de plataforma não foram alterados.</span><span class="sxs-lookup"><span data-stu-id="60d21-120">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="60d21-121">Se qualquer um desses serviços for alterado enquanto a proteção Criptografia de Unidade de Disco BitLocker (BDE) permanecer ativada, o TPM não liberará a chave de criptografia para desbloquear o volume do disco e o computador entrará no modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="60d21-121">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="60d21-122">Se esse parâmetro for especificado enquanto a configuração de Política de Grupo correspondente tiver sido habilitada, ela deverá corresponder à configuração de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="60d21-122">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="60d21-123">Se esse parâmetro não for especificado, o padrão 0, 2, 4, 5, 8, 9, 10 e 11 será usado.</span><span class="sxs-lookup"><span data-stu-id="60d21-123">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="60d21-124">O perfil de validação de plataforma padrão protege a chave de criptografia contra alterações nos seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="60d21-124">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="60d21-125">Principal raiz de confiança de medida (CRTM)</span><span class="sxs-lookup"><span data-stu-id="60d21-125">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="60d21-126">BIOS</span><span class="sxs-lookup"><span data-stu-id="60d21-126">BIOS</span></span>
-   <span data-ttu-id="60d21-127">Extensões de plataforma (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="60d21-127">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="60d21-128">Código ROM de opção (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="60d21-128">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="60d21-129">Código de MBR (registro mestre de inicialização) (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="60d21-129">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="60d21-130">Tabela de partição MBR (registro mestre de inicialização) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="60d21-130">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="60d21-131">Setor de inicialização NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="60d21-131">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="60d21-132">Bloco de inicialização NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="60d21-132">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="60d21-133">Gerenciador de inicialização (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="60d21-133">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="60d21-134">Controle de acesso do BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="60d21-134">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="60d21-135">Para a segurança do seu computador, recomendamos o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="60d21-135">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="60d21-136">Para proteção adicional contra alterações de configuração de inicialização antecipada, use um perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="60d21-136">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="60d21-137">Os computadores baseados em Unified Extensible Firmware Interface (UEFI) não usam a PCR 5 por padrão.</span><span class="sxs-lookup"><span data-stu-id="60d21-137">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="60d21-138">A alteração do perfil padrão afeta a segurança e a capacidade de gerenciamento do seu computador.</span><span class="sxs-lookup"><span data-stu-id="60d21-138">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="60d21-139">A sensibilidade do BitLocker com as modificações de plataforma (maliciosas ou autorizadas) é aumentada ou reduzida, dependendo da inclusão ou exclusão, respectivamente, do PCRs.</span><span class="sxs-lookup"><span data-stu-id="60d21-139">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="60d21-140">Para que a proteção do BitLocker seja habilitada, o perfil de validação de plataforma deve incluir o PCR 11.</span><span class="sxs-lookup"><span data-stu-id="60d21-140">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="60d21-141">Valor</span><span class="sxs-lookup"><span data-stu-id="60d21-141">Value</span></span>                                                                         | <span data-ttu-id="60d21-142">Significado</span><span class="sxs-lookup"><span data-stu-id="60d21-142">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60d21-143"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-143"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="60d21-144">Principal raiz de CRTM (relação de confiança de medida), BIOS e extensões de plataforma</span><span class="sxs-lookup"><span data-stu-id="60d21-144">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="60d21-145"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-145"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="60d21-146">Configuração e dados da plataforma e da placa-mãe</span><span class="sxs-lookup"><span data-stu-id="60d21-146">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="60d21-147"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-147"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="60d21-148">Código da ROM de opção</span><span class="sxs-lookup"><span data-stu-id="60d21-148">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="60d21-149"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-149"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="60d21-150">Configuração de ROM de opção e dados</span><span class="sxs-lookup"><span data-stu-id="60d21-150">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="60d21-151"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-151"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="60d21-152">Código de registro mestre de inicialização (MBR)</span><span class="sxs-lookup"><span data-stu-id="60d21-152">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="60d21-153"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-153"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="60d21-154">Tabela de partição MBR (registro mestre de inicialização)</span><span class="sxs-lookup"><span data-stu-id="60d21-154">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="60d21-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-155"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="60d21-156">Transição de estado e eventos de ativação</span><span class="sxs-lookup"><span data-stu-id="60d21-156">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="60d21-157"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-157"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="60d21-158">Manufacturer-Specific do computador</span><span class="sxs-lookup"><span data-stu-id="60d21-158">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="60d21-159"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-159"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="60d21-160">Setor de inicialização NTFS</span><span class="sxs-lookup"><span data-stu-id="60d21-160">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="60d21-161"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-161"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="60d21-162">Bloco de inicialização NTFS</span><span class="sxs-lookup"><span data-stu-id="60d21-162">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="60d21-163"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-163"><dt>10</dt></span></span> </dl> | <span data-ttu-id="60d21-164">Gerenciador de inicialização</span><span class="sxs-lookup"><span data-stu-id="60d21-164">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="60d21-165"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-165"><dt>11</dt></span></span> </dl> | <span data-ttu-id="60d21-166">Controle de acesso do BitLocker</span><span class="sxs-lookup"><span data-stu-id="60d21-166">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="60d21-167"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-167"><dt>12</dt></span></span> </dl> | <span data-ttu-id="60d21-168">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="60d21-168">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="60d21-169"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-169"><dt>13</dt></span></span> </dl> | <span data-ttu-id="60d21-170">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="60d21-170">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="60d21-171"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-171"><dt>14</dt></span></span> </dl> | <span data-ttu-id="60d21-172">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="60d21-172">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="60d21-173"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-173"><dt>15</dt></span></span> </dl> | <span data-ttu-id="60d21-174">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="60d21-174">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="60d21-175"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-175"><dt>16</dt></span></span> </dl> | <span data-ttu-id="60d21-176">Usado para depuração</span><span class="sxs-lookup"><span data-stu-id="60d21-176">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="60d21-177"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-177"><dt>17</dt></span></span> </dl> | <span data-ttu-id="60d21-178">CRTM dinâmico</span><span class="sxs-lookup"><span data-stu-id="60d21-178">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="60d21-179"><dt>anos</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-179"><dt>18</dt></span></span> </dl> | <span data-ttu-id="60d21-180">Definido pela plataforma</span><span class="sxs-lookup"><span data-stu-id="60d21-180">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="60d21-181"><dt>aprimora</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-181"><dt>19</dt></span></span> </dl> | <span data-ttu-id="60d21-182">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="60d21-182">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="60d21-183"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-183"><dt>20</dt></span></span> </dl> | <span data-ttu-id="60d21-184">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="60d21-184">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="60d21-185"><dt>Abril</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-185"><dt>21</dt></span></span> </dl> | <span data-ttu-id="60d21-186">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="60d21-186">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="60d21-187"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-187"><dt>22</dt></span></span> </dl> | <span data-ttu-id="60d21-188">Usado por um sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="60d21-188">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="60d21-189"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-189"><dt>23</dt></span></span> </dl> | <span data-ttu-id="60d21-190">Suporte a aplicativos</span><span class="sxs-lookup"><span data-stu-id="60d21-190">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="60d21-191">*Fixar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60d21-191">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60d21-192">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60d21-192">Type: **string**</span></span>

<span data-ttu-id="60d21-193">Uma cadeia de caracteres de identificação pessoal especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="60d21-193">A user-specified personal identification string.</span></span> <span data-ttu-id="60d21-194">Essa cadeia de caracteres deve consistir em uma sequência de 6 a 20 dígitos ou, se a política de grupo "permitir PINs avançados para inicialização" estiver habilitada, de 6 a 20 letras, símbolos, espaços ou números.</span><span class="sxs-lookup"><span data-stu-id="60d21-194">This string must consist of a sequence of 6 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 6 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> <dt>

<span data-ttu-id="60d21-195">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="60d21-195">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60d21-196">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60d21-196">Type: **string**</span></span>

<span data-ttu-id="60d21-197">O identificador de cadeia de caracteres exclusivo atualizado usado para gerenciar um protetor de chave de volume criptografado.</span><span class="sxs-lookup"><span data-stu-id="60d21-197">The updated unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="60d21-198">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="60d21-198">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60d21-199">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60d21-199">Return value</span></span>

<span data-ttu-id="60d21-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60d21-200">Type: **uint32**</span></span>

<span data-ttu-id="60d21-201">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="60d21-201">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="60d21-202">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="60d21-202">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="60d21-203">Descrição</span><span class="sxs-lookup"><span data-stu-id="60d21-203">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60d21-204"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-204"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="60d21-205">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="60d21-205">The method was successful.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="60d21-206"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-206"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                        | <span data-ttu-id="60d21-207">O parâmetro *PlatformValidationProfile* é fornecido, mas seus valores não estão dentro do intervalo conhecido ou não correspondem à configuração de política de grupo atualmente em vigor.</span><span class="sxs-lookup"><span data-stu-id="60d21-207">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="60d21-208"><dt>**FVE \_ E \_ inicializável \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-208"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="60d21-209">Um CD/DVD inicializável foi encontrado neste computador.</span><span class="sxs-lookup"><span data-stu-id="60d21-209">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="60d21-210">Remova o CD/DVD e reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="60d21-210">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="60d21-211"><dt>**FVE \_ E \_ o \_ VOLUME externo**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-211"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>              | <span data-ttu-id="60d21-212">O TPM não pode proteger a chave de criptografia do volume porque o volume não contém o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="60d21-212">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                            |
| <dl> <span data-ttu-id="60d21-213"><dt>**FVE \_ E \_ \_ \_ caracteres de PIN inválidos**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-213"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="60d21-214">O parâmetro *NewPIN* contém caracteres que não são válidos.</span><span class="sxs-lookup"><span data-stu-id="60d21-214">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="60d21-215">Quando a Política de Grupo "permitir PINs avançados para inicialização" está desabilitada, somente os números têm suporte.</span><span class="sxs-lookup"><span data-stu-id="60d21-215">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>          |
| <dl> <span data-ttu-id="60d21-216"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-216"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="60d21-217">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="60d21-217">The volume is locked.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="60d21-218"><dt>**FVE \_ \_Política E \_ \_ \_ comprimento de PIN inválido**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-218"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="60d21-219">O parâmetro *NewPIN* fornecido tem mais de 20 caracteres, menos de seis caracteres ou menos que o comprimento mínimo especificado por política de grupo.</span><span class="sxs-lookup"><span data-stu-id="60d21-219">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 6 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>            |
| <dl> <span data-ttu-id="60d21-220"><dt>**FVE \_ O \_ protetor E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="60d21-221">Já existe um protetor de chave deste tipo.</span><span class="sxs-lookup"><span data-stu-id="60d21-221">A key protector of this type already exists.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="60d21-222"><dt>**TBS \_ O \_ serviço E \_ não \_ está executando**</dt> o <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-222"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="60d21-223">Nenhum TPM compatível foi encontrado neste computador.</span><span class="sxs-lookup"><span data-stu-id="60d21-223">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="60d21-224">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="60d21-224">Security Considerations</span></span>

<span data-ttu-id="60d21-225">Para a segurança do seu computador, recomendamos o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="60d21-225">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="60d21-226">Para proteção adicional contra alterações de código de inicialização antecipada, use um perfil de PCRs 0, 2, 4, 5, 8, 9, 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="60d21-226">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="60d21-227">Para proteção adicional contra alterações de configuração de inicialização antecipada, use um perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="60d21-227">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="60d21-228">A alteração do perfil padrão afeta a segurança ou a usabilidade do seu computador.</span><span class="sxs-lookup"><span data-stu-id="60d21-228">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="60d21-229">Comentários</span><span class="sxs-lookup"><span data-stu-id="60d21-229">Remarks</span></span>

<span data-ttu-id="60d21-230">No máximo um protetor de chave do tipo "TPM e PIN" pode existir para um volume a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="60d21-230">At most one key protector of type "TPM And PIN" can exist for a volume at any time.</span></span> <span data-ttu-id="60d21-231">Se você quiser alterar o nome de exibição ou o perfil de validação de plataforma usado por um protetor de chave "TPM e PIN" existente, primeiro deverá remover o protetor de chave existente e, em seguida, chamar **ProtectKeyWithTPMAndPIN** para criar um novo.</span><span class="sxs-lookup"><span data-stu-id="60d21-231">If you want to change the display name or the platform validation profile used by an existing "TPM And PIN" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndPIN** to create a new one.</span></span>

<span data-ttu-id="60d21-232">Protetores de chave adicionais devem ser especificados para desbloquear o volume em cenários de recuperação em que o acesso à chave de criptografia do volume não pode ser obtido; por exemplo, quando o TPM não puder ser validado com êxito no perfil de validação de plataforma ou quando o PIN for perdido.</span><span class="sxs-lookup"><span data-stu-id="60d21-232">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when the PIN is lost.</span></span>

<span data-ttu-id="60d21-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para criar um ou mais protetores de chave para recuperar um volume bloqueado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="60d21-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="60d21-234">Embora seja possível ter tanto um protetor de chave do tipo "TPM" quanto outro do tipo "TPM e PIN", a presença do tipo de protetor de chave "TPM" nega os efeitos de outros protetores de chave baseados em TPM.</span><span class="sxs-lookup"><span data-stu-id="60d21-234">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And PIN", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="60d21-235">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="60d21-235">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60d21-236">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="60d21-236">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="60d21-237">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="60d21-237">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60d21-238">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="60d21-238">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60d21-239">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60d21-239">Requirements</span></span>



| <span data-ttu-id="60d21-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="60d21-240">Requirement</span></span> | <span data-ttu-id="60d21-241">Valor</span><span class="sxs-lookup"><span data-stu-id="60d21-241">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60d21-242">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60d21-242">Minimum supported client</span></span><br/> | <span data-ttu-id="60d21-243">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="60d21-243">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="60d21-244">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60d21-244">Minimum supported server</span></span><br/> | <span data-ttu-id="60d21-245">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60d21-245">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60d21-246">Namespace</span><span class="sxs-lookup"><span data-stu-id="60d21-246">Namespace</span></span><br/>                | <span data-ttu-id="60d21-247">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="60d21-247">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="60d21-248">MOF</span><span class="sxs-lookup"><span data-stu-id="60d21-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60d21-249"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60d21-249"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d21-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="60d21-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d21-251">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="60d21-251">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="60d21-252">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="60d21-252">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
