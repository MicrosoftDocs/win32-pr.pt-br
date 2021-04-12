---
title: Função DsBackupPrepare (Ntdsbcli. h)
description: Prepara o diretório no servidor especificado para o backup online e retorna um identificador de contexto de backup usado nas chamadas subsequentes para outras funções de backup.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Função DsBackupPrepare Active Directory
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455285"
---
# <a name="dsbackupprepare-function"></a><span data-ttu-id="2321a-104">Função DsBackupPrepare</span><span class="sxs-lookup"><span data-stu-id="2321a-104">DsBackupPrepare function</span></span>

<span data-ttu-id="2321a-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2321a-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2321a-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2321a-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2321a-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="2321a-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="2321a-108">A função **DsBackupPrepare** prepara o diretório no servidor especificado para o backup online e retorna um identificador de contexto de backup usado em chamadas subsequentes para outras funções de backup.</span><span class="sxs-lookup"><span data-stu-id="2321a-108">The **DsBackupPrepare** function prepares the directory on the specified server for the online backup and returns a backup context handle used in subsequent calls to other backup functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2321a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2321a-109">Syntax</span></span>


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="2321a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2321a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2321a-111">*szBackupServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2321a-111">*szBackupServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2321a-112">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor para backup.</span><span class="sxs-lookup"><span data-stu-id="2321a-112">Pointer to a null-terminated string that contains the name of the server to backup.</span></span> <span data-ttu-id="2321a-113">Barras invertidas precedentes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="2321a-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="2321a-114">O servidor deve ser o mesmo computador do qual essa função é chamada.</span><span class="sxs-lookup"><span data-stu-id="2321a-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="2321a-115">O nome do servidor não pode conter um caractere de sublinhado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="2321a-115">The server name cannot contain an underscore (\_) character.</span></span> <span data-ttu-id="2321a-116">Um exemplo de um nome de servidor é " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="2321a-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="2321a-117">*grbit* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2321a-117">*grbit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2321a-118">Determina se será feito backup dos arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="2321a-118">Determines if the log files will be backed up.</span></span> <span data-ttu-id="2321a-119">Esse valor deve ser sempre 0 porque não há suporte para backups incrementais.</span><span class="sxs-lookup"><span data-stu-id="2321a-119">This value should always be 0 because incremental backups are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2321a-120">*btBackupType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2321a-120">*btBackupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2321a-121">Especifica o tipo de backup.</span><span class="sxs-lookup"><span data-stu-id="2321a-121">Specifies the type of backup.</span></span> <span data-ttu-id="2321a-122">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2321a-122">This can be one of the following values.</span></span>

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span data-ttu-id="2321a-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**tipo de BACKUP \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="2321a-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP\_TYPE\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="2321a-124">Especifica um backup completo.</span><span class="sxs-lookup"><span data-stu-id="2321a-124">Specifies a full backup.</span></span> <span data-ttu-id="2321a-125">O backup do diretório completo (DIT, arquivos de log e arquivos de atualização) é feito.</span><span class="sxs-lookup"><span data-stu-id="2321a-125">The complete directory (DIT, log files, and update files) are backed up.</span></span> <span data-ttu-id="2321a-126">Todos os dados são submetidos a backup e os arquivos de log de transações são truncados.</span><span class="sxs-lookup"><span data-stu-id="2321a-126">All data is backed up and transaction log files are truncated.</span></span> <span data-ttu-id="2321a-127">Somente backups completos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="2321a-127">Only full backups are supported.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span data-ttu-id="2321a-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_ \_ somente logs de tipo de backup \_**</span><span class="sxs-lookup"><span data-stu-id="2321a-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**BACKUP\_TYPE\_LOGS\_ONLY**</span></span>


</dt> <dd>

<span data-ttu-id="2321a-129">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="2321a-129">This value is not supported.</span></span> <span data-ttu-id="2321a-130">Especifica que somente os logs de banco de dados, e não o banco de dados, serão submetidos a backup.</span><span class="sxs-lookup"><span data-stu-id="2321a-130">Specifies that only the database logs, and not the database itself, will be backed up.</span></span> <span data-ttu-id="2321a-131">Isso normalmente é usado ao executar um backup diferencial ou incremental.</span><span class="sxs-lookup"><span data-stu-id="2321a-131">This is normally used when performing a differential or incremental backup.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span data-ttu-id="2321a-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**tipo de BACKUP \_ \_ incremental**</span><span class="sxs-lookup"><span data-stu-id="2321a-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**BACKUP\_TYPE\_INCREMENTAL**</span></span>


</dt> <dd>

<span data-ttu-id="2321a-133">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="2321a-133">This value is not supported.</span></span> <span data-ttu-id="2321a-134">**DsBackupPrepare** retorna **um \_ \_ parâmetro inválido de erro**.</span><span class="sxs-lookup"><span data-stu-id="2321a-134">**DsBackupPrepare** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2321a-135">*ppvExpiryToken* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2321a-135">*ppvExpiryToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2321a-136">Ponteiro para um valor **pVoid** que recebe um ponteiro para um token de expiração associado a este backup.</span><span class="sxs-lookup"><span data-stu-id="2321a-136">Pointer to a **PVOID** value that receives a pointer to an expiry token associated with this backup.</span></span> <span data-ttu-id="2321a-137">*pcbExpiryTokenSize* recebe o tamanho, em bytes, desses dados.</span><span class="sxs-lookup"><span data-stu-id="2321a-137">*pcbExpiryTokenSize* receives the size, in bytes, of this data.</span></span> <span data-ttu-id="2321a-138">O chamador deve salvar o conteúdo desse token com o backup, pois o token deve ser passado para [**DsRestorePrepare**](dsrestoreprepare.md) ao tentar restaurar os dados.</span><span class="sxs-lookup"><span data-stu-id="2321a-138">The caller must save the contents of this token with the backup because the token must be passed to [**DsRestorePrepare**](dsrestoreprepare.md) when attempting to restore data.</span></span> <span data-ttu-id="2321a-139">Depois que o token tiver sido armazenado e não for mais necessário, o chamador deverá liberar a memória alocada usando [**DsBackupFree**](dsbackupfree.md).</span><span class="sxs-lookup"><span data-stu-id="2321a-139">After the token has been stored and is no longer required, the caller should free the allocated memory using [**DsBackupFree**](dsbackupfree.md).</span></span>

