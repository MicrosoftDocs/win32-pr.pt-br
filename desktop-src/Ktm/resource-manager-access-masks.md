---
description: O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir um Gerenciador de recursos.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Máscaras de acesso do Gerenciador de recursos (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091555"
---
# <a name="resource-manager-access-masks"></a><span data-ttu-id="09e31-103">Máscaras de acesso do Gerenciador de recursos</span><span class="sxs-lookup"><span data-stu-id="09e31-103">Resource Manager Access Masks</span></span>

<span data-ttu-id="09e31-104">O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir um Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="09e31-104">KTM defines the following enlistment access masks to be used when opening a resource manager.</span></span>

<dl> <dt>

<span data-ttu-id="09e31-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_informações de consulta de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="09e31-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-106">O chamador pode consultar as informações do Gerenciador de recursos (RM).</span><span class="sxs-lookup"><span data-stu-id="09e31-106">The caller can query for the resource manager (RM) information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09e31-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_informações do conjunto de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="09e31-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-108">O chamador pode definir as informações do RM.</span><span class="sxs-lookup"><span data-stu-id="09e31-108">The caller can set the RM information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09e31-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**recuperação de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="09e31-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-110">O chamador pode recuperar o RM especificado.</span><span class="sxs-lookup"><span data-stu-id="09e31-110">The caller can recover the specified RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09e31-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**inscrição de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="09e31-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-112">O chamador pode inscrever um RM em uma transação.</span><span class="sxs-lookup"><span data-stu-id="09e31-112">The caller can enlist an RM in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09e31-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**\_notificação de obtenção de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="09e31-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER\_GET\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-114">O chamador pode receber uma notificação para um RM.</span><span class="sxs-lookup"><span data-stu-id="09e31-114">The caller can receive a notification for an RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09e31-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_leitura genérica de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="09e31-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-116">O chamador tem os seguintes privilégios: \_ leitura de direitos padrão \_ , informações de consulta de ResourceManager \_ \_ e recuperação de ResourceManager \_ .</span><span class="sxs-lookup"><span data-stu-id="09e31-116">The caller has the following privileges: STANDARD\_RIGHTS\_READ, RESOURCEMANAGER\_QUERY\_INFORMATION, and RESOURCEMANAGER\_RECOVER.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09e31-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_gravação genérica de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="09e31-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-118">O chamador tem os seguintes privilégios: \_ gravação de direitos padrão \_ , informações do conjunto de ResourceManager \_ \_ , \_ inscrição de ResourceManager e notificação de obtenção de ResourceManager \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="09e31-118">The caller has the following privileges: STANDARD\_RIGHTS\_WRITE, RESOURCEMANAGER\_SET\_INFORMATION, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09e31-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_execução genérica de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="09e31-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-120">O chamador tem os seguintes privilégios: \_ execução de direitos padrão \_ , \_ inscrição de ResourceManager e \_ notificação de obtenção de ResourceManager \_ .</span><span class="sxs-lookup"><span data-stu-id="09e31-120">The caller has the following privileges: STANDARD\_RIGHTS\_EXECUTE, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09e31-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**\_todos os \_ acessos do RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="09e31-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="09e31-122">O chamador tem o seguinte privilégio: \_ direitos padrão \_ necessários.</span><span class="sxs-lookup"><span data-stu-id="09e31-122">The caller has the following privilege: STANDARD\_RIGHTS\_REQUIRED.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09e31-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e31-123">Requirements</span></span>



| <span data-ttu-id="09e31-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e31-124">Requirement</span></span> | <span data-ttu-id="09e31-125">Valor</span><span class="sxs-lookup"><span data-stu-id="09e31-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09e31-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e31-126">Minimum supported client</span></span><br/> | <span data-ttu-id="09e31-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09e31-127">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="09e31-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e31-128">Minimum supported server</span></span><br/> | <span data-ttu-id="09e31-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09e31-129">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="09e31-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09e31-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="09e31-131"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="09e31-131"><dt>WinNT.h</dt></span></span> </dl> |



 

 




