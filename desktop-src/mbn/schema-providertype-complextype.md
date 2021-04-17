---
description: Especifica informações sobre uma rede de celular.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: Tipo complexo providerType (banda larga móvel)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754579"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="99ab1-103">Tipo complexo providerType</span><span class="sxs-lookup"><span data-stu-id="99ab1-103">providerType Complex Type</span></span>

<span data-ttu-id="99ab1-104">O tipo complexo **ProviderType** especifica informações sobre uma rede de celular.</span><span class="sxs-lookup"><span data-stu-id="99ab1-104">The **providerType** complex type specifies information about a cellular network.</span></span>

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="99ab1-105">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="99ab1-105">Child elements</span></span>



| <span data-ttu-id="99ab1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="99ab1-106">Element</span></span>                                                          | <span data-ttu-id="99ab1-107">Type</span><span class="sxs-lookup"><span data-stu-id="99ab1-107">Type</span></span>                                                           | <span data-ttu-id="99ab1-108">Description</span><span class="sxs-lookup"><span data-stu-id="99ab1-108">Description</span></span>               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="99ab1-109">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="99ab1-109">**ProviderID**</span></span>](schema-providerid-providertype-element.md)     | [<span data-ttu-id="99ab1-110">**providerIdType**</span><span class="sxs-lookup"><span data-stu-id="99ab1-110">**providerIdType**</span></span>](schema-provideridtype-simpletype.md)     | <span data-ttu-id="99ab1-111">ID do provedor.</span><span class="sxs-lookup"><span data-stu-id="99ab1-111">Provider ID.</span></span><br/>   |
| [<span data-ttu-id="99ab1-112">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="99ab1-112">**ProviderName**</span></span>](schema-providername-providertype-element.md) | [<span data-ttu-id="99ab1-113">**providerNametype**</span><span class="sxs-lookup"><span data-stu-id="99ab1-113">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="99ab1-114">Nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="99ab1-114">Provider name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="99ab1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99ab1-115">Requirements</span></span>



| <span data-ttu-id="99ab1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="99ab1-116">Requirement</span></span> | <span data-ttu-id="99ab1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="99ab1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="99ab1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99ab1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="99ab1-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="99ab1-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="99ab1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99ab1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="99ab1-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="99ab1-121">None supported</span></span><br/>                         |



 

 




