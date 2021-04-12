---
title: Estrutura de RAS_USER_0 (Rassapi. h)
description: A \_ estrutura do usuário 0 do RAS \_ é usada nas funções RasAdminUserSetInfo e RasAdminUserGetInfo para especificar informações sobre um usuário.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS da estrutura de RAS_USER_0
- RAS de ponteiro de estrutura de PRAS_USER_0
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499354"
---
# <a name="ras_user_0-structure"></a><span data-ttu-id="63631-105">\_Estrutura do usuário 0 do RAS \_</span><span class="sxs-lookup"><span data-stu-id="63631-105">RAS\_USER\_0 structure</span></span>

<span data-ttu-id="63631-106">\[Esta versão da estrutura **do \_ usuário \_ do RAS 0** não tem suporte a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="63631-106">\[This version of the **RAS\_USER\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="63631-107">Use o [**usuário RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) mais recente definido em mprapi. h em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="63631-107">Use the newer [**RAS\_USER\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="63631-108">A estrutura do **\_ usuário \_ 0 do RAS** é usada nas funções [**RasAdminUserSetInfo**](rasadminusersetinfo.md) e [**RasAdminUserGetInfo**](rasadminusergetinfo.md) para especificar informações sobre um usuário.</span><span class="sxs-lookup"><span data-stu-id="63631-108">The **RAS\_USER\_0** structure is used in the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) and [**RasAdminUserGetInfo**](rasadminusergetinfo.md) functions to specify information about a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="63631-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63631-109">Syntax</span></span>


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a><span data-ttu-id="63631-110">Membros</span><span class="sxs-lookup"><span data-stu-id="63631-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="63631-111">**bfPrivilege**</span><span class="sxs-lookup"><span data-stu-id="63631-111">**bfPrivilege**</span></span>
</dt> <dd>

<span data-ttu-id="63631-112">Um conjunto de sinalizadores de bits que especificam os privilégios de RAS do usuário.</span><span class="sxs-lookup"><span data-stu-id="63631-112">A set of bit flags that specify the RAS privileges of the user.</span></span> <span data-ttu-id="63631-113">Esse membro pode ser uma combinação do sinalizador RASPRIV \_ DialinPrivilege e um dos sinalizadores de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="63631-113">This member can be a combination of the RASPRIV\_DialinPrivilege flag and one of the call-back flags.</span></span> <span data-ttu-id="63631-114">Use a \_ máscara de retorno de chamada RASPRIV para identificar o tipo de privilégio de recall fornecido ao usuário.</span><span class="sxs-lookup"><span data-stu-id="63631-114">Use the RASPRIV\_CallbackType mask to identify the type of call-back privilege provided to the user.</span></span> <span data-ttu-id="63631-115">Os sinalizadores a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="63631-115">The following flags are defined.</span></span>



| <span data-ttu-id="63631-116">Valor</span><span class="sxs-lookup"><span data-stu-id="63631-116">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="63631-117">Significado</span><span class="sxs-lookup"><span data-stu-id="63631-117">Meaning</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <span data-ttu-id="63631-118"><dt>**RASPRIV \_ Nocallback**</dt></span><span class="sxs-lookup"><span data-stu-id="63631-118"><dt>**RASPRIV\_NoCallback**</dt></span></span> </dl>                             | <span data-ttu-id="63631-119">O usuário não tem nenhum privilégio de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="63631-119">The user has no call-back privilege.</span></span><br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <span data-ttu-id="63631-120"><dt>**RASPRIV \_ AdminSetCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="63631-120"><dt>**RASPRIV\_AdminSetCallback**</dt></span></span> </dl>     | <span data-ttu-id="63631-121">A conta de usuário é configurada para que o administrador defina o número de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="63631-121">The user account is configured to have the administrator set the call-back number.</span></span><br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <span data-ttu-id="63631-122"><dt>**RASPRIV \_ CallerSetCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="63631-122"><dt>**RASPRIV\_CallerSetCallback**</dt></span></span> </dl> | <span data-ttu-id="63631-123">O usuário remoto pode especificar um número de telefone de retorno ao discar no.</span><span class="sxs-lookup"><span data-stu-id="63631-123">The remote user can specify a call-back phone number when dialing in.</span></span><br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <span data-ttu-id="63631-124"><dt>**RASPRIV \_ DialinPrivilege**</dt></span><span class="sxs-lookup"><span data-stu-id="63631-124"><dt>**RASPRIV\_DialinPrivilege**</dt></span></span> </dl>         | <span data-ttu-id="63631-125">O usuário tem permissão para fazer a conexão com este servidor.</span><span class="sxs-lookup"><span data-stu-id="63631-125">The user has permission to dial in to this server.</span></span><br/>                                 |



 

<span data-ttu-id="63631-126">Especifique um dos sinalizadores de retorno de chamada na chamada para a função [**RasAdminUserSetInfo**](rasadminusersetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="63631-126">Specify one of the call-back flags in the call to the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="63631-127">**szPhoneNumber**</span><span class="sxs-lookup"><span data-stu-id="63631-127">**szPhoneNumber**</span></span>
</dt> <dd>

<span data-ttu-id="63631-128">Uma cadeia de caracteres Unicode terminada em nulo que especifica o número de telefone de retorno para o usuário.</span><span class="sxs-lookup"><span data-stu-id="63631-128">A null-terminated Unicode string that specifies the call-back phone number for the user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63631-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63631-129">Requirements</span></span>



| <span data-ttu-id="63631-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="63631-130">Requirement</span></span> | <span data-ttu-id="63631-131">Valor</span><span class="sxs-lookup"><span data-stu-id="63631-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="63631-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63631-132">Minimum supported client</span></span><br/> | <span data-ttu-id="63631-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63631-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="63631-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63631-134">Minimum supported server</span></span><br/> | <span data-ttu-id="63631-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63631-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="63631-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="63631-136">End of client support</span></span><br/>    | <span data-ttu-id="63631-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="63631-137">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="63631-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="63631-138">End of server support</span></span><br/>    | <span data-ttu-id="63631-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63631-139">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="63631-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63631-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="63631-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="63631-141"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63631-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="63631-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63631-143">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="63631-143">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="63631-144">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="63631-144">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="63631-145">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="63631-145">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="63631-146">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="63631-146">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

 





