---
title: Função DsRestoreGetDatabaseLocations (Ntdsbcli. h)
description: Obtém os locais em que os arquivos de backup devem ser copiados durante uma operação de restauração.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Função DsRestoreGetDatabaseLocations Active Directory
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824574"
---
# <a name="dsrestoregetdatabaselocations-function"></a><span data-ttu-id="2c632-104">Função DsRestoreGetDatabaseLocations</span><span class="sxs-lookup"><span data-stu-id="2c632-104">DsRestoreGetDatabaseLocations function</span></span>

<span data-ttu-id="2c632-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2c632-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2c632-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2c632-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2c632-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="2c632-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="2c632-108">A função **DsRestoreGetDatabaseLocations** Obtém os locais em que os arquivos de backup devem ser copiados durante uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="2c632-108">The **DsRestoreGetDatabaseLocations** function obtains the locations where backup files should be copied during a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c632-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c632-109">Syntax</span></span>


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="2c632-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c632-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c632-111">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c632-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c632-112">Contém o identificador de contexto de restauração obtido com a função [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="2c632-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2c632-113">*pszDatabaseLocationList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2c632-113">*pszDatabaseLocationList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c632-114">Ponteiro para um ponteiro de cadeia de caracteres que recebe a lista de locais de banco de dados como caminhos UNC.</span><span class="sxs-lookup"><span data-stu-id="2c632-114">Pointer to a string pointer that receives the list of database locations as UNC paths.</span></span> <span data-ttu-id="2c632-115">Essa lista recebe uma lista terminada por nulo de cadeias de caracteres com terminação nula.</span><span class="sxs-lookup"><span data-stu-id="2c632-115">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="2c632-116">Esse buffer é alocado pela função **DsRestoreGetDatabaseLocations** e deve ser liberado quando não for mais necessário chamando a função [**DsBackupFree**](dsbackupfree.md) .</span><span class="sxs-lookup"><span data-stu-id="2c632-116">This buffer is allocated by the **DsRestoreGetDatabaseLocations** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="2c632-117">O primeiro caractere de cada um dos nomes de arquivo contém uma das [**constantes BFT**](bft-constants.md) que identifica o tipo de nome.</span><span class="sxs-lookup"><span data-stu-id="2c632-117">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the name type.</span></span> <span data-ttu-id="2c632-118">A função **DsRestoreGetDatabaseLocations** fornece apenas os seguintes tipos de nome.</span><span class="sxs-lookup"><span data-stu-id="2c632-118">The **DsRestoreGetDatabaseLocations** function only supplies the following name types.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="2c632-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_banco de \_ dados NTDS BFT**</span><span class="sxs-lookup"><span data-stu-id="2c632-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="2c632-120">O arquivo de banco de dados NTDS deve ser copiado para esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="2c632-120">The NTDS database file should be copied to this file.</span></span> <span data-ttu-id="2c632-121">Esse é o arquivo que foi identificado como **\_ banco de \_ dados BFT NTDS** quando o backup foi executado.</span><span class="sxs-lookup"><span data-stu-id="2c632-121">This is the file that was identified as **BFT\_NTDS\_DATABASE** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span data-ttu-id="2c632-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**Dir. de log do BFT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c632-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="2c632-123">Todos os arquivos de log são copiados para esse diretório.</span><span class="sxs-lookup"><span data-stu-id="2c632-123">All log files are copied to this directory.</span></span> <span data-ttu-id="2c632-124">Os arquivos de log foram identificados **como \_ log de BFT** quando o backup foi executado.</span><span class="sxs-lookup"><span data-stu-id="2c632-124">The log files were identified as **BFT\_LOG** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span data-ttu-id="2c632-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT de \_ ponto de verificação de \_ diretório**</span><span class="sxs-lookup"><span data-stu-id="2c632-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="2c632-126">Todos os arquivos de patch são copiados para esse diretório.</span><span class="sxs-lookup"><span data-stu-id="2c632-126">All patch files are copied to this directory.</span></span> <span data-ttu-id="2c632-127">Os arquivos de patch foram identificados como um **\_ \_ arquivo de patch BFT** quando o backup foi executado.</span><span class="sxs-lookup"><span data-stu-id="2c632-127">The patch files were identified as **BFT\_PATCH\_FILE** when the backup was performed.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2c632-128">*pcbSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2c632-128">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c632-129">Ponteiro para o valor **DWORD** que recebe o tamanho, em bytes, do buffer *pszDatabaseLocationList* .</span><span class="sxs-lookup"><span data-stu-id="2c632-129">Pointer to **DWORD** value that receives the size, in bytes, of the *pszDatabaseLocationList* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c632-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c632-130">Return value</span></span>

