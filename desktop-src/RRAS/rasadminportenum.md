---
title: Função RasAdminPortEnum (Rassapi. h)
description: A função RasAdminPortEnum enumera todas as portas no servidor RAS especificado. Para cada porta no servidor, a função retorna a estrutura de \_ porta \_ 0 do RAS que contém informações sobre a porta.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- Função RasAdminPortEnum RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752346"
---
# <a name="rasadminportenum-function"></a><span data-ttu-id="c9958-105">Função RasAdminPortEnum</span><span class="sxs-lookup"><span data-stu-id="c9958-105">RasAdminPortEnum function</span></span>

<span data-ttu-id="c9958-106">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="c9958-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="c9958-107">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c9958-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="c9958-108">Os aplicativos devem usar a função [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]</span><span class="sxs-lookup"><span data-stu-id="c9958-108">Applications should use the [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) function.\]</span></span>

<span data-ttu-id="c9958-109">A função **RasAdminPortEnum** enumera todas as portas no servidor RAS especificado.</span><span class="sxs-lookup"><span data-stu-id="c9958-109">The **RasAdminPortEnum** function enumerates all ports on the specified RAS server.</span></span> <span data-ttu-id="c9958-110">Para cada porta no servidor, a função retorna a estrutura [**de \_ porta \_ 0 do RAS**](ras-port-0-str.md) que contém informações sobre a porta.</span><span class="sxs-lookup"><span data-stu-id="c9958-110">For each port on the server, the function returns the [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9958-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9958-111">Syntax</span></span>


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a><span data-ttu-id="c9958-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9958-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9958-113">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9958-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9958-114">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="c9958-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="c9958-115">Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="c9958-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="c9958-116">*ppRasPort0* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c9958-116">*ppRasPort0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9958-117">Ponteiro para uma variável que recebe um ponteiro para um buffer que contém uma matriz de estruturas de [**\_ porta RAS \_ 0**](ras-port-0-str.md) .</span><span class="sxs-lookup"><span data-stu-id="c9958-117">Pointer to a variable that receives a pointer to a buffer that contains an array of [**RAS\_PORT\_0**](ras-port-0-str.md) structures.</span></span> <span data-ttu-id="c9958-118">Quando o aplicativo for concluído com a memória, libere-o chamando a função [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c9958-118">When the application has finished with the memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c9958-119">*pcEntriesRead* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c9958-119">*pcEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9958-120">Ponteiro para uma variável de 16 bits que recebe o número total de estruturas de [**porta do RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) retornadas na matriz *ppRasPort0* .</span><span class="sxs-lookup"><span data-stu-id="c9958-120">Pointer to a 16-bit variable that receives the total number of [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) structures returned in the *ppRasPort0* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9958-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9958-121">Return value</span></span>

<span data-ttu-id="c9958-122">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="c9958-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c9958-123">Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.</span><span class="sxs-lookup"><span data-stu-id="c9958-123">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="c9958-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c9958-124">Value</span></span>                                                                                             | <span data-ttu-id="c9958-125">Significado</span><span class="sxs-lookup"><span data-stu-id="c9958-125">Meaning</span></span>                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9958-126"><dt>**NERR \_ ItemNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="c9958-126"><dt>**NERR\_ItemNotFound**</dt></span></span> </dl> | <span data-ttu-id="c9958-127">Nenhuma porta pode ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="c9958-127">No ports could be enumerated.</span></span> <span data-ttu-id="c9958-128">Isso pode ocorrer porque todas as portas configuradas no servidor estão sendo usadas para a discagem.</span><span class="sxs-lookup"><span data-stu-id="c9958-128">This could be because all configured ports on the server are currently being used for dialing out.</span></span><br/> |



 

<span data-ttu-id="c9958-129">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c9958-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9958-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9958-130">Requirements</span></span>



| <span data-ttu-id="c9958-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9958-131">Requirement</span></span> | <span data-ttu-id="c9958-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c9958-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9958-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c9958-133">End of client support</span></span><br/> | <span data-ttu-id="c9958-134">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c9958-134">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="c9958-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c9958-135">End of server support</span></span><br/> | <span data-ttu-id="c9958-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c9958-136">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="c9958-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9958-137">Header</span></span><br/>                | <dl> <span data-ttu-id="c9958-138"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9958-138"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9958-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9958-139">Library</span></span><br/>               | <dl> <span data-ttu-id="c9958-140"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9958-140"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c9958-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c9958-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c9958-142"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9958-142"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9958-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9958-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9958-144">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="c9958-144">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c9958-145">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="c9958-145">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="c9958-146">**\_Porta RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c9958-146">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="c9958-147">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="c9958-147">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

