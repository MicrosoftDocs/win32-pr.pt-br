---
title: Função RasAdminPortGetInfo (Rassapi. h)
description: A função RasAdminPortGetInfo recupera informações sobre uma porta especificada em um servidor especificado.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- Função RasAdminPortGetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785396"
---
# <a name="rasadminportgetinfo-function"></a><span data-ttu-id="31ca1-104">Função RasAdminPortGetInfo</span><span class="sxs-lookup"><span data-stu-id="31ca1-104">RasAdminPortGetInfo function</span></span>

<span data-ttu-id="31ca1-105">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="31ca1-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="31ca1-106">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="31ca1-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="31ca1-107">Os aplicativos devem usar a função [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="31ca1-107">Applications should use the [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) function.\]</span></span>

<span data-ttu-id="31ca1-108">A função **RasAdminPortGetInfo** recupera informações sobre uma porta especificada em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="31ca1-108">The **RasAdminPortGetInfo** function retrieves information about a specified port on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ca1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31ca1-109">Syntax</span></span>


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a><span data-ttu-id="31ca1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31ca1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ca1-111">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31ca1-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ca1-112">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="31ca1-112">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="31ca1-113">Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="31ca1-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="31ca1-114">*lpszPort* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31ca1-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ca1-115">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta no servidor.</span><span class="sxs-lookup"><span data-stu-id="31ca1-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> <dt>

<span data-ttu-id="31ca1-116">*pRasPort1* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31ca1-116">*pRasPort1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31ca1-117">Ponteiro para a estrutura da [**porta do RAS \_ \_ 1**](ras-port-1-str.md) que a função preenche com informações sobre o estado da porta.</span><span class="sxs-lookup"><span data-stu-id="31ca1-117">Pointer to the [**RAS\_PORT\_1**](ras-port-1-str.md) structure that the function fills in with information about the state of the port.</span></span>

</dd> <dt>

<span data-ttu-id="31ca1-118">*pRasStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31ca1-118">*pRasStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31ca1-119">Ponteiro para a estrutura de [**\_ \_ Estatísticas de porta de Ras**](ras-port-statistics-str.md) que a função preenche com estatísticas sobre a porta.</span><span class="sxs-lookup"><span data-stu-id="31ca1-119">Pointer to the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure that the function fills in with statistics about the port.</span></span>

</dd> <dt>

<span data-ttu-id="31ca1-120">*ppRasParams* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31ca1-120">*ppRasParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31ca1-121">Ponteiro para uma variável de ponteiro que recebe o endereço de uma matriz de estruturas de [**\_ parâmetros de Ras**](ras-parameters-str.md) .</span><span class="sxs-lookup"><span data-stu-id="31ca1-121">Pointer to a pointer variable that receives the address of an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures.</span></span> <span data-ttu-id="31ca1-122">Cada estrutura contém o nome de uma chave específica de mídia, como MAXCONNECTBPS, e seu valor associado.</span><span class="sxs-lookup"><span data-stu-id="31ca1-122">Each structure contains the name of a media-specific key, such as MAXCONNECTBPS, and its associated value.</span></span> <span data-ttu-id="31ca1-123">Quando o aplicativo for concluído com essa memória, libere-o chamando a função [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="31ca1-123">When the application is finished with this memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ca1-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31ca1-124">Return value</span></span>

<span data-ttu-id="31ca1-125">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="31ca1-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="31ca1-126">Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="31ca1-126">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="31ca1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="31ca1-127">Value</span></span>                                                                                                     | <span data-ttu-id="31ca1-128">Significado</span><span class="sxs-lookup"><span data-stu-id="31ca1-128">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31ca1-129"><dt>**\_desenvolvimento de \_ erro \_ inexistente**</dt></span><span class="sxs-lookup"><span data-stu-id="31ca1-129"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl>     | <span data-ttu-id="31ca1-130">A porta especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="31ca1-130">The specified port is invalid.</span></span><br/>                                        |
| <dl> <span data-ttu-id="31ca1-131"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31ca1-131"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="31ca1-132">Memória insuficiente para alocar um buffer para a matriz *ppRasParams* .</span><span class="sxs-lookup"><span data-stu-id="31ca1-132">Insufficient memory to allocate a buffer for the *ppRasParams* array.</span></span><br/> |



 

<span data-ttu-id="31ca1-133">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="31ca1-133">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="31ca1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31ca1-134">Requirements</span></span>



| <span data-ttu-id="31ca1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="31ca1-135">Requirement</span></span> | <span data-ttu-id="31ca1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="31ca1-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31ca1-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="31ca1-137">End of client support</span></span><br/> | <span data-ttu-id="31ca1-138">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="31ca1-138">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="31ca1-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="31ca1-139">End of server support</span></span><br/> | <span data-ttu-id="31ca1-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31ca1-140">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="31ca1-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31ca1-141">Header</span></span><br/>                | <dl> <span data-ttu-id="31ca1-142"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="31ca1-142"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="31ca1-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31ca1-143">Library</span></span><br/>               | <dl> <span data-ttu-id="31ca1-144"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31ca1-144"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="31ca1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="31ca1-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="31ca1-146"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31ca1-146"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31ca1-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="31ca1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ca1-148">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="31ca1-148">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="31ca1-149">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="31ca1-149">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="31ca1-150">**parâmetros de RAS \_**</span><span class="sxs-lookup"><span data-stu-id="31ca1-150">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="31ca1-151">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="31ca1-151">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="31ca1-152">**\_Estatísticas de porta RAS \_**</span><span class="sxs-lookup"><span data-stu-id="31ca1-152">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="31ca1-153">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="31ca1-153">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

