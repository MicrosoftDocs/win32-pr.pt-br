---
description: Se o Trusted Platform Module (TPM) estiver disponível, esse método protegerá a chave de criptografia do volume.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Método ProtectKeyWithTPM da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753718"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b3d52-103">Método ProtectKeyWithTPM da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="b3d52-103">ProtectKeyWithTPM method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b3d52-104">O método **ProtectKeyWithTPM** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protege a chave de criptografia do volume usando o hardware de segurança Trusted Platform Module (TPM) no computador, se disponível.</span><span class="sxs-lookup"><span data-stu-id="b3d52-104">The **ProtectKeyWithTPM** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available.</span></span>

<span data-ttu-id="b3d52-105">Um protetor de chave do tipo "TPM" será criado para o volume, se ainda não existir um.</span><span class="sxs-lookup"><span data-stu-id="b3d52-105">A key protector of type "TPM" is created for the volume, if one does not already exist.</span></span>

<span data-ttu-id="b3d52-106">Esse método só é aplicável para o volume que contém o sistema operacional em execução no momento e se um protetor de chave ainda não existir no volume.</span><span class="sxs-lookup"><span data-stu-id="b3d52-106">This method is only applicable for the volume that contains the currently running operating system, and if a key protector does not already exist on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d52-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3d52-107">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="b3d52-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3d52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3d52-109">*FriendlyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b3d52-109">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d52-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3d52-110">Type: **string**</span></span>

<span data-ttu-id="b3d52-111">Uma cadeia de caracteres que especifica um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="b3d52-111">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="b3d52-112">Se esse parâmetro não for especificado, um valor em branco será usado.</span><span class="sxs-lookup"><span data-stu-id="b3d52-112">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="b3d52-113">*PlatformValidationProfile* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b3d52-113">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d52-114">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b3d52-114">Type: **uint8\[\]**</span></span>

