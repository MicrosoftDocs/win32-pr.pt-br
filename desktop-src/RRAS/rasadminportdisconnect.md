---
title: Função RasAdminPortDisconnect (Rassapi. h)
description: A função RasAdminPortDisconnect desconecta uma porta que está em uso no momento.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- Função RasAdminPortDisconnect RAS
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759176"
---
# <a name="rasadminportdisconnect-function"></a><span data-ttu-id="3f580-104">Função RasAdminPortDisconnect</span><span class="sxs-lookup"><span data-stu-id="3f580-104">RasAdminPortDisconnect function</span></span>

<span data-ttu-id="3f580-105">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="3f580-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="3f580-106">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3f580-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="3f580-107">Os aplicativos devem usar a função [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]</span><span class="sxs-lookup"><span data-stu-id="3f580-107">Applications should use the [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) function.\]</span></span>

<span data-ttu-id="3f580-108">A função **RasAdminPortDisconnect** desconecta uma porta que está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="3f580-108">The **RasAdminPortDisconnect** function disconnects a port that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f580-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f580-109">Syntax</span></span>


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="3f580-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f580-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f580-111">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f580-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f580-112">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do servidor RAS do Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3f580-112">Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="3f580-113">Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="3f580-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="3f580-114">*lpszPort* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f580-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f580-115">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta no servidor.</span><span class="sxs-lookup"><span data-stu-id="3f580-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f580-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f580-116">Return value</span></span>

<span data-ttu-id="3f580-117">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="3f580-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3f580-118">Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="3f580-118">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="3f580-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3f580-119">Value</span></span>                                                                                               | <span data-ttu-id="3f580-120">Significado</span><span class="sxs-lookup"><span data-stu-id="3f580-120">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3f580-121"><dt>**porta de erro \_ inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f580-121"><dt>**ERROR\_INVALID\_PORT**</dt></span></span> </dl> | <span data-ttu-id="3f580-122">A porta especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="3f580-122">The specified port is invalid.</span></span><br/>    |
| <dl> <span data-ttu-id="3f580-123"><dt>**NERR \_ UserNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="3f580-123"><dt>**NERR\_UserNotFound**</dt></span></span> </dl>   | <span data-ttu-id="3f580-124">A porta não está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="3f580-124">The port is not currently in use.</span></span><br/> |



 

<span data-ttu-id="3f580-125">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3f580-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f580-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f580-126">Requirements</span></span>



| <span data-ttu-id="3f580-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f580-127">Requirement</span></span> | <span data-ttu-id="3f580-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3f580-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f580-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3f580-129">End of client support</span></span><br/> | <span data-ttu-id="3f580-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3f580-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="3f580-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3f580-131">End of server support</span></span><br/> | <span data-ttu-id="3f580-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f580-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="3f580-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f580-133">Header</span></span><br/>                | <dl> <span data-ttu-id="3f580-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f580-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f580-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f580-135">Library</span></span><br/>               | <dl> <span data-ttu-id="3f580-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f580-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f580-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3f580-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3f580-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f580-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f580-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f580-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f580-140">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="3f580-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="3f580-141">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="3f580-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> </dl>

 

