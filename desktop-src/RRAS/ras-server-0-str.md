---
title: Estrutura de RAS_SERVER_0 (Rassapi. h)
description: A \_ estrutura do servidor RAS \_ 0 é usada pela função RasAdminServerGetInfo para retornar informações sobre as portas configuradas em um servidor RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS da estrutura de RAS_SERVER_0
- RAS de ponteiro de estrutura de PRAS_SERVER_0
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752833"
---
# <a name="ras_server_0-structure"></a><span data-ttu-id="196b1-105">\_Estrutura do servidor RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="196b1-105">RAS\_SERVER\_0 structure</span></span>

<span data-ttu-id="196b1-106">\[A estrutura do **\_ servidor RAS \_ 0** não tem suporte a partir do Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="196b1-106">\[The **RAS\_SERVER\_0** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="196b1-107">A estrutura do **\_ servidor RAS \_ 0** é usada pela função [**RasAdminServerGetInfo**](rasadminservergetinfo.md) para retornar informações sobre as portas configuradas em um servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="196b1-107">The **RAS\_SERVER\_0** structure is used by the [**RasAdminServerGetInfo**](rasadminservergetinfo.md) function to return information about the ports configured on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="196b1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="196b1-108">Syntax</span></span>


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a><span data-ttu-id="196b1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="196b1-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="196b1-110">**TotalPorts**</span><span class="sxs-lookup"><span data-stu-id="196b1-110">**TotalPorts**</span></span>
</dt> <dd>

<span data-ttu-id="196b1-111">Especifica o número total de portas configuradas no servidor RAS que estão disponíveis para os clientes remotos se conectarem.</span><span class="sxs-lookup"><span data-stu-id="196b1-111">Specifies the total number of ports configured on the RAS server that are available for remote clients to connect to.</span></span> <span data-ttu-id="196b1-112">Por exemplo, se o número total de portas configuradas para discagem em um servidor for de quatro, mas uma das portas estiver em uso no momento para discar, **TotalPorts** será três.</span><span class="sxs-lookup"><span data-stu-id="196b1-112">For example, if the total number of ports configured for dialing in to a server is four, but one of the ports is currently in use for dialing out, **TotalPorts** is three.</span></span>

</dd> <dt>

<span data-ttu-id="196b1-113">**PortsInUse**</span><span class="sxs-lookup"><span data-stu-id="196b1-113">**PortsInUse**</span></span>
</dt> <dd>

<span data-ttu-id="196b1-114">Especifica o número de portas atualmente em uso por clientes remotos.</span><span class="sxs-lookup"><span data-stu-id="196b1-114">Specifies the number of ports currently in use by remote clients.</span></span>

</dd> <dt>

<span data-ttu-id="196b1-115">**RasVersion**</span><span class="sxs-lookup"><span data-stu-id="196b1-115">**RasVersion**</span></span>
</dt> <dd>

<span data-ttu-id="196b1-116">Especifica a versão do servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="196b1-116">Specifies the version of the RAS server.</span></span> <span data-ttu-id="196b1-117">Use essas informações para executar a ação específica da versão.</span><span class="sxs-lookup"><span data-stu-id="196b1-117">Use this information to take version-specific action.</span></span> <span data-ttu-id="196b1-118">Esse membro é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="196b1-118">This member is one of the following values.</span></span>



| <span data-ttu-id="196b1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="196b1-119">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="196b1-120">Significado</span><span class="sxs-lookup"><span data-stu-id="196b1-120">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <span data-ttu-id="196b1-121"><dt>**RASDOWNLEVEL**</dt></span><span class="sxs-lookup"><span data-stu-id="196b1-121"><dt>**RASDOWNLEVEL**</dt></span></span> </dl>              | <span data-ttu-id="196b1-122">Indica um servidor RAS da versão 1,0 do LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="196b1-122">Indicates a LAN Manager version 1.0 RAS server.</span></span><br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <span data-ttu-id="196b1-123"><dt>**RASADMIN \_ 35**</dt></span><span class="sxs-lookup"><span data-stu-id="196b1-123"><dt>**RASADMIN\_35**</dt></span></span> </dl>                | <span data-ttu-id="196b1-124">Indica um servidor ou cliente RAS do Windows NT Server 3,51 e anterior.</span><span class="sxs-lookup"><span data-stu-id="196b1-124">Indicates a Windows NT Server 3.51 and earlier RAS server or client.</span></span><br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <span data-ttu-id="196b1-125"><dt>**RASADMIN \_ atual**</dt></span><span class="sxs-lookup"><span data-stu-id="196b1-125"><dt>**RASADMIN\_CURRENT**</dt></span></span> </dl> | <span data-ttu-id="196b1-126">Indica um cliente ou servidor RAS do Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="196b1-126">Indicates a Windows NT 4.0 RAS server or client.</span></span><br/>                     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="196b1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="196b1-127">Requirements</span></span>



| <span data-ttu-id="196b1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="196b1-128">Requirement</span></span> | <span data-ttu-id="196b1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="196b1-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="196b1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="196b1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="196b1-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="196b1-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="196b1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="196b1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="196b1-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="196b1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="196b1-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="196b1-134">End of client support</span></span><br/>    | <span data-ttu-id="196b1-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="196b1-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="196b1-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="196b1-136">End of server support</span></span><br/>    | <span data-ttu-id="196b1-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="196b1-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="196b1-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="196b1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="196b1-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="196b1-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="196b1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="196b1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="196b1-141">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="196b1-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="196b1-142">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="196b1-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="196b1-143">**RasAdminServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="196b1-143">**RasAdminServerGetInfo**</span></span>](rasadminservergetinfo.md)
</dt> </dl>

 

 





