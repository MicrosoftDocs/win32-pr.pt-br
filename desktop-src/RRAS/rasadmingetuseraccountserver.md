---
title: Função RasAdminGetUserAccountServer (Rassapi. h)
description: A função RasAdminGetUserAccountServer recupera o nome do servidor que tem o banco de dados da conta de usuário. Use o nome do servidor retornado nas funções RasAdminUserGetInfo e RasAdminUserSetInfo para obter ou definir informações sobre um usuário especificado.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- Função RasAdminGetUserAccountServer RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779586"
---
# <a name="rasadmingetuseraccountserver-function"></a><span data-ttu-id="e70a2-105">Função RasAdminGetUserAccountServer</span><span class="sxs-lookup"><span data-stu-id="e70a2-105">RasAdminGetUserAccountServer function</span></span>

<span data-ttu-id="e70a2-106">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="e70a2-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="e70a2-107">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e70a2-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="e70a2-108">Os aplicativos devem usar a função [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]</span><span class="sxs-lookup"><span data-stu-id="e70a2-108">Applications should use the [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) function.\]</span></span>

<span data-ttu-id="e70a2-109">A função **RasAdminGetUserAccountServer** recupera o nome do servidor que tem o banco de dados da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="e70a2-109">The **RasAdminGetUserAccountServer** function retrieves the name of the server that has the user account database.</span></span> <span data-ttu-id="e70a2-110">Use o nome do servidor retornado nas funções [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obter ou definir informações sobre um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="e70a2-110">Use the returned server name in the [**RasAdminUserGetInfo**](rasadminusergetinfo.md) and [**RasAdminUserSetInfo**](rasadminusersetinfo.md) functions to get or set information about a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70a2-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e70a2-111">Syntax</span></span>


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a><span data-ttu-id="e70a2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e70a2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70a2-113">*lpszDomain* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e70a2-113">*lpszDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70a2-114">Ponteiro para uma cadeia de caracteres Unicode terminada em **nulo** que especifica o nome do domínio ao qual o servidor RAS pertence.</span><span class="sxs-lookup"><span data-stu-id="e70a2-114">Pointer to a **null**-terminated Unicode string that specifies the name of the domain to which the RAS server belongs.</span></span> <span data-ttu-id="e70a2-115">Esse parâmetro é **nulo** para os aplicativos de administração de Ras em execução em estações de trabalho ou servidores que não são membros de um domínio.</span><span class="sxs-lookup"><span data-stu-id="e70a2-115">This parameter is **NULL** for the RAS administration applications running on workstations or servers that are not members of a domain.</span></span> <span data-ttu-id="e70a2-116">Se esse parâmetro for **NULL**, o parâmetro *lpszServer* deverá ser não **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e70a2-116">If this parameter is **NULL**, the *lpszServer* parameter must be non-**NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e70a2-117">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e70a2-117">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70a2-118">Ponteiro para uma cadeia de caracteres Unicode terminada em **nulo** que especifica o nome do servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="e70a2-118">Pointer to a **null**-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="e70a2-119">Especifique o nome com " \\ \\ " caracteres à esquerda, no formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="e70a2-119">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span> <span data-ttu-id="e70a2-120">Esse parâmetro poderá ser **nulo** se o parâmetro *LpszDomain* não for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e70a2-120">This parameter can be **NULL** if the *lpszDomain* parameter is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e70a2-121">*lpszUserAccountServer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e70a2-121">*lpszUserAccountServer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e70a2-122">Ponteiro para um buffer que recebe uma cadeia de caracteres Unicode terminada em **nulo** que especifica o nome de um controlador de domínio que tem o banco de dados de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="e70a2-122">Pointer to a buffer that receives a **null**-terminated Unicode string that specifies the name of a domain controller that has the user account database.</span></span> <span data-ttu-id="e70a2-123">O buffer deve ser grande o suficiente para conter o nome do servidor (UNCLEN + 1).</span><span class="sxs-lookup"><span data-stu-id="e70a2-123">The buffer should be big enough to hold the server name (UNCLEN +1).</span></span> <span data-ttu-id="e70a2-124">A função prefixa o nome do servidor retornado com caracteres "" à esquerda \\ \\ , no formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="e70a2-124">The function prefixes the returned server name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e70a2-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e70a2-125">Return value</span></span>

<span data-ttu-id="e70a2-126">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="e70a2-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e70a2-127">Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.</span><span class="sxs-lookup"><span data-stu-id="e70a2-127">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="e70a2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e70a2-128">Value</span></span>                                                                                                    | <span data-ttu-id="e70a2-129">Significado</span><span class="sxs-lookup"><span data-stu-id="e70a2-129">Meaning</span></span>                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="e70a2-130"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e70a2-130"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="e70a2-131">*LpszDomain* e *lpszServer* são **nulos**.</span><span class="sxs-lookup"><span data-stu-id="e70a2-131">Both *lpszDomain* and *lpszServer* are **NULL**.</span></span><br/> |



 

<span data-ttu-id="e70a2-132">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="e70a2-132">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e70a2-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="e70a2-133">Remarks</span></span>

<span data-ttu-id="e70a2-134">A função **RasAdminGetUserAccountServer** Obtém o nome do servidor com o banco de dados de contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="e70a2-134">The **RasAdminGetUserAccountServer** function obtains the name of the server with the user accounts database.</span></span> <span data-ttu-id="e70a2-135">Essa função requer o nome do servidor RAS ou o nome do domínio no qual o servidor RAS reside.</span><span class="sxs-lookup"><span data-stu-id="e70a2-135">This function requires the name of the RAS server or the name of the domain in which the RAS server resides.</span></span>

<span data-ttu-id="e70a2-136">O parâmetro *lpszDomain* deve especificar um nome de domínio válido.</span><span class="sxs-lookup"><span data-stu-id="e70a2-136">The *lpszDomain* parameter should specify a valid domain name.</span></span> <span data-ttu-id="e70a2-137">Esse parâmetro é **nulo** para aplicativos de administração de Ras em execução em servidores que não são membros de um domínio (por exemplo, o servidor está em seu próprio grupo de trabalho).</span><span class="sxs-lookup"><span data-stu-id="e70a2-137">This parameter is **NULL** for RAS administration applications running on servers that are not members of a domain (for example, the server is in its own workgroup).</span></span> <span data-ttu-id="e70a2-138">Nesse caso, o parâmetro *lpszServer* deve especificar o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e70a2-138">In this case, the *lpszServer* parameter must specify the server name.</span></span> <span data-ttu-id="e70a2-139">Para obter o nome do servidor, chame a função [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) .</span><span class="sxs-lookup"><span data-stu-id="e70a2-139">To get the server name, call the [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) function.</span></span> <span data-ttu-id="e70a2-140">Certifique-se de prefixar o nome do servidor com os \\ \\ caracteres "".</span><span class="sxs-lookup"><span data-stu-id="e70a2-140">Be sure to prefix the server name with the "\\\\" characters.</span></span>

<span data-ttu-id="e70a2-141">Se o nome do servidor especificado por *lpszServer* for um servidor autônomo (ou seja, o servidor ou a estação de trabalho não for um membro de um domínio), o nome do servidor em si será retornado no buffer *lpszUserAccountServer* .</span><span class="sxs-lookup"><span data-stu-id="e70a2-141">If the server name specified by *lpszServer* is a stand-alone server (that is, the server or workstation is not a member of a domain), then the server name itself is returned in the *lpszUserAccountServer* buffer.</span></span>

<span data-ttu-id="e70a2-142">Em seguida, use o nome do servidor de conta de usuário em uma chamada para a função [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar os usuários no banco de dados de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="e70a2-142">Then use the name of the user account server in a call to the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function to enumerate the users in the user account database.</span></span>

## <a name="requirements"></a><span data-ttu-id="e70a2-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e70a2-143">Requirements</span></span>



| <span data-ttu-id="e70a2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70a2-144">Requirement</span></span> | <span data-ttu-id="e70a2-145">Valor</span><span class="sxs-lookup"><span data-stu-id="e70a2-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e70a2-146">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e70a2-146">End of client support</span></span><br/> | <span data-ttu-id="e70a2-147">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e70a2-147">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="e70a2-148">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e70a2-148">End of server support</span></span><br/> | <span data-ttu-id="e70a2-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e70a2-149">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="e70a2-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e70a2-150">Header</span></span><br/>                | <dl> <span data-ttu-id="e70a2-151"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e70a2-151"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="e70a2-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e70a2-152">Library</span></span><br/>               | <dl> <span data-ttu-id="e70a2-153"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e70a2-153"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e70a2-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e70a2-154">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e70a2-155"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e70a2-155"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e70a2-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="e70a2-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70a2-157">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="e70a2-157">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="e70a2-158">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="e70a2-158">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="e70a2-159">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="e70a2-159">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[<span data-ttu-id="e70a2-160">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e70a2-160">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="e70a2-161">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="e70a2-161">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

