---
title: Função DsBackupOpenFile (Ntdsbcli. h)
description: Abre o arquivo especificado e executa as operações de cliente e servidor necessárias para preparar o arquivo para backup.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Função DsBackupOpenFile Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085681"
---
# <a name="dsbackupopenfile-function"></a><span data-ttu-id="af80e-104">Função DsBackupOpenFile</span><span class="sxs-lookup"><span data-stu-id="af80e-104">DsBackupOpenFile function</span></span>

<span data-ttu-id="af80e-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="af80e-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af80e-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="af80e-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="af80e-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="af80e-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="af80e-108">A função **DsBackupOpenFile** abre o arquivo especificado e executa as operações de cliente e servidor necessárias para preparar o arquivo para backup.</span><span class="sxs-lookup"><span data-stu-id="af80e-108">The **DsBackupOpenFile** function opens the specified file and performs the client and server operations necessary to prepare the file for backup.</span></span>

## <a name="syntax"></a><span data-ttu-id="af80e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af80e-109">Syntax</span></span>


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a><span data-ttu-id="af80e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af80e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af80e-111">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af80e-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af80e-112">Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="af80e-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="af80e-113">*szAttachmentName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af80e-113">*szAttachmentName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af80e-114">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do arquivo de backup a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="af80e-114">Pointer to a null-terminated string that specifies the name of the backup file to open.</span></span>

</dd> <dt>

<span data-ttu-id="af80e-115">*cbReadHintSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af80e-115">*cbReadHintSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af80e-116">Contém o tamanho possível, em bytes, do buffer passado como o argumento *pvBuffer* na função [**DsBackupRead**](dsbackupread.md) .</span><span class="sxs-lookup"><span data-stu-id="af80e-116">Contains the possible size, in bytes, of the buffer passed as the *pvBuffer* argument in the [**DsBackupRead**](dsbackupread.md) function.</span></span> <span data-ttu-id="af80e-117">As funções de backup usam esse valor como uma dica para otimizar o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="af80e-117">The backup functions use this value as a hint to optimize the network traffic.</span></span> <span data-ttu-id="af80e-118">Esse valor deve ser um múltiplo de 8192 e deve ser maior ou igual a 24576.</span><span class="sxs-lookup"><span data-stu-id="af80e-118">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="af80e-119">*pliFileSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="af80e-119">*pliFileSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af80e-120">Ponteiro para um **valor \_ inteiro grande** que recebe o tamanho, em bytes, do arquivo de backup aberto.</span><span class="sxs-lookup"><span data-stu-id="af80e-120">Pointer to a **LARGE\_INTEGER** value that receives the size, in bytes, of the backup file opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af80e-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af80e-121">Return value</span></span>

<span data-ttu-id="af80e-122">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="af80e-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="af80e-123">A lista a seguir lista outros códigos de erro possíveis.</span><span class="sxs-lookup"><span data-stu-id="af80e-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="af80e-124">**ERRO de \_ acesso \_ negado**</span><span class="sxs-lookup"><span data-stu-id="af80e-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="af80e-125">O chamador não tem os privilégios de acesso apropriados para chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="af80e-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="af80e-126">A função [**DsSetAuthIdentity**](dssetauthidentity.md) pode ser usada para definir as credenciais a serem usadas para as funções de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="af80e-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="af80e-127">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="af80e-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="af80e-128">*HBC*, *szAttachmentName* ou *pliFileSize* são inválidos.</span><span class="sxs-lookup"><span data-stu-id="af80e-128">*hbc*, *szAttachmentName*, or *pliFileSize* are invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af80e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af80e-129">Requirements</span></span>



| <span data-ttu-id="af80e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="af80e-130">Requirement</span></span> | <span data-ttu-id="af80e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="af80e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af80e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af80e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="af80e-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af80e-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af80e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af80e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="af80e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af80e-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af80e-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af80e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="af80e-137"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="af80e-137"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="af80e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af80e-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="af80e-139"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af80e-139"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="af80e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="af80e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af80e-141"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af80e-141"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="af80e-142">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="af80e-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="af80e-143">**DsBackupOpenFileW** (Unicode) e **DsBackupOpenFileA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="af80e-143">**DsBackupOpenFileW** (Unicode) and **DsBackupOpenFileA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="af80e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="af80e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af80e-145">**DsBackupRead**</span><span class="sxs-lookup"><span data-stu-id="af80e-145">**DsBackupRead**</span></span>](dsbackupread.md)
</dt> <dt>

[<span data-ttu-id="af80e-146">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="af80e-146">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="af80e-147">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="af80e-147">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

