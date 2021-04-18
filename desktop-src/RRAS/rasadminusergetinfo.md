---
title: Função RasAdminUserGetInfo (Rassapi. h)
description: A função RasAdminUserGetInfo Obtém as permissões RAS e as informações de número de telefone de retorno de chamada para um usuário especificado.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- Função RasAdminUserGetInfo RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759602"
---
# <a name="rasadminusergetinfo-function"></a><span data-ttu-id="2bae1-104">Função RasAdminUserGetInfo</span><span class="sxs-lookup"><span data-stu-id="2bae1-104">RasAdminUserGetInfo function</span></span>

<span data-ttu-id="2bae1-105">\[Essa função é fornecida somente para compatibilidade com versões anteriores do Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="2bae1-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="2bae1-106">Ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2bae1-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="2bae1-107">Os aplicativos devem usar a função [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="2bae1-107">Applications should use the [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) function.\]</span></span>

<span data-ttu-id="2bae1-108">A função **RasAdminUserGetInfo** Obtém as permissões RAS e as informações de número de telefone de retorno de chamada para um usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="2bae1-108">The **RasAdminUserGetInfo** function gets the RAS permissions and callback phone number information for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bae1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bae1-109">Syntax</span></span>


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="2bae1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bae1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bae1-111">*lpszUserAccountServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bae1-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bae1-112">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do controlador de domínio primário ou de backup que tem o banco de dados de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="2bae1-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="2bae1-113">Use a função [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obter esse nome de servidor.</span><span class="sxs-lookup"><span data-stu-id="2bae1-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="2bae1-114">*lpszUser* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bae1-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bae1-115">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do usuário para quem obter informações de RAS.</span><span class="sxs-lookup"><span data-stu-id="2bae1-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom to get RAS information.</span></span>

</dd> <dt>

<span data-ttu-id="2bae1-116">*pRasUser0*</span><span class="sxs-lookup"><span data-stu-id="2bae1-116">*pRasUser0*</span></span> 
</dt> <dd>

<span data-ttu-id="2bae1-117">Ponteiro para a estrutura do [**usuário do RAS \_ \_ 0**](ras-user-0-str.md) que recebe os dados RAS para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="2bae1-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that receives the RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bae1-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bae1-118">Return value</span></span>

<span data-ttu-id="2bae1-119">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="2bae1-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="2bae1-120">Se a função falhar, o valor de retorno poderá ser o seguinte código de erro.</span><span class="sxs-lookup"><span data-stu-id="2bae1-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="2bae1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2bae1-121">Value</span></span>                                                                                            | <span data-ttu-id="2bae1-122">Significado</span><span class="sxs-lookup"><span data-stu-id="2bae1-122">Meaning</span></span>                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="2bae1-123"><dt>**NERR \_ BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="2bae1-123"><dt>**NERR\_BufTooSmall**</dt></span></span> </dl> | <span data-ttu-id="2bae1-124">Memória insuficiente para executar esta função.</span><span class="sxs-lookup"><span data-stu-id="2bae1-124">Insufficient memory to perform this function.</span></span><br/> |



 

<span data-ttu-id="2bae1-125">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="2bae1-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bae1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bae1-126">Requirements</span></span>



| <span data-ttu-id="2bae1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bae1-127">Requirement</span></span> | <span data-ttu-id="2bae1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2bae1-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bae1-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2bae1-129">End of client support</span></span><br/> | <span data-ttu-id="2bae1-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2bae1-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="2bae1-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2bae1-131">End of server support</span></span><br/> | <span data-ttu-id="2bae1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2bae1-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="2bae1-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2bae1-133">Header</span></span><br/>                | <dl> <span data-ttu-id="2bae1-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bae1-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bae1-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bae1-135">Library</span></span><br/>               | <dl> <span data-ttu-id="2bae1-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bae1-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2bae1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2bae1-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2bae1-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bae1-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bae1-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bae1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bae1-140">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="2bae1-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="2bae1-141">Funções de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="2bae1-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="2bae1-142">**Usuário do RAS \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="2bae1-142">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="2bae1-143">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="2bae1-143">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="2bae1-144">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2bae1-144">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

