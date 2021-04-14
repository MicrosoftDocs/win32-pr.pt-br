---
title: Função DsBackupClose (Ntdsbcli. h)
description: Fecha um arquivo de backup aberto com a função DsBackupOpenFile.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Função DsBackupClose Active Directory
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455027"
---
# <a name="dsbackupclose-function"></a><span data-ttu-id="ecace-104">Função DsBackupClose</span><span class="sxs-lookup"><span data-stu-id="ecace-104">DsBackupClose function</span></span>

<span data-ttu-id="ecace-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ecace-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ecace-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ecace-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ecace-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="ecace-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="ecace-108">A função **DsBackupClose** fecha um arquivo de backup aberto com a função [**DsBackupOpenFile**](dsbackupopenfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ecace-108">The **DsBackupClose** function closes a backup file opened with the [**DsBackupOpenFile**](dsbackupopenfile.md) function.</span></span> <span data-ttu-id="ecace-109">Para cada identificador de backup, somente um arquivo pode ser aberto por vez, portanto, essa função fecha o arquivo aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="ecace-109">For each backup handle, only one file can be opened at a time, so this function closes the currently open file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecace-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecace-110">Syntax</span></span>


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="ecace-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecace-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecace-112">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecace-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecace-113">Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="ecace-113">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecace-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ecace-114">Return value</span></span>

<span data-ttu-id="ecace-115">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="ecace-115">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="ecace-116">A lista a seguir lista outros códigos de erro possíveis.</span><span class="sxs-lookup"><span data-stu-id="ecace-116">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="ecace-117">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="ecace-117">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="ecace-118">*HBC* não é válido.</span><span class="sxs-lookup"><span data-stu-id="ecace-118">*hbc* is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ecace-119">**hrInvalidHandle**</span><span class="sxs-lookup"><span data-stu-id="ecace-119">**hrInvalidHandle**</span></span>
</dt> <dd>

<span data-ttu-id="ecace-120">Nenhum arquivo está aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="ecace-120">No file is currently open.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecace-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecace-121">Requirements</span></span>



| <span data-ttu-id="ecace-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecace-122">Requirement</span></span> | <span data-ttu-id="ecace-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ecace-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecace-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecace-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ecace-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecace-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ecace-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecace-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ecace-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecace-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ecace-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ecace-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecace-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecace-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecace-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ecace-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecace-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecace-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="ecace-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ecace-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecace-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecace-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecace-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecace-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecace-135">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="ecace-135">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="ecace-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="ecace-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="ecace-137">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="ecace-137">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="ecace-138">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="ecace-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

