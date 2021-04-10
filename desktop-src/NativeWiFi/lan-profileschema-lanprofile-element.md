---
description: Contém um perfil de rede com fio.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Elemento LANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170414"
---
# <a name="lanprofile-element"></a><span data-ttu-id="b4e46-103">Elemento LANProfile</span><span class="sxs-lookup"><span data-stu-id="b4e46-103">LANProfile Element</span></span>

<span data-ttu-id="b4e46-104">O elemento LANProfile contém um perfil de rede com fio.</span><span class="sxs-lookup"><span data-stu-id="b4e46-104">The LANProfile element contains a wired network profile.</span></span> <span data-ttu-id="b4e46-105">Esse é o elemento raiz exclusivo para um perfil de rede com fio.</span><span class="sxs-lookup"><span data-stu-id="b4e46-105">This element is the unique root element for a wired network profile.</span></span>

<span data-ttu-id="b4e46-106">O namespace de destino para o elemento LANProfile é `https://www.microsoft.com/networking/LAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="b4e46-106">The target namespace for the LANProfile element is `https://www.microsoft.com/networking/LAN/profile/v1`.</span></span>

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="MSM">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="security">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OneXEnforced"
                                        type="boolean"
                                     />
                                    <xs:element name="OneXEnabled"
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
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="b4e46-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b4e46-107">Child elements</span></span>



| <span data-ttu-id="b4e46-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b4e46-108">Element</span></span>                                                                 | <span data-ttu-id="b4e46-109">Type</span><span class="sxs-lookup"><span data-stu-id="b4e46-109">Type</span></span>    | <span data-ttu-id="b4e46-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4e46-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4e46-111">**MSM**</span><span class="sxs-lookup"><span data-stu-id="b4e46-111">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)                 |         | <span data-ttu-id="b4e46-112">Contém configurações do módulo de mídia específica (MSM).</span><span class="sxs-lookup"><span data-stu-id="b4e46-112">Contains media-specific module (MSM) settings.</span></span> <br/>                                                                               |
| [<span data-ttu-id="b4e46-113">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="b4e46-113">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="b4e46-114">booleano</span><span class="sxs-lookup"><span data-stu-id="b4e46-114">boolean</span></span> | <span data-ttu-id="b4e46-115">Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="b4e46-115">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="b4e46-116">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="b4e46-116">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="b4e46-117">booleano</span><span class="sxs-lookup"><span data-stu-id="b4e46-117">boolean</span></span> | <span data-ttu-id="b4e46-118">Especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 X para autenticação de porta.</span><span class="sxs-lookup"><span data-stu-id="b4e46-118">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="b4e46-119">**segurança**</span><span class="sxs-lookup"><span data-stu-id="b4e46-119">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="b4e46-120">Contém configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="b4e46-120">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="b4e46-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4e46-121">Remarks</span></span>

<span data-ttu-id="b4e46-122">Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [ \_ elementos do esquema de perfil de LAN](lan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="b4e46-122">To view the list of child elements in a tree-like structure, see [LAN\_profile Schema Elements](lan-profileschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e46-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4e46-123">Requirements</span></span>



| <span data-ttu-id="b4e46-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4e46-124">Requirement</span></span> | <span data-ttu-id="b4e46-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b4e46-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4e46-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4e46-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4e46-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4e46-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b4e46-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4e46-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4e46-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b4e46-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




