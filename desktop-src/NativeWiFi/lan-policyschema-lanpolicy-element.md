---
description: Contém uma política de LAN com fio.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Elemento LANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811081"
---
# <a name="lanpolicy-element"></a><span data-ttu-id="3b272-103">Elemento LANPolicy</span><span class="sxs-lookup"><span data-stu-id="3b272-103">LANPolicy Element</span></span>

<span data-ttu-id="3b272-104">O elemento LANPolicy contém uma política de LAN com fio.</span><span class="sxs-lookup"><span data-stu-id="3b272-104">The LANPolicy element contains a wired LAN policy.</span></span> <span data-ttu-id="3b272-105">Esse é o elemento raiz exclusivo para um perfil de diretiva de rede com fio.</span><span class="sxs-lookup"><span data-stu-id="3b272-105">This element is the unique root element for a wired network policy profile.</span></span>

<span data-ttu-id="3b272-106">O namespace de destino para o elemento **LANPolicy** é `https://www.microsoft.com/networking/LAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="3b272-106">The target namespace for the **LANPolicy** element is `https://www.microsoft.com/networking/LAN/policy/v1`.</span></span>

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="3b272-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3b272-107">Child elements</span></span>



| <span data-ttu-id="3b272-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3b272-108">Element</span></span>                                                                           | <span data-ttu-id="3b272-109">Type</span><span class="sxs-lookup"><span data-stu-id="3b272-109">Type</span></span>                                                     | <span data-ttu-id="3b272-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b272-110">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b272-111">**ndescrição**</span><span class="sxs-lookup"><span data-stu-id="3b272-111">**description**</span></span>](lan-policyschema-description-lanpolicy-element.md)             | [<span data-ttu-id="3b272-112">**nometype**</span><span class="sxs-lookup"><span data-stu-id="3b272-112">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="3b272-113">Contém a descrição de uma política de LAN com fio.</span><span class="sxs-lookup"><span data-stu-id="3b272-113">Contains the description of a wired LAN policy.</span></span> <br/>                                                                                                                          |
| [<span data-ttu-id="3b272-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="3b272-114">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="3b272-115">booleano</span><span class="sxs-lookup"><span data-stu-id="3b272-115">boolean</span></span>                                                  | <span data-ttu-id="3b272-116">Especifica se os computadores usam o serviço de configuração automática interno para gerenciar conexões com redes com fio que exigem autenticação de camada 2 (como 802.1 X).</span><span class="sxs-lookup"><span data-stu-id="3b272-116">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |
| [<span data-ttu-id="3b272-117">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="3b272-117">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | <span data-ttu-id="3b272-118">Contém as configurações globais para a configuração automática de redes com fio.</span><span class="sxs-lookup"><span data-stu-id="3b272-118">Contains the global settings for the automatic configuration of wired networks.</span></span> <br/>                                                                                          |
| [<span data-ttu-id="3b272-119">**nomes**</span><span class="sxs-lookup"><span data-stu-id="3b272-119">**name**</span></span>](lan-policyschema-name-lanpolicy-element.md)                           | [<span data-ttu-id="3b272-120">**nometype**</span><span class="sxs-lookup"><span data-stu-id="3b272-120">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="3b272-121">Contém o nome de uma política de LAN com fio.</span><span class="sxs-lookup"><span data-stu-id="3b272-121">Contains the name of a wired LAN policy.</span></span> <br/>                                                                                                                                 |
| [<span data-ttu-id="3b272-122">**ProfileList**</span><span class="sxs-lookup"><span data-stu-id="3b272-122">**profileList**</span></span>](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | <span data-ttu-id="3b272-123">Contém uma lista de perfis a serem aplicados no nível de domínio ou computador.</span><span class="sxs-lookup"><span data-stu-id="3b272-123">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                                                                |



## <a name="remarks"></a><span data-ttu-id="3b272-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b272-124">Remarks</span></span>

<span data-ttu-id="3b272-125">Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [ \_ elementos do esquema de política de LAN](lan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="3b272-125">To view the list of child elements in a tree-like structure, see [LAN\_policy Schema Elements](lan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b272-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b272-126">Requirements</span></span>



| <span data-ttu-id="3b272-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b272-127">Requirement</span></span> | <span data-ttu-id="3b272-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3b272-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b272-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b272-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3b272-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b272-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3b272-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b272-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3b272-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b272-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




