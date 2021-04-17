---
description: Especifica como lidar com senhas ao atualizar perfis.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Elemento IgnorePassword (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812310"
---
# <a name="ignorepassword-userlogoncred-element"></a><span data-ttu-id="a5c05-103">Elemento IgnorePassword (UserLogonCred)</span><span class="sxs-lookup"><span data-stu-id="a5c05-103">IgnorePassword (UserLogonCred) Element</span></span>

<span data-ttu-id="a5c05-104">O elemento **IgnorePassword (UserLogonCred)** especifica como lidar com senhas ao atualizar perfis.</span><span class="sxs-lookup"><span data-stu-id="a5c05-104">The **IgnorePassword (UserLogonCred)** element specifies how to handle passwords when upgrading profiles.</span></span>

<span data-ttu-id="a5c05-105">Se definido como **true** e um perfil com o mesmo nome existir no momento da operação de atualização, a senha desse perfil será executada e armazenada em um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="a5c05-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in new profile.</span></span>

<span data-ttu-id="a5c05-106">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="a5c05-106">This element is optional.</span></span>

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

<span data-ttu-id="a5c05-107">O elemento **IgnorePassword** é definido pelo elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a5c05-107">The **IgnorePassword** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c05-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5c05-108">Requirements</span></span>



| <span data-ttu-id="a5c05-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5c05-109">Requirement</span></span> | <span data-ttu-id="a5c05-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a5c05-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a5c05-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5c05-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c05-112">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a5c05-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a5c05-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5c05-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c05-114">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a5c05-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="a5c05-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5c05-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="a5c05-116">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a5c05-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a5c05-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="a5c05-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="a5c05-118">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a5c05-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a5c05-119">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="a5c05-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




