---
title: Função RasAdminFreeBuffer (Rassapi. h)
description: A função RasAdminFreeBuffer libera a memória que foi alocada pelo RAS em nome do chamador.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- Função RasAdminFreeBuffer RAS
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757739"
---
# <a name="rasadminfreebuffer-function"></a><span data-ttu-id="7ba7e-104">Função RasAdminFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7ba7e-104">RasAdminFreeBuffer function</span></span>

<span data-ttu-id="7ba7e-105">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="7ba7e-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="7ba7e-106">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7ba7e-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="7ba7e-107">Os aplicativos devem usar a função [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]</span><span class="sxs-lookup"><span data-stu-id="7ba7e-107">Applications should use the [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) function.\]</span></span>

<span data-ttu-id="7ba7e-108">A função **RasAdminFreeBuffer** libera a memória que foi alocada pelo RAS em nome do chamador.</span><span class="sxs-lookup"><span data-stu-id="7ba7e-108">The **RasAdminFreeBuffer** function frees memory that was allocated by RAS on behalf of the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba7e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ba7e-109">Syntax</span></span>


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a><span data-ttu-id="7ba7e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ba7e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ba7e-111">*Ponteiro* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7ba7e-111">*Pointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba7e-112">Ponteiro para o buffer a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="7ba7e-112">Pointer to the buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ba7e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ba7e-113">Return value</span></span>

<span data-ttu-id="7ba7e-114">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="7ba7e-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="7ba7e-115">Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.</span><span class="sxs-lookup"><span data-stu-id="7ba7e-115">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="7ba7e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7ba7e-116">Value</span></span>                                                                                                    | <span data-ttu-id="7ba7e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="7ba7e-117">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7ba7e-118"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7ba7e-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="7ba7e-119">O parâmetro de *ponteiro* é inválido.</span><span class="sxs-lookup"><span data-stu-id="7ba7e-119">The *Pointer* parameter is invalid.</span></span><br/> |



 

<span data-ttu-id="7ba7e-120">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="7ba7e-120">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ba7e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ba7e-121">Remarks</span></span>

<span data-ttu-id="7ba7e-122">Use a função **RasAdminFreeBuffer** para liberar os buffers alocados pelas funções [**RasAdminPortEnum**](rasadminportenum.md) e [**RasAdminPortGetInfo**](rasadminportgetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba7e-122">Use the **RasAdminFreeBuffer** function to free the buffers allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba7e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ba7e-123">Requirements</span></span>



| <span data-ttu-id="7ba7e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ba7e-124">Requirement</span></span> | <span data-ttu-id="7ba7e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7ba7e-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba7e-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7ba7e-126">End of client support</span></span><br/> | <span data-ttu-id="7ba7e-127">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7ba7e-127">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="7ba7e-128">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7ba7e-128">End of server support</span></span><br/> | <span data-ttu-id="7ba7e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ba7e-129">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="7ba7e-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ba7e-130">Header</span></span><br/>                | <dl> <span data-ttu-id="7ba7e-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ba7e-131"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ba7e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ba7e-132">Library</span></span><br/>               | <dl> <span data-ttu-id="7ba7e-133"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ba7e-133"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ba7e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7ba7e-134">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7ba7e-135"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ba7e-135"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ba7e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ba7e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba7e-137">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="7ba7e-137">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="7ba7e-138">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="7ba7e-138">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="7ba7e-139">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="7ba7e-139">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> <dt>

[<span data-ttu-id="7ba7e-140">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="7ba7e-140">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

