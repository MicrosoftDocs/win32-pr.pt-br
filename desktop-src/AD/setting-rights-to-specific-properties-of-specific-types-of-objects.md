---
title: Definindo direitos para propriedades específicas de tipos específicos de objetos
description: Permissões específicas de propriedade podem ser usadas em combinação com herança específica de objeto para fornecer a delegação avançada e detalhada de administração.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- definindo direitos para propriedades específicas de tipos específicos de objetos AD
- Active Directory, usando, segurança, definindo direitos para propriedades específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453900"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>Definindo direitos para propriedades específicas de tipos específicos de objetos

Permissões específicas de propriedade podem ser usadas em combinação com herança específica de objeto para fornecer a delegação avançada e detalhada de administração. Você pode definir uma ACE herdada de objeto específico de propriedade para permitir que um usuário ou grupo especificado Leia e/ou grave um atributo específico em uma classe especificada de objetos filho em um contêiner. Por exemplo, você pode definir uma ACE em uma UO (unidade organizacional) para habilitar um grupo para ler e gravar o atributo de número de telefone de todos os objetos de usuário na UO.

**Para definir ACEs herdáveis de objeto específico de propriedade**

1.  Defina [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ ao \_ objeto permitido** ou ao objeto **ADS \_ AceType \_ acesso \_ negado \_**.
2.  Defina [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o **schemaIDGUID** do atributo. Por exemplo, o **schemaIDGUID** do atributo **telephoneNumber** é {bf967a49-0de6-11D0-a285-00aa003049e2}.
3.  Defina [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ ACEFLAG \_ INHERIT \_ Ace**.
4.  Defina [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o **schemaIDGUID** da classe de objeto que pode herdar a Ace. Por exemplo, o **schemaIDGUID** da classe **User** é {bf967aba-0de6-11D0-a285-00aa003049e2}.
5.  Defina [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de objeto sinalizador ADS \_ \_ \_ presente** e o **tipo de \_ \_ objeto herdado sinalizador ADS \_ \_ \_ presente**.

> [!IMPORTANT]
> Defina ADS \_ ACEFLAG \_ INHERIT \_ Ace para fazer com que a Ace seja herdada. Além disso, Set ADS \_ ACEFLAG \_ herdará \_ somente \_ Ace se o tipo de objeto ao qual essa Ace se aplica não corresponder ao tipo de objeto do contêiner onde a ACE é especificada. Se isso não for feito, a ACE também entrará em vigor no contêiner e poderá conceder direitos inesperados.

 

Para obter mais informações e exemplos de código que podem ser usados para definir esse tipo de ACE, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 