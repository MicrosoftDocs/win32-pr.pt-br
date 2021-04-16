---
title: Função RasAdminPortClearStatistics (Rassapi. h)
description: A função RasAdminPortClearStatistics redefine os contadores que representam as várias estatísticas relatadas pela função RasAdminPortGetInfo na \_ estrutura de estatísticas de porta de Ras \_ . Os contadores são redefinidos para zero e começam a acumular.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- Função RasAdminPortClearStatistics RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750105"
---
# <a name="rasadminportclearstatistics-function"></a><span data-ttu-id="12ff8-105">Função RasAdminPortClearStatistics</span><span class="sxs-lookup"><span data-stu-id="12ff8-105">RasAdminPortClearStatistics function</span></span>

<span data-ttu-id="12ff8-106">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="12ff8-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="12ff8-107">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="12ff8-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="12ff8-108">Os aplicativos devem usar a função [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]</span><span class="sxs-lookup"><span data-stu-id="12ff8-108">Applications should use the [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) function.\]</span></span>

<span data-ttu-id="12ff8-109">A função **RasAdminPortClearStatistics** redefine os contadores que representam as várias estatísticas relatadas pela função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) na estrutura de [**\_ \_ Estatísticas de porta de Ras**](ras-port-statistics-str.md) .</span><span class="sxs-lookup"><span data-stu-id="12ff8-109">The **RasAdminPortClearStatistics** function resets the counters representing the various statistics reported by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function in the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure.</span></span> <span data-ttu-id="12ff8-110">Os contadores são redefinidos para zero e começam a acumular.</span><span class="sxs-lookup"><span data-stu-id="12ff8-110">The counters are reset to zero and start accumulating.</span></span>

## <a name="syntax"></a><span data-ttu-id="12ff8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12ff8-111">Syntax</span></span>


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="12ff8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12ff8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ff8-113">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12ff8-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ff8-114">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="12ff8-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="12ff8-115">Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="12ff8-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="12ff8-116">*lpszPort* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12ff8-116">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ff8-117">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta no servidor.</span><span class="sxs-lookup"><span data-stu-id="12ff8-117">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ff8-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12ff8-118">Return value</span></span>

<span data-ttu-id="12ff8-119">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="12ff8-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="12ff8-120">Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.</span><span class="sxs-lookup"><span data-stu-id="12ff8-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="12ff8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="12ff8-121">Value</span></span>                                                                                                 | <span data-ttu-id="12ff8-122">Significado</span><span class="sxs-lookup"><span data-stu-id="12ff8-122">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="12ff8-123"><dt>**\_desenvolvimento de \_ erro \_ inexistente**</dt></span><span class="sxs-lookup"><span data-stu-id="12ff8-123"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="12ff8-124">A porta especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="12ff8-124">The specified port is invalid.</span></span><br/> |



 

<span data-ttu-id="12ff8-125">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="12ff8-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="12ff8-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="12ff8-126">Remarks</span></span>

<span data-ttu-id="12ff8-127">A função **RasAdminPortClearStatistics** limpa as estatísticas no servidor, não localmente no aplicativo que faz a chamada.</span><span class="sxs-lookup"><span data-stu-id="12ff8-127">The **RasAdminPortClearStatistics** function clears the statistics on the server, not locally within the application that makes the call.</span></span> <span data-ttu-id="12ff8-128">Isso significa que as estatísticas também são redefinidas para qualquer outro aplicativo que esteja monitorando a porta especificada.</span><span class="sxs-lookup"><span data-stu-id="12ff8-128">This means that the statistics are also reset for any other application that is monitoring the specified port.</span></span>

<span data-ttu-id="12ff8-129">Se a porta *lpszPort* fizer parte de uma conexão Multilink, o **RasAdminPortClearStatistics** redefinirá as estatísticas para a porta especificada, a função também redefinirá as estatísticas cumulativas para a conexão de vínculos múltiplos.</span><span class="sxs-lookup"><span data-stu-id="12ff8-129">If the *lpszPort* port is part of a multilink connection, **RasAdminPortClearStatistics** resets the statistics for the specified port, The function also resets the cumulative statistics for the multilink connection.</span></span> <span data-ttu-id="12ff8-130">No entanto, a função não afeta as estatísticas individuais para outras portas que fazem parte da conexão de vínculos múltiplos.</span><span class="sxs-lookup"><span data-stu-id="12ff8-130">However, the function does not effect the individual statistics for other ports that are part of the multilink connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ff8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12ff8-131">Requirements</span></span>



| <span data-ttu-id="12ff8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ff8-132">Requirement</span></span> | <span data-ttu-id="12ff8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="12ff8-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12ff8-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="12ff8-134">End of client support</span></span><br/> | <span data-ttu-id="12ff8-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="12ff8-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="12ff8-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="12ff8-136">End of server support</span></span><br/> | <span data-ttu-id="12ff8-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12ff8-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="12ff8-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12ff8-138">Header</span></span><br/>                | <dl> <span data-ttu-id="12ff8-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="12ff8-139"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="12ff8-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12ff8-140">Library</span></span><br/>               | <dl> <span data-ttu-id="12ff8-141"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12ff8-141"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="12ff8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="12ff8-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="12ff8-143"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12ff8-143"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ff8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="12ff8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ff8-145">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="12ff8-145">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="12ff8-146">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="12ff8-146">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="12ff8-147">**\_Estatísticas de porta RAS \_**</span><span class="sxs-lookup"><span data-stu-id="12ff8-147">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="12ff8-148">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="12ff8-148">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

