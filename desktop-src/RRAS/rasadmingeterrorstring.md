---
title: Função RasAdminGetErrorString (Rassapi. h)
description: A função RasAdminGetErrorString recupera uma cadeia de caracteres de mensagem que corresponde a um código de erro RAS retornado por uma das funções de administração do servidor RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- Função RasAdminGetErrorString RAS
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750581"
---
# <a name="rasadmingeterrorstring-function"></a><span data-ttu-id="a99be-104">Função RasAdminGetErrorString</span><span class="sxs-lookup"><span data-stu-id="a99be-104">RasAdminGetErrorString function</span></span>

<span data-ttu-id="a99be-105">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="a99be-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="a99be-106">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a99be-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="a99be-107">Os aplicativos devem usar a função [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]</span><span class="sxs-lookup"><span data-stu-id="a99be-107">Applications should use the [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) function.\]</span></span>

<span data-ttu-id="a99be-108">A função **RasAdminGetErrorString** recupera uma cadeia de caracteres de mensagem que corresponde a um código de erro RAS retornado por uma das funções de administração do servidor RAS (RasAdmin).</span><span class="sxs-lookup"><span data-stu-id="a99be-108">The **RasAdminGetErrorString** function retrieves a message string that corresponds to a RAS error code returned by one of the RAS server administration (RasAdmin) functions.</span></span> <span data-ttu-id="a99be-109">Essas cadeias de caracteres de mensagem são recuperadas do Rasmsg.dll que é instalado como parte do RAS.</span><span class="sxs-lookup"><span data-stu-id="a99be-109">These message strings are retrieved from the Rasmsg.dll that is installed as part of RAS.</span></span>

## <a name="syntax"></a><span data-ttu-id="a99be-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a99be-110">Syntax</span></span>


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="a99be-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a99be-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a99be-112">*ResourceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a99be-112">*ResourceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a99be-113">Especifica um código de erro retornado por uma das funções RasAdmin.</span><span class="sxs-lookup"><span data-stu-id="a99be-113">Specifies an error code returned by one of the RasAdmin functions.</span></span> <span data-ttu-id="a99be-114">Esse valor deve estar no intervalo de códigos de erro de RASBASE para RASBASEEND.</span><span class="sxs-lookup"><span data-stu-id="a99be-114">This value must be in the range of error codes from RASBASE to RASBASEEND.</span></span> <span data-ttu-id="a99be-115">Eles são definidos em Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="a99be-115">These are defined in Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="a99be-116">*lpszString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a99be-116">*lpszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a99be-117">Ponteiro para um buffer que recebe a mensagem de erro que corresponde ao código de erro especificado.</span><span class="sxs-lookup"><span data-stu-id="a99be-117">Pointer to a buffer that receives the error message that corresponds to the specified error code.</span></span>

</dd> <dt>

<span data-ttu-id="a99be-118">*InBufSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a99be-118">*InBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a99be-119">Especifica o tamanho, em caracteres, do buffer *lpszString* .</span><span class="sxs-lookup"><span data-stu-id="a99be-119">Specifies the size, in characters, of the *lpszString* buffer.</span></span> <span data-ttu-id="a99be-120">Normalmente, as mensagens de erro são de 80 caracteres ou menos; um tamanho de buffer de 512 caracteres é sempre adequado.</span><span class="sxs-lookup"><span data-stu-id="a99be-120">Error messages are typically 80 characters or less; a buffer size of 512 characters is always adequate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a99be-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a99be-121">Return value</span></span>

<span data-ttu-id="a99be-122">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="a99be-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a99be-123">Se a função falhar, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="a99be-123">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="a99be-124">Esse valor pode ser um último valor de erro definido pelas funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)ou [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) ; ou pode ser um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="a99be-124">This value can be a last error value set by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc), or [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) functions; or it can be one of the following error codes.</span></span>



| <span data-ttu-id="a99be-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a99be-125">Value</span></span>                                                                                                      | <span data-ttu-id="a99be-126">Significado</span><span class="sxs-lookup"><span data-stu-id="a99be-126">Meaning</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a99be-127"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a99be-127"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="a99be-128">Os parâmetros *ResourceId* ou *lpszString* são inválidos.</span><span class="sxs-lookup"><span data-stu-id="a99be-128">The *ResourceId* or *lpszString* parameters are invalid.</span></span><br/>      |
| <dl> <span data-ttu-id="a99be-129"><dt>**ERRO \_ de \_ buffer insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="a99be-129"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="a99be-130">O tamanho especificado pelo parâmetro *InBufSize* é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="a99be-130">The size specified by the *InBufSize* parameter is too small.</span></span><br/> |



 

<span data-ttu-id="a99be-131">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a99be-131">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a99be-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a99be-132">Remarks</span></span>

<span data-ttu-id="a99be-133">As funções RasAdmin podem retornar códigos de erro que não estão no intervalo com suporte da função **RasAdminGetErrorString** .</span><span class="sxs-lookup"><span data-stu-id="a99be-133">The RasAdmin functions can return error codes that are not in the range supported by the **RasAdminGetErrorString** function.</span></span> <span data-ttu-id="a99be-134">Por exemplo, as funções RasAdmin podem retornar códigos de erro que são definidos em Lmerr. h e Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a99be-134">For example, the RasAdmin functions can return error codes that are defined in Lmerr.h and Winerror.h.</span></span> <span data-ttu-id="a99be-135">Antes de chamar **RasAdminGetErrorString**, verifique se o código de erro está no intervalo RASBASE para RASBASEEND, conforme definido em Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="a99be-135">Before calling **RasAdminGetErrorString**, verify that the error code is in the range RASBASE to RASBASEEND, as defined in Raserror.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="a99be-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a99be-136">Requirements</span></span>



| <span data-ttu-id="a99be-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a99be-137">Requirement</span></span> | <span data-ttu-id="a99be-138">Valor</span><span class="sxs-lookup"><span data-stu-id="a99be-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a99be-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a99be-139">End of client support</span></span><br/> | <span data-ttu-id="a99be-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a99be-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a99be-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a99be-141">End of server support</span></span><br/> | <span data-ttu-id="a99be-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a99be-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a99be-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a99be-143">Header</span></span><br/>                | <dl> <span data-ttu-id="a99be-144"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a99be-144"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a99be-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a99be-145">Library</span></span><br/>               | <dl> <span data-ttu-id="a99be-146"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a99be-146"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a99be-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a99be-147">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a99be-148"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a99be-148"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a99be-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="a99be-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a99be-150">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="a99be-150">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a99be-151">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="a99be-151">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="a99be-152">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="a99be-152">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="a99be-153">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="a99be-153">**GlobalAlloc**</span></span>](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[<span data-ttu-id="a99be-154">**Cadeia de caracteres LoadString**</span><span class="sxs-lookup"><span data-stu-id="a99be-154">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

