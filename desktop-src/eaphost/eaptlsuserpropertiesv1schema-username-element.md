---
title: Elemento username (TLS)
description: Saiba mais sobre o elemento username. Esse elemento captura o nome de usuário a ser enviado na resposta EAP-Identity.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Elemento username EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105807861"
---
# <a name="username-element-tls"></a><span data-ttu-id="be702-105">Elemento username (TLS)</span><span class="sxs-lookup"><span data-stu-id="be702-105">Username element (TLS)</span></span>

<span data-ttu-id="be702-106">O elemento **username** captura o nome de usuário a ser enviado na resposta EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="be702-106">The **Username** element captures the user name to be sent in the EAP-Identity response.</span></span>

<span data-ttu-id="be702-107">Se o elemento **username** estiver ausente, o EAP-TLS usará o nome no certificado referido no elemento [**usercert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="be702-107">If the **Username** element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a><span data-ttu-id="be702-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be702-108">Requirements</span></span>



| <span data-ttu-id="be702-109">Função</span><span class="sxs-lookup"><span data-stu-id="be702-109">Role</span></span> | <span data-ttu-id="be702-110">Versões mínimas do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="be702-110">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="be702-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="be702-111">Client</span></span><br/> | <span data-ttu-id="be702-112">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be702-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="be702-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="be702-113">Server</span></span><br/> | <span data-ttu-id="be702-114">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be702-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be702-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="be702-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be702-116">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="be702-116">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="be702-117">Esquema eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="be702-117">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





