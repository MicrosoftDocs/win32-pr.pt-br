---
title: Função DsRestoreRegister (Ntdsbcli. h)
description: Registra uma operação de restauração.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Função DsRestoreRegister Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009487"
---
# <a name="dsrestoreregister-function"></a><span data-ttu-id="058cb-104">Função DsRestoreRegister</span><span class="sxs-lookup"><span data-stu-id="058cb-104">DsRestoreRegister function</span></span>

<span data-ttu-id="058cb-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="058cb-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="058cb-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="058cb-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="058cb-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="058cb-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="058cb-108">A função **DsRestoreRegister** registra uma operação de restauração. Essa função interbloqueia todas as operações de restauração subsequentes e impede que o destino de restauração seja iniciado até que a função [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) seja chamada.</span><span class="sxs-lookup"><span data-stu-id="058cb-108">The **DsRestoreRegister** function registers a restore operation.This function interlocks all subsequent restore operations and prevents the restore target from starting until the [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="058cb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="058cb-109">Syntax</span></span>


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a><span data-ttu-id="058cb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="058cb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="058cb-111">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="058cb-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="058cb-112">Contém o identificador de contexto de restauração obtido com a função [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="058cb-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-113">*szCheckPointFilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="058cb-113">*szCheckPointFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="058cb-114">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho para o arquivo de ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="058cb-114">Pointer to a null-terminated string that contains the path to the checkpoint file.</span></span> <span data-ttu-id="058cb-115">Esse caminho é fornecido pela função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e tem um valor **BFT** de **BFT de \_ ponto \_ de verificação**.</span><span class="sxs-lookup"><span data-stu-id="058cb-115">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_CHECKPOINT\_DIR**.</span></span> <span data-ttu-id="058cb-116">Normalmente, isso é o mesmo que o caminho do banco de dados do sistema.</span><span class="sxs-lookup"><span data-stu-id="058cb-116">Typically this is the same as the system database path.</span></span> <span data-ttu-id="058cb-117">Esse caminho é necessário para a função de restauração de backup apropriada.</span><span class="sxs-lookup"><span data-stu-id="058cb-117">This path is required for proper backup restore function.</span></span> <span data-ttu-id="058cb-118">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="058cb-118">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="058cb-119">A passagem de **NULL** nesse parâmetro causará um erro durante o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="058cb-119">Passing **NULL** in this parameter will cause an error during the restore process.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-120">*szLogPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="058cb-120">*szLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="058cb-121">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho onde os arquivos de log serão restaurados.</span><span class="sxs-lookup"><span data-stu-id="058cb-121">Pointer to a null-terminated string that contains the path where the log files will be restored.</span></span> <span data-ttu-id="058cb-122">Esse caminho é fornecido pela função [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e tem um valor **BFT** de **BFT \_ log \_ dir**.</span><span class="sxs-lookup"><span data-stu-id="058cb-122">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_LOG\_DIR**.</span></span> <span data-ttu-id="058cb-123">Se o caminho apontar para um diretório vazio, novos arquivos de log serão criados lá.</span><span class="sxs-lookup"><span data-stu-id="058cb-123">If the path points to an empty directory, new log files are created there.</span></span> <span data-ttu-id="058cb-124">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="058cb-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-125">*rgrstmap* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="058cb-125">*rgrstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="058cb-126">Uma matriz de [**estruturas \_ RSTMAP EDB**](edb-rstmap.md) que contém os caminhos novos e antigos para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="058cb-126">An array of [**EDB\_RSTMAP**](edb-rstmap.md) structures that contains the old and new paths for each database.</span></span> <span data-ttu-id="058cb-127">Há uma estrutura para cada banco de dados.</span><span class="sxs-lookup"><span data-stu-id="058cb-127">There is one structure for each database.</span></span> <span data-ttu-id="058cb-128">Para o diretório, há uma estrutura para o banco de dados do sistema e outra estrutura para o banco de dados de diretório.</span><span class="sxs-lookup"><span data-stu-id="058cb-128">For the directory, there is a structure for the system database and another structure for the directory database.</span></span> <span data-ttu-id="058cb-129">A ordem dos elementos na matriz não importa.</span><span class="sxs-lookup"><span data-stu-id="058cb-129">The order of the elements in the array does not matter.</span></span> <span data-ttu-id="058cb-130">O parâmetro *crstmap* contém o número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="058cb-130">The *crstmap* parameter contains the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-131">*crstmap* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="058cb-131">*crstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="058cb-132">Contém o número de elementos na matriz *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="058cb-132">Contains the number of elements in the *rgrstmap* array.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-133">*szBackupLogPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="058cb-133">*szBackupLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="058cb-134">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho onde os arquivos de log de backup residem atualmente.</span><span class="sxs-lookup"><span data-stu-id="058cb-134">Pointer to a null-terminated string that contains the path where the backed up log files currently reside.</span></span> <span data-ttu-id="058cb-135">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="058cb-135">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-136">*genLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="058cb-136">*genLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="058cb-137">Contém o número de log mais baixo a ser restaurado nesta sessão de restauração.</span><span class="sxs-lookup"><span data-stu-id="058cb-137">Contains the lowest log number to restore in this restore session.</span></span> <span data-ttu-id="058cb-138">Este é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="058cb-138">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-139">*genHigh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="058cb-139">*genHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="058cb-140">Contém o número de log mais alto a ser restaurado nesta sessão de restauração.</span><span class="sxs-lookup"><span data-stu-id="058cb-140">Contains the highest log number to restore in this restore session.</span></span> <span data-ttu-id="058cb-141">Este é um número hexadecimal no intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="058cb-141">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="058cb-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="058cb-142">Return value</span></span>

<span data-ttu-id="058cb-143">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="058cb-143">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="058cb-144">A lista a seguir lista os possíveis códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="058cb-144">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="058cb-145">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="058cb-145">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="058cb-146">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="058cb-146">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="058cb-147">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="058cb-147">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-148">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="058cb-148">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="058cb-149">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="058cb-149">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="058cb-150">**hrMissingExpiryToken**</span><span class="sxs-lookup"><span data-stu-id="058cb-150">**hrMissingExpiryToken**</span></span>
</dt> <dd>

<span data-ttu-id="058cb-151">O token de expiração fornecido a [**DsRestorePrepare**](dsrestoreprepare.md) era inválido.</span><span class="sxs-lookup"><span data-stu-id="058cb-151">The expiry token supplied to [**DsRestorePrepare**](dsrestoreprepare.md) was invalid.</span></span> <span data-ttu-id="058cb-152">Esse valor é definido em Ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="058cb-152">This value is defined in Ntdsbmsg.h.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="058cb-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="058cb-153">Requirements</span></span>



| <span data-ttu-id="058cb-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="058cb-154">Requirement</span></span> | <span data-ttu-id="058cb-155">Valor</span><span class="sxs-lookup"><span data-stu-id="058cb-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="058cb-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="058cb-156">Minimum supported client</span></span><br/> | <span data-ttu-id="058cb-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="058cb-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="058cb-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="058cb-158">Minimum supported server</span></span><br/> | <span data-ttu-id="058cb-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="058cb-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="058cb-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="058cb-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="058cb-161"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="058cb-161"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="058cb-162">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="058cb-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="058cb-163"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="058cb-163"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="058cb-164">DLL</span><span class="sxs-lookup"><span data-stu-id="058cb-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="058cb-165"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="058cb-165"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="058cb-166">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="058cb-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="058cb-167">**DsRestoreRegisterW** (Unicode) e **DsRestoreRegisterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="058cb-167">**DsRestoreRegisterW** (Unicode) and **DsRestoreRegisterA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="058cb-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="058cb-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="058cb-169">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="058cb-169">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="058cb-170">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="058cb-170">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="058cb-171">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="058cb-171">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="058cb-172">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="058cb-172">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> <dt>

[<span data-ttu-id="058cb-173">**\_RSTMAP EDB**</span><span class="sxs-lookup"><span data-stu-id="058cb-173">**EDB\_RSTMAP**</span></span>](edb-rstmap.md)
</dt> <dt>

[<span data-ttu-id="058cb-174">Restaurando Active Directory</span><span class="sxs-lookup"><span data-stu-id="058cb-174">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="058cb-175">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="058cb-175">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

