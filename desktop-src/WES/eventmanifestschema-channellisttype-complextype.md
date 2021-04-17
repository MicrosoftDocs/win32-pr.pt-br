---
title: Tipo complexo ChannelListType
description: Define uma lista de canais para os quais os provedores podem registrar eventos. | Tipo complexo ChannelListType
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Log de eventos do tipo complexo ChannelListType
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760912"
---
# <a name="channellisttype-complex-type"></a><span data-ttu-id="8be5a-105">Tipo complexo ChannelListType</span><span class="sxs-lookup"><span data-stu-id="8be5a-105">ChannelListType Complex Type</span></span>

<span data-ttu-id="8be5a-106">Define uma lista de canais para os quais os provedores podem registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="8be5a-106">Defines a list of channels to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8be5a-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8be5a-107">Child elements</span></span>



| <span data-ttu-id="8be5a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8be5a-108">Element</span></span>                                                                            | <span data-ttu-id="8be5a-109">Type</span><span class="sxs-lookup"><span data-stu-id="8be5a-109">Type</span></span>                                                                           | <span data-ttu-id="8be5a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8be5a-110">Description</span></span>                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8be5a-111">**canaliza**</span><span class="sxs-lookup"><span data-stu-id="8be5a-111">**channel**</span></span>](eventmanifestschema-channel-channellisttype-element.md)             | [<span data-ttu-id="8be5a-112">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="8be5a-112">**ChannelType**</span></span>](eventmanifestschema-channeltype-complextype.md)             | <span data-ttu-id="8be5a-113">Define um canal no qual os eventos podem ser registrados.</span><span class="sxs-lookup"><span data-stu-id="8be5a-113">Defines a channel to which events can be logged.</span></span><br/>                                                                  |
| [<span data-ttu-id="8be5a-114">**importChannel**</span><span class="sxs-lookup"><span data-stu-id="8be5a-114">**importChannel**</span></span>](eventmanifestschema-importchannel-channellisttype-element.md) | [<span data-ttu-id="8be5a-115">**ImportChannelType**</span><span class="sxs-lookup"><span data-stu-id="8be5a-115">**ImportChannelType**</span></span>](eventmanifestschema-importchanneltype-complextype.md) | <span data-ttu-id="8be5a-116">Identifica um canal que foi definido por outro provedor ou em um manifesto que contém uma seção de metadados.</span><span class="sxs-lookup"><span data-stu-id="8be5a-116">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8be5a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8be5a-117">Remarks</span></span>

<span data-ttu-id="8be5a-118">Você pode especificar até oito canais (qualquer combinação de canais ou canais importados que você definir).</span><span class="sxs-lookup"><span data-stu-id="8be5a-118">You can specify up to eight channels (any combination of imported channels or channels that you define).</span></span>

## <a name="requirements"></a><span data-ttu-id="8be5a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8be5a-119">Requirements</span></span>



| <span data-ttu-id="8be5a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be5a-120">Requirement</span></span> | <span data-ttu-id="8be5a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8be5a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8be5a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8be5a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8be5a-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8be5a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8be5a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8be5a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8be5a-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8be5a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