<span data-ttu-id="b3d52-115">Uma matriz de inteiros que especifica como o hardware de segurança do Trusted Platform Module do computador (TPM) protege a chave de criptografia do volume do disco.</span><span class="sxs-lookup"><span data-stu-id="b3d52-115">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="b3d52-116">Um perfil de validação de plataforma consiste em um conjunto de índices de PCR (registro de configuração de plataforma) que variam de 0 a 23, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b3d52-116">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="b3d52-117">Os valores de repetição no parâmetro são ignorados.</span><span class="sxs-lookup"><span data-stu-id="b3d52-117">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="b3d52-118">Cada índice de PCR é associado a serviços que são executados quando o sistema operacional é iniciado.</span><span class="sxs-lookup"><span data-stu-id="b3d52-118">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="b3d52-119">Cada vez que o computador for iniciado, o TPM verificará se os serviços especificados no perfil de validação de plataforma não foram alterados.</span><span class="sxs-lookup"><span data-stu-id="b3d52-119">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="b3d52-120">Se qualquer um desses serviços for alterado enquanto a proteção do Criptografia de Unidade de Disco BitLocker (BDE) permanecer ativada, o TPM não liberará a chave de criptografia para desbloquear o volume do disco e o computador entrará no modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b3d52-120">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="b3d52-121">Se esse parâmetro for especificado enquanto a configuração de Política de Grupo correspondente tiver sido habilitada, ela deverá corresponder à configuração de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="b3d52-121">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="b3d52-122">Se esse parâmetro não for especificado, o padrão 0, 2, 4, 5, 8, 9, 10 e 11 será usado.</span><span class="sxs-lookup"><span data-stu-id="b3d52-122">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="b3d52-123">O perfil de validação de plataforma padrão protege a chave de criptografia contra alterações na raiz principal da CRTM (relação de confiança de medida), BIOS e extensões de plataforma (PCR 0), o código de ROM de opção (PCR 2), o código MBR (registro mestre de inicialização) (PCR 4), a tabela de partição MBR (registro mestre de inicialização) (PCR 5), o setor de inicialização NTFS (PCR 8), o código de inicialização NTFS (PCR 9) e o controle de acesso de Criptografia de Unidade de Disco BitLocker (PCR 11).</span><span class="sxs-lookup"><span data-stu-id="b3d52-123">The default platform validation profile secures the encryption key against changes to the Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions (PCR 0), Option ROM Code (PCR 2), the Master Boot Record (MBR) Code (PCR 4), the Master Boot Record (MBR) Partition Table (PCR 5), the NTFS Boot Sector (PCR 8), the NTFS Boot Code (PCR 9), the Boot Manager (PCR 10), and the BitLocker Drive Encryption Access Control (PCR 11).</span></span> <span data-ttu-id="b3d52-124">Para a segurança do seu computador, recomendamos o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="b3d52-124">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="b3d52-125">Os computadores baseados em Unified Extensible Firmware Interface (UEFI) não usam a PCR 5 por padrão.</span><span class="sxs-lookup"><span data-stu-id="b3d52-125">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span> <span data-ttu-id="b3d52-126">Para proteção adicional contra alterações de configuração de inicialização antecipada, use um perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="b3d52-126">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="b3d52-127">A alteração do perfil padrão afeta a segurança e a capacidade de gerenciamento do seu computador.</span><span class="sxs-lookup"><span data-stu-id="b3d52-127">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="b3d52-128">A sensibilidade do BitLocker com as modificações de plataforma (maliciosas ou autorizadas) é aumentada ou reduzida, dependendo da inclusão ou exclusão, respectivamente, do PCRs.</span><span class="sxs-lookup"><span data-stu-id="b3d52-128">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="b3d52-129">Para que a proteção do BitLocker seja habilitada, o perfil de validação de plataforma deve incluir o PCR 11.</span><span class="sxs-lookup"><span data-stu-id="b3d52-129">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="b3d52-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b3d52-130">Value</span></span>                                                                         | <span data-ttu-id="b3d52-131">Significado</span><span class="sxs-lookup"><span data-stu-id="b3d52-131">Meaning</span></span>                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3d52-132"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-132"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="b3d52-133">Principal raiz de CRTM (relação de confiança de medida), BIOS e extensões de plataforma.</span><span class="sxs-lookup"><span data-stu-id="b3d52-133">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions.</span></span><br/> |
| <dl> <span data-ttu-id="b3d52-134"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-134"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="b3d52-135">Configuração e dados da plataforma e da placa-mãe</span><span class="sxs-lookup"><span data-stu-id="b3d52-135">Platform and Motherboard Configuration and Data</span></span><br/>                          |
| <dl> <span data-ttu-id="b3d52-136"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-136"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="b3d52-137">Código da ROM de opção</span><span class="sxs-lookup"><span data-stu-id="b3d52-137">Option ROM Code</span></span><br/>                                                          |
| <dl> <span data-ttu-id="b3d52-138"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-138"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="b3d52-139">Configuração de ROM de opção e dados</span><span class="sxs-lookup"><span data-stu-id="b3d52-139">Option ROM Configuration and Data</span></span><br/>                                        |
| <dl> <span data-ttu-id="b3d52-140"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-140"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="b3d52-141">Código de registro mestre de inicialização (MBR)</span><span class="sxs-lookup"><span data-stu-id="b3d52-141">Master Boot Record (MBR) Code</span></span><br/>                                            |
| <dl> <span data-ttu-id="b3d52-142"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-142"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="b3d52-143">Tabela de partição MBR (registro mestre de inicialização)</span><span class="sxs-lookup"><span data-stu-id="b3d52-143">Master Boot Record (MBR) Partition Table</span></span><br/>                                 |
| <dl> <span data-ttu-id="b3d52-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-144"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="b3d52-145">Transição de estado e eventos de ativação</span><span class="sxs-lookup"><span data-stu-id="b3d52-145">State Transition and Wake Events</span></span><br/>                                         |
| <dl> <span data-ttu-id="b3d52-146"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-146"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="b3d52-147">Manufacturer-Specific do computador</span><span class="sxs-lookup"><span data-stu-id="b3d52-147">Computer Manufacturer-Specific</span></span><br/>                                           |
| <dl> <span data-ttu-id="b3d52-148"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-148"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="b3d52-149">Setor de inicialização NTFS</span><span class="sxs-lookup"><span data-stu-id="b3d52-149">NTFS Boot Sector</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b3d52-150"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-150"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="b3d52-151">Código de inicialização NTFS</span><span class="sxs-lookup"><span data-stu-id="b3d52-151">NTFS Boot Code</span></span><br/>                                                           |
| <dl> <span data-ttu-id="b3d52-152"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-152"><dt>10</dt></span></span> </dl> | <span data-ttu-id="b3d52-153">Gerenciador de inicialização</span><span class="sxs-lookup"><span data-stu-id="b3d52-153">Boot Manager</span></span><br/>                                                             |
| <dl> <span data-ttu-id="b3d52-154"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-154"><dt>11</dt></span></span> </dl> | <span data-ttu-id="b3d52-155">Controle de acesso Criptografia de Unidade de Disco BitLocker</span><span class="sxs-lookup"><span data-stu-id="b3d52-155">BitLocker Drive Encryption Access Control</span></span><br/>                                |
| <dl> <span data-ttu-id="b3d52-156"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-156"><dt>12</dt></span></span> </dl> | <span data-ttu-id="b3d52-157">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="b3d52-157">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="b3d52-158"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-158"><dt>13</dt></span></span> </dl> | <span data-ttu-id="b3d52-159">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="b3d52-159">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="b3d52-160"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-160"><dt>14</dt></span></span> </dl> | <span data-ttu-id="b3d52-161">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="b3d52-161">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="b3d52-162"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-162"><dt>15</dt></span></span> </dl> | <span data-ttu-id="b3d52-163">Definido para uso pelo sistema operacional estático</span><span class="sxs-lookup"><span data-stu-id="b3d52-163">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="b3d52-164"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-164"><dt>16</dt></span></span> </dl> | <span data-ttu-id="b3d52-165">Usado para depuração</span><span class="sxs-lookup"><span data-stu-id="b3d52-165">Used for debugging</span></span><br/>                                                       |
| <dl> <span data-ttu-id="b3d52-166"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-166"><dt>17</dt></span></span> </dl> | <span data-ttu-id="b3d52-167">CRTM dinâmico</span><span class="sxs-lookup"><span data-stu-id="b3d52-167">Dynamic CRTM</span></span><br/>                                                             |
| <dl> <span data-ttu-id="b3d52-168"><dt>anos</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-168"><dt>18</dt></span></span> </dl> | <span data-ttu-id="b3d52-169">Definido pela plataforma</span><span class="sxs-lookup"><span data-stu-id="b3d52-169">Platform defined</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b3d52-170"><dt>aprimora</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-170"><dt>19</dt></span></span> </dl> | <span data-ttu-id="b3d52-171">Usado pelo sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="b3d52-171">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="b3d52-172"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-172"><dt>20</dt></span></span> </dl> | <span data-ttu-id="b3d52-173">Usado pelo sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="b3d52-173">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="b3d52-174"><dt>Abril</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-174"><dt>21</dt></span></span> </dl> | <span data-ttu-id="b3d52-175">Usado pelo sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="b3d52-175">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="b3d52-176"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-176"><dt>22</dt></span></span> </dl> | <span data-ttu-id="b3d52-177">Usado pelo sistema operacional confiável</span><span class="sxs-lookup"><span data-stu-id="b3d52-177">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="b3d52-178"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-178"><dt>23</dt></span></span> </dl> | <span data-ttu-id="b3d52-179">Suporte a aplicativos</span><span class="sxs-lookup"><span data-stu-id="b3d52-179">Application support</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="b3d52-180">*VolumeKeyProtectorID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b3d52-180">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d52-181">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3d52-181">Type: **string**</span></span>

