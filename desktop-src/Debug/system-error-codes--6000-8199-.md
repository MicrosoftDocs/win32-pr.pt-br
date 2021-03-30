---
description: Descreve os códigos de erro 6000-8199 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Códigos de erro do sistema (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826518"
---
# <a name="system-error-codes-6000-8199"></a><span data-ttu-id="6bebd-103">Códigos de erro do sistema (6000-8199)</span><span class="sxs-lookup"><span data-stu-id="6bebd-103">System Error Codes (6000-8199)</span></span>

> [!NOTE]
> <span data-ttu-id="6bebd-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="6bebd-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6bebd-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="6bebd-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 6000 a 8199).</span><span class="sxs-lookup"><span data-stu-id="6bebd-106">The following list describes [system error codes](system-error-codes.md) (errors 6000 to 8199).</span></span> <span data-ttu-id="6bebd-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="6bebd-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="6bebd-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="6bebd-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="6bebd-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**\_falha na criptografia de erro \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR\_ENCRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-110">6000 (0x1770)</span><span class="sxs-lookup"><span data-stu-id="6bebd-110">6000 (0x1770)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-111">O arquivo especificado não pôde ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-111">The specified file could not be encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**\_falha na descriptografia de erro \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERROR\_DECRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-113">6001 (0x1771)</span><span class="sxs-lookup"><span data-stu-id="6bebd-113">6001 (0x1771)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-114">O arquivo especificado não pôde ser descriptografado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-114">The specified file could not be decrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**arquivo de erro \_ \_ criptografado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**ERROR\_FILE\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-116">6002 (0x1772)</span><span class="sxs-lookup"><span data-stu-id="6bebd-116">6002 (0x1772)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-117">O arquivo especificado é criptografado e o usuário não tem a capacidade de descriptografá-lo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-117">The specified file is encrypted and the user does not have the ability to decrypt it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERRO \_ sem \_ política de recuperação \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR\_NO\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-119">6003 (0x1773)</span><span class="sxs-lookup"><span data-stu-id="6bebd-119">6003 (0x1773)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-120">Não há uma política de recuperação de criptografia válida configurada para este sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-120">There is no valid encryption recovery policy configured for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERRO \_ sem \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="6bebd-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR\_NO\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-122">6004 (0x1774)</span><span class="sxs-lookup"><span data-stu-id="6bebd-122">6004 (0x1774)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-123">O driver de criptografia necessário não está carregado para este sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-123">The required encryption driver is not loaded for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERRO \_ de \_ EFS incorreto**</span><span class="sxs-lookup"><span data-stu-id="6bebd-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR\_WRONG\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-125">6005 (0x1775)</span><span class="sxs-lookup"><span data-stu-id="6bebd-125">6005 (0x1775)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-126">O arquivo foi criptografado com um driver de criptografia diferente do que está carregado no momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-126">The file was encrypted with a different encryption driver than is currently loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERRO \_ sem \_ chaves de usuário \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR\_NO\_USER\_KEYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-128">6006 (0x1776)</span><span class="sxs-lookup"><span data-stu-id="6bebd-128">6006 (0x1776)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-129">Não há chaves EFS definidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6bebd-129">There are no EFS keys defined for the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**arquivo de erro \_ \_ não \_ criptografado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**ERROR\_FILE\_NOT\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-131">6007 (0x1777)</span><span class="sxs-lookup"><span data-stu-id="6bebd-131">6007 (0x1777)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-132">O arquivo especificado não está criptografado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-132">The specified file is not encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERRO de \_ não \_ Exportar \_ formato**</span><span class="sxs-lookup"><span data-stu-id="6bebd-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERROR\_NOT\_EXPORT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-134">6008 (0x1778)</span><span class="sxs-lookup"><span data-stu-id="6bebd-134">6008 (0x1778)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-135">O arquivo especificado não está no formato de exportação EFS definido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-135">The specified file is not in the defined EFS export format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**\_arquivo de \_ erro \_ somente leitura**</span><span class="sxs-lookup"><span data-stu-id="6bebd-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**ERROR\_FILE\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-137">6009 (0x1779)</span><span class="sxs-lookup"><span data-stu-id="6bebd-137">6009 (0x1779)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-138">O arquivo especificado é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6bebd-138">The specified file is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERRO de \_ dir do \_ DFS não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR\_DIR\_EFS\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-140">6010 (0x177A)</span><span class="sxs-lookup"><span data-stu-id="6bebd-140">6010 (0x177A)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-141">O diretório foi desabilitado para criptografia.</span><span class="sxs-lookup"><span data-stu-id="6bebd-141">The directory has been disabled for encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERRO \_ de \_ servidor EFS \_ não \_ confiável**</span><span class="sxs-lookup"><span data-stu-id="6bebd-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR\_EFS\_SERVER\_NOT\_TRUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-143">6011 (0x177B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-143">6011 (0x177B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-144">O servidor não é confiável para a operação de criptografia remota.</span><span class="sxs-lookup"><span data-stu-id="6bebd-144">The server is not trusted for remote encryption operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERRO \_ de \_ política de recuperação inadequada \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR\_BAD\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-146">6012 (0x177C)</span><span class="sxs-lookup"><span data-stu-id="6bebd-146">6012 (0x177C)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-147">A política de recuperação configurada para este sistema contém um certificado de recuperação inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-147">Recovery policy configured for this system contains invalid recovery certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERRO \_ de \_ blob de alg EFS \_ \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="6bebd-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR\_EFS\_ALG\_BLOB\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-149">6013 (0x177D)</span><span class="sxs-lookup"><span data-stu-id="6bebd-149">6013 (0x177D)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-150">O algoritmo de criptografia usado no arquivo de origem precisa de um buffer de chave maior do que aquele no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6bebd-150">The encryption algorithm used on the source file needs a bigger key buffer than the one on the destination file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**o \_ volume de erros \_ não \_ dá suporte ao \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="6bebd-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**ERROR\_VOLUME\_NOT\_SUPPORT\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-152">6014 (0x177E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-152">6014 (0x177E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-153">A partição de disco não dá suporte à criptografia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-153">The disk partition does not support file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERRO \_ EFS \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR\_EFS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-155">6015 (0x177F)</span><span class="sxs-lookup"><span data-stu-id="6bebd-155">6015 (0x177F)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-156">Este computador está desabilitado para criptografia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-156">This machine is disabled for file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERRO \_ de \_ versão do EFS \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="6bebd-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR\_EFS\_VERSION\_NOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-158">6016 (0x1780)</span><span class="sxs-lookup"><span data-stu-id="6bebd-158">6016 (0x1780)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-159">Um sistema mais recente é necessário para descriptografar esse arquivo criptografado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-159">A newer system is required to decrypt this encrypted file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERRO \_ cs \_ Encryption \_ inválida \_ do servidor de \_ resposta**</span><span class="sxs-lookup"><span data-stu-id="6bebd-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR\_CS\_ENCRYPTION\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-161">6017 (0x1781)</span><span class="sxs-lookup"><span data-stu-id="6bebd-161">6017 (0x1781)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-162">O servidor remoto enviou uma resposta inválida para um arquivo que está sendo aberto com criptografia do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-162">The remote server sent an invalid response for a file being opened with Client Side Encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERRO \_ cs \_ criptografia \_ \_ do servidor sem suporte**</span><span class="sxs-lookup"><span data-stu-id="6bebd-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR\_CS\_ENCRYPTION\_UNSUPPORTED\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-164">6018 (0x1782)</span><span class="sxs-lookup"><span data-stu-id="6bebd-164">6018 (0x1782)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-165">A criptografia do lado do cliente não é compatível com o servidor remoto, mesmo que ele alega oferecer suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="6bebd-165">Client Side Encryption is not supported by the remote server even though it claims to support it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERRO \_ cs \_ criptografia \_ \_ arquivo criptografado existente \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_EXISTING\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-167">6019 (0x1783)</span><span class="sxs-lookup"><span data-stu-id="6bebd-167">6019 (0x1783)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-168">O arquivo é criptografado e deve ser aberto no modo de criptografia do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-168">File is encrypted and should be opened in Client Side Encryption mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERRO \_ cs \_ criptografia \_ novo \_ arquivo criptografado \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_NEW\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-170">6020 (0x1784)</span><span class="sxs-lookup"><span data-stu-id="6bebd-170">6020 (0x1784)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-171">Um novo arquivo criptografado está sendo criado e um $EFS precisa ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-171">A new encrypted file is being created and a $EFS needs to be provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERRO \_ cs \_ criptografia \_ arquivo \_ não \_ CSE**</span><span class="sxs-lookup"><span data-stu-id="6bebd-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR\_CS\_ENCRYPTION\_FILE\_NOT\_CSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-173">6021 (0x1785)</span><span class="sxs-lookup"><span data-stu-id="6bebd-173">6021 (0x1785)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-174">O cliente SMB solicitou um CSE FSCTL em um arquivo que não é CSE.</span><span class="sxs-lookup"><span data-stu-id="6bebd-174">The SMB client requested a CSE FSCTL on a non-CSE file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**\_operação de \_ negação de política de criptografia de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERROR\_ENCRYPTION\_POLICY\_DENIES\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-176">6022 (0x1786)</span><span class="sxs-lookup"><span data-stu-id="6bebd-176">6022 (0x1786)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-177">A operação solicitada foi bloqueada pela política.</span><span class="sxs-lookup"><span data-stu-id="6bebd-177">The requested operation was blocked by policy.</span></span> <span data-ttu-id="6bebd-178">Para obter mais informações, contate o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-178">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERRO \_ nenhum \_ servidor de navegador \_ \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR\_NO\_BROWSER\_SERVERS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-180">6118 (0x17E6)</span><span class="sxs-lookup"><span data-stu-id="6bebd-180">6118 (0x17E6)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-181">A lista de servidores para este grupo de trabalho não está disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-181">The list of servers for this workgroup is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED \_ E \_ serviço \_ não \_ LOCALSYSTEM**</span><span class="sxs-lookup"><span data-stu-id="6bebd-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED\_E\_SERVICE\_NOT\_LOCALSYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-183">6200 (0x1838)</span><span class="sxs-lookup"><span data-stu-id="6bebd-183">6200 (0x1838)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-184">O serviço de Agendador de Tarefas deve ser configurado para ser executado na conta do sistema para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-184">The Task Scheduler service must be configured to run in the System account to function properly.</span></span> <span data-ttu-id="6bebd-185">Tarefas individuais podem ser configuradas para serem executadas em outras contas.</span><span class="sxs-lookup"><span data-stu-id="6bebd-185">Individual tasks may be configured to run in other accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**setor de log de erros \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**ERROR\_LOG\_SECTOR\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-187">6600 (0x19C8)</span><span class="sxs-lookup"><span data-stu-id="6bebd-187">6600 (0x19C8)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-188">O serviço de log encontrou um setor de log inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-188">Log service encountered an invalid log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**paridade de setor de log de erros \_ \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**ERROR\_LOG\_SECTOR\_PARITY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-190">6601 (0x19C9)</span><span class="sxs-lookup"><span data-stu-id="6bebd-190">6601 (0x19C9)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-191">O serviço de log encontrou um setor de log com paridade de bloco inválida.</span><span class="sxs-lookup"><span data-stu-id="6bebd-191">Log service encountered a log sector with invalid block parity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**setor de log de erros \_ \_ \_ remapeado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**ERROR\_LOG\_SECTOR\_REMAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-193">6602 (0x19CA)</span><span class="sxs-lookup"><span data-stu-id="6bebd-193">6602 (0x19CA)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-194">O serviço de log encontrou um setor de log remapeado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-194">Log service encountered a remapped log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**bloco de log de erros \_ \_ \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="6bebd-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**ERROR\_LOG\_BLOCK\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-196">6603 (0x19CB)</span><span class="sxs-lookup"><span data-stu-id="6bebd-196">6603 (0x19CB)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-197">O serviço de log encontrou um bloco de log parcial ou incompleto.</span><span class="sxs-lookup"><span data-stu-id="6bebd-197">Log service encountered a partial or incomplete log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ intervalo inválido do log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**ERROR\_LOG\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-199">6604 (0x19CC)</span><span class="sxs-lookup"><span data-stu-id="6bebd-199">6604 (0x19CC)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-200">O serviço de log encontrou uma tentativa de acessar dados fora do intervalo de log ativo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-200">Log service encountered an attempt access data outside the active log range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**blocos de log de erros \_ \_ \_ esgotados**</span><span class="sxs-lookup"><span data-stu-id="6bebd-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**ERROR\_LOG\_BLOCKS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-202">6605 (0x19CD)</span><span class="sxs-lookup"><span data-stu-id="6bebd-202">6605 (0x19CD)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-203">Os buffers de Marshalling de usuário do serviço de log estão esgotados.</span><span class="sxs-lookup"><span data-stu-id="6bebd-203">Log service user marshalling buffers are exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**contexto de leitura do log de erros \_ \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**ERROR\_LOG\_READ\_CONTEXT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-205">6606 (0x19CE)</span><span class="sxs-lookup"><span data-stu-id="6bebd-205">6606 (0x19CE)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-206">O serviço de log encontrou uma tentativa de leitura de uma área de Marshalling com um contexto de leitura inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-206">Log service encountered an attempt read from a marshalling area with an invalid read context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**reinicialização do log de erros \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**ERROR\_LOG\_RESTART\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-208">6607 (0x19CF)</span><span class="sxs-lookup"><span data-stu-id="6bebd-208">6607 (0x19CF)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-209">O serviço de log encontrou uma área de reinício de log inválida.</span><span class="sxs-lookup"><span data-stu-id="6bebd-209">Log service encountered an invalid log restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_versão do \_ bloco de log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**ERROR\_LOG\_BLOCK\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-211">6608 (0x19D0)</span><span class="sxs-lookup"><span data-stu-id="6bebd-211">6608 (0x19D0)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-212">O serviço de log encontrou uma versão de bloco de log inválida.</span><span class="sxs-lookup"><span data-stu-id="6bebd-212">Log service encountered an invalid log block version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**bloco de log de erros \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**ERROR\_LOG\_BLOCK\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-214">6609 (0x19D1)</span><span class="sxs-lookup"><span data-stu-id="6bebd-214">6609 (0x19D1)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-215">O serviço de log encontrou um bloco de log inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-215">Log service encountered an invalid log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**modo de leitura de log de erros \_ \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**ERROR\_LOG\_READ\_MODE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-217">6610 (0x19D2)</span><span class="sxs-lookup"><span data-stu-id="6bebd-217">6610 (0x19D2)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-218">O serviço de log encontrou uma tentativa de ler o log com um modo de leitura inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-218">Log service encountered an attempt to read the log with an invalid read mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**LOG de erros \_ \_ sem \_ reinicialização**</span><span class="sxs-lookup"><span data-stu-id="6bebd-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**ERROR\_LOG\_NO\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-220">6611 (0x19D3)</span><span class="sxs-lookup"><span data-stu-id="6bebd-220">6611 (0x19D3)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-221">O serviço de log encontrou um fluxo de log sem área de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="6bebd-221">Log service encountered a log stream with no restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**metadados do log de erros \_ \_ \_ corrompidos**</span><span class="sxs-lookup"><span data-stu-id="6bebd-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**ERROR\_LOG\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-223">6612 (0x19D4)</span><span class="sxs-lookup"><span data-stu-id="6bebd-223">6612 (0x19D4)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-224">O serviço de log encontrou um arquivo de metadados corrompido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-224">Log service encountered a corrupted metadata file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**metadados de log de erros \_ \_ \_ inválidos**</span><span class="sxs-lookup"><span data-stu-id="6bebd-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**ERROR\_LOG\_METADATA\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-226">6613 (0x19D5)</span><span class="sxs-lookup"><span data-stu-id="6bebd-226">6613 (0x19D5)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-227">O serviço de log encontrou um arquivo de metadados que não pôde ser criado pelo sistema de arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-227">Log service encountered a metadata file that could not be created by the log file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**metadados do log de erros \_ \_ \_ inconsistentes**</span><span class="sxs-lookup"><span data-stu-id="6bebd-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**ERROR\_LOG\_METADATA\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-229">6614 (0x19D6)</span><span class="sxs-lookup"><span data-stu-id="6bebd-229">6614 (0x19D6)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-230">O serviço de log encontrou um arquivo de metadados com dados inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="6bebd-230">Log service encountered a metadata file with inconsistent data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**Reserva de log de erros \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**ERROR\_LOG\_RESERVATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-232">6615 (0x19D7)</span><span class="sxs-lookup"><span data-stu-id="6bebd-232">6615 (0x19D7)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-233">O serviço de log encontrou uma tentativa de alocar ou descartar o espaço de reserva.</span><span class="sxs-lookup"><span data-stu-id="6bebd-233">Log service encountered an attempt to erroneous allocate or dispose reservation space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**o log de erros não \_ \_ consegue \_ excluir**</span><span class="sxs-lookup"><span data-stu-id="6bebd-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**ERROR\_LOG\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-235">6616 (0x19D8)</span><span class="sxs-lookup"><span data-stu-id="6bebd-235">6616 (0x19D8)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-236">O serviço de log não pode excluir o arquivo de log ou o contêiner do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-236">Log service cannot delete log file or file system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**limite de contêiner de log de erros \_ \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**ERROR\_LOG\_CONTAINER\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-238">6617 (0x19D9)</span><span class="sxs-lookup"><span data-stu-id="6bebd-238">6617 (0x19D9)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-239">O serviço de log atingiu o máximo de contêineres permitidos alocados para um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-239">Log service has reached the maximum allowable containers allocated to a log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_ \_ início do log \_ de erros do \_ log**</span><span class="sxs-lookup"><span data-stu-id="6bebd-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**ERROR\_LOG\_START\_OF\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-241">6618 (0x19DA)</span><span class="sxs-lookup"><span data-stu-id="6bebd-241">6618 (0x19DA)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-242">O serviço de log tentou ler ou gravar para trás após o início do log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-242">Log service has attempted to read or write backward past the start of the log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**política de log de erros \_ \_ \_ já \_ instalada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**ERROR\_LOG\_POLICY\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-244">6619 (0x19DB)</span><span class="sxs-lookup"><span data-stu-id="6bebd-244">6619 (0x19DB)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-245">Não foi possível instalar a política de log porque já existe uma política do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-245">Log policy could not be installed because a policy of the same type is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**política de log de erros \_ \_ \_ não \_ instalada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**ERROR\_LOG\_POLICY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-247">6620 (0x19DC)</span><span class="sxs-lookup"><span data-stu-id="6bebd-247">6620 (0x19DC)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-248">A política de log em questão não foi instalada no momento da solicitação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-248">Log policy in question was not installed at the time of the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**política de log de erros \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**ERROR\_LOG\_POLICY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-250">6621 (0x19DD)</span><span class="sxs-lookup"><span data-stu-id="6bebd-250">6621 (0x19DD)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-251">O conjunto de políticas instalado no log é inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-251">The installed set of policies on the log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_conflito de \_ política de log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**ERROR\_LOG\_POLICY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-253">6622 (0x19DE)</span><span class="sxs-lookup"><span data-stu-id="6bebd-253">6622 (0x19DE)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-254">Uma política no log em questão impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-254">A policy on the log in question prevented the operation from completing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_final do \_ \_ arquivo fixado do log \_ de erros**</span><span class="sxs-lookup"><span data-stu-id="6bebd-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**ERROR\_LOG\_PINNED\_ARCHIVE\_TAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-256">6623 (0x19DF)</span><span class="sxs-lookup"><span data-stu-id="6bebd-256">6623 (0x19DF)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-257">O espaço de log não pode ser recuperado porque o log está fixado pela parte final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-257">Log space cannot be reclaimed because the log is pinned by the archive tail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**registro de log de erros não \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="6bebd-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**ERROR\_LOG\_RECORD\_NONEXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-259">6624 (0x19E0)</span><span class="sxs-lookup"><span data-stu-id="6bebd-259">6624 (0x19E0)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-260">O registro de log não é um registro no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-260">Log record is not a record in the log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**registros de log de erros \_ \_ \_ reservados \_ inválidos**</span><span class="sxs-lookup"><span data-stu-id="6bebd-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**ERROR\_LOG\_RECORDS\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-262">6625 (0x19E1)</span><span class="sxs-lookup"><span data-stu-id="6bebd-262">6625 (0x19E1)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-263">O número de registros de log reservados ou o ajuste do número de registros de log reservados é inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-263">Number of reserved log records or the adjustment of the number of reserved log records is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**\_espaço reservado para log de erros \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**ERROR\_LOG\_SPACE\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-265">6626 (0x19E2)</span><span class="sxs-lookup"><span data-stu-id="6bebd-265">6626 (0x19E2)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-266">O espaço de log reservado ou o ajuste do espaço de log é inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-266">Reserved log space or the adjustment of the log space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**cauda do log de erros \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**ERROR\_LOG\_TAIL\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-268">6627 (0x19E3)</span><span class="sxs-lookup"><span data-stu-id="6bebd-268">6627 (0x19E3)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-269">Uma parte final ou uma base de arquivo novo ou existente do log ativo é inválida.</span><span class="sxs-lookup"><span data-stu-id="6bebd-269">An new or existing archive tail or base of the active log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**LOG de erros \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="6bebd-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**ERROR\_LOG\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-271">6628 (0x19E4)</span><span class="sxs-lookup"><span data-stu-id="6bebd-271">6628 (0x19E4)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-272">Espaço de log esgotado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-272">Log space is exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERRO \_ não foi possível \_ \_ redimensionar o \_ log**</span><span class="sxs-lookup"><span data-stu-id="6bebd-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR\_COULD\_NOT\_RESIZE\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-274">6629 (0x19E5)</span><span class="sxs-lookup"><span data-stu-id="6bebd-274">6629 (0x19E5)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-275">Não foi possível definir o log para o tamanho solicitado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-275">The log could not be set to the requested size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**LOG de erros \_ \_ multiplexado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**ERROR\_LOG\_MULTIPLEXED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-277">6630 (0x19E6)</span><span class="sxs-lookup"><span data-stu-id="6bebd-277">6630 (0x19E6)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-278">O log é multiplexado, não é permitida nenhuma gravação direta no log físico.</span><span class="sxs-lookup"><span data-stu-id="6bebd-278">Log is multiplexed, no direct writes to the physical log is allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**LOG de erros \_ \_ dedicado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**ERROR\_LOG\_DEDICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-280">6631 (0x19E7)</span><span class="sxs-lookup"><span data-stu-id="6bebd-280">6631 (0x19E7)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-281">A operação falhou porque o log é um log dedicado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-281">The operation failed because the log is a dedicated log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_ \_ arquivo morto \_ de log de erros não está \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="6bebd-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-283">6632 (0x19E8)</span><span class="sxs-lookup"><span data-stu-id="6bebd-283">6632 (0x19E8)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-284">A operação requer um contexto de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-284">The operation requires an archive context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ arquivo de log \_ de erros em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="6bebd-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-286">6633 (0x19E9)</span><span class="sxs-lookup"><span data-stu-id="6bebd-286">6633 (0x19E9)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-287">O arquivamento de log está em andamento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-287">Log archival is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**LOG de erros \_ \_ efêmero**</span><span class="sxs-lookup"><span data-stu-id="6bebd-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR\_LOG\_EPHEMERAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-289">6634 (0x19EA)</span><span class="sxs-lookup"><span data-stu-id="6bebd-289">6634 (0x19EA)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-290">A operação requer um log não efêmero, mas o log é efêmero.</span><span class="sxs-lookup"><span data-stu-id="6bebd-290">The operation requires a non-ephemeral log, but the log is ephemeral.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**LOG de erros \_ \_ sem \_ \_ contêineres suficientes**</span><span class="sxs-lookup"><span data-stu-id="6bebd-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**ERROR\_LOG\_NOT\_ENOUGH\_CONTAINERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-292">6635 (0x19EB)</span><span class="sxs-lookup"><span data-stu-id="6bebd-292">6635 (0x19EB)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-293">O log deve ter pelo menos dois contêineres para que possa ser lido ou gravado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-293">The log must have at least two containers before it can be read from or written to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**cliente de log de erros \_ \_ \_ já \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**ERROR\_LOG\_CLIENT\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-295">6636 (0x19EC)</span><span class="sxs-lookup"><span data-stu-id="6bebd-295">6636 (0x19EC)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-296">Um cliente de log já foi registrado no fluxo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-296">A log client has already registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**cliente de log de erros \_ \_ \_ não \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**ERROR\_LOG\_CLIENT\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-298">6637 (0x19ED)</span><span class="sxs-lookup"><span data-stu-id="6bebd-298">6637 (0x19ED)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-299">Um cliente de log não foi registrado no fluxo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-299">A log client has not been registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_ \_ \_ manipulador completo do log \_ de erros em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="6bebd-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**ERROR\_LOG\_FULL\_HANDLER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-301">6638 (0x19EE)</span><span class="sxs-lookup"><span data-stu-id="6bebd-301">6638 (0x19EE)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-302">Uma solicitação já foi feita para lidar com a condição completa de log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-302">A request has already been made to handle the log full condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**\_ \_ \_ falha ao ler contêiner de log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**ERROR\_LOG\_CONTAINER\_READ\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-304">6639 (0x19EF)</span><span class="sxs-lookup"><span data-stu-id="6bebd-304">6639 (0x19EF)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-305">O serviço de log encontrou um erro ao tentar ler um contêiner de log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-305">Log service encountered an error when attempting to read from a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**\_ \_ \_ falha na gravação do contêiner de log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**ERROR\_LOG\_CONTAINER\_WRITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-307">6640 (0x19F0)</span><span class="sxs-lookup"><span data-stu-id="6bebd-307">6640 (0x19F0)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-308">O serviço de log encontrou um erro ao tentar gravar em um contêiner de log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-308">Log service encountered an error when attempting to write to a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**\_ \_ \_ falha na abertura do contêiner de log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**ERROR\_LOG\_CONTAINER\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-310">6641 (0x19F1)</span><span class="sxs-lookup"><span data-stu-id="6bebd-310">6641 (0x19F1)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-311">O serviço de log encontrou um erro ao tentar abrir um contêiner de log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-311">Log service encountered an error when attempting open a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**Estado do contêiner do log de erros \_ \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**ERROR\_LOG\_CONTAINER\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-313">6642 (0x19F2)</span><span class="sxs-lookup"><span data-stu-id="6bebd-313">6642 (0x19F2)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-314">O serviço de log encontrou um estado de contêiner inválido ao tentar uma ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-314">Log service encountered an invalid container state when attempting a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**Estado do log de erros \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**ERROR\_LOG\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-316">6643 (0x19F3)</span><span class="sxs-lookup"><span data-stu-id="6bebd-316">6643 (0x19F3)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-317">O serviço de log não está no estado correto para executar uma ação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-317">Log service is not in the correct state to perform a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**LOG de erros \_ \_ fixado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**ERROR\_LOG\_PINNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-319">6644 (0x19F4)</span><span class="sxs-lookup"><span data-stu-id="6bebd-319">6644 (0x19F4)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-320">O espaço de log não pode ser recuperado porque o log está fixado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-320">Log space cannot be reclaimed because the log is pinned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_ \_ \_ falha na liberação de metadados do log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**ERROR\_LOG\_METADATA\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-322">6645 (0x19F5)</span><span class="sxs-lookup"><span data-stu-id="6bebd-322">6645 (0x19F5)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-323">Falha na liberação de metadados do log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-323">Log metadata flush failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**\_ \_ segurança inconsistente no log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**ERROR\_LOG\_INCONSISTENT\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-325">6646 (0x19F6)</span><span class="sxs-lookup"><span data-stu-id="6bebd-325">6646 (0x19F6)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-326">A segurança no log e seus contêineres são inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="6bebd-326">Security on the log and its containers is inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**\_ \_ \_ falha ao liberar o log \_ de erros**</span><span class="sxs-lookup"><span data-stu-id="6bebd-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**ERROR\_LOG\_APPENDED\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-328">6647 (0x19F7)</span><span class="sxs-lookup"><span data-stu-id="6bebd-328">6647 (0x19F7)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-329">Os registros foram anexados ao log ou as alterações de reserva foram feitas, mas o log não pôde ser liberado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-329">Records were appended to the log or reservation changes were made, but the log could not be flushed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**Reserva de log de erros \_ \_ fixa \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**ERROR\_LOG\_PINNED\_RESERVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-331">6648 (0x19F8)</span><span class="sxs-lookup"><span data-stu-id="6bebd-331">6648 (0x19F8)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-332">O log é fixado devido a uma reserva que consome a maior parte do espaço de log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-332">The log is pinned due to reservation consuming most of the log space.</span></span> <span data-ttu-id="6bebd-333">Libere alguns registros reservados para disponibilizar espaço.</span><span class="sxs-lookup"><span data-stu-id="6bebd-333">Free some reserved records to make space available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERRO \_ de \_ transação inválida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR\_INVALID\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-335">6700 (0x1A2C)</span><span class="sxs-lookup"><span data-stu-id="6bebd-335">6700 (0x1A2C)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-336">O identificador de transação associado a esta operação não é válido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-336">The transaction handle associated with this operation is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**transação de erro \_ \_ não \_ ativa**</span><span class="sxs-lookup"><span data-stu-id="6bebd-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR\_TRANSACTION\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-338">6701 (0x1A2D)</span><span class="sxs-lookup"><span data-stu-id="6bebd-338">6701 (0x1A2D)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-339">A operação solicitada foi feita no contexto de uma transação que não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="6bebd-339">The requested operation was made in the context of a transaction that is no longer active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**solicitação de transação de erro \_ \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR\_TRANSACTION\_REQUEST\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-341">6702 (0x1A2E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-341">6702 (0x1A2E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-342">A operação solicitada não é válida no objeto de transação em seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="6bebd-342">The requested operation is not valid on the Transaction object in its current state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**transação de erro \_ \_ não \_ solicitada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ERROR\_TRANSACTION\_NOT\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-344">6703 (0x1A2F)</span><span class="sxs-lookup"><span data-stu-id="6bebd-344">6703 (0x1A2F)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-345">O chamador chamou uma API de resposta, mas a resposta não é esperada porque a TM não emitiu a solicitação correspondente ao chamador.</span><span class="sxs-lookup"><span data-stu-id="6bebd-345">The caller has called a response API, but the response is not expected because the TM did not issue the corresponding request to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**transação de erro \_ \_ já \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**ERROR\_TRANSACTION\_ALREADY\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-347">6704 (0x1A30)</span><span class="sxs-lookup"><span data-stu-id="6bebd-347">6704 (0x1A30)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-348">É tarde demais para executar a operação solicitada, já que a transação já foi anulada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-348">It is too late to perform the requested operation, since the Transaction has already been aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**transação de erro \_ \_ já \_ confirmada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**ERROR\_TRANSACTION\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-350">6705 (0x1A31)</span><span class="sxs-lookup"><span data-stu-id="6bebd-350">6705 (0x1A31)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-351">É tarde demais para executar a operação solicitada, já que a transação já foi confirmada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-351">It is too late to perform the requested operation, since the Transaction has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERRO \_ de \_ inicialização de TM \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="6bebd-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR\_TM\_INITIALIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-353">6706 (0x1A32)</span><span class="sxs-lookup"><span data-stu-id="6bebd-353">6706 (0x1A32)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-354">O Gerenciador de transações não pôde ser inicializado com êxito.</span><span class="sxs-lookup"><span data-stu-id="6bebd-354">The Transaction Manager was unable to be successfully initialized.</span></span> <span data-ttu-id="6bebd-355">Não há suporte para operações transacionadas.</span><span class="sxs-lookup"><span data-stu-id="6bebd-355">Transacted operations are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERRO \_ \_ somente leitura de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR\_RESOURCEMANAGER\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-357">6707 (0x1A33)</span><span class="sxs-lookup"><span data-stu-id="6bebd-357">6707 (0x1A33)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-358">O ResourceManager especificado não fez alterações ou atualizações no recurso sob esta transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-358">The specified ResourceManager made no changes or updates to the resource under this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**transação de erro \_ \_ não \_ unida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR\_TRANSACTION\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-360">6708 (0x1A34)</span><span class="sxs-lookup"><span data-stu-id="6bebd-360">6708 (0x1A34)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-361">O Gerenciador de recursos tentou preparar uma transação que não ingressou com êxito.</span><span class="sxs-lookup"><span data-stu-id="6bebd-361">The resource manager has attempted to prepare a transaction that it has not successfully joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**a \_ transação de erro \_ superior \_ existe**</span><span class="sxs-lookup"><span data-stu-id="6bebd-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERROR\_TRANSACTION\_SUPERIOR\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-363">6709 (0x1A35)</span><span class="sxs-lookup"><span data-stu-id="6bebd-363">6709 (0x1A35)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-364">O objeto de transação já tem uma inscrição superior e o chamador tentou uma operação que teria criado um novo superior.</span><span class="sxs-lookup"><span data-stu-id="6bebd-364">The Transaction object already has a superior enlistment, and the caller attempted an operation that would have created a new superior.</span></span> <span data-ttu-id="6bebd-365">Apenas uma única inscrição superior é permitida.</span><span class="sxs-lookup"><span data-stu-id="6bebd-365">Only a single superior enlistment is allow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERRO \_ o \_ protocolo CRM \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="6bebd-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR\_CRM\_PROTOCOL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-367">6710 (0x1A36)</span><span class="sxs-lookup"><span data-stu-id="6bebd-367">6710 (0x1A36)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-368">O RM tentou registrar um protocolo que já existe.</span><span class="sxs-lookup"><span data-stu-id="6bebd-368">The RM tried to register a protocol that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**\_ \_ falha na propagação da transação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR\_TRANSACTION\_PROPAGATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-370">6711 (0x1A37)</span><span class="sxs-lookup"><span data-stu-id="6bebd-370">6711 (0x1A37)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-371">Falha na tentativa de propagar a transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-371">The attempt to propagate the Transaction failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERRO \_ do \_ protocolo CRM \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR\_CRM\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-373">6712 (0x1A38)</span><span class="sxs-lookup"><span data-stu-id="6bebd-373">6712 (0x1A38)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-374">O protocolo de propagação solicitado não foi registrado como um CRM.</span><span class="sxs-lookup"><span data-stu-id="6bebd-374">The requested propagation protocol was not registered as a CRM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**\_buffer de \_ \_ Marshall inválido de transação \_ de erro**</span><span class="sxs-lookup"><span data-stu-id="6bebd-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR\_TRANSACTION\_INVALID\_MARSHALL\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-376">6713 (0x1A39)</span><span class="sxs-lookup"><span data-stu-id="6bebd-376">6713 (0x1A39)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-377">O buffer passado para PushTransaction ou PullTransaction não está em um formato válido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-377">The buffer passed in to PushTransaction or PullTransaction is not in a valid format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**a \_ transação atual do erro \_ \_ não é \_ válida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR\_CURRENT\_TRANSACTION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-379">6714 (0x1A3A)</span><span class="sxs-lookup"><span data-stu-id="6bebd-379">6714 (0x1A3A)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-380">O contexto de transação atual associado ao thread não é um identificador válido para um objeto de transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-380">The current transaction context associated with the thread is not a valid handle to a transaction object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**transação de erro \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**ERROR\_TRANSACTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-382">6715 (0x1A3B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-382">6715 (0x1A3B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-383">Não foi possível abrir o objeto de transação especificado porque ele não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-383">The specified Transaction object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERRO \_ RESOURCEMANAGER \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR\_RESOURCEMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-385">6716 (0x1A3C)</span><span class="sxs-lookup"><span data-stu-id="6bebd-385">6716 (0x1A3C)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-386">Não foi possível abrir o objeto ResourceManager especificado, pois ele não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-386">The specified ResourceManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**inscrição de erro \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**ERROR\_ENLISTMENT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-388">6717 (0x1A3D)</span><span class="sxs-lookup"><span data-stu-id="6bebd-388">6717 (0x1A3D)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-389">Não foi possível abrir o objeto de inscrição especificado, pois ele não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-389">The specified Enlistment object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERRO de \_ TRANSacçãomanager \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-391">6718 (0x1A3E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-391">6718 (0x1A3E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-392">Não foi possível abrir o objeto TransactionManager especificado porque ele não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-392">The specified TransactionManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERRO de \_ TRANSacçãomanager \_ não \_ online**</span><span class="sxs-lookup"><span data-stu-id="6bebd-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-394">6719 (0x1A3F)</span><span class="sxs-lookup"><span data-stu-id="6bebd-394">6719 (0x1A3F)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-395">O objeto especificado não pôde ser criado ou aberto, pois seu TransactionManager associado não está online.</span><span class="sxs-lookup"><span data-stu-id="6bebd-395">The object specified could not be created or opened, because its associated TransactionManager is not online.</span></span> <span data-ttu-id="6bebd-396">O TransactionManager deve ser colocado totalmente online chamando RecoverTransactionManager para recuperar no final de seu arquivo de log antes que os objetos em seus namespaces de transação ou ResourceManager possam ser abertos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-396">The TransactionManager must be brought fully Online by calling RecoverTransactionManager to recover to the end of its LogFile before objects in its Transaction or ResourceManager namespaces can be opened.</span></span> <span data-ttu-id="6bebd-397">Além disso, os erros de gravação de registros em seu arquivo de log podem fazer com que um TransactionManager fique offline.</span><span class="sxs-lookup"><span data-stu-id="6bebd-397">In addition, errors in writing records to its LogFile can cause a TransactionManager to go offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERRO de \_ colisão de \_ nome de recuperação de transacionador \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR\_TRANSACTIONMANAGER\_RECOVERY\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-399">6720 (0x1A40)</span><span class="sxs-lookup"><span data-stu-id="6bebd-399">6720 (0x1A40)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-400">O TransactionManager especificado não pôde criar os objetos contidos em seu arquivo de log no namespace OB.</span><span class="sxs-lookup"><span data-stu-id="6bebd-400">The specified TransactionManager was unable to create the objects contained in its logfile in the Ob namespace.</span></span> <span data-ttu-id="6bebd-401">Portanto, o TransactionManager não pôde ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-401">Therefore, the TransactionManager was unable to recover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**transação de erro \_ \_ não \_ raiz**</span><span class="sxs-lookup"><span data-stu-id="6bebd-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR\_TRANSACTION\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-403">6721 (0x1A41)</span><span class="sxs-lookup"><span data-stu-id="6bebd-403">6721 (0x1A41)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-404">Não foi possível concluir a chamada para criar uma inscrição superior neste objeto de transação, pois o objeto de transação especificado para a inscrição é uma ramificação subordinada da transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-404">The call to create a superior Enlistment on this Transaction object could not be completed, because the Transaction object specified for the enlistment is a subordinate branch of the Transaction.</span></span> <span data-ttu-id="6bebd-405">Somente a raiz da transação pode ser inscrito em como uma superior.</span><span class="sxs-lookup"><span data-stu-id="6bebd-405">Only the root of the Transaction can be enlisted on as a superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**objeto de transação de erro \_ \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERROR\_TRANSACTION\_OBJECT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-407">6722 (0x1A42)</span><span class="sxs-lookup"><span data-stu-id="6bebd-407">6722 (0x1A42)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-408">Como o Gerenciador de transações associado ou o Gerenciador de recursos foi fechado, o identificador não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-408">Because the associated transaction manager or resource manager has been closed, the handle is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**resposta de transação de erro \_ \_ \_ não \_ listada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERROR\_TRANSACTION\_RESPONSE\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-410">6723 (0x1A43)</span><span class="sxs-lookup"><span data-stu-id="6bebd-410">6723 (0x1A43)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-411">A operação especificada não pôde ser executada nesta inscrição superior, pois a inscrição não foi criada com a resposta de conclusão correspondente no NotificationMask.</span><span class="sxs-lookup"><span data-stu-id="6bebd-411">The specified operation could not be performed on this Superior enlistment, because the enlistment was not created with the corresponding completion response in the NotificationMask.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**registro de transação de erro \_ \_ \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="6bebd-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**ERROR\_TRANSACTION\_RECORD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-413">6724 (0x1A44)</span><span class="sxs-lookup"><span data-stu-id="6bebd-413">6724 (0x1A44)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-414">A operação especificada não pôde ser executada, pois o registro que seria registrado era muito longo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-414">The specified operation could not be performed, because the record that would be logged was too long.</span></span> <span data-ttu-id="6bebd-415">Isso pode ocorrer devido a duas condições: há muitas inlistagens nessa transação ou a RecoveryInformation combinada que está sendo registrada em nome dessas inlistagens é muito longa.</span><span class="sxs-lookup"><span data-stu-id="6bebd-415">This can occur because of two conditions: either there are too many Enlistments on this Transaction, or the combined RecoveryInformation being logged on behalf of those Enlistments is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERRO \_ de \_ transação implícita \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="6bebd-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR\_IMPLICIT\_TRANSACTION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-417">6725 (0x1A45)</span><span class="sxs-lookup"><span data-stu-id="6bebd-417">6725 (0x1A45)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-418">Não há suporte para a transação implícita.</span><span class="sxs-lookup"><span data-stu-id="6bebd-418">Implicit transaction are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**integridade da transação de erro \_ \_ \_ violada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR\_TRANSACTION\_INTEGRITY\_VIOLATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-420">6726 (0x1A46)</span><span class="sxs-lookup"><span data-stu-id="6bebd-420">6726 (0x1A46)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-421">O Gerenciador de transações do kernel teve que anular ou esquecer a transação porque ela bloqueou o progresso.</span><span class="sxs-lookup"><span data-stu-id="6bebd-421">The kernel transaction manager had to abort or forget the transaction because it blocked forward progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERRO de \_ \_ incompatibilidade de identidade do TransactionManager \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR\_TRANSACTIONMANAGER\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-423">6727 (0x1A47)</span><span class="sxs-lookup"><span data-stu-id="6bebd-423">6727 (0x1A47)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-424">A identidade do transacionator fornecida não corresponde à que foi registrada no arquivo de log do TransactionManager.</span><span class="sxs-lookup"><span data-stu-id="6bebd-424">The TransactionManager identity that was supplied did not match the one recorded in the TransactionManager's log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERRO \_ RM \_ não pode \_ ser \_ congelado \_ para \_ instantâneo**</span><span class="sxs-lookup"><span data-stu-id="6bebd-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERROR\_RM\_CANNOT\_BE\_FROZEN\_FOR\_SNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-426">6728 (0x1A48)</span><span class="sxs-lookup"><span data-stu-id="6bebd-426">6728 (0x1A48)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-427">Esta operação de instantâneo não pode continuar porque um Gerenciador de recursos transacionais não pode ser congelado em seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="6bebd-427">This snapshot operation cannot continue because a transactional resource manager cannot be frozen in its current state.</span></span> <span data-ttu-id="6bebd-428">Tente novamente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-428">Please try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**a \_ transação de erro \_ deve \_ WRITETHROUGH**</span><span class="sxs-lookup"><span data-stu-id="6bebd-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR\_TRANSACTION\_MUST\_WRITETHROUGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-430">6729 (0x1A49)</span><span class="sxs-lookup"><span data-stu-id="6bebd-430">6729 (0x1A49)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-431">A transação não pode ser enlistada com o EnlistmentMask especificado, pois a transação já concluiu a fase de preprepare.</span><span class="sxs-lookup"><span data-stu-id="6bebd-431">The transaction cannot be enlisted on with the specified EnlistmentMask, because the transaction has already completed the PrePrepare phase.</span></span> <span data-ttu-id="6bebd-432">Para garantir a exatidão, o ResourceManager deve alternar para um modo de write-through e deixar de armazenar em cache os dados nessa transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-432">In order to ensure correctness, the ResourceManager must switch to a write- through mode and cease caching data within this transaction.</span></span> <span data-ttu-id="6bebd-433">A inscreveção para apenas fases de transação subsequentes ainda pode ter sucesso.</span><span class="sxs-lookup"><span data-stu-id="6bebd-433">Enlisting for only subsequent transaction phases may still succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**transação de erro \_ \_ não \_ superior**</span><span class="sxs-lookup"><span data-stu-id="6bebd-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR\_TRANSACTION\_NO\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-435">6730 (0x1A4A)</span><span class="sxs-lookup"><span data-stu-id="6bebd-435">6730 (0x1A4A)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-436">A transação não tem uma inscrição superior.</span><span class="sxs-lookup"><span data-stu-id="6bebd-436">The transaction does not have a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERRO \_ de \_ dano heurístico \_ possível**</span><span class="sxs-lookup"><span data-stu-id="6bebd-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERROR\_HEURISTIC\_DAMAGE\_POSSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-438">6731 (0x1A4B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-438">6731 (0x1A4B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-439">A tentativa de confirmar a transação foi concluída, mas é possível que alguma parte da árvore de transação não tenha sido confirmada com êxito devido à heurística.</span><span class="sxs-lookup"><span data-stu-id="6bebd-439">The attempt to commit the Transaction completed, but it is possible that some portion of the transaction tree did not commit successfully due to heuristics.</span></span> <span data-ttu-id="6bebd-440">Portanto, é possível que alguns dados modificados na transação possam não ter sido confirmados, resultando em inconsistência transacional.</span><span class="sxs-lookup"><span data-stu-id="6bebd-440">Therefore it is possible that some data modified in the transaction may not have committed, resulting in transactional inconsistency.</span></span> <span data-ttu-id="6bebd-441">Se possível, verifique a consistência dos dados associados.</span><span class="sxs-lookup"><span data-stu-id="6bebd-441">If possible, check the consistency of the associated data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERRO de \_ conflito TRANSacional \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR\_TRANSACTIONAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-443">6800 (0x1A90)</span><span class="sxs-lookup"><span data-stu-id="6bebd-443">6800 (0x1A90)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-444">A função tentou usar um nome que está reservado para uso por outra transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-444">The function attempted to use a name that is reserved for use by another transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERRO \_ RM \_ não \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="6bebd-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR\_RM\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-446">6801 (0x1A91)</span><span class="sxs-lookup"><span data-stu-id="6bebd-446">6801 (0x1A91)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-447">O suporte de transação no Gerenciador de recursos especificado não foi iniciado ou foi desligado devido a um erro.</span><span class="sxs-lookup"><span data-stu-id="6bebd-447">Transaction support within the specified resource manager is not started or was shut down due to an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERRO \_ de \_ metadados do RM \_ corrompidos**</span><span class="sxs-lookup"><span data-stu-id="6bebd-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR\_RM\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-449">6802 (0x1A92)</span><span class="sxs-lookup"><span data-stu-id="6bebd-449">6802 (0x1A92)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-450">Os metadados do RM foram corrompidos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-450">The metadata of the RM has been corrupted.</span></span> <span data-ttu-id="6bebd-451">O RM não funcionará.</span><span class="sxs-lookup"><span data-stu-id="6bebd-451">The RM will not function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**diretório de erros \_ \_ não \_ RM**</span><span class="sxs-lookup"><span data-stu-id="6bebd-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR\_DIRECTORY\_NOT\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-453">6803 (0x1A93)</span><span class="sxs-lookup"><span data-stu-id="6bebd-453">6803 (0x1A93)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-454">O diretório especificado não contém um Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-454">The specified directory does not contain a resource manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**transações de erro \_ \_ sem suporte \_ remoto**</span><span class="sxs-lookup"><span data-stu-id="6bebd-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**ERROR\_TRANSACTIONS\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-456">6805 (0x1A95)</span><span class="sxs-lookup"><span data-stu-id="6bebd-456">6805 (0x1A95)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-457">O servidor ou compartilhamento remoto não oferece suporte a operações de arquivo transacionadas.</span><span class="sxs-lookup"><span data-stu-id="6bebd-457">The remote server or share does not support transacted file operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**\_ \_ tamanho inválido de redimensionamento do log de \_ erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**ERROR\_LOG\_RESIZE\_INVALID\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-459">6806 (0x1A96)</span><span class="sxs-lookup"><span data-stu-id="6bebd-459">6806 (0x1A96)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-460">O tamanho de log solicitado é inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-460">The requested log size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**o \_ objeto de erro \_ não \_ \_ existe mais**</span><span class="sxs-lookup"><span data-stu-id="6bebd-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**ERROR\_OBJECT\_NO\_LONGER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-462">6807 (0x1A97)</span><span class="sxs-lookup"><span data-stu-id="6bebd-462">6807 (0x1A97)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-463">O objeto (arquivo, fluxo, link) correspondente ao identificador foi excluído por uma reversão de salvamento de transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-463">The object (file, stream, link) corresponding to the handle has been deleted by a Transaction Savepoint Rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**fluxo de erro \_ \_ miniversão \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-465">6808 (0x1A98)</span><span class="sxs-lookup"><span data-stu-id="6bebd-465">6808 (0x1A98)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-466">O arquivo especificado miniversão não foi encontrado para este arquivo transacionado aberto.</span><span class="sxs-lookup"><span data-stu-id="6bebd-466">The specified file miniversion was not found for this transacted file open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**o \_ fluxo de erro \_ miniversão \_ não é \_ válido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-468">6809 (0x1A99)</span><span class="sxs-lookup"><span data-stu-id="6bebd-468">6809 (0x1A99)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-469">O arquivo especificado miniversão foi encontrado, mas foi invalidado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-469">The specified file miniversion was found but has been invalidated.</span></span> <span data-ttu-id="6bebd-470">A causa mais provável é a reversão do salvamento de uma transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-470">Most likely cause is a transaction savepoint rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERRO \_ miniversão \_ inacessível \_ da \_ \_ transação especificada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR\_MINIVERSION\_INACCESSIBLE\_FROM\_SPECIFIED\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-472">6810 (0x1A9A)</span><span class="sxs-lookup"><span data-stu-id="6bebd-472">6810 (0x1A9A)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-473">Um miniversão só pode ser aberto no contexto da transação que o criou.</span><span class="sxs-lookup"><span data-stu-id="6bebd-473">A miniversion may only be opened in the context of the transaction that created it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERRO não é possível \_ \_ abrir \_ miniversão \_ com a \_ intenção de modificação \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR\_CANT\_OPEN\_MINIVERSION\_WITH\_MODIFY\_INTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-475">6811 (0x1A9B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-475">6811 (0x1A9B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-476">Não é possível abrir um miniversão com o acesso de modificação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-476">It is not possible to open a miniversion with modify access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERRO não é possível \_ \_ criar \_ mais \_ fluxo \_ MINIVERSIONS**</span><span class="sxs-lookup"><span data-stu-id="6bebd-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR\_CANT\_CREATE\_MORE\_STREAM\_MINIVERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-478">6812 (0x1A9C)</span><span class="sxs-lookup"><span data-stu-id="6bebd-478">6812 (0x1A9C)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-479">Não é possível criar mais miniversions para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-479">It is not possible to create any more miniversions for this stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de versão de arquivo remoto \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR\_REMOTE\_FILE\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-481">6814 (0x1A9E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-481">6814 (0x1A9E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-482">O servidor remoto enviou uma incompatibilidade de número de versão ou FID para um arquivo aberto com transações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-482">The remote server sent mismatching version number or Fid for a file opened with transactions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**o \_ identificador de erro \_ não é \_ mais \_ válido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**ERROR\_HANDLE\_NO\_LONGER\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-484">6815 (0x1A9F)</span><span class="sxs-lookup"><span data-stu-id="6bebd-484">6815 (0x1A9F)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-485">O identificador foi invalidado por uma transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-485">The handle has been invalidated by a transaction.</span></span> <span data-ttu-id="6bebd-486">A causa mais provável é a presença de mapeamento de memória em um arquivo ou um identificador aberto quando a transação foi encerrada ou revertida para o salvamento de pontos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-486">The most likely cause is the presence of memory mapping on a file or an open handle when the transaction ended or rolled back to savepoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERRO \_ nenhum \_ \_ metadado TxF**</span><span class="sxs-lookup"><span data-stu-id="6bebd-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR\_NO\_TXF\_METADATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-488">6816 (0x1AA0)</span><span class="sxs-lookup"><span data-stu-id="6bebd-488">6816 (0x1AA0)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-489">Não há nenhum metadado de transação no arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-489">There is no transaction metadata on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**corrupção do log de erros \_ \_ \_ detectada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**ERROR\_LOG\_CORRUPTION\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-491">6817 (0x1AA1)</span><span class="sxs-lookup"><span data-stu-id="6bebd-491">6817 (0x1AA1)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-492">Os dados de log estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-492">The log data is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERRO não é possível \_ \_ recuperar \_ com o \_ identificador \_ aberto**</span><span class="sxs-lookup"><span data-stu-id="6bebd-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR\_CANT\_RECOVER\_WITH\_HANDLE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-494">6818 (0x1AA2)</span><span class="sxs-lookup"><span data-stu-id="6bebd-494">6818 (0x1AA2)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-495">O arquivo não pode ser recuperado porque ainda há um identificador aberto nele.</span><span class="sxs-lookup"><span data-stu-id="6bebd-495">The file can't be recovered because there is a handle still open on it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERRO \_ RM \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR\_RM\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-497">6819 (0x1AA3)</span><span class="sxs-lookup"><span data-stu-id="6bebd-497">6819 (0x1AA3)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-498">O resultado da transação não está disponível porque o Gerenciador de recursos responsável por ele foi desconectado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-498">The transaction outcome is unavailable because the resource manager responsible for it has disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**inscrição de erro \_ \_ não \_ superior**</span><span class="sxs-lookup"><span data-stu-id="6bebd-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**ERROR\_ENLISTMENT\_NOT\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-500">6820 (0x1AA4)</span><span class="sxs-lookup"><span data-stu-id="6bebd-500">6820 (0x1AA4)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-501">A solicitação foi rejeitada porque a inscrição em questão não é uma inscrição superior.</span><span class="sxs-lookup"><span data-stu-id="6bebd-501">The request was rejected because the enlistment in question is not a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**recuperação de erro \_ \_ não \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="6bebd-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**ERROR\_RECOVERY\_NOT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-503">6821 (0x1AA5)</span><span class="sxs-lookup"><span data-stu-id="6bebd-503">6821 (0x1AA5)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-504">O Gerenciador de recursos transacionais já está consistente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-504">The transactional resource manager is already consistent.</span></span> <span data-ttu-id="6bebd-505">A recuperação não é necessária.</span><span class="sxs-lookup"><span data-stu-id="6bebd-505">Recovery is not needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**o \_ RM de erro \_ já \_ foi iniciado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR\_RM\_ALREADY\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-507">6822 (0x1AA6)</span><span class="sxs-lookup"><span data-stu-id="6bebd-507">6822 (0x1AA6)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-508">O Gerenciador de recursos transacionais já foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-508">The transactional resource manager has already been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**identidade do arquivo de erro \_ \_ \_ não \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="6bebd-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**ERROR\_FILE\_IDENTITY\_NOT\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-510">6823 (0x1AA7)</span><span class="sxs-lookup"><span data-stu-id="6bebd-510">6823 (0x1AA7)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-511">O arquivo não pode ser aberto transacionalmente, porque sua identidade depende do resultado de uma transação não resolvida.</span><span class="sxs-lookup"><span data-stu-id="6bebd-511">The file cannot be opened transactionally, because its identity depends on the outcome of an unresolved transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERRO não é possível \_ \_ interromper a \_ dependência transacional \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR\_CANT\_BREAK\_TRANSACTIONAL\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-513">6824 (0x1AA8)</span><span class="sxs-lookup"><span data-stu-id="6bebd-513">6824 (0x1AA8)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-514">A operação não pode ser executada porque outra transação está dependendo do fato de que essa propriedade não será alterada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-514">The operation cannot be performed because another transaction is depending on the fact that this property will not change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERRO não é possível \_ \_ cruzar o \_ limite do RM \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERROR\_CANT\_CROSS\_RM\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-516">6825 (0x1AA9)</span><span class="sxs-lookup"><span data-stu-id="6bebd-516">6825 (0x1AA9)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-517">A operação envolveria um único arquivo com dois gerenciadores de recursos transacionais e, portanto, não é permitida.</span><span class="sxs-lookup"><span data-stu-id="6bebd-517">The operation would involve a single file with two transactional resource managers and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERRO \_ de \_ dir do TxF \_ não \_ vazio**</span><span class="sxs-lookup"><span data-stu-id="6bebd-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR\_TXF\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-519">6826 (0x1AAA)</span><span class="sxs-lookup"><span data-stu-id="6bebd-519">6826 (0x1AAA)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-520">O diretório $Txf deve estar vazio para que essa operação tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="6bebd-520">The $Txf directory must be empty for this operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**\_existem transações INcertas de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**ERROR\_INDOUBT\_TRANSACTIONS\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-522">6827 (0x1AAB)</span><span class="sxs-lookup"><span data-stu-id="6bebd-522">6827 (0x1AAB)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-523">A operação deixaria um Gerenciador de recursos transacionais em um estado inconsistente e, portanto, não é permitida.</span><span class="sxs-lookup"><span data-stu-id="6bebd-523">The operation would leave a transactional resource manager in an inconsistent state and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERRO \_ TM \_ volátil**</span><span class="sxs-lookup"><span data-stu-id="6bebd-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR\_TM\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-525">6828 (0x1AAC)</span><span class="sxs-lookup"><span data-stu-id="6bebd-525">6828 (0x1AAC)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-526">A operação não pôde ser concluída porque o Gerenciador de transações não tem um log.</span><span class="sxs-lookup"><span data-stu-id="6bebd-526">The operation could not be completed because the transaction manager does not have a log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERRO de \_ reversão do \_ temporizador \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR\_ROLLBACK\_TIMER\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-528">6829 (0x1AAD)</span><span class="sxs-lookup"><span data-stu-id="6bebd-528">6829 (0x1AAD)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-529">Não foi possível agendar uma reversão porque uma reversão agendada anteriormente já foi executada ou foi enfileirada para execução.</span><span class="sxs-lookup"><span data-stu-id="6bebd-529">A rollback could not be scheduled because a previously scheduled rollback has already executed or been queued for execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERRO \_ de \_ atributo TxF \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERROR\_TXF\_ATTRIBUTE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-531">6830 (0x1AAE)</span><span class="sxs-lookup"><span data-stu-id="6bebd-531">6830 (0x1AAE)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-532">O atributo de metadados transacionais no arquivo ou diretório está corrompido e ilegível.</span><span class="sxs-lookup"><span data-stu-id="6bebd-532">The transactional metadata attribute on the file or directory is corrupt and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERRO \_ EFS \_ não \_ permitido \_ na \_ transação**</span><span class="sxs-lookup"><span data-stu-id="6bebd-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR\_EFS\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-534">6831 (0x1AAF)</span><span class="sxs-lookup"><span data-stu-id="6bebd-534">6831 (0x1AAF)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-535">A operação de criptografia não pôde ser concluída porque uma transação está ativa.</span><span class="sxs-lookup"><span data-stu-id="6bebd-535">The encryption operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERRO de \_ abertura TRANSacional \_ \_ não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR\_TRANSACTIONAL\_OPEN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-537">6832 (0x1AB0)</span><span class="sxs-lookup"><span data-stu-id="6bebd-537">6832 (0x1AB0)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-538">Este objeto não pode ser aberto em uma transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-538">This object is not allowed to be opened in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**\_ \_ falha no crescimento do log de erros \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**ERROR\_LOG\_GROWTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-540">6833 (0x1AB1)</span><span class="sxs-lookup"><span data-stu-id="6bebd-540">6833 (0x1AB1)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-541">Falha ao tentar criar espaço no log do Gerenciador de recursos transacionais.</span><span class="sxs-lookup"><span data-stu-id="6bebd-541">An attempt to create space in the transactional resource manager's log failed.</span></span> <span data-ttu-id="6bebd-542">O status de falha foi registrado no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-542">The failure status has been recorded in the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERRO de \_ mapeamento transacionado \_ \_ sem suporte \_ remoto**</span><span class="sxs-lookup"><span data-stu-id="6bebd-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR\_TRANSACTED\_MAPPING\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-544">6834 (0x1AB2)</span><span class="sxs-lookup"><span data-stu-id="6bebd-544">6834 (0x1AB2)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-545">Não há suporte para o mapeamento de memória (criando uma seção mapeada) de um arquivo remoto em uma transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-545">Memory mapping (creating a mapped section) a remote file under a transaction is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**os \_ metadados TxF de erro \_ \_ já estão \_ presentes**</span><span class="sxs-lookup"><span data-stu-id="6bebd-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERROR\_TXF\_METADATA\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-547">6835 (0x1AB3)</span><span class="sxs-lookup"><span data-stu-id="6bebd-547">6835 (0x1AB3)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-548">Os metadados da transação já estão presentes neste arquivo e não podem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-548">Transaction metadata is already present on this file and cannot be superseded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERRO \_ de \_ retornos de chamada de escopo de transação \_ \_ não \_ definido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR\_TRANSACTION\_SCOPE\_CALLBACKS\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-550">6836 (0x1AB4)</span><span class="sxs-lookup"><span data-stu-id="6bebd-550">6836 (0x1AB4)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-551">Não foi possível inserir um escopo de transação porque o manipulador de escopo não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-551">A transaction scope could not be entered because the scope handler has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**\_ \_ promoção necessária da transação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**ERROR\_TRANSACTION\_REQUIRED\_PROMOTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-553">6837 (0x1AB5)</span><span class="sxs-lookup"><span data-stu-id="6bebd-553">6837 (0x1AB5)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-554">A promoção era necessária para permitir que o Gerenciador de recursos se inscreva, mas a transação foi definida para não permitir.</span><span class="sxs-lookup"><span data-stu-id="6bebd-554">Promotion was required in order to allow the resource manager to enlist, but the transaction was set to disallow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERRO \_ não é possível \_ executar o \_ arquivo \_ na \_ transação**</span><span class="sxs-lookup"><span data-stu-id="6bebd-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR\_CANNOT\_EXECUTE\_FILE\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-556">6838 (0x1AB6)</span><span class="sxs-lookup"><span data-stu-id="6bebd-556">6838 (0x1AB6)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-557">Este arquivo está aberto para modificação em uma transação não resolvida e pode ser aberto para execução somente por um leitor transacionado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-557">This file is open for modification in an unresolved transaction and may be opened for execute only by a transacted reader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**transações de erro \_ \_ não \_ congeladas**</span><span class="sxs-lookup"><span data-stu-id="6bebd-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ERROR\_TRANSACTIONS\_NOT\_FROZEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-559">6839 (0x1AB7)</span><span class="sxs-lookup"><span data-stu-id="6bebd-559">6839 (0x1AB7)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-560">A solicitação para descongelar transações congeladas foi ignorada porque as transações não tinham sido congeladas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-560">The request to thaw frozen transactions was ignored because transactions had not previously been frozen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERRO \_ ao \_ congelar transação \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="6bebd-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR\_TRANSACTION\_FREEZE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-562">6840 (0x1AB8)</span><span class="sxs-lookup"><span data-stu-id="6bebd-562">6840 (0x1AB8)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-563">As transações não podem ser congeladas porque um congelamento já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-563">Transactions cannot be frozen because a freeze is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERRO \_ não \_ volume de instantâneo \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR\_NOT\_SNAPSHOT\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-565">6841 (0x1AB9)</span><span class="sxs-lookup"><span data-stu-id="6bebd-565">6841 (0x1AB9)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-566">O volume de destino não é um volume de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-566">The target volume is not a snapshot volume.</span></span> <span data-ttu-id="6bebd-567">Esta operação só é válida em um volume montado como um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-567">This operation is only valid on a volume mounted as a snapshot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERRO \_ sem \_ pontos \_ de salvamento com \_ \_ arquivos abertos**</span><span class="sxs-lookup"><span data-stu-id="6bebd-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR\_NO\_SAVEPOINT\_WITH\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-569">6842 (0x1ABA)</span><span class="sxs-lookup"><span data-stu-id="6bebd-569">6842 (0x1ABA)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-570">A operação de salvamento falhou porque os arquivos estão abertos na transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-570">The savepoint operation failed because files are open on the transaction.</span></span> <span data-ttu-id="6bebd-571">Isso não é permitido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-571">This is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**reparo de dados de erro \_ \_ perdido \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERROR\_DATA\_LOST\_REPAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-573">6843 (0x1ABB)</span><span class="sxs-lookup"><span data-stu-id="6bebd-573">6843 (0x1ABB)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-574">O Windows descobriu corrupção em um arquivo e esse arquivo foi reparado desde então.</span><span class="sxs-lookup"><span data-stu-id="6bebd-574">Windows has discovered corruption in a file, and that file has since been repaired.</span></span> <span data-ttu-id="6bebd-575">Pode ter ocorrido perda de dados.</span><span class="sxs-lookup"><span data-stu-id="6bebd-575">Data loss may have occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERRO \_ esparso \_ não \_ permitido \_ na \_ transação**</span><span class="sxs-lookup"><span data-stu-id="6bebd-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR\_SPARSE\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-577">6844 (0x1ABC)</span><span class="sxs-lookup"><span data-stu-id="6bebd-577">6844 (0x1ABC)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-578">A operação esparsa não pôde ser concluída porque uma transação está ativa no arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-578">The sparse operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**incompatibilidade de \_ identidade TM de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR\_TM\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-580">6845 (0x1ABD)</span><span class="sxs-lookup"><span data-stu-id="6bebd-580">6845 (0x1ABD)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-581">Falha na chamada para criar um objeto TransactionManager porque a identidade TM armazenada no arquivo de log não corresponde à identidade de TM que foi passada como um argumento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-581">The call to create a TransactionManager object failed because the Tm Identity stored in the logfile does not match the Tm Identity that was passed in as an argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERRO na \_ \_ seção flutuante**</span><span class="sxs-lookup"><span data-stu-id="6bebd-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR\_FLOATED\_SECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-583">6846 (0x1ABE)</span><span class="sxs-lookup"><span data-stu-id="6bebd-583">6846 (0x1ABE)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-584">Houve uma tentativa de e/s em um objeto de seção que foi flutuado como resultado de uma transação terminando.</span><span class="sxs-lookup"><span data-stu-id="6bebd-584">I/O was attempted on a section object that has been floated as a result of a transaction ending.</span></span> <span data-ttu-id="6bebd-585">Não há dados válidos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-585">There is no valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERRO \_ não é possível \_ aceitar \_ trabalho transacionado \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR\_CANNOT\_ACCEPT\_TRANSACTED\_WORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-587">6847 (0x1ABF)</span><span class="sxs-lookup"><span data-stu-id="6bebd-587">6847 (0x1ABF)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-588">Atualmente, o Gerenciador de recursos transacionais não pode aceitar o trabalho de transação devido a uma condição transitória, como baixa de recursos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-588">The transactional resource manager cannot currently accept transacted work due to a transient condition such as low resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERRO \_ não é possível \_ anular \_ Transações**</span><span class="sxs-lookup"><span data-stu-id="6bebd-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR\_CANNOT\_ABORT\_TRANSACTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-590">6848 (0x1AC0)</span><span class="sxs-lookup"><span data-stu-id="6bebd-590">6848 (0x1AC0)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-591">O Gerenciador de recursos transacionais tinha muitos transações pendentes que não puderam ser anulados.</span><span class="sxs-lookup"><span data-stu-id="6bebd-591">The transactional resource manager had too many tranactions outstanding that could not be aborted.</span></span> <span data-ttu-id="6bebd-592">O Gerenciador de recursos transacionais foi desligado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-592">The transactional resource manger has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROS \_ de \_ clusters inválidos**</span><span class="sxs-lookup"><span data-stu-id="6bebd-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR\_BAD\_CLUSTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-594">6849 (0x1AC1)</span><span class="sxs-lookup"><span data-stu-id="6bebd-594">6849 (0x1AC1)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-595">A operação não pôde ser concluída devido a clusters inválidos no disco.</span><span class="sxs-lookup"><span data-stu-id="6bebd-595">The operation could not be completed due to bad clusters on disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_compactação \_ de erro não \_ permitida \_ na \_ transação**</span><span class="sxs-lookup"><span data-stu-id="6bebd-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**ERROR\_COMPRESSION\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-597">6850 (0x1AC2)</span><span class="sxs-lookup"><span data-stu-id="6bebd-597">6850 (0x1AC2)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-598">Não foi possível concluir a operação de compactação porque uma transação está ativa no arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-598">The compression operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERRO de \_ volume \_ sujo**</span><span class="sxs-lookup"><span data-stu-id="6bebd-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR\_VOLUME\_DIRTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-600">6851 (0x1AC3)</span><span class="sxs-lookup"><span data-stu-id="6bebd-600">6851 (0x1AC3)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-601">A operação não pôde ser concluída porque o volume está sujo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-601">The operation could not be completed because the volume is dirty.</span></span> <span data-ttu-id="6bebd-602">Execute Chkdsk e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-602">Please run chkdsk and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERRO \_ sem \_ \_ rastreamento \_ de link na \_ transação**</span><span class="sxs-lookup"><span data-stu-id="6bebd-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR\_NO\_LINK\_TRACKING\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-604">6852 (0x1AC4)</span><span class="sxs-lookup"><span data-stu-id="6bebd-604">6852 (0x1AC4)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-605">A operação de rastreamento de link não pôde ser concluída porque uma transação está ativa.</span><span class="sxs-lookup"><span data-stu-id="6bebd-605">The link tracking operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_operação \_ de erro sem \_ suporte \_ na \_ transação**</span><span class="sxs-lookup"><span data-stu-id="6bebd-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**ERROR\_OPERATION\_NOT\_SUPPORTED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-607">6853 (0x1AC5)</span><span class="sxs-lookup"><span data-stu-id="6bebd-607">6853 (0x1AC5)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-608">Esta operação não pode ser executada em uma transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-608">This operation cannot be performed in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**identificador de erro \_ expirado \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERROR\_EXPIRED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-610">6854 (0x1AC6)</span><span class="sxs-lookup"><span data-stu-id="6bebd-610">6854 (0x1AC6)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-611">O identificador não está mais corretamente associado à sua transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-611">The handle is no longer properly associated with its transaction.</span></span> <span data-ttu-id="6bebd-612">Ele pode ter sido aberto em um Gerenciador de recursos transacionais que foi subsequentemente forçado a reiniciar.</span><span class="sxs-lookup"><span data-stu-id="6bebd-612">It may have been opened in a transactional resource manager that was subsequently forced to restart.</span></span> <span data-ttu-id="6bebd-613">Feche a alça e abra uma nova.</span><span class="sxs-lookup"><span data-stu-id="6bebd-613">Please close the handle and open a new one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**transação de erro \_ \_ não \_ listada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ERROR\_TRANSACTION\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-615">6855 (0x1AC7)</span><span class="sxs-lookup"><span data-stu-id="6bebd-615">6855 (0x1AC7)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-616">A operação especificada não pôde ser executada porque o Gerenciador de recursos não está inscrito na transação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-616">The specified operation could not be performed because the resource manager is not enlisted in the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERRO \_ CTX \_ WINSTATION \_ nome \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR\_CTX\_WINSTATION\_NAME\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-618">7001 (0x1B59)</span><span class="sxs-lookup"><span data-stu-id="6bebd-618">7001 (0x1B59)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-619">O nome de sessão especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-619">The specified session name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERRO \_ CTX \_ \_ PD inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR\_CTX\_INVALID\_PD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-621">7002 (0x1B5A)</span><span class="sxs-lookup"><span data-stu-id="6bebd-621">7002 (0x1B5A)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-622">O driver de protocolo especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-622">The specified protocol driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERRO \_ CTX \_ PD \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR\_CTX\_PD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-624">7003 (0x1B5B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-624">7003 (0x1B5B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-625">O driver de protocolo especificado não foi encontrado no caminho do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-625">The specified protocol driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERRO \_ CTX \_ WD \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR\_CTX\_WD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-627">7004 (0x1B5C)</span><span class="sxs-lookup"><span data-stu-id="6bebd-627">7004 (0x1B5C)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-628">O driver de conexão de terminal especificado não foi encontrado no caminho do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-628">The specified terminal connection driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERRO \_ CTX \_ não é possível \_ criar a \_ entrada de EventLog \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR\_CTX\_CANNOT\_MAKE\_EVENTLOG\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-630">7005 (0x1B5D)</span><span class="sxs-lookup"><span data-stu-id="6bebd-630">7005 (0x1B5D)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-631">Não foi possível criar uma chave do registro para o log de eventos para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="6bebd-631">A registry key for event logging could not be created for this session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERRO \_ de \_ \_ colisão de nome de serviço CTX \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR\_CTX\_SERVICE\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-633">7006 (0x1B5E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-633">7006 (0x1B5E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-634">Já existe um serviço com o mesmo nome no sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-634">A service with the same name already exists on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERRO \_ CTX \_ fechar \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="6bebd-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR\_CTX\_CLOSE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-636">7007 (0x1B5F)</span><span class="sxs-lookup"><span data-stu-id="6bebd-636">7007 (0x1B5F)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-637">Uma operação de fechamento está pendente na sessão.</span><span class="sxs-lookup"><span data-stu-id="6bebd-637">A close operation is pending on the session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERRO \_ CTX \_ \_ OUTBUF**</span><span class="sxs-lookup"><span data-stu-id="6bebd-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR\_CTX\_NO\_OUTBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-639">7008 (0x1B60)</span><span class="sxs-lookup"><span data-stu-id="6bebd-639">7008 (0x1B60)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-640">Não há buffers de saída livres disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6bebd-640">There are no free output buffers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERRO \_ CTX de \_ modem \_ inf \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR\_CTX\_MODEM\_INF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-642">7009 (0x1B61)</span><span class="sxs-lookup"><span data-stu-id="6bebd-642">7009 (0x1B61)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-643">O MODEM. O arquivo INF não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-643">The MODEM.INF file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERRO de \_ CTX de \_ \_ modem inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR\_CTX\_INVALID\_MODEMNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-645">7010 (0x1B62)</span><span class="sxs-lookup"><span data-stu-id="6bebd-645">7010 (0x1B62)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-646">O nome do modem não foi encontrado em MODEM. INF.</span><span class="sxs-lookup"><span data-stu-id="6bebd-646">The modem name was not found in MODEM.INF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**erro \_ CTX \_ \_ erro de resposta do modem \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-648">7011 (0x1B63)</span><span class="sxs-lookup"><span data-stu-id="6bebd-648">7011 (0x1B63)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-649">O modem não aceitou o comando enviado a ele.</span><span class="sxs-lookup"><span data-stu-id="6bebd-649">The modem did not accept the command sent to it.</span></span> <span data-ttu-id="6bebd-650">Verifique se o nome do modem configurado corresponde ao modem conectado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-650">Verify that the configured modem name matches the attached modem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERRO \_ CTX \_ \_ tempo limite de resposta de modem \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-652">7012 (0x1B64)</span><span class="sxs-lookup"><span data-stu-id="6bebd-652">7012 (0x1B64)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-653">O modem não respondeu ao comando enviado a ele.</span><span class="sxs-lookup"><span data-stu-id="6bebd-653">The modem did not respond to the command sent to it.</span></span> <span data-ttu-id="6bebd-654">Verifique se o modem está corretamente conectado e ligado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-654">Verify that the modem is properly cabled and powered on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERRO \_ CTX \_ resposta de modem \_ \_ sem \_ portadora**</span><span class="sxs-lookup"><span data-stu-id="6bebd-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_CARRIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-656">7013 (0x1B65)</span><span class="sxs-lookup"><span data-stu-id="6bebd-656">7013 (0x1B65)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-657">A detecção da operadora falhou ou a portadora foi descartada devido à desconexão.</span><span class="sxs-lookup"><span data-stu-id="6bebd-657">Carrier detect has failed or carrier has been dropped due to disconnect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERRO \_ CTX \_ resposta do modem \_ \_ sem \_ Tom de sinal de**</span><span class="sxs-lookup"><span data-stu-id="6bebd-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-659">7014 (0x1B66)</span><span class="sxs-lookup"><span data-stu-id="6bebd-659">7014 (0x1B66)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-660">Tom de discagem não detectado dentro do tempo necessário.</span><span class="sxs-lookup"><span data-stu-id="6bebd-660">Dial tone not detected within the required time.</span></span> <span data-ttu-id="6bebd-661">Verifique se o cabo do telefone está corretamente conectado e funcional.</span><span class="sxs-lookup"><span data-stu-id="6bebd-661">Verify that the phone cable is properly attached and functional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERRO \_ CTX \_ resposta de modem \_ \_ ocupada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-663">7015 (0x1B67)</span><span class="sxs-lookup"><span data-stu-id="6bebd-663">7015 (0x1B67)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-664">Sinal de ocupado detectado no site remoto no retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-664">Busy signal detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERRO \_ CTX \_ de \_ resposta de modem \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-666">7016 (0x1B68)</span><span class="sxs-lookup"><span data-stu-id="6bebd-666">7016 (0x1B68)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-667">Voz detectada no site remoto no retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-667">Voice detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**erro \_ CTX erro \_ td \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERROR\_CTX\_TD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-669">7017 (0x1B69)</span><span class="sxs-lookup"><span data-stu-id="6bebd-669">7017 (0x1B69)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-670">Erro do driver de transporte.</span><span class="sxs-lookup"><span data-stu-id="6bebd-670">Transport driver error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERRO \_ CTX \_ WINSTATION \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR\_CTX\_WINSTATION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-672">7022 (0x1B6E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-672">7022 (0x1B6E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-673">Não é possível encontrar a sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-673">The specified session cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERRO \_ CTX \_ WINSTATION \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="6bebd-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERROR\_CTX\_WINSTATION\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-675">7023 (0x1B6F)</span><span class="sxs-lookup"><span data-stu-id="6bebd-675">7023 (0x1B6F)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-676">O nome de sessão especificado já está em uso.</span><span class="sxs-lookup"><span data-stu-id="6bebd-676">The specified session name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERRO \_ CTX \_ WINSTATION \_ Busy**</span><span class="sxs-lookup"><span data-stu-id="6bebd-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR\_CTX\_WINSTATION\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-678">7024 (0x1B70)</span><span class="sxs-lookup"><span data-stu-id="6bebd-678">7024 (0x1B70)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-679">A tarefa que você está tentando fazer não pode ser concluída porque Serviços de Área de Trabalho Remota está ocupada no momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-679">The task you are trying to do can't be completed because Remote Desktop Services is currently busy.</span></span> <span data-ttu-id="6bebd-680">Tente novamente em alguns minutos.</span><span class="sxs-lookup"><span data-stu-id="6bebd-680">Please try again in a few minutes.</span></span> <span data-ttu-id="6bebd-681">Outros usuários ainda devem ser capazes de fazer logon.</span><span class="sxs-lookup"><span data-stu-id="6bebd-681">Other users should still be able to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERRO \_ CTX \_ \_ modo de vídeo defeituoso \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR\_CTX\_BAD\_VIDEO\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-683">7025 (0x1B71)</span><span class="sxs-lookup"><span data-stu-id="6bebd-683">7025 (0x1B71)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-684">Foi feita uma tentativa de conexão a uma sessão cujo modo de vídeo não é suportado pelo cliente atual.</span><span class="sxs-lookup"><span data-stu-id="6bebd-684">An attempt has been made to connect to a session whose video mode is not supported by the current client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERRO \_ CTX \_ gráficos \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR\_CTX\_GRAPHICS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-686">7035 (0x1B7B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-686">7035 (0x1B7B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-687">O aplicativo tentou habilitar o modo gráfico do DOS.</span><span class="sxs-lookup"><span data-stu-id="6bebd-687">The application attempted to enable DOS graphics mode.</span></span> <span data-ttu-id="6bebd-688">Não há suporte para o modo gráfico do DOS.</span><span class="sxs-lookup"><span data-stu-id="6bebd-688">DOS graphics mode is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERRO \_ CTX \_ logon \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR\_CTX\_LOGON\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-690">7037 (0x1B7D)</span><span class="sxs-lookup"><span data-stu-id="6bebd-690">7037 (0x1B7D)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-691">O privilégio de logon interativo foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-691">Your interactive logon privilege has been disabled.</span></span> <span data-ttu-id="6bebd-692">Contate o administrador.</span><span class="sxs-lookup"><span data-stu-id="6bebd-692">Please contact your administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERRO \_ CTX \_ não \_ console**</span><span class="sxs-lookup"><span data-stu-id="6bebd-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR\_CTX\_NOT\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-694">7038 (0x1B7E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-694">7038 (0x1B7E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-695">A operação solicitada pode ser executada somente no console do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-695">The requested operation can be performed only on the system console.</span></span> <span data-ttu-id="6bebd-696">Isso é geralmente o resultado de um driver ou DLL do sistema que requer acesso direto ao console.</span><span class="sxs-lookup"><span data-stu-id="6bebd-696">This is most often the result of a driver or system DLL requiring direct console access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERRO \_ CTX \_ \_ tempo limite de consulta do cliente \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR\_CTX\_CLIENT\_QUERY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-698">7040 (0x1B80)</span><span class="sxs-lookup"><span data-stu-id="6bebd-698">7040 (0x1B80)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-699">Falha do cliente ao responder à mensagem de conexão do servidor.</span><span class="sxs-lookup"><span data-stu-id="6bebd-699">The client failed to respond to the server connect message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERRO \_ CTX \_ \_ desconexão do console**</span><span class="sxs-lookup"><span data-stu-id="6bebd-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR\_CTX\_CONSOLE\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-701">7041 (0x1B81)</span><span class="sxs-lookup"><span data-stu-id="6bebd-701">7041 (0x1B81)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-702">Não há suporte para a desconexão da sessão de console.</span><span class="sxs-lookup"><span data-stu-id="6bebd-702">Disconnecting the console session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERRO \_ CTX \_ console \_ Connect**</span><span class="sxs-lookup"><span data-stu-id="6bebd-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR\_CTX\_CONSOLE\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-704">7042 (0x1B82)</span><span class="sxs-lookup"><span data-stu-id="6bebd-704">7042 (0x1B82)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-705">Não há suporte para a reconexão de uma sessão desconectada ao console.</span><span class="sxs-lookup"><span data-stu-id="6bebd-705">Reconnecting a disconnected session to the console is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERRO de \_ CTX de \_ sombra \_ negado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR\_CTX\_SHADOW\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-707">7044 (0x1B84)</span><span class="sxs-lookup"><span data-stu-id="6bebd-707">7044 (0x1B84)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-708">A solicitação para controlar outra sessão remotamente foi negada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-708">The request to control another session remotely was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERRO \_ CTX \_ WINSTATION \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR\_CTX\_WINSTATION\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-710">7045 (0x1B85)</span><span class="sxs-lookup"><span data-stu-id="6bebd-710">7045 (0x1B85)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-711">O acesso à sessão solicitado foi negado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-711">The requested session access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERRO \_ CTX \_ com \_ WD inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR\_CTX\_INVALID\_WD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-713">7049 (0x1B89)</span><span class="sxs-lookup"><span data-stu-id="6bebd-713">7049 (0x1B89)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-714">O driver de conexão de terminal especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-714">The specified terminal connection driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERRO \_ de \_ sombra de CTX \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR\_CTX\_SHADOW\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-716">7050 (0x1B8A)</span><span class="sxs-lookup"><span data-stu-id="6bebd-716">7050 (0x1B8A)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-717">A sessão solicitada não pode ser controlada remotamente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-717">The requested session cannot be controlled remotely.</span></span> <span data-ttu-id="6bebd-718">Isso pode ocorrer porque a sessão está desconectada ou não tem um usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-718">This may be because the session is disconnected or does not currently have a user logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERRO \_ de \_ sombra de CTX \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR\_CTX\_SHADOW\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-720">7051 (0x1B8B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-720">7051 (0x1B8B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-721">A sessão solicitada não está configurada para permitir o controle remoto.</span><span class="sxs-lookup"><span data-stu-id="6bebd-721">The requested session is not configured to allow remote control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERRO \_ CTX \_ \_ licença \_ de cliente em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="6bebd-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-723">7052 (0x1B8C)</span><span class="sxs-lookup"><span data-stu-id="6bebd-723">7052 (0x1B8C)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-724">Sua solicitação para se conectar a este Terminal Server foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-724">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="6bebd-725">Seu número de licença de cliente do Terminal Server está sendo usado por outro usuário no momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-725">Your Terminal Server client license number is currently being used by another user.</span></span> <span data-ttu-id="6bebd-726">Entre em contato com o administrador do sistema para obter um número de licença exclusivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-726">Please call your system administrator to obtain a unique license number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERRO \_ CTX \_ licença de cliente \_ \_ não \_ definida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-728">7053 (0x1B8D)</span><span class="sxs-lookup"><span data-stu-id="6bebd-728">7053 (0x1B8D)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-729">Sua solicitação para se conectar a este Terminal Server foi rejeitada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-729">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="6bebd-730">Seu número de licença de cliente Terminal Server não foi inserido para esta cópia do cliente de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="6bebd-730">Your Terminal Server client license number has not been entered for this copy of the Terminal Server client.</span></span> <span data-ttu-id="6bebd-731">Entre em contato com o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-731">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**a \_ licença CTX de erro \_ \_ não \_ está disponível**</span><span class="sxs-lookup"><span data-stu-id="6bebd-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR\_CTX\_LICENSE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-733">7054 (0x1B8E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-733">7054 (0x1B8E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-734">O número de conexões a este computador é limitado e todas as conexões estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-734">The number of connections to this computer is limited and all connections are in use right now.</span></span> <span data-ttu-id="6bebd-735">Tente se conectar mais tarde ou contate o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-735">Try connecting later or contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERRO \_ de \_ cliente de licença CTX \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6bebd-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR\_CTX\_LICENSE\_CLIENT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-737">7055 (0x1B8F)</span><span class="sxs-lookup"><span data-stu-id="6bebd-737">7055 (0x1B8F)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-738">O cliente que você está usando não está licenciado para usar este sistema.</span><span class="sxs-lookup"><span data-stu-id="6bebd-738">The client you are using is not licensed to use this system.</span></span> <span data-ttu-id="6bebd-739">Sua solicitação de logon foi negada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-739">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERRO \_ CTX \_ licença \_ expirada**</span><span class="sxs-lookup"><span data-stu-id="6bebd-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR\_CTX\_LICENSE\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-741">7056 (0x1B90)</span><span class="sxs-lookup"><span data-stu-id="6bebd-741">7056 (0x1B90)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-742">A licença do sistema expirou.</span><span class="sxs-lookup"><span data-stu-id="6bebd-742">The system license has expired.</span></span> <span data-ttu-id="6bebd-743">Sua solicitação de logon foi negada.</span><span class="sxs-lookup"><span data-stu-id="6bebd-743">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERRO \_ CTX \_ sombra \_ não \_ está em execução**</span><span class="sxs-lookup"><span data-stu-id="6bebd-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR\_CTX\_SHADOW\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-745">7057 (0x1B91)</span><span class="sxs-lookup"><span data-stu-id="6bebd-745">7057 (0x1B91)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-746">O controle remoto não pôde ser encerrado porque a sessão especificada não está sendo controlada remotamente no momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-746">Remote control could not be terminated because the specified session is not currently being remotely controlled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERRO \_ CTX \_ sombra \_ encerrada \_ por \_ alteração de modo \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR\_CTX\_SHADOW\_ENDED\_BY\_MODE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-748">7058 (0x1B92)</span><span class="sxs-lookup"><span data-stu-id="6bebd-748">7058 (0x1B92)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-749">O controle remoto do console foi encerrado porque o modo de exibição foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-749">The remote control of the console was terminated because the display mode was changed.</span></span> <span data-ttu-id="6bebd-750">Não há suporte para a alteração do modo de exibição em uma sessão de controle remoto.</span><span class="sxs-lookup"><span data-stu-id="6bebd-750">Changing the display mode in a remote control session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**contagem de ativação de erro \_ \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="6bebd-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**ERROR\_ACTIVATION\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-752">7059 (0x1B93)</span><span class="sxs-lookup"><span data-stu-id="6bebd-752">7059 (0x1B93)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-753">A ativação já foi redefinida para o número máximo de vezes para essa instalação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-753">Activation has already been reset the maximum number of times for this installation.</span></span> <span data-ttu-id="6bebd-754">Seu temporizador de ativação não será limpo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-754">Your activation timer will not be cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERRO \_ CTX \_ WINSTATIONS \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR\_CTX\_WINSTATIONS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-756">7060 (0x1B94)</span><span class="sxs-lookup"><span data-stu-id="6bebd-756">7060 (0x1B94)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-757">Os logons remotos estão desabilitados no momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-757">Remote logins are currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERRO \_ CTX \_ nível de criptografia \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="6bebd-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR\_CTX\_ENCRYPTION\_LEVEL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-759">7061 (0x1B95)</span><span class="sxs-lookup"><span data-stu-id="6bebd-759">7061 (0x1B95)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-760">Você não tem o nível de criptografia adequado para acessar esta sessão.</span><span class="sxs-lookup"><span data-stu-id="6bebd-760">You do not have the proper encryption level to access this Session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERRO \_ \_ de sessão CTX \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="6bebd-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR\_CTX\_SESSION\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-762">7062 (0x1B96)</span><span class="sxs-lookup"><span data-stu-id="6bebd-762">7062 (0x1B96)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-763">O usuário% s \\ \\ % s está conectado atualmente a este computador.</span><span class="sxs-lookup"><span data-stu-id="6bebd-763">The user %s\\\\%s is currently logged on to this computer.</span></span> <span data-ttu-id="6bebd-764">Somente o usuário atual ou um administrador pode fazer logon neste computador.</span><span class="sxs-lookup"><span data-stu-id="6bebd-764">Only the current user or an administrator can log on to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERRO \_ CTX \_ não \_ forçar \_ logoff**</span><span class="sxs-lookup"><span data-stu-id="6bebd-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR\_CTX\_NO\_FORCE\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-766">7063 (0x1B97)</span><span class="sxs-lookup"><span data-stu-id="6bebd-766">7063 (0x1B97)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-767">O usuário% s \\ \\ % s já está conectado ao console deste computador.</span><span class="sxs-lookup"><span data-stu-id="6bebd-767">The user %s\\\\%s is already logged on to the console of this computer.</span></span> <span data-ttu-id="6bebd-768">Você não tem permissão para fazer logon neste momento.</span><span class="sxs-lookup"><span data-stu-id="6bebd-768">You do not have permission to log in at this time.</span></span> <span data-ttu-id="6bebd-769">Para resolver esse problema, entre em contato com% s \\ \\ % s e faça logoff.</span><span class="sxs-lookup"><span data-stu-id="6bebd-769">To resolve this issue, contact %s\\\\%s and have them log off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERRO \_ de \_ restrição de conta do CTX \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR\_CTX\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-771">7064 (0x1B98)</span><span class="sxs-lookup"><span data-stu-id="6bebd-771">7064 (0x1B98)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-772">Não é possível fazer logon devido a uma restrição de conta.</span><span class="sxs-lookup"><span data-stu-id="6bebd-772">Unable to log you on because of an account restriction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**erro \_ de \_ erro de protocolo RDP \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERROR\_RDP\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-774">7065 (0x1B99)</span><span class="sxs-lookup"><span data-stu-id="6bebd-774">7065 (0x1B99)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-775">O componente de protocolo RDP %2 detectou um erro no fluxo de protocolo e desconectou o cliente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-775">The RDP protocol component %2 detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERRO \_ CTX \_ CDM \_ Connect**</span><span class="sxs-lookup"><span data-stu-id="6bebd-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR\_CTX\_CDM\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-777">7066 (0x1B9A)</span><span class="sxs-lookup"><span data-stu-id="6bebd-777">7066 (0x1B9A)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-778">O serviço de mapeamento de unidade de cliente conectou-se à conexão de terminal.</span><span class="sxs-lookup"><span data-stu-id="6bebd-778">The Client Drive Mapping Service Has Connected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERRO \_ CTX \_ CDM \_ Disconnect**</span><span class="sxs-lookup"><span data-stu-id="6bebd-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR\_CTX\_CDM\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-780">7067 (0x1B9B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-780">7067 (0x1B9B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-781">O serviço de mapeamento de unidade do cliente foi desconectado da conexão de terminal.</span><span class="sxs-lookup"><span data-stu-id="6bebd-781">The Client Drive Mapping Service Has Disconnected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**erro de erro de \_ \_ camada de segurança CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERROR\_CTX\_SECURITY\_LAYER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-783">7068 (0x1B9C)</span><span class="sxs-lookup"><span data-stu-id="6bebd-783">7068 (0x1B9C)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-784">A camada de segurança Terminal Server detectou um erro no fluxo de protocolo e desconectou o cliente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-784">The Terminal Server security layer detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERRO \_ de \_ sessões TS incompatíveis \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR\_TS\_INCOMPATIBLE\_SESSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-786">7069 (0x1B9D)</span><span class="sxs-lookup"><span data-stu-id="6bebd-786">7069 (0x1B9D)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-787">A sessão de destino é incompatível com a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6bebd-787">The target session is incompatible with the current session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**erro erro de \_ \_ \_ subsistema de vídeo TS \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR\_TS\_VIDEO\_SUBSYSTEM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-789">7070 (0x1B9E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-789">7070 (0x1B9E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-790">O Windows não pode se conectar à sua sessão porque ocorreu um problema no subsistema de vídeo do Windows.</span><span class="sxs-lookup"><span data-stu-id="6bebd-790">Windows can't connect to your session because a problem occurred in the Windows video subsystem.</span></span> <span data-ttu-id="6bebd-791">Tente se conectar novamente mais tarde ou contate o administrador do servidor para obter assistência.</span><span class="sxs-lookup"><span data-stu-id="6bebd-791">Try connecting again later, or contact the server administrator for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**sequência de API de erro do FRS \_ \_ inválida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS\_ERR\_INVALID\_API\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-793">8001 (0x1F41)</span><span class="sxs-lookup"><span data-stu-id="6bebd-793">8001 (0x1F41)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-794">A API do serviço de replicação de arquivo foi chamada incorretamente.</span><span class="sxs-lookup"><span data-stu-id="6bebd-794">The file replication service API was called incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**\_serviço de \_ inicialização de erro do FRS \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS\_ERR\_STARTING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-796">8002 (0x1F42)</span><span class="sxs-lookup"><span data-stu-id="6bebd-796">8002 (0x1F42)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-797">Não é possível iniciar o serviço de replicação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6bebd-797">The file replication service cannot be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**erro do FRS ao \_ \_ parar o \_ serviço**</span><span class="sxs-lookup"><span data-stu-id="6bebd-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS\_ERR\_STOPPING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-799">8003 (0x1F43)</span><span class="sxs-lookup"><span data-stu-id="6bebd-799">8003 (0x1F43)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-800">O serviço de replicação de arquivo não pode ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-800">The file replication service cannot be stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ API interna de erro do FRS \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS\_ERR\_INTERNAL\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-802">8004 (0x1F44)</span><span class="sxs-lookup"><span data-stu-id="6bebd-802">8004 (0x1F44)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-803">A API do serviço de replicação de arquivo encerrou a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-803">The file replication service API terminated the request.</span></span> <span data-ttu-id="6bebd-804">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-804">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**\_erro \_ interno do FRS**</span><span class="sxs-lookup"><span data-stu-id="6bebd-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS\_ERR\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-806">8005 (0x1F45)</span><span class="sxs-lookup"><span data-stu-id="6bebd-806">8005 (0x1F45)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-807">O serviço de replicação de arquivo encerrou a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-807">The file replication service terminated the request.</span></span> <span data-ttu-id="6bebd-808">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-808">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**\_comunicação do \_ serviço de erro do FRS \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS\_ERR\_SERVICE\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-810">8006 (0x1F46)</span><span class="sxs-lookup"><span data-stu-id="6bebd-810">8006 (0x1F46)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-811">O serviço de replicação de arquivo não pode ser contatado.</span><span class="sxs-lookup"><span data-stu-id="6bebd-811">The file replication service cannot be contacted.</span></span> <span data-ttu-id="6bebd-812">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-812">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**erro de FRS \_ \_ insuficiente \_ priv**</span><span class="sxs-lookup"><span data-stu-id="6bebd-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS\_ERR\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-814">8007 (0x1F47)</span><span class="sxs-lookup"><span data-stu-id="6bebd-814">8007 (0x1F47)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-815">O serviço de replicação de arquivo não pode atender à solicitação porque o usuário tem privilégios insuficientes.</span><span class="sxs-lookup"><span data-stu-id="6bebd-815">The file replication service cannot satisfy the request because the user has insufficient privileges.</span></span> <span data-ttu-id="6bebd-816">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-816">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**\_autenticação de erro do FRS \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS\_ERR\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-818">8008 (0x1F48)</span><span class="sxs-lookup"><span data-stu-id="6bebd-818">8008 (0x1F48)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-819">O serviço de replicação de arquivo não pode atender à solicitação porque o RPC autenticado não está disponível.</span><span class="sxs-lookup"><span data-stu-id="6bebd-819">The file replication service cannot satisfy the request because authenticated RPC is not available.</span></span> <span data-ttu-id="6bebd-820">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-820">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**o FRS \_ Err \_ pai é \_ insuficiente \_ priv**</span><span class="sxs-lookup"><span data-stu-id="6bebd-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS\_ERR\_PARENT\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-822">8009 (0x1F49)</span><span class="sxs-lookup"><span data-stu-id="6bebd-822">8009 (0x1F49)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-823">O serviço de replicação de arquivo não pode atender à solicitação porque o usuário tem privilégios insuficientes no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="6bebd-823">The file replication service cannot satisfy the request because the user has insufficient privileges on the domain controller.</span></span> <span data-ttu-id="6bebd-824">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-824">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_autenticação do \_ pai de erro do FRS \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS\_ERR\_PARENT\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-826">8010 (0x1F4A)</span><span class="sxs-lookup"><span data-stu-id="6bebd-826">8010 (0x1F4A)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-827">O serviço de replicação de arquivo não pode atender à solicitação porque o RPC autenticado não está disponível no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="6bebd-827">The file replication service cannot satisfy the request because authenticated RPC is not available on the domain controller.</span></span> <span data-ttu-id="6bebd-828">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-828">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**\_erro \_ de FRS filho \_ para \_ pai \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS\_ERR\_CHILD\_TO\_PARENT\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-830">8011 (0x1F4B)</span><span class="sxs-lookup"><span data-stu-id="6bebd-830">8011 (0x1F4B)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-831">O serviço de replicação de arquivo não pode se comunicar com o serviço de replicação de arquivo no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="6bebd-831">The file replication service cannot communicate with the file replication service on the domain controller.</span></span> <span data-ttu-id="6bebd-832">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-832">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ \_ de Err pai \_ para \_ filho \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS\_ERR\_PARENT\_TO\_CHILD\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-834">8012 (0x1F4C)</span><span class="sxs-lookup"><span data-stu-id="6bebd-834">8012 (0x1F4C)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-835">O serviço de replicação de arquivo no controlador de domínio não pode se comunicar com o serviço de replicação de arquivo neste computador.</span><span class="sxs-lookup"><span data-stu-id="6bebd-835">The file replication service on the domain controller cannot communicate with the file replication service on this computer.</span></span> <span data-ttu-id="6bebd-836">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-836">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**\_preenchimento do \_ SYSVOL de erro do FRS \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS\_ERR\_SYSVOL\_POPULATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-838">8013 (0x1F4D)</span><span class="sxs-lookup"><span data-stu-id="6bebd-838">8013 (0x1F4D)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-839">O serviço de replicação de arquivo não pode popular o volume do sistema devido a um erro interno.</span><span class="sxs-lookup"><span data-stu-id="6bebd-839">The file replication service cannot populate the system volume because of an internal error.</span></span> <span data-ttu-id="6bebd-840">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-840">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_ \_ \_ tempo limite de preenchimento de SYSVOL de erro do FRS \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS\_ERR\_SYSVOL\_POPULATE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-842">8014 (0x1F4E)</span><span class="sxs-lookup"><span data-stu-id="6bebd-842">8014 (0x1F4E)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-843">O serviço de replicação de arquivo não pode popular o volume do sistema devido a um tempo limite interno.</span><span class="sxs-lookup"><span data-stu-id="6bebd-843">The file replication service cannot populate the system volume because of an internal timeout.</span></span> <span data-ttu-id="6bebd-844">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-844">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**o \_ SYSVOL de erro do FRS \_ \_ está \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="6bebd-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS\_ERR\_SYSVOL\_IS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-846">8015 (0x1F4F)</span><span class="sxs-lookup"><span data-stu-id="6bebd-846">8015 (0x1F4F)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-847">O serviço de replicação de arquivo não pode processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6bebd-847">The file replication service cannot process the request.</span></span> <span data-ttu-id="6bebd-848">O volume do sistema está ocupado com uma solicitação anterior.</span><span class="sxs-lookup"><span data-stu-id="6bebd-848">The system volume is busy with a previous request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**\_rebaixar SYSVOL de erro do FRS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6bebd-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS\_ERR\_SYSVOL\_DEMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-850">8016 (0x1F50)</span><span class="sxs-lookup"><span data-stu-id="6bebd-850">8016 (0x1F50)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-851">O serviço de replicação de arquivo não pode parar de replicar o volume do sistema devido a um erro interno.</span><span class="sxs-lookup"><span data-stu-id="6bebd-851">The file replication service cannot stop replicating the system volume because of an internal error.</span></span> <span data-ttu-id="6bebd-852">O log de eventos pode ter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6bebd-852">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6bebd-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_parâmetro de \_ \_ serviço inválido \_ do FRS Err**</span><span class="sxs-lookup"><span data-stu-id="6bebd-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS\_ERR\_INVALID\_SERVICE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bebd-854">8017 (0x1F51)</span><span class="sxs-lookup"><span data-stu-id="6bebd-854">8017 (0x1F51)</span></span>
</dt> <dt>



<span data-ttu-id="6bebd-855">O serviço de replicação de arquivo detectou um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="6bebd-855">The file replication service detected an invalid parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bebd-856">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bebd-856">Requirements</span></span>



| <span data-ttu-id="6bebd-857">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bebd-857">Requirement</span></span> | <span data-ttu-id="6bebd-858">Valor</span><span class="sxs-lookup"><span data-stu-id="6bebd-858">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bebd-859">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bebd-859">Minimum supported client</span></span><br/> | <span data-ttu-id="6bebd-860">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6bebd-860">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6bebd-861">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bebd-861">Minimum supported server</span></span><br/> | <span data-ttu-id="6bebd-862">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6bebd-862">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6bebd-863">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bebd-863">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bebd-864"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bebd-864"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bebd-865">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bebd-865">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bebd-866">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="6bebd-866">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




