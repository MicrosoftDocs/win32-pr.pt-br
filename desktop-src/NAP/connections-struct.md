---
title: Estrutura de conexões (NapEnforcementClient. h)
description: Contém informações sobre a lista de conexões mantidas por um aplicador.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- NAP da estrutura de conexões
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919214"
---
# <a name="connections-structure"></a><span data-ttu-id="e18d5-104">Estrutura de conexões</span><span class="sxs-lookup"><span data-stu-id="e18d5-104">Connections structure</span></span>

> [!Note]  
> <span data-ttu-id="e18d5-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="e18d5-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e18d5-106">A estrutura **conexões** contém informações sobre a lista de conexões mantidas por um aplicador.</span><span class="sxs-lookup"><span data-stu-id="e18d5-106">The **Connections** structure contains information about the list of connections maintained by an enforcer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e18d5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e18d5-107">Syntax</span></span>


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a><span data-ttu-id="e18d5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e18d5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e18d5-109">**contagem**</span><span class="sxs-lookup"><span data-stu-id="e18d5-109">**count**</span></span>
</dt> <dd>

<span data-ttu-id="e18d5-110">O número de conexões ativas atualmente mantidas por um aplicador dentro do intervalo de 0 (zero) a [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e18d5-110">The number of active connections currently maintained by an enforcer within the range 0 (zero) to [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e18d5-111">**connections**</span><span class="sxs-lookup"><span data-stu-id="e18d5-111">**connections**</span></span>
</dt> <dd>

<span data-ttu-id="e18d5-112">Um ponteiro COM para uma lista de interfaces [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) que representam conexões de cliente.</span><span class="sxs-lookup"><span data-stu-id="e18d5-112">A COM pointer to a list of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interfaces that represent client connections.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e18d5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e18d5-113">Requirements</span></span>



| <span data-ttu-id="e18d5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e18d5-114">Requirement</span></span> | <span data-ttu-id="e18d5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e18d5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e18d5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e18d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e18d5-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e18d5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e18d5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e18d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e18d5-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e18d5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e18d5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e18d5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e18d5-121"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e18d5-121"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e18d5-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="e18d5-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e18d5-123"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e18d5-123"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e18d5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e18d5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18d5-125">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="e18d5-125">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="e18d5-126">Estruturas de NAP</span><span class="sxs-lookup"><span data-stu-id="e18d5-126">NAP Structures</span></span>](nap-structures.md)
</dt> <dt>

[<span data-ttu-id="e18d5-127">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e18d5-127">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