<span data-ttu-id="b3d52-182">Uma cadeia de caracteres que identifica exclusivamente o protetor criado e que pode ser usado para gerenciar o protetor de chave.</span><span class="sxs-lookup"><span data-stu-id="b3d52-182">A string that uniquely identifies the created protector and which can be used to manage the key protector.</span></span>

<span data-ttu-id="b3d52-183">Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.</span><span class="sxs-lookup"><span data-stu-id="b3d52-183">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3d52-184">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3d52-184">Return value</span></span>

<span data-ttu-id="b3d52-185">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3d52-185">Type: **uint32**</span></span>

<span data-ttu-id="b3d52-186">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="b3d52-186">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b3d52-187">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b3d52-187">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="b3d52-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3d52-188">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3d52-189"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-189"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="b3d52-190">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b3d52-190">The method was successful.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="b3d52-191"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-191"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="b3d52-192">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="b3d52-192">The volume is locked.</span></span><br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="b3d52-193"><dt>**TBS \_ O \_ serviço E \_ não \_ está executando**</dt> o <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-193"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="b3d52-194">Nenhum TPM compatível foi encontrado neste computador.</span><span class="sxs-lookup"><span data-stu-id="b3d52-194">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="b3d52-195"><dt>**FVE \_ E \_ o \_ VOLUME externo**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-195"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="b3d52-196">O TPM não pode proteger a chave de criptografia do volume porque o volume não contém o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="b3d52-196">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                           |
| <dl> <span data-ttu-id="b3d52-197"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-197"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="b3d52-198">O parâmetro *PlatformValidationProfile* é fornecido, mas seus valores não estão dentro do intervalo conhecido ou não correspondem à configuração de política de grupo atualmente em vigor.</span><span class="sxs-lookup"><span data-stu-id="b3d52-198">The *PlatformValidationProfile* parameter is provided but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="b3d52-199"><dt>**FVE \_ O \_ protetor E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-199"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="b3d52-200">Já existe um protetor de chave deste tipo.</span><span class="sxs-lookup"><span data-stu-id="b3d52-200">A key protector of this type already exists.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="b3d52-201">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="b3d52-201">Security Considerations</span></span>

