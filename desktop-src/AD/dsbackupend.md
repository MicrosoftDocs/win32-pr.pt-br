---
title: Função DsBackupEnd (Ntdsbcli. h)
description: Chamado para encerrar uma operação de backup.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Função DsBackupEnd Active Directory
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824347"
---
# <a name="dsbackupend-function"></a><span data-ttu-id="8eb88-104">Função DsBackupEnd</span><span class="sxs-lookup"><span data-stu-id="8eb88-104">DsBackupEnd function</span></span>

<span data-ttu-id="8eb88-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8eb88-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8eb88-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8eb88-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8eb88-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="8eb88-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="8eb88-108">A função **DsBackupEnd** é chamada para encerrar uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="8eb88-108">The **DsBackupEnd** function is called to terminate a backup operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb88-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eb88-109">Syntax</span></span>


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="8eb88-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8eb88-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb88-111">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8eb88-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eb88-112">Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="8eb88-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb88-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8eb88-113">Return value</span></span>

<span data-ttu-id="8eb88-114">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="8eb88-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="8eb88-115">A lista a seguir lista outros códigos de erro possíveis.</span><span class="sxs-lookup"><span data-stu-id="8eb88-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="8eb88-116">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="8eb88-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="8eb88-117">*HBC* não é válido.</span><span class="sxs-lookup"><span data-stu-id="8eb88-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8eb88-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8eb88-118">Remarks</span></span>

<span data-ttu-id="8eb88-119">A função **DsBackupEnd** fecha identificadores de associação pendentes e executa uma limpeza após uma tentativa de backup bem-sucedida ou malsucedida.</span><span class="sxs-lookup"><span data-stu-id="8eb88-119">The **DsBackupEnd** function closes outstanding binding handles and performs a cleanup after a successful or unsuccessful backup attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb88-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eb88-120">Requirements</span></span>



| <span data-ttu-id="8eb88-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb88-121">Requirement</span></span> | <span data-ttu-id="8eb88-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8eb88-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb88-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eb88-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb88-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8eb88-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8eb88-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eb88-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb88-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8eb88-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8eb88-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8eb88-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eb88-128"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eb88-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="8eb88-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8eb88-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="8eb88-130"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8eb88-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="8eb88-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8eb88-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eb88-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eb88-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eb88-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eb88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb88-134">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="8eb88-134">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="8eb88-135">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="8eb88-135">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="8eb88-136">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="8eb88-136">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

