---
title: Função DsBackupRead (Ntdsbcli. h)
description: Lê um bloco de dados do arquivo aberto atual em um buffer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Função DsBackupRead Active Directory
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918354"
---
# <a name="dsbackupread-function"></a><span data-ttu-id="e698f-104">Função DsBackupRead</span><span class="sxs-lookup"><span data-stu-id="e698f-104">DsBackupRead function</span></span>

<span data-ttu-id="e698f-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e698f-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e698f-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e698f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e698f-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="e698f-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="e698f-108">A função **DsBackupRead** lê um bloco de dados do arquivo aberto atual em um buffer.</span><span class="sxs-lookup"><span data-stu-id="e698f-108">The **DsBackupRead** function reads a block of data from the current open file, into a buffer.</span></span> <span data-ttu-id="e698f-109">O aplicativo cliente deve chamar essa função repetidamente até que todo o arquivo de backup tenha sido recebido.</span><span class="sxs-lookup"><span data-stu-id="e698f-109">The client application is expected to call this function repeatedly until the entire backup file has been received.</span></span> <span data-ttu-id="e698f-110">A função [**DsBackupOpenFile**](dsbackupopenfile.md) fornece todo o tamanho do arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="e698f-110">The [**DsBackupOpenFile**](dsbackupopenfile.md) function provides the entire size of the backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e698f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e698f-111">Syntax</span></span>


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="e698f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e698f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e698f-113">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e698f-113">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e698f-114">Contém o identificador de contexto de backup obtido com a função [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="e698f-114">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e698f-115">*pvBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e698f-115">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e698f-116">Ponteiro para um buffer que recebe os dados.</span><span class="sxs-lookup"><span data-stu-id="e698f-116">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="e698f-117">Esse buffer deve ter pelo menos *cbBuffer* bytes de tamanho.</span><span class="sxs-lookup"><span data-stu-id="e698f-117">This buffer must be at least *cbBuffer* bytes in size.</span></span>

</dd> <dt>

<span data-ttu-id="e698f-118">*cbBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e698f-118">*cbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e698f-119">Contém o tamanho, em bytes, do buffer em *pvBuffer*.</span><span class="sxs-lookup"><span data-stu-id="e698f-119">Contains the size, in bytes, of the buffer at *pvBuffer*.</span></span> <span data-ttu-id="e698f-120">Esse valor deve ser um múltiplo de 8192 e deve ser maior ou igual a 24576.</span><span class="sxs-lookup"><span data-stu-id="e698f-120">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="e698f-121">*pcbRead* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e698f-121">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e698f-122">Ponteiro para um valor **DWORD** que recebe o número real de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="e698f-122">Pointer to a **DWORD** value that receives the actual number of bytes read.</span></span> <span data-ttu-id="e698f-123">Isso pode ser menor que o número de bytes solicitados porque alguns transportes fragmentam o buffer que está sendo transmitido em vez de preencher todo o buffer com os dados.</span><span class="sxs-lookup"><span data-stu-id="e698f-123">This may be less than the number of bytes requested because some transports fragment the buffer being transmitted instead of filling the entire buffer with data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e698f-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e698f-124">Return value</span></span>

<span data-ttu-id="e698f-125">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="e698f-125">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="e698f-126">Os códigos de erro possíveis incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="e698f-126">Possible error codes include the following.</span></span>

<dl> <dt>

<span data-ttu-id="e698f-127">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="e698f-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="e698f-128">Um ou mais parâmetros não são válidos.</span><span class="sxs-lookup"><span data-stu-id="e698f-128">One or more parameters are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e698f-129">**identificador de erro \_ \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="e698f-129">**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd>

<span data-ttu-id="e698f-130">O fim do arquivo de backup foi atingido.</span><span class="sxs-lookup"><span data-stu-id="e698f-130">The end of the backup file was reached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e698f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e698f-131">Requirements</span></span>



| <span data-ttu-id="e698f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e698f-132">Requirement</span></span> | <span data-ttu-id="e698f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e698f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e698f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e698f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e698f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e698f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e698f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e698f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e698f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e698f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e698f-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e698f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e698f-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="e698f-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="e698f-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e698f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="e698f-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e698f-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="e698f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e698f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e698f-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e698f-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e698f-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e698f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e698f-145">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="e698f-145">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="e698f-146">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="e698f-146">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="e698f-147">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="e698f-147">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="e698f-148">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="e698f-148">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="e698f-149">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="e698f-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