<span data-ttu-id="b3d52-202">Para a segurança do seu computador, recomendamos o perfil padrão.</span><span class="sxs-lookup"><span data-stu-id="b3d52-202">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="b3d52-203">Para proteção adicional contra alterações de configuração de inicialização antecipada, use um perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="b3d52-203">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="b3d52-204">A alteração do perfil padrão afeta a segurança ou a usabilidade do seu computador.</span><span class="sxs-lookup"><span data-stu-id="b3d52-204">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d52-205">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3d52-205">Remarks</span></span>

<span data-ttu-id="b3d52-206">No máximo um protetor de chave do tipo "TPM" pode existir para um volume a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="b3d52-206">At most one key protector of type "TPM" can exist for a volume at any time.</span></span> <span data-ttu-id="b3d52-207">Se você quiser alterar o nome de exibição ou o perfil de validação de plataforma usado por um protetor de chave "TPM" existente, primeiro deverá remover o protetor de chave existente e, em seguida, chamar **ProtectKeyWithTPM** para criar um novo.</span><span class="sxs-lookup"><span data-stu-id="b3d52-207">If you want to change the display name or the platform validation profile used by an existing "TPM" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPM** to create a new one.</span></span>

<span data-ttu-id="b3d52-208">Para os índices de PCR de 0 a 5, as medidas atuais nos registros são usadas para proteger a chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b3d52-208">For PCR indices 0 through 5, the current measurements in the registers are used to protect the encryption key.</span></span> <span data-ttu-id="b3d52-209">Para os valores de PCR 8 a 11, as medidas usadas são aquelas que devem existir no próximo ciclo de início.</span><span class="sxs-lookup"><span data-stu-id="b3d52-209">For PCR values 8 through 11, the measurements used are the ones expected to exist on the next start cycle.</span></span>

<span data-ttu-id="b3d52-210">Protetores de chave adicionais devem ser especificados para desbloquear o volume em cenários de recuperação em que o acesso à chave de criptografia do volume não pode ser obtido; por exemplo, quando o TPM não pode validar com êxito em relação ao perfil de validação de plataforma.</span><span class="sxs-lookup"><span data-stu-id="b3d52-210">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile.</span></span> <span data-ttu-id="b3d52-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para criar um ou mais protetores de chave para recuperar um volume bloqueado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="b3d52-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="b3d52-212">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b3d52-212">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b3d52-213">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b3d52-213">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b3d52-214">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b3d52-214">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b3d52-215">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b3d52-215">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d52-216">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3d52-216">Requirements</span></span>



| <span data-ttu-id="b3d52-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d52-217">Requirement</span></span> | <span data-ttu-id="b3d52-218">Valor</span><span class="sxs-lookup"><span data-stu-id="b3d52-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d52-219">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3d52-219">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d52-220">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="b3d52-220">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b3d52-221">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3d52-221">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d52-222">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3d52-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3d52-223">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3d52-223">Namespace</span></span><br/>                | <span data-ttu-id="b3d52-224">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b3d52-224">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b3d52-225">MOF</span><span class="sxs-lookup"><span data-stu-id="b3d52-225">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3d52-226"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3d52-226"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3d52-227">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3d52-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d52-228">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b3d52-228">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="b3d52-229">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="b3d52-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
