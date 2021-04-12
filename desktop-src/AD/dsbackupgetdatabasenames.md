---
title: Função DsBackupGetDatabaseNames (Ntdsbcli. h)
description: Obtém a lista de arquivos de banco de dados cujo backup será feito para o contexto de backup fornecido.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Função DsBackupGetDatabaseNames Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455286"
---
# <a name="dsbackupgetdatabasenames-function"></a><span data-ttu-id="85546-104">Função DsBackupGetDatabaseNames</span><span class="sxs-lookup"><span data-stu-id="85546-104">DsBackupGetDatabaseNames function</span></span>

<span data-ttu-id="85546-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="85546-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="85546-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="85546-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="85546-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="85546-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="85546-108">A função **DsBackupGetDatabaseNames** Obtém a lista de arquivos de banco de dados cujo backup será feito para o contexto de backup fornecido.</span><span class="sxs-lookup"><span data-stu-id="85546-108">The **DsBackupGetDatabaseNames** function obtains the list of database files to be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="85546-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85546-109">Syntax</span></span>


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="85546-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85546-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85546-111">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85546-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85546-112">Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="85546-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="85546-113">*pszAttachmentInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85546-113">*pszAttachmentInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85546-114">Ponteiro para um ponteiro de cadeia de caracteres que recebe a lista de nomes de arquivo de banco de dados como caminhos UNC.</span><span class="sxs-lookup"><span data-stu-id="85546-114">Pointer to a string pointer that receives the list of database file names as UNC paths.</span></span> <span data-ttu-id="85546-115">Esse valor deve ser inicializado para **NULL** antes de chamar **DsBackupGetDatabaseNames**.</span><span class="sxs-lookup"><span data-stu-id="85546-115">This value must be initialized to **NULL** prior to calling **DsBackupGetDatabaseNames**.</span></span>

<span data-ttu-id="85546-116">Essa lista recebe uma lista terminada por nulo de cadeias de caracteres com terminação nula.</span><span class="sxs-lookup"><span data-stu-id="85546-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="85546-117">Esse buffer é alocado pela função **DsBackupGetDatabaseNames** e deve ser liberado quando não for mais necessário chamando a função [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="85546-117">This buffer is allocated by the **DsBackupGetDatabaseNames** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="85546-118">O primeiro caractere de cada nome de arquivo contém uma das [**constantes BFT**](bft-constants.md) que identifica o tipo de nome.</span><span class="sxs-lookup"><span data-stu-id="85546-118">The first character of each file name contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span> <span data-ttu-id="85546-119">A função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) fornece apenas os seguintes tipos de nomes.</span><span class="sxs-lookup"><span data-stu-id="85546-119">The [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function only supplies the following types of names.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="85546-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_banco de \_ dados NTDS BFT**</span><span class="sxs-lookup"><span data-stu-id="85546-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="85546-121">O arquivo é um arquivo de banco de dados NTDS.</span><span class="sxs-lookup"><span data-stu-id="85546-121">The file is an NTDS database file.</span></span> <span data-ttu-id="85546-122">Esse arquivo deve ser copiado para o arquivo identificado **como \_ \_ banco de dados BFT NTDS** quando os dados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="85546-122">This file should be copied to the file identified as **BFT\_NTDS\_DATABASE** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span data-ttu-id="85546-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**LOG do BFT \_**</span><span class="sxs-lookup"><span data-stu-id="85546-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>


</dt> <dd>

<span data-ttu-id="85546-124">O arquivo é um arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="85546-124">The file is a log file.</span></span> <span data-ttu-id="85546-125">Todos os arquivos de log são copiados para o diretório identificado como **BFT \_ log \_ dir** quando os dados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="85546-125">All log files are copied to the directory identified as **BFT\_LOG\_DIR** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span data-ttu-id="85546-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_arquivo de patch do BFT \_**</span><span class="sxs-lookup"><span data-stu-id="85546-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>


</dt> <dd>

