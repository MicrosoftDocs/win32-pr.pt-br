---
title: Definindo permissões para uma propriedade específica
description: As permissões podem ser definidas para aplicar a uma propriedade específica de um objeto.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Definindo permissões para um anúncio de propriedade específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007287"
---
# <a name="setting-permissions-to-a-specific-property"></a>Definindo permissões para uma propriedade específica

As permissões podem ser definidas para aplicar a uma propriedade específica de um objeto.

**Para definir permissões que se aplicam a uma propriedade específica de um objeto**

1.  Defina a propriedade [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ Rights \_ DS \_ Read \_ prop** e/ou **ADS \_ Right \_ DS \_ Write \_ prop**.
2.  Defina a propriedade [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ de \_ objeto permitido** ou o **\_ objeto ADS AceType \_ acesso \_ negado \_**.
3.  Defina a propriedade [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o **schemaIDGUID** da propriedade. Esse é o **schemaIDGUID** do objeto **attributeSchema** que define a propriedade no esquema. O GUID deve ser especificado como uma cadeia de caracteres do formulário produzido pela função [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) na biblioteca com.
4.  Defina [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de objeto sinalizador ADS \_ \_ \_ presente**.

Para obter mais informações sobre o **schemaIDGUID** de um atributo predefinido, consulte [referência de Active Directory Domain Services](active-directory-domain-services-reference.md).

Para obter mais informações e um exemplo de código que pode ser usado para recuperar um schemaIDGUID, consulte [lendo objetos attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).

Para obter mais informações sobre como criar uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE específica de propriedade, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 