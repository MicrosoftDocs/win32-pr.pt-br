---
title: Atributos (AD DS)
description: Cada objeto no Active Directory Domain Services contém um conjunto de atributos que definem as características do objeto.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- AD de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007362"
---
# <a name="attributes-ad-ds"></a>Atributos (AD DS)

Cada objeto no Active Directory Domain Services contém um conjunto de atributos que definem as características do objeto. Cada atributo é descrito por um objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) no contêiner de esquema que define o atributo. A definição de atributo inclui uma variedade de dados, por exemplo, os tipos de objeto aos quais o atributo se aplica e o tipo de sintaxe do atributo. Para obter mais informações sobre definições de esquema de atributo, consulte [características de atributos](characteristics-of-attributes.md).

A lista a seguir lista os tipos de atributos que são armazenados em Active Directory Domain Services.

<dl> <dt>

<span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Atributos armazenados replicados pelo domínio
</dt> <dd>

Alguns atributos são armazenados no diretório (como [**CN**](/windows/desktop/ADSchema/a-cn), [**NTSECURITYDESCRIPTOR**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) e replicados para todos os controladores de domínio em um domínio. Um subconjunto desses atributos também é replicado para o catálogo global. Se você enumerar atributos de um objeto do catálogo global, somente os atributos replicados para o catálogo global serão retornados. Alguns atributos também são indexados porque a inclusão de uma propriedade indexada em uma consulta melhora o desempenho da consulta.

</dd> <dt>

<span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Atributos armazenados localmente e não replicados
</dt> <dd>

Atributos não replicados, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-login**](/windows/desktop/ADSchema/a-lastlogon)e [**Last-logoff**](/windows/desktop/ADSchema/a-lastlogoff) , são armazenados em cada controlador de domínio, mas não são replicados. Os atributos não replicados são atributos que pertencem a um controlador de domínio específico. Por exemplo, o **último atributo de logon** é a última data e hora em que o logon de rede do usuário foi validado por esse controlador de domínio específico que retornou a propriedade. Esses atributos podem ser recuperados da mesma maneira que os atributos de todo o domínio descritos anteriormente. No entanto, para esses atributos, cada controlador de domínio armazena apenas os valores que pertencem a esse controlador de domínio específico. Por exemplo, para obter a última vez que um usuário fez logon no domínio, recupere o último atributo de **logon** para o usuário de cada controlador de domínio no domínio e localize a data e a hora mais recentes.

</dd> <dt>

<span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Atributos construídos e não armazenados
</dt> <dd>

Um objeto de usuário também tem atributos construídos que não são armazenados no diretório, mas são calculados pelo controlador de domínio, como [**canônicaname**](/windows/desktop/ADSchema/a-canonicalname) e [**allowedattributes**](/windows/desktop/ADSchema/a-allowedattributes).

</dd> </dl>

 

 