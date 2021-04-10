---
title: Definindo permissões em operações de objeto filho
description: As permissões, como criar filho e excluir filho, também podem ser concedidas ou negadas para operações em todos os subobjetos ou subobjetos de uma classe específica.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Definindo permissões no AD de operações do objeto filho
- objetos AD, Child, definindo permissões em operações de objeto filho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084433"
---
# <a name="setting-permissions-on-child-object-operations"></a>Definindo permissões em operações de objeto filho

As permissões, como criar filho e excluir filho, também podem ser concedidas ou negadas para operações em todos os subobjetos ou subobjetos de uma classe específica.

O procedimento a seguir pode ser usado para definir permissões para um tipo de subobjeto específico.

**Para definir permissões para um tipo de subobjeto específico**

1.  Defina a propriedade [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ de \_ objeto permitido** ou o **\_ objeto ADS AceType \_ acesso \_ negado \_**.
2.  Defina a propriedade [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o GUID da classe de objeto. Essa é a propriedade **schemaIDGUID** do objeto classSchema que define a classe de objeto. Se a propriedade **objecttype** for **nula**, a Ace se aplicará a subobjetos de qualquer classe.
3.  Defina a propriedade [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de objeto sinalizador ADS \_ \_ \_ presente**.

Para obter mais informações e um procedimento para criar uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE que controla operações de objeto filho, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 