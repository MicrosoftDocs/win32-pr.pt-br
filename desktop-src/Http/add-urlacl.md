---
title: add urlacl
description: Reserva a URL especificada para usuários e contas não administradores.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Adicionar HTTP urlacl
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103930529"
---
# <a name="add-urlacl"></a>add urlacl

Reserva a URL especificada para usuários e contas não administradores. A DACL (lista de controle de acesso discricionário) pode ser especificada usando um nome de conta com os parâmetros Listen e delegate ou usando uma cadeia de caracteres SDDL (Security Descriptor Definition Language).

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url =] cadeia de caracteres**
</dt> <dd>

Especifica a URL totalmente qualificada.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[User =] cadeia de caracteres**
</dt> <dd>

Especifica o nome do usuário ou grupo de usuários.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[escutar = {sim \| não}\]**
</dt> <dd>

Especifica um dos seguintes valores:

-   Sim: permite que o usuário registre URLs. Esse é o valor padrão.
-   Não: nega o usuário de registrar URLs.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate = {sim \| não}\]**
</dt> <dd>

Especifica um dos seguintes valores:

-   Sim: permite que o usuário delegue URLs.
-   Não: nega o usuário de delegar URLs. Esse é o valor padrão.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] cadeia de caracteres**
</dt> <dd>

Especifica a cadeia de caracteres SDDL que descreve a DACL.

</dd> </dl>

## <a name="examples"></a>Exemplos

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Consulte Também

* [Comandos Netsh http](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 