<span data-ttu-id="85546-127">O arquivo é um arquivo de patch.</span><span class="sxs-lookup"><span data-stu-id="85546-127">The file is a patch file.</span></span> <span data-ttu-id="85546-128">Todos os arquivos de patch são copiados para o diretório identificado como **BFT \_ Checkpoint \_ dir** quando os dados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="85546-128">All patch files are copied to the directory identified as **BFT\_CHECKPOINT\_DIR** when the data is restored.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="85546-129">*pcbSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85546-129">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85546-130">Ponteiro para o valor **DWORD** que recebe o tamanho, em bytes, do buffer *pszAttachmentInfo* .</span><span class="sxs-lookup"><span data-stu-id="85546-130">Pointer to **DWORD** value that receives the size, in bytes, of the *pszAttachmentInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85546-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85546-131">Return value</span></span>

<span data-ttu-id="85546-132">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="85546-132">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="85546-133">A lista a seguir lista outros códigos de erro possíveis.</span><span class="sxs-lookup"><span data-stu-id="85546-133">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="85546-134">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="85546-134">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="85546-135">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="85546-135">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="85546-136">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="85546-136">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="85546-137">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="85546-137">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="85546-138">*HBC*, *pszAttachmentInfo* ou *pcbSize* são inválidos.</span><span class="sxs-lookup"><span data-stu-id="85546-138">*hbc*, *pszAttachmentInfo*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="85546-139">**ERRO \_ de \_ memória insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="85546-139">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="85546-140">Ocorreu uma falha de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="85546-140">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85546-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="85546-141">Remarks</span></span>

<span data-ttu-id="85546-142">A função **DsBackupGetDatabaseNames** fornece uma lista dos arquivos de banco de dados necessários para um backup.</span><span class="sxs-lookup"><span data-stu-id="85546-142">The **DsBackupGetDatabaseNames** function provides a list of the database files necessary for a backup.</span></span> <span data-ttu-id="85546-143">Um backup completo consiste nos arquivos de banco de dados e nos arquivos de log fornecidos pela função [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) .</span><span class="sxs-lookup"><span data-stu-id="85546-143">A full backup consists of the database files and the log files provided by the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function.</span></span> <span data-ttu-id="85546-144">Não há suporte para backups incrementais de servidores Active Directory.</span><span class="sxs-lookup"><span data-stu-id="85546-144">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="85546-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85546-145">Requirements</span></span>



| <span data-ttu-id="85546-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="85546-146">Requirement</span></span> | <span data-ttu-id="85546-147">Valor</span><span class="sxs-lookup"><span data-stu-id="85546-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="85546-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85546-148">Minimum supported client</span></span><br/> | <span data-ttu-id="85546-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85546-149">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="85546-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85546-150">Minimum supported server</span></span><br/> | <span data-ttu-id="85546-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85546-151">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="85546-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85546-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="85546-153"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="85546-153"><dt>Ntdsbcli.h</dt></span></span> </dl>       |
| <span data-ttu-id="85546-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85546-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="85546-155"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85546-155"><dt>Ntdsbcli.lib</dt></span></span> </dl>     |
| <span data-ttu-id="85546-156">DLL</span><span class="sxs-lookup"><span data-stu-id="85546-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85546-157"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85546-157"><dt>Ntdsbcli.dll</dt></span></span> </dl>     |
| <span data-ttu-id="85546-158">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="85546-158">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="85546-159">**DsBackupGetDatabaseNamesW** (Unicode) e **DsBackupGetDatabaseNamesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="85546-159">**DsBackupGetDatabaseNamesW** (Unicode) and **DsBackupGetDatabaseNamesA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85546-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="85546-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85546-161">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="85546-161">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="85546-162">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="85546-162">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="85546-163">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="85546-163">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="85546-164">**Constantes BFT**</span><span class="sxs-lookup"><span data-stu-id="85546-164">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="85546-165">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="85546-165">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="85546-166">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="85546-166">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

