---
description: Especifica a senha usada para autenticar um usuário.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Elemento Password (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753688"
---
# <a name="password-userlogoncred-element"></a><span data-ttu-id="3a084-103">Elemento Password (UserLogonCred)</span><span class="sxs-lookup"><span data-stu-id="3a084-103">Password (UserLogonCred) Element</span></span>

<span data-ttu-id="3a084-104">O elemento [**password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) especifica a senha usada para autenticar um usuário.</span><span class="sxs-lookup"><span data-stu-id="3a084-104">The [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) element specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="3a084-105">O elemento é uma cadeia de até 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3a084-105">The element is a string of up to 255 characters.</span></span>

<span data-ttu-id="3a084-106">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="3a084-106">This element is optional.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="3a084-107">O elemento **password** é definido pelo elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3a084-107">The **Password** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a084-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a084-108">Requirements</span></span>



| <span data-ttu-id="3a084-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a084-109">Requirement</span></span> | <span data-ttu-id="3a084-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3a084-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="3a084-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a084-111">Minimum supported client</span></span><br/> | <span data-ttu-id="3a084-112">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3a084-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="3a084-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a084-113">Minimum supported server</span></span><br/> | <span data-ttu-id="3a084-114">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3a084-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="3a084-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a084-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a084-116">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="3a084-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3a084-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="3a084-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="3a084-118">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="3a084-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3a084-119">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="3a084-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




