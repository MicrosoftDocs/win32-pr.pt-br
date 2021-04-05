---
title: Função DsSetCurrentBackupLog (Ntdsbcli. h)
description: Define o número do log de backup atual após uma restauração bem-sucedida.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Função DsSetCurrentBackupLog Active Directory
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824536"
---
# <a name="dssetcurrentbackuplog-function"></a><span data-ttu-id="21108-104">Função DsSetCurrentBackupLog</span><span class="sxs-lookup"><span data-stu-id="21108-104">DsSetCurrentBackupLog function</span></span>

<span data-ttu-id="21108-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="21108-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="21108-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="21108-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="21108-107">A partir do Windows Vista, use [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="21108-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="21108-108">A função **DsSetCurrentBackupLog** define o número do log de backup atual após uma restauração bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="21108-108">The **DsSetCurrentBackupLog** function sets the current backup log number after a successful restore.</span></span> <span data-ttu-id="21108-109">Como Active Directory Domain Services dá suporte apenas ao registro em log circular, essa função não é usada normalmente.</span><span class="sxs-lookup"><span data-stu-id="21108-109">Because Active Directory Domain Services only support circular logging, this function is not normally used.</span></span>

## <a name="syntax"></a><span data-ttu-id="21108-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21108-110">Syntax</span></span>


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a><span data-ttu-id="21108-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21108-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21108-112">*szServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="21108-112">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21108-113">Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do servidor para o qual definir o número de log de backup.</span><span class="sxs-lookup"><span data-stu-id="21108-113">Pointer to a null-terminated string that contains the name of the server to set the backup log number for.</span></span> <span data-ttu-id="21108-114">Barras invertidas precedentes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="21108-114">Preceding backslashes are optional.</span></span> <span data-ttu-id="21108-115">O servidor deve ser o mesmo computador do qual essa função é chamada.</span><span class="sxs-lookup"><span data-stu-id="21108-115">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="21108-116">O nome do servidor não pode conter nenhum caractere de sublinhado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="21108-116">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="21108-117">Um exemplo de um nome de servidor é " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="21108-117">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="21108-118">*dwCurrentLog* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="21108-118">*dwCurrentLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21108-119">Contém o número do log de backup a ser definido.</span><span class="sxs-lookup"><span data-stu-id="21108-119">Contains the backup log number to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21108-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21108-120">Return value</span></span>

<span data-ttu-id="21108-121">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="21108-121">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="21108-122">A lista a seguir lista os possíveis códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="21108-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="21108-123">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="21108-123">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="21108-124">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="21108-124">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="21108-125">**ERRO \_ de \_ memória insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="21108-125">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="21108-126">Ocorreu uma falha de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="21108-126">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21108-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="21108-127">Remarks</span></span>

<span data-ttu-id="21108-128">Normalmente, não é necessário chamar a função **DsSetCurrentBackupLog** .</span><span class="sxs-lookup"><span data-stu-id="21108-128">It is not normally required to call the **DsSetCurrentBackupLog** function.</span></span> <span data-ttu-id="21108-129">As funções de backup determinam e definem automaticamente o backup do último número de log.</span><span class="sxs-lookup"><span data-stu-id="21108-129">The backup functions automatically determine and set the last log number backed up.</span></span> <span data-ttu-id="21108-130">Use **DsSetCurrentBackupLog** para impedir que outro backup incremental seja realizado com sucesso até que um backup completo seja executado.</span><span class="sxs-lookup"><span data-stu-id="21108-130">Use **DsSetCurrentBackupLog** to prevent another incremental backup from succeeding until a full backup is performed.</span></span>

## <a name="requirements"></a><span data-ttu-id="21108-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21108-131">Requirements</span></span>



| <span data-ttu-id="21108-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="21108-132">Requirement</span></span> | <span data-ttu-id="21108-133">Valor</span><span class="sxs-lookup"><span data-stu-id="21108-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21108-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21108-134">Minimum supported client</span></span><br/> | <span data-ttu-id="21108-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21108-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21108-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21108-136">Minimum supported server</span></span><br/> | <span data-ttu-id="21108-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21108-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21108-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21108-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="21108-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="21108-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="21108-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21108-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="21108-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21108-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="21108-142">DLL</span><span class="sxs-lookup"><span data-stu-id="21108-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21108-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21108-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="21108-144">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="21108-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="21108-145">**DsSetCurrentBackupLogW** (Unicode) e **DsSetCurrentBackupLogA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="21108-145">**DsSetCurrentBackupLogW** (Unicode) and **DsSetCurrentBackupLogA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="21108-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="21108-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21108-147">Fazendo backup e restaurando um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="21108-147">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="21108-148">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="21108-148">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

