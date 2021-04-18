---
description: Fornece informações de status sobre um teste de hardware de um volume de sistema operacional totalmente descriptografado.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Método GetHardwareTestStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796357"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5fd23-103">Método GetHardwareTestStatus da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5fd23-103">GetHardwareTestStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5fd23-104">O método **GetHardwareTestStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) fornece informações de status sobre um teste de hardware de um volume de sistema operacional totalmente descriptografado.</span><span class="sxs-lookup"><span data-stu-id="5fd23-104">The **GetHardwareTestStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class provides status information about a hardware test of a fully decrypted operating system volume.</span></span>

<span data-ttu-id="5fd23-105">Use esse método para mostrar se um teste de hardware está pendente, bem como o êxito ou a falha de um teste de hardware concluído na última reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="5fd23-105">Use this method to show whether a hardware test is pending, as well as the success or failure of a hardware test that completed on the last computer restart.</span></span> <span data-ttu-id="5fd23-106">Para solicitar um teste de hardware, use o método [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="5fd23-106">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd23-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fd23-107">Syntax</span></span>


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a><span data-ttu-id="5fd23-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fd23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd23-109">*TestStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5fd23-109">*TestStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd23-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fd23-110">Type: **uint32**</span></span>

<span data-ttu-id="5fd23-111">Especifica se um teste de hardware está pendente, bem como o sucesso da falha de um teste de hardware concluído na última reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="5fd23-111">Specifies whether a hardware test is pending, as well as the success of failure of a hardware test that completed on the last computer restart.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fd23-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5fd23-112">Value</span></span></th>
<th><span data-ttu-id="5fd23-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5fd23-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <span data-ttu-id="5fd23-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="5fd23-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="5fd23-115">Se um teste foi solicitado, o teste foi bem-sucedido na última reinicialização do computador e a criptografia do volume agora está em andamento.</span><span class="sxs-lookup"><span data-stu-id="5fd23-115">If a test was requested, the test has succeeded on the last computer restart and volume encryption is now in progress.</span></span> <span data-ttu-id="5fd23-116">Para obter o status de criptografia, consulte o método <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5fd23-116">For the encryption status, see the <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> method.</span></span> <span data-ttu-id="5fd23-117">Caso contrário, nenhum teste foi executado na última reinicialização do computador e nenhum está pendente.</span><span class="sxs-lookup"><span data-stu-id="5fd23-117">Otherwise, no test ran on the last computer restart and none is pending.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <span data-ttu-id="5fd23-118"><dt><strong>Com falha</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="5fd23-118"><dt><strong>Failed</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="5fd23-119">A criptografia do volume não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="5fd23-119">Volume encryption did not start.</span></span> <span data-ttu-id="5fd23-120">Todos os protetores de chave foram removidos.</span><span class="sxs-lookup"><span data-stu-id="5fd23-120">All key protectors were removed.</span></span><br/> <span data-ttu-id="5fd23-121">Para resolver um teste com falha:</span><span class="sxs-lookup"><span data-stu-id="5fd23-121">To resolve a failed test:</span></span><br/>
<ul>
<li><span data-ttu-id="5fd23-122">Consulte as informações no parâmetro <em>TestError</em> .</span><span class="sxs-lookup"><span data-stu-id="5fd23-122">Consult the information in the <em>TestError</em> parameter.</span></span></li>
<li><span data-ttu-id="5fd23-123">Adicione protetores de chave e use o método <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> novamente.</span><span class="sxs-lookup"><span data-stu-id="5fd23-123">Add key protectors and use the <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> method again.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <span data-ttu-id="5fd23-124"><dt><strong>Pendente</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="5fd23-124"><dt><strong>Pending</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="5fd23-125">Um teste foi solicitado e será executado na próxima reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="5fd23-125">A test has been requested and will run on the next computer restart.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="5fd23-126">*TestError* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5fd23-126">*TestError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd23-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fd23-127">Type: **uint32**</span></span>

<span data-ttu-id="5fd23-128">Especifica o erro do último teste de hardware concluído.</span><span class="sxs-lookup"><span data-stu-id="5fd23-128">Specifies the error from the last completed hardware test.</span></span>



| <span data-ttu-id="5fd23-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5fd23-129">Value</span></span>                                                                                               | <span data-ttu-id="5fd23-130">Significado</span><span class="sxs-lookup"><span data-stu-id="5fd23-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5fd23-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-131"><dt>0</dt></span></span> </dl>                        | <span data-ttu-id="5fd23-132">Nenhum erro ocorreu ou nenhum teste de hardware foi executado na última reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="5fd23-132">No errors occurred or no hardware test ran on the last computer restart.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="5fd23-133"><dt> 2150694972 (0x8031003C)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-133"><dt> 2150694972 (0x8031003C)</dt></span></span> </dl> | <span data-ttu-id="5fd23-134">FVE \_ E \_ keyfile \_ não \_ encontrado</span><span class="sxs-lookup"><span data-stu-id="5fd23-134">FVE\_E\_KEYFILE\_NOT\_FOUND</span></span><br/> <span data-ttu-id="5fd23-135">Uma unidade flash USB com um arquivo de chave externa não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="5fd23-135">A USB flash drive with an external key file was not found.</span></span> <span data-ttu-id="5fd23-136">Se essa falha persistir, o computador não poderá ler unidades USB durante a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="5fd23-136">If this failure persists, the computer cannot read USB drives during restart.</span></span> <span data-ttu-id="5fd23-137">Talvez você não consiga usar chaves externas para desbloquear o volume do sistema operacional durante a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="5fd23-137">You may not be able to use external keys to unlock the operating system volume during restart.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="5fd23-138"><dt> 2150694973 (0x8031003D)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-138"><dt> 2150694973 (0x8031003D)</dt></span></span> </dl> | <span data-ttu-id="5fd23-139">FVE \_ E \_ keyfile \_ inválido</span><span class="sxs-lookup"><span data-stu-id="5fd23-139">FVE\_E\_KEYFILE\_INVALID</span></span><br/> <span data-ttu-id="5fd23-140">O arquivo de chave externa na unidade flash USB estava corrompido.</span><span class="sxs-lookup"><span data-stu-id="5fd23-140">The external key file on the USB flash drive was corrupt.</span></span> <span data-ttu-id="5fd23-141">Tente uma unidade flash USB diferente para armazenar o arquivo de chave externa.</span><span class="sxs-lookup"><span data-stu-id="5fd23-141">Try a different USB flash drive to store the external key file.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="5fd23-142"><dt> 2150694975 (0x8031003F)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-142"><dt> 2150694975 (0x8031003F)</dt></span></span> </dl> | <span data-ttu-id="5fd23-143">FVE \_ E \_ TPM \_ desabilitado</span><span class="sxs-lookup"><span data-stu-id="5fd23-143">FVE\_E\_TPM\_DISABLED</span></span><br/> <span data-ttu-id="5fd23-144">O TPM está desabilitado ou desativado ou desabilitado e desativado.</span><span class="sxs-lookup"><span data-stu-id="5fd23-144">The TPM is either disabled or deactivated or both disabled and deactivated.</span></span> <span data-ttu-id="5fd23-145">Para ativar o TPM, use o provedor WMI do [**\_ TPM do Win32**](win32-tpm.md) ou execute o snap-in de gerenciamento do TPM (TPM. msc).</span><span class="sxs-lookup"><span data-stu-id="5fd23-145">To turn on the TPM, use the [**Win32\_Tpm**](win32-tpm.md) WMI provider or run the TPM management snap-in (Tpm.msc).</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="5fd23-146"><dt> 2150694977 (0x80310041)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-146"><dt> 2150694977 (0x80310041)</dt></span></span> </dl> | <span data-ttu-id="5fd23-147">FVE \_ E \_ TPM \_ inválido \_ PCR</span><span class="sxs-lookup"><span data-stu-id="5fd23-147">FVE\_E\_TPM\_INVALID\_PCR</span></span><br/> <span data-ttu-id="5fd23-148">O TPM detectou uma alteração nos serviços de reinicialização do sistema operacional no perfil de validação da plataforma atual.</span><span class="sxs-lookup"><span data-stu-id="5fd23-148">The TPM detected a change in operating system restart services within the current platform validation profile.</span></span> <span data-ttu-id="5fd23-149">Remova qualquer CD ou DVD de inicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="5fd23-149">Remove any startup CD or DVD from the computer.</span></span> <span data-ttu-id="5fd23-150">Se essa falha persistir, verifique se as atualizações mais recentes do firmware e do BIOS estão instaladas e se o TPM está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5fd23-150">If this failure persists, check that the latest firmware and BIOS upgrades are installed, and that the TPM is otherwise working properly.</span></span><br/> |
| <dl> <span data-ttu-id="5fd23-151"><dt>2150694979 (0x80310043)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-151"><dt>2150694979 (0x80310043)</dt></span></span> </dl>  | <span data-ttu-id="5fd23-152">\_PIN FVE \_ E \_ inválido</span><span class="sxs-lookup"><span data-stu-id="5fd23-152">FVE\_E\_PIN\_INVALID</span></span><br/> <span data-ttu-id="5fd23-153">O PIN fornecido estava incorreto.</span><span class="sxs-lookup"><span data-stu-id="5fd23-153">The provided PIN was incorrect.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd23-154">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fd23-154">Return value</span></span>

<span data-ttu-id="5fd23-155">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fd23-155">Type: **uint32**</span></span>

<span data-ttu-id="5fd23-156">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="5fd23-156">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="5fd23-157">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5fd23-157">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="5fd23-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fd23-158">Description</span></span>                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5fd23-159"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-159"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="5fd23-160">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5fd23-160">The method succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="5fd23-161"><dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-161"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="5fd23-162">O volume está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5fd23-162">The volume is locked.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5fd23-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fd23-163">Remarks</span></span>

<span data-ttu-id="5fd23-164">Para solicitar um teste de hardware, use o método [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="5fd23-164">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="5fd23-165">Para executar um teste de hardware quando seu status estiver pendente, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="5fd23-165">To run a hardware test when its status is pending, follow these steps:</span></span>

1.  <span data-ttu-id="5fd23-166">Insira no computador uma unidade flash USB que contenha um arquivo de chave externa.</span><span class="sxs-lookup"><span data-stu-id="5fd23-166">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="5fd23-167">Esta etapa se aplica somente se o volume tiver um protetor de chave do tipo "chave externa" ou "TPM e chave de inicialização".</span><span class="sxs-lookup"><span data-stu-id="5fd23-167">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="5fd23-168">Reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="5fd23-168">Restart the computer.</span></span> <span data-ttu-id="5fd23-169">Na reinicialização do computador, o teste de hardware é executado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5fd23-169">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="5fd23-170">Para cancelar o teste de hardware, use o método [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="5fd23-170">To cancel the hardware test, use the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="5fd23-171">Um teste bem-sucedido determina que:</span><span class="sxs-lookup"><span data-stu-id="5fd23-171">A successful test determines that:</span></span>

-   <span data-ttu-id="5fd23-172">O TPM poderá desbloquear o volume se houver um protetor de chave relacionado ao TPM.</span><span class="sxs-lookup"><span data-stu-id="5fd23-172">The TPM can unlock the volume if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="5fd23-173">O computador pode ler uma unidade flash USB que contém um arquivo de chave externa durante a inicialização se o volume puder ser desbloqueado por uma chave externa (incluindo uma chave de inicialização).</span><span class="sxs-lookup"><span data-stu-id="5fd23-173">The computer can read a USB flash drive that contains an external key file during startup if the volume can be unlocked by an external key (including a startup key).</span></span>

<span data-ttu-id="5fd23-174">Os resultados de teste de hardware não estarão disponíveis após as alterações na conversão ou após a próxima reinicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="5fd23-174">Hardware test results will not be available after any changes in conversion or after the next computer restart.</span></span> <span data-ttu-id="5fd23-175">Verifique o log de eventos do sistema para obter as informações sobre os testes de hardware que foram executados anteriormente no computador.</span><span class="sxs-lookup"><span data-stu-id="5fd23-175">Check the System event log for the information about any hardware tests that previously ran on the computer.</span></span>

<span data-ttu-id="5fd23-176">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5fd23-176">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5fd23-177">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="5fd23-177">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5fd23-178">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5fd23-178">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5fd23-179">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5fd23-179">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd23-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fd23-180">Requirements</span></span>



| <span data-ttu-id="5fd23-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd23-181">Requirement</span></span> | <span data-ttu-id="5fd23-182">Valor</span><span class="sxs-lookup"><span data-stu-id="5fd23-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd23-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fd23-183">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd23-184">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="5fd23-184">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5fd23-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fd23-185">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd23-186">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5fd23-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5fd23-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fd23-187">Namespace</span></span><br/>                | <span data-ttu-id="5fd23-188">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5fd23-188">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5fd23-189">MOF</span><span class="sxs-lookup"><span data-stu-id="5fd23-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fd23-190"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-190"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd23-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fd23-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd23-192">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5fd23-192">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