</dd> <dt>

<span data-ttu-id="2321a-140">*pcbExpiryTokenSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2321a-140">*pcbExpiryTokenSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2321a-141">Ponteiro para um valor **DWORD** que recebe o tamanho, em bytes, do token em *ppvExpiryToken*.</span><span class="sxs-lookup"><span data-stu-id="2321a-141">Pointer to a **DWORD** value that receives the size, in bytes, of the token in *ppvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="2321a-142">*phbc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2321a-142">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2321a-143">Aponta para um valor **HBC** que recebe o identificador para o backup.</span><span class="sxs-lookup"><span data-stu-id="2321a-143">Pointer to an **HBC** value that receives the handle for the backup.</span></span> <span data-ttu-id="2321a-144">Esse identificador é usado ao chamar outras funções de backup do serviço de diretório, como [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsBackupEnd**](dsbackupend.md).</span><span class="sxs-lookup"><span data-stu-id="2321a-144">This handle is used when calling other Directory Service backup functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsBackupEnd**](dsbackupend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2321a-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2321a-145">Return value</span></span>

<span data-ttu-id="2321a-146">Retornará **S \_ OK** se a função for bem-sucedida ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="2321a-146">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="2321a-147">A lista a seguir lista outros códigos de erro possíveis.</span><span class="sxs-lookup"><span data-stu-id="2321a-147">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="2321a-148">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="2321a-148">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="2321a-149">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="2321a-149">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="2321a-150">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="2321a-150">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="2321a-151">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="2321a-151">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="2321a-152">*szBackupServer* ou *phbcBackupContext* não são válidos.</span><span class="sxs-lookup"><span data-stu-id="2321a-152">*szBackupServer* or *phbcBackupContext* are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2321a-153">**ERRO \_ de \_ memória insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="2321a-153">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="2321a-154">Ocorreu uma falha de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="2321a-154">A memory allocation failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2321a-155">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="2321a-155">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="2321a-156">O servidor no *szBackupServer* não pôde ser encontrado, não é um controlador de domínio ou *szBackupServer* não está formatado corretamente.</span><span class="sxs-lookup"><span data-stu-id="2321a-156">The server in *szBackupServer* could not be found, is not a domain controller or *szBackupServer* is not formatted correctly.</span></span> <span data-ttu-id="2321a-157">Esse valor é definido em ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="2321a-157">This value is defined in ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="2321a-158">**hrInvalidParam**</span><span class="sxs-lookup"><span data-stu-id="2321a-158">**hrInvalidParam**</span></span>
</dt> <dd>

<span data-ttu-id="2321a-159">*ppvExpiryToken* e/ou *pcbExpiryTokenSize* são inválidos.</span><span class="sxs-lookup"><span data-stu-id="2321a-159">*ppvExpiryToken* and/or *pcbExpiryTokenSize* are invalid.</span></span> <span data-ttu-id="2321a-160">Esse valor é definido em Ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="2321a-160">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="2321a-161">**Associação de RPC \_ S \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="2321a-161">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="2321a-162">A função é chamada remotamente ou o servidor no *szServerName* não é um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="2321a-162">The function is called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2321a-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="2321a-163">Remarks</span></span>

<span data-ttu-id="2321a-164">Essa função requer que o chamador tenha o **privilégio \_ \_ nome de backup se** .</span><span class="sxs-lookup"><span data-stu-id="2321a-164">This function requires that the caller has the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="2321a-165">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para alterar o contexto de segurança no qual essa função é chamada.</span><span class="sxs-lookup"><span data-stu-id="2321a-165">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to change the security context under which this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="2321a-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2321a-166">Requirements</span></span>



| <span data-ttu-id="2321a-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="2321a-167">Requirement</span></span> | <span data-ttu-id="2321a-168">Valor</span><span class="sxs-lookup"><span data-stu-id="2321a-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2321a-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2321a-169">Minimum supported client</span></span><br/> | <span data-ttu-id="2321a-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2321a-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2321a-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2321a-171">Minimum supported server</span></span><br/> | <span data-ttu-id="2321a-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2321a-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2321a-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2321a-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="2321a-174"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="2321a-174"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="2321a-175">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2321a-175">Library</span></span><br/>                  | <dl> <span data-ttu-id="2321a-176"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2321a-176"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="2321a-177">DLL</span><span class="sxs-lookup"><span data-stu-id="2321a-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2321a-178"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2321a-178"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="2321a-179">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2321a-179">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2321a-180">**DsBackupPrepareW** (Unicode) e **DsBackupPrepareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2321a-180">**DsBackupPrepareW** (Unicode) and **DsBackupPrepareA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2321a-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="2321a-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2321a-182">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="2321a-182">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="2321a-183">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="2321a-183">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="2321a-184">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="2321a-184">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="2321a-185">**DsBackupEnd**</span><span class="sxs-lookup"><span data-stu-id="2321a-185">**DsBackupEnd**</span></span>](dsbackupend.md)
</dt> <dt>

[<span data-ttu-id="2321a-186">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="2321a-186">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="2321a-187">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="2321a-187">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="2321a-188">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="2321a-188">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

