---
title: Função DsBackupTruncateLogs (Ntdsbcli. h)
description: Trunca os logs de backup lidos anteriormente.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Função DsBackupTruncateLogs Active Directory
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499337"
---
# <a name="dsbackuptruncatelogs-function"></a><span data-ttu-id="98c37-104">Função DsBackupTruncateLogs</span><span class="sxs-lookup"><span data-stu-id="98c37-104">DsBackupTruncateLogs function</span></span>

<span data-ttu-id="98c37-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="98c37-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="98c37-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="98c37-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="98c37-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="98c37-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="98c37-108">A função **DsBackupTruncateLogs** trunca os logs de backup lidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="98c37-108">The **DsBackupTruncateLogs** function truncates the previously read backup logs.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c37-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98c37-109">Syntax</span></span>


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="98c37-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98c37-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c37-111">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98c37-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c37-112">Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="98c37-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c37-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98c37-113">Return value</span></span>

<span data-ttu-id="98c37-114">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="98c37-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="98c37-115">A lista a seguir lista outros códigos de erro possíveis.</span><span class="sxs-lookup"><span data-stu-id="98c37-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="98c37-116">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="98c37-116">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="98c37-117">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="98c37-117">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="98c37-118">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="98c37-118">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="98c37-119">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="98c37-119">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="98c37-120">*HBC* é inválido.</span><span class="sxs-lookup"><span data-stu-id="98c37-120">*hbc* is invalid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98c37-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="98c37-121">Remarks</span></span>

<span data-ttu-id="98c37-122">Use a função **DsBackupTruncateLogs** quando um backup completo ou incremental tiver sido concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="98c37-122">Use the **DsBackupTruncateLogs** function when a full or incremental backup has completed successfully.</span></span>

> [!Caution]  
> <span data-ttu-id="98c37-123">Se essa função for chamada após um backup diferencial, todas as informações de backup incremental serão perdidas.</span><span class="sxs-lookup"><span data-stu-id="98c37-123">If this function is called after a differential backup, all of the incremental backup information will be lost.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98c37-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c37-124">Requirements</span></span>



| <span data-ttu-id="98c37-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c37-125">Requirement</span></span> | <span data-ttu-id="98c37-126">Valor</span><span class="sxs-lookup"><span data-stu-id="98c37-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98c37-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98c37-127">Minimum supported client</span></span><br/> | <span data-ttu-id="98c37-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98c37-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98c37-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98c37-129">Minimum supported server</span></span><br/> | <span data-ttu-id="98c37-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98c37-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98c37-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98c37-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c37-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c37-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="98c37-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98c37-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="98c37-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98c37-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="98c37-135">DLL</span><span class="sxs-lookup"><span data-stu-id="98c37-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98c37-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98c37-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c37-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="98c37-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c37-138">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="98c37-138">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="98c37-139">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="98c37-139">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="98c37-140">**DsSetCurrentBackupLog**</span><span class="sxs-lookup"><span data-stu-id="98c37-140">**DsSetCurrentBackupLog**</span></span>](dssetcurrentbackuplog.md)
</dt> <dt>

[<span data-ttu-id="98c37-141">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="98c37-141">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="98c37-142">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="98c37-142">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

