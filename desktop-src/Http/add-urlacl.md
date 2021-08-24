---
title: add urlacl
description: Reserva a URL especificada para contas e usuários não administradores.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- adicionar urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: e3f4c715df70255ede8bd9ca5fc23131102983f8a3aeeb25735d5fc81d5ad9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638776"
---
# <a name="add-urlacl"></a>add urlacl

Reserva a URL especificada para contas e usuários não administradores. A DACL (lista de controle de acesso discricionário) pode ser especificada usando um nome de conta com os parâmetros listen e delegate ou usando uma cadeia de caracteres SDDL (linguagem de definição do descritor de segurança).

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] cadeia de caracteres**
</dt> <dd>

Especifica a URL totalmente qualificada.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> <dd>

Especifica o nome de usuário ou grupo de usuários.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes \| no}\]**
</dt> <dd>

Especifica um dos seguintes valores:

-   sim: permite que o usuário registre URLs. Esse é o valor padrão.
-   não: nega que o usuário registre URLs.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes \| no}\]**
</dt> <dd>

Especifica um dos seguintes valores:

-   sim: permite que o usuário delegar URLs.
-   não: nega ao usuário a delegação de URLs. Esse é o valor padrão.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**Cadeia de caracteres [sddl=]**
</dt> <dd>

Especifica a cadeia de caracteres SDDL que descreve a DACL.

</dd> </dl>

## <a name="examples"></a>Exemplos

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Consulte Também

* [Comandos Netsh http](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 