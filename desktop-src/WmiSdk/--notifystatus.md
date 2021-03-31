---
description: Serve como a classe pai para classes de erro definidas pelo provedor.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: Classe __NotifyStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663135"
---
# <a name="__notifystatus-class"></a><span data-ttu-id="fd781-103">\_\_Classe NotifyStatus</span><span class="sxs-lookup"><span data-stu-id="fd781-103">\_\_NotifyStatus class</span></span>

<span data-ttu-id="fd781-104">A classe de sistema abstrata **\_ \_ NotifyStatus** serve como a classe pai para classes de erro definidas pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="fd781-104">The **\_\_NotifyStatus** abstract system class serves as the parent class for provider-defined error classes.</span></span>

<span data-ttu-id="fd781-105">A sintaxe a seguir é simplificada do código formato MOF (MF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fd781-105">The following syntax is simplified from Managed Object Format (MF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd781-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd781-106">Syntax</span></span>

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="fd781-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fd781-107">Members</span></span>

<span data-ttu-id="fd781-108">A classe **\_ \_ NotifyStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fd781-108">The **\_\_NotifyStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="fd781-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fd781-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd781-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fd781-110">Properties</span></span>

<span data-ttu-id="fd781-111">A classe **\_ \_ NotifyStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fd781-111">The **\_\_NotifyStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd781-112">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="fd781-112">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd781-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd781-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd781-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fd781-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd781-115">Contém um código de erro ou informações para uma operação.</span><span class="sxs-lookup"><span data-stu-id="fd781-115">Contains an error or information code for an operation.</span></span> <span data-ttu-id="fd781-116">Pode ser qualquer código definido pelo usuário, mas o valor 0 (zero) geralmente é reservado para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="fd781-116">This can be any user-defined code, but the value 0 (zero) is usually reserved to indicate success.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd781-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd781-117">Remarks</span></span>

<span data-ttu-id="fd781-118">Embora a classe **\_ \_ NotifyStatus** possa ser a classe pai para classes de erro definidas pelo provedor, é recomendável que os provedores derivem classes Error de [**\_ \_ ExtendedStatus**](--extendedstatus.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="fd781-118">Although the **\_\_NotifyStatus** class can be the parent class for provider-defined error classes, it is recommended that providers derive error classes from [**\_\_ExtendedStatus**](--extendedstatus.md) instead.</span></span> <span data-ttu-id="fd781-119">O uso de **\_ \_ ExtendedStatus** permite uma maior padronização das classes Error.</span><span class="sxs-lookup"><span data-stu-id="fd781-119">Using **\_\_ExtendedStatus** allows for greater standardization of error classes.</span></span>

<span data-ttu-id="fd781-120">Os provedores nunca devem criar instâncias do **\_ \_ NotifyStatus** diretamente, pois essas instâncias não transmitem mais informações do que um código de retorno simples.</span><span class="sxs-lookup"><span data-stu-id="fd781-120">Providers should never create instances of **\_\_NotifyStatus** directly, because these instances convey no more information than a simple return code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd781-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd781-121">Requirements</span></span>



| <span data-ttu-id="fd781-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd781-122">Requirement</span></span> | <span data-ttu-id="fd781-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fd781-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fd781-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd781-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fd781-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd781-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fd781-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd781-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fd781-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd781-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="fd781-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd781-128">Namespace</span></span><br/>                | <span data-ttu-id="fd781-129">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="fd781-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="fd781-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd781-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd781-131">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="fd781-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




