---
title: Tipo complexo networkSettingsType
description: Define os elementos que fornecem as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- Agendador de Tarefas tipo complexo networkSettingsType
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918663"
---
# <a name="networksettingstype-complex-type"></a><span data-ttu-id="b4f20-104">Tipo complexo networkSettingsType</span><span class="sxs-lookup"><span data-stu-id="b4f20-104">networkSettingsType Complex Type</span></span>

<span data-ttu-id="b4f20-105">Define os elementos que fornecem as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="b4f20-105">Defines the elements that provide the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b4f20-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b4f20-106">Child elements</span></span>



| <span data-ttu-id="b4f20-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b4f20-107">Element</span></span>                                                              | <span data-ttu-id="b4f20-108">Type</span><span class="sxs-lookup"><span data-stu-id="b4f20-108">Type</span></span>                                                        | <span data-ttu-id="b4f20-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4f20-109">Description</span></span>                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4f20-110">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="b4f20-110">**Id**</span></span>](taskschedulerschema-id-networksettingstype-element.md)     | [<span data-ttu-id="b4f20-111">**guidtype**</span><span class="sxs-lookup"><span data-stu-id="b4f20-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md) | <span data-ttu-id="b4f20-112">Especifica um valor de GUID que identifica um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="b4f20-112">Specifies a GUID value that identifies a network profile.</span></span> <br/>                       |
| [<span data-ttu-id="b4f20-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b4f20-113">**Name**</span></span>](taskschedulerschema-name-networksettingstype-element.md) | <span data-ttu-id="b4f20-114">não vazio</span><span class="sxs-lookup"><span data-stu-id="b4f20-114">nonEmptyString</span></span>                                              | <span data-ttu-id="b4f20-115">Especifica o nome de um perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="b4f20-115">Specifies the name of a network profile.</span></span> <span data-ttu-id="b4f20-116">O nome é usado para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="b4f20-116">The name is used for display purposes.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="b4f20-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4f20-117">Requirements</span></span>



| <span data-ttu-id="b4f20-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4f20-118">Requirement</span></span> | <span data-ttu-id="b4f20-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b4f20-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4f20-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4f20-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f20-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4f20-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b4f20-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4f20-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f20-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b4f20-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





