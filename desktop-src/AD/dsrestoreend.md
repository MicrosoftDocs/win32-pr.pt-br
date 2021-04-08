---
title: Função DsRestoreEnd (Ntdsbcli. h)
description: Chamado para encerrar uma operação de restauração.
ms.assetid: 2c3b9aba-3e92-4e5b-afff-3ed9bf64832b
ms.tgt_platform: multiple
keywords:
- Função DsRestoreEnd Active Directory
topic_type:
- apiref
api_name:
- DsRestoreEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabbe216875c2fe934f3c87e32688cd17bc8992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009275"
---
# <a name="dsrestoreend-function"></a><span data-ttu-id="fef00-104">Função DsRestoreEnd</span><span class="sxs-lookup"><span data-stu-id="fef00-104">DsRestoreEnd function</span></span>

<span data-ttu-id="fef00-105">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="fef00-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fef00-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fef00-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fef00-107">Em vez disso, use o [serviço de cópias de sombra de volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="fef00-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="fef00-108">A função **DsRestoreEnd** é chamada para encerrar uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="fef00-108">The **DsRestoreEnd** function is called to terminate a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef00-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fef00-109">Syntax</span></span>


```C++
HRESULT DsRestoreEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="fef00-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fef00-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fef00-111">*HBC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fef00-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef00-112">Contém o identificador de contexto de restauração obtido com a função [**DsRestorePrepare**](dsrestoreprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="fef00-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fef00-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fef00-113">Return value</span></span>

<span data-ttu-id="fef00-114">Retornará **S \_ OK** se a função for bem-sucedida, ou um código de erro Win32 ou RPC.</span><span class="sxs-lookup"><span data-stu-id="fef00-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="fef00-115">A lista a seguir lista os possíveis códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="fef00-115">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="fef00-116">**\_parâmetro inválido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="fef00-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="fef00-117">*HBC* não é válido.</span><span class="sxs-lookup"><span data-stu-id="fef00-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fef00-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fef00-118">Remarks</span></span>

<span data-ttu-id="fef00-119">A função **DsRestoreEnd** fecha identificadores de associação pendentes e executa uma operação de limpeza após uma tentativa de restauração.</span><span class="sxs-lookup"><span data-stu-id="fef00-119">The **DsRestoreEnd** function closes outstanding binding handles and performs a cleanup operation after a restore attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="fef00-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fef00-120">Requirements</span></span>



| <span data-ttu-id="fef00-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef00-121">Requirement</span></span> | <span data-ttu-id="fef00-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fef00-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fef00-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fef00-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fef00-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fef00-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fef00-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fef00-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fef00-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fef00-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fef00-127">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fef00-127">End of client support</span></span><br/>    | <span data-ttu-id="fef00-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fef00-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fef00-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="fef00-129">End of server support</span></span><br/>    | <span data-ttu-id="fef00-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fef00-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fef00-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fef00-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fef00-132"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef00-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="fef00-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fef00-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="fef00-134"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fef00-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="fef00-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fef00-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fef00-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fef00-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef00-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="fef00-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef00-138">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="fef00-138">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="fef00-139">Restaurando um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="fef00-139">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="fef00-140">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="fef00-140">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

