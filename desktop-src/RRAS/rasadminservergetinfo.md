---
title: Função RasAdminServerGetInfo (Rassapi. h)
description: A função RasAdminServerGetInfo Obtém a configuração de servidor de um servidor RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- Função RasAdminServerGetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782293"
---
# <a name="rasadminservergetinfo-function"></a><span data-ttu-id="c0fea-104">Função RasAdminServerGetInfo</span><span class="sxs-lookup"><span data-stu-id="c0fea-104">RasAdminServerGetInfo function</span></span>

<span data-ttu-id="c0fea-105">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="c0fea-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="c0fea-106">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c0fea-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="c0fea-107">Os aplicativos devem usar a função [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="c0fea-107">Applications should use the [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) function.\]</span></span>

<span data-ttu-id="c0fea-108">A função **RasAdminServerGetInfo** Obtém a configuração de servidor de um servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="c0fea-108">The **RasAdminServerGetInfo** function gets the server configuration of a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0fea-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0fea-109">Syntax</span></span>


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a><span data-ttu-id="c0fea-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0fea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0fea-111">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0fea-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0fea-112">Ponteiro para uma cadeia de caracteres Unicode terminada em **nulo** que especifica o nome do servidor RAS do Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c0fea-112">Pointer to a **null**-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="c0fea-113">Se esse parâmetro for **nulo**, a função retornará informações sobre o computador local.</span><span class="sxs-lookup"><span data-stu-id="c0fea-113">If this parameter is **NULL**, the function returns information about the local computer.</span></span> <span data-ttu-id="c0fea-114">Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="c0fea-114">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="c0fea-115">*pRasServer0* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c0fea-115">*pRasServer0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0fea-116">Ponteiro para a estrutura do [**\_ servidor RAS \_ 0**](ras-server-0-str.md) que recebe o número de portas configuradas no servidor, o número de portas em uso no momento e o número de versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="c0fea-116">Pointer to the [**RAS\_SERVER\_0**](ras-server-0-str.md) structure that receives the number of ports configured on the server, the number of ports currently in use, and the server version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0fea-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0fea-117">Return value</span></span>

<span data-ttu-id="c0fea-118">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="c0fea-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c0fea-119">Se a função falhar, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="c0fea-119">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="c0fea-120">Os códigos de erro possíveis incluem aqueles retornados por [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para a função [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="c0fea-120">Possible error codes include those returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) function.</span></span> <span data-ttu-id="c0fea-121">Não há informações de erro estendidas para esta função; Não chame **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="c0fea-121">There is no extended error information for this function; do not call **GetLastError**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0fea-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0fea-122">Remarks</span></span>

<span data-ttu-id="c0fea-123">Para enumerar todos os servidores RAS em um domínio, chame a função [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) e especifique a \_ \_ discagem do tipo VA para o parâmetro *ServerType* .</span><span class="sxs-lookup"><span data-stu-id="c0fea-123">To enumerate all RAS servers in a domain, call the [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) function and specify SV\_TYPE\_DIALIN for the *servertype* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0fea-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0fea-124">Requirements</span></span>



| <span data-ttu-id="c0fea-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0fea-125">Requirement</span></span> | <span data-ttu-id="c0fea-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c0fea-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fea-127">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c0fea-127">End of client support</span></span><br/> | <span data-ttu-id="c0fea-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c0fea-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="c0fea-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c0fea-129">End of server support</span></span><br/> | <span data-ttu-id="c0fea-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c0fea-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="c0fea-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0fea-131">Header</span></span><br/>                | <dl> <span data-ttu-id="c0fea-132"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0fea-132"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0fea-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0fea-133">Library</span></span><br/>               | <dl> <span data-ttu-id="c0fea-134"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0fea-134"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0fea-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c0fea-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c0fea-136"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0fea-136"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0fea-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0fea-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0fea-138">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="c0fea-138">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c0fea-139">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="c0fea-139">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="c0fea-140">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="c0fea-140">**NetServerEnum**</span></span>](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[<span data-ttu-id="c0fea-141">**\_Servidor RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c0fea-141">**RAS\_SERVER\_0**</span></span>](ras-server-0-str.md)
</dt> </dl>

 

