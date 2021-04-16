---
title: Função RasAdminUserSetInfo (Rassapi. h)
description: A função RasAdminUserSetInfo define as permissões RAS e o número de telefone de retorno de chamada para um usuário especificado.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- Função RasAdminUserSetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751332"
---
# <a name="rasadminusersetinfo-function"></a><span data-ttu-id="c93d9-104">Função RasAdminUserSetInfo</span><span class="sxs-lookup"><span data-stu-id="c93d9-104">RasAdminUserSetInfo function</span></span>

<span data-ttu-id="c93d9-105">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="c93d9-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="c93d9-106">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c93d9-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="c93d9-107">Os aplicativos devem usar a função [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="c93d9-107">Applications should use the [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) function.\]</span></span>

<span data-ttu-id="c93d9-108">A função **RasAdminUserSetInfo** define as permissões RAS e o número de telefone de retorno de chamada para um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="c93d9-108">The **RasAdminUserSetInfo** function sets the RAS permissions and call-back phone number for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93d9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c93d9-109">Syntax</span></span>


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="c93d9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c93d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93d9-111">*lpszUserAccountServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c93d9-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93d9-112">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do controlador de domínio primário ou de backup que tem o banco de dados de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="c93d9-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="c93d9-113">Use a função [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obter esse nome de servidor.</span><span class="sxs-lookup"><span data-stu-id="c93d9-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="c93d9-114">*lpszUser* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c93d9-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93d9-115">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do usuário para quem as informações de RAS serão definidas.</span><span class="sxs-lookup"><span data-stu-id="c93d9-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom RAS information is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="c93d9-116">*pRasUser0* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c93d9-116">*pRasUser0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93d9-117">Ponteiro para a estrutura do [**usuário do RAS \_ \_ 0**](ras-user-0-str.md) que especifica os novos dados RAS para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="c93d9-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that specifies the new RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93d9-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c93d9-118">Return value</span></span>

<span data-ttu-id="c93d9-119">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="c93d9-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c93d9-120">Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="c93d9-120">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="c93d9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c93d9-121">Value</span></span>                                                                                                           | <span data-ttu-id="c93d9-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="c93d9-122">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c93d9-123"><dt>**ERRO de \_ dados inválidos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c93d9-123"><dt>**ERROR\_INVALID\_DATA**</dt></span></span> </dl>             | <span data-ttu-id="c93d9-124">O buffer *pRasUser0* contém dados inválidos.</span><span class="sxs-lookup"><span data-stu-id="c93d9-124">The *pRasUser0* buffer contains invalid data.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c93d9-125"><dt>**ERRO \_ \_ número de retorno de chamada inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c93d9-125"><dt>**ERROR\_INVALID\_CALLBACK\_NUMBER**</dt></span></span> </dl> | <span data-ttu-id="c93d9-126">O número de retorno de chamada especificado no buffer *pRasUser0* contém caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="c93d9-126">The callback number specified in the *pRasUser0* buffer contains invalid characters.</span></span><br/> |
| <dl> <span data-ttu-id="c93d9-127"><dt>**NERR \_ BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="c93d9-127"><dt>**NERR\_BufTooSmall** </dt></span></span> </dl>               | <span data-ttu-id="c93d9-128">Memória insuficiente para executar esta função.</span><span class="sxs-lookup"><span data-stu-id="c93d9-128">Insufficient memory to perform this function.</span></span><br/>                                        |



 

<span data-ttu-id="c93d9-129">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c93d9-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c93d9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="c93d9-130">Remarks</span></span>

<span data-ttu-id="c93d9-131">Ao definir as permissões de RAS para um usuário, o membro **bfPrivilege** da estrutura do [**usuário do RAS \_ \_ 0**](ras-user-0-str.md) deve especificar pelo menos um dos sinalizadores de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c93d9-131">When setting the RAS permissions for a user, the **bfPrivilege** member of the [**RAS\_USER\_0**](ras-user-0-str.md) structure must specify at least one of the call-back flags.</span></span> <span data-ttu-id="c93d9-132">Por exemplo, para definir privilégios de um usuário para permitir o privilégio de discagem, mas sem privilégios de retorno de chamada, defina **bfPrivilege** como RASPRIV \_ DialinPrivilege \| RASPRIV \_ nocallback.</span><span class="sxs-lookup"><span data-stu-id="c93d9-132">For example, to set a user's privileges to allow dial-in privilege but no call-back privilege, set **bfPrivilege** to RASPRIV\_DialinPrivilege \| RASPRIV\_NoCallback.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93d9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c93d9-133">Requirements</span></span>



| <span data-ttu-id="c93d9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c93d9-134">Requirement</span></span> | <span data-ttu-id="c93d9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c93d9-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c93d9-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c93d9-136">End of client support</span></span><br/> | <span data-ttu-id="c93d9-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c93d9-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="c93d9-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c93d9-138">End of server support</span></span><br/> | <span data-ttu-id="c93d9-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c93d9-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="c93d9-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c93d9-140">Header</span></span><br/>                | <dl> <span data-ttu-id="c93d9-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c93d9-141"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c93d9-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c93d9-142">Library</span></span><br/>               | <dl> <span data-ttu-id="c93d9-143"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c93d9-143"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c93d9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c93d9-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c93d9-145"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c93d9-145"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93d9-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="c93d9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93d9-147">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="c93d9-147">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c93d9-148">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="c93d9-148">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="c93d9-149">**Usuário do RAS \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c93d9-149">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="c93d9-150">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="c93d9-150">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="c93d9-151">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="c93d9-151">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> </dl>

 