<span data-ttu-id="2c632-131">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="2c632-131">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="2c632-132">A lista a seguir lista os possíveis códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="2c632-132">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="2c632-133">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="2c632-133">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="2c632-134">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="2c632-134">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="2c632-135">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="2c632-135">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="2c632-136">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="2c632-136">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="2c632-137">*HBC*, *pszDatabaseLocationList* ou *pcbSize* são inválidos.</span><span class="sxs-lookup"><span data-stu-id="2c632-137">*hbc*, *pszDatabaseLocationList*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="2c632-138">**ERRO \_ de \_ memória insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="2c632-138">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="2c632-139">Ocorreu uma falha de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="2c632-139">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c632-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c632-140">Remarks</span></span>

<span data-ttu-id="2c632-141">A função **DsRestoreGetDatabaseLocations** pode ser usada para obter os diretórios de restauração sem acesso aos dados de backup.</span><span class="sxs-lookup"><span data-stu-id="2c632-141">The **DsRestoreGetDatabaseLocations** function can be used to obtain the restoration directories without access to the backed up data.</span></span> <span data-ttu-id="2c632-142">Para fazer isso, chame [**DsRestorePrepare**](dsrestoreprepare.md) com **NULL** para o parâmetro *pvExpiryToken* .</span><span class="sxs-lookup"><span data-stu-id="2c632-142">To do this, call [**DsRestorePrepare**](dsrestoreprepare.md) with **NULL** for the *pvExpiryToken* parameter.</span></span> <span data-ttu-id="2c632-143">Isso faz com que o **DsRestorePrepare** retorne um identificador de contexto restrito que só pode ser usado com a função **DsRestoreGetDatabaseLocations** .</span><span class="sxs-lookup"><span data-stu-id="2c632-143">This causes **DsRestorePrepare** to return a restricted context handle which can only be used with the **DsRestoreGetDatabaseLocations** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c632-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c632-144">Requirements</span></span>



| <span data-ttu-id="2c632-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c632-145">Requirement</span></span> | <span data-ttu-id="2c632-146">Valor</span><span class="sxs-lookup"><span data-stu-id="2c632-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c632-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c632-147">Minimum supported client</span></span><br/> | <span data-ttu-id="2c632-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c632-148">Windows Vista</span></span><br/>                                                                              |
| <span data-ttu-id="2c632-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c632-149">Minimum supported server</span></span><br/> | <span data-ttu-id="2c632-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c632-150">Windows Server 2008</span></span><br/>                                                                        |
| <span data-ttu-id="2c632-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c632-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c632-152"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c632-152"><dt>Ntdsbcli.h</dt></span></span> </dl>                 |
| <span data-ttu-id="2c632-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2c632-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c632-154"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c632-154"><dt>Ntdsbcli.lib</dt></span></span> </dl>               |
| <span data-ttu-id="2c632-155">DLL</span><span class="sxs-lookup"><span data-stu-id="2c632-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c632-156"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c632-156"><dt>Ntdsbcli.dll</dt></span></span> </dl>               |
| <span data-ttu-id="2c632-157">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2c632-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2c632-158">**DsRestoreGetDatabaseLocationsW** (Unicode) e **DsRestoreGetDatabaseLocationsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2c632-158">**DsRestoreGetDatabaseLocationsW** (Unicode) and **DsRestoreGetDatabaseLocationsA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c632-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c632-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c632-160">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="2c632-160">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="2c632-161">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="2c632-161">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="2c632-162">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="2c632-162">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="2c632-163">Restaurando Active Directory</span><span class="sxs-lookup"><span data-stu-id="2c632-163">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> </dl>

 

