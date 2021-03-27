---
description: A \_ classe NIC HWConfig é a classe de tipo de evento para eventos de configuração de placa de interface de rede. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: Classe HWConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011606"
---
# <a name="hwconfig_nic-class"></a><span data-ttu-id="80b4b-104">\_Classe NIC HWConfig</span><span class="sxs-lookup"><span data-stu-id="80b4b-104">HWConfig\_NIC class</span></span>

<span data-ttu-id="80b4b-105">A **classe \_ NIC HWConfig** é a classe de tipo de evento para eventos de configuração de placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="80b4b-105">The **HWConfig\_NIC** class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="80b4b-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="80b4b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b4b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80b4b-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a><span data-ttu-id="80b4b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="80b4b-108">Members</span></span>

<span data-ttu-id="80b4b-109">A **classe \_ NIC HWConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="80b4b-109">The **HWConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="80b4b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80b4b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80b4b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80b4b-111">Properties</span></span>

<span data-ttu-id="80b4b-112">A **classe \_ NIC HWConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="80b4b-112">The **HWConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80b4b-113">NICName</span><span class="sxs-lookup"><span data-stu-id="80b4b-113">NICName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80b4b-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="80b4b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80b4b-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80b4b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80b4b-116">Qualificadores: WmiDataId (1), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="80b4b-116">Qualifiers: WmiDataId(1), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="80b4b-117">Nome da placa de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="80b4b-117">Name of the network interface card.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80b4b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80b4b-118">Requirements</span></span>



| <span data-ttu-id="80b4b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="80b4b-119">Requirement</span></span> | <span data-ttu-id="80b4b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="80b4b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="80b4b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80b4b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="80b4b-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="80b4b-122">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="80b4b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80b4b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="80b4b-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="80b4b-124">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="80b4b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="80b4b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b4b-126">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="80b4b-126">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




