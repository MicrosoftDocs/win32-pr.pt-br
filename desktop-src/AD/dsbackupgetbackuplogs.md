---
title: Função DsBackupGetBackupLogs (Ntdsbcli. h)
description: Obtém a lista de arquivos de log cujo backup deve ser feito para o contexto de backup fornecido.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Função DsBackupGetBackupLogs Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918569"
---
# <a name="dsbackupgetbackuplogs-function"></a><span data-ttu-id="8d048-104">Função DsBackupGetBackupLogs</span><span class="sxs-lookup"><span data-stu-id="8d048-104">DsBackupGetBackupLogs function</span></span>

<span data-ttu-id="8d048-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8d048-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8d048-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8d048-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8d048-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="8d048-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="8d048-108">A função **DsBackupGetBackupLogs** Obtém a lista de arquivos de log que devem ser submetidos a backup para o contexto de backup fornecido.</span><span class="sxs-lookup"><span data-stu-id="8d048-108">The **DsBackupGetBackupLogs** function obtains the list of log files that must be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d048-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d048-109">Syntax</span></span>


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="8d048-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d048-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d048-111">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d048-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d048-112">Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="8d048-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8d048-113">*pszBackupLogFiles* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d048-113">*pszBackupLogFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d048-114">Ponteiro para um ponteiro de cadeia de caracteres que recebe a lista de nomes de arquivos de log como caminhos UNC.</span><span class="sxs-lookup"><span data-stu-id="8d048-114">Pointer to a string pointer that receives the list of log file names as UNC paths.</span></span> <span data-ttu-id="8d048-115">Inicialize esse valor como **NULL** antes de chamar **DsBackupGetBackupLogs**.</span><span class="sxs-lookup"><span data-stu-id="8d048-115">Initialize this value to **NULL** before calling **DsBackupGetBackupLogs**.</span></span>

<span data-ttu-id="8d048-116">Essa lista recebe uma lista terminada por nulo de cadeias de caracteres com terminação nula.</span><span class="sxs-lookup"><span data-stu-id="8d048-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="8d048-117">Esse buffer é alocado pela função **DsBackupGetBackupLogs** e deve ser liberado quando não for mais necessário chamando a função [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="8d048-117">This buffer is allocated by the **DsBackupGetBackupLogs** function and must be freed when no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="8d048-118">O primeiro caractere de cada um dos nomes de arquivo contém uma das [**constantes BFT**](bft-constants.md) que identifica o tipo de nome.</span><span class="sxs-lookup"><span data-stu-id="8d048-118">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span>

</dd> <dt>

<span data-ttu-id="8d048-119">*pcbSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d048-119">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d048-120">Ponteiro para o valor **DWORD** que recebe o tamanho, em bytes, do buffer *pszBackupLogFiles* .</span><span class="sxs-lookup"><span data-stu-id="8d048-120">Pointer to **DWORD** value that receives the size, in bytes, of the *pszBackupLogFiles* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d048-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d048-121">Return value</span></span>

<span data-ttu-id="8d048-122">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="8d048-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="8d048-123">A lista a seguir lista outros códigos de erro possíveis.</span><span class="sxs-lookup"><span data-stu-id="8d048-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="8d048-124">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="8d048-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="8d048-125">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="8d048-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="8d048-126">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="8d048-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="8d048-127">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="8d048-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="8d048-128">*HBC*, *pszBackupLogFiles* ou *pcbSize* é inválido.</span><span class="sxs-lookup"><span data-stu-id="8d048-128">*hbc*, *pszBackupLogFiles*, or *pcbSize* is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="8d048-129">**ERRO \_ de \_ memória insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="8d048-129">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="8d048-130">Ocorreu uma falha de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="8d048-130">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d048-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d048-131">Remarks</span></span>

<span data-ttu-id="8d048-132">A função **DsBackupGetBackupLogs** fornece uma lista dos arquivos de log necessários para um backup.</span><span class="sxs-lookup"><span data-stu-id="8d048-132">The **DsBackupGetBackupLogs** function provides a list of the log files necessary for a backup.</span></span> <span data-ttu-id="8d048-133">Um backup completo consiste nos arquivos de banco de dados fornecidos pela função [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) e os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8d048-133">A full backup consists of the database files provided by the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function and the log files.</span></span> <span data-ttu-id="8d048-134">Não há suporte para backups incrementais de servidores Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d048-134">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d048-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d048-135">Requirements</span></span>



| <span data-ttu-id="8d048-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d048-136">Requirement</span></span> | <span data-ttu-id="8d048-137">Valor</span><span class="sxs-lookup"><span data-stu-id="8d048-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d048-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d048-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8d048-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d048-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d048-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d048-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8d048-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d048-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d048-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d048-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d048-143"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d048-143"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d048-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d048-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d048-145"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d048-145"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d048-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8d048-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d048-147"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d048-147"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d048-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8d048-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8d048-149">**DsBackupGetBackupLogsW** (Unicode) e **DsBackupGetBackupLogsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8d048-149">**DsBackupGetBackupLogsW** (Unicode) and **DsBackupGetBackupLogsA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="8d048-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d048-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d048-151">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="8d048-151">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="8d048-152">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="8d048-152">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="8d048-153">**Constantes BFT**</span><span class="sxs-lookup"><span data-stu-id="8d048-153">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="8d048-154">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="8d048-154">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="8d048-155">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="8d048-155">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

