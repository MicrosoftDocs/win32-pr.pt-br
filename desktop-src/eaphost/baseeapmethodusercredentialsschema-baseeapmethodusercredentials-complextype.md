---
title: Tipo complexo BaseEapMethodUserCredentials
description: Saiba mais sobre o tipo complexo BaseEapMethodUserCredentials. Esse tipo é um elemento de espaço reservado para dados de credenciais de método.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- BaseEapMethodUserCredentials tipo complexo EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641819"
---
# <a name="baseeapmethodusercredentials-complex-type"></a><span data-ttu-id="f4be9-105">Tipo complexo BaseEapMethodUserCredentials</span><span class="sxs-lookup"><span data-stu-id="f4be9-105">BaseEapMethodUserCredentials Complex Type</span></span>

<span data-ttu-id="f4be9-106">O tipo complexo **BaseEapMethodUserCredentials** é um elemento de espaço reservado para dados de credenciais de método.</span><span class="sxs-lookup"><span data-stu-id="f4be9-106">The **BaseEapMethodUserCredentials** complex type is a placeholder element for method credential data.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="f4be9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4be9-107">Remarks</span></span>

<span data-ttu-id="f4be9-108">O método EAP executa a validação de esquema no conteúdo de **BaseEapMethodUserCredentials**.</span><span class="sxs-lookup"><span data-stu-id="f4be9-108">The EAP method performs schema validation on the contents of **BaseEapMethodUserCredentials**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4be9-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4be9-109">Requirements</span></span>



| <span data-ttu-id="f4be9-110">Função</span><span class="sxs-lookup"><span data-stu-id="f4be9-110">Role</span></span> | <span data-ttu-id="f4be9-111">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="f4be9-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="f4be9-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="f4be9-112">Client</span></span><br/> | <span data-ttu-id="f4be9-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4be9-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4be9-114">Servidor</span><span class="sxs-lookup"><span data-stu-id="f4be9-114">Server</span></span><br/> | <span data-ttu-id="f4be9-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4be9-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4be9-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4be9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4be9-117">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f4be9-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f4be9-118">Esquema baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="f4be9-118">baseeapmethodusercredentials Schema</span></span>](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





