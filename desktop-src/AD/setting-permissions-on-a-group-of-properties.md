---
title: Definindo permissões em um grupo de propriedades
description: As permissões podem ser aplicadas a um grupo de propriedades.
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- Definindo permissões em um grupo de propriedades AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f2993a537b76b64c7e8e6323c850494b3ce306
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640377"
---
# <a name="setting-permissions-on-a-group-of-properties"></a>Definindo permissões em um grupo de propriedades

As permissões podem ser aplicadas a um grupo de propriedades. Um conjunto de propriedades é identificado pelo GUID no atributo [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) de um objeto [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) . Esse GUID é definido no atributo [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) do objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo no grupo.

O procedimento a seguir mostra como definir permissões que se aplicam a um grupo de propriedades de objeto.

**Para definir permissões que se aplicam a um grupo de propriedades de objeto**

1.  Defina a propriedade [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ Rights \_ DS \_ Read \_ prop**, **ADS \_ Right \_ DS \_ Write \_ prop** ou ambos os valores combinados.
2.  Defina a propriedade [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType acesso de \_ \_ \_ objeto permitido** ou o **\_ \_ \_ \_ objeto acesso negado do ADS AceType**.
3.  Defina a propriedade [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o GUID do conjunto de propriedades. Essa é a propriedade [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) do objeto [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) que identifica o conjunto de propriedades. Esse GUID também é definido como o [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) no objeto attributeSchema de cada propriedade no grupo.
4.  Defina a propriedade [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de objeto sinalizador ADS \_ \_ \_ presente**.

Lembre-se de que você não deve definir o sinalizador de **\_ \_ \_ \_ acesso de controle DS direito do ADS** na propriedade [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) . Esse sinalizador é usado apenas para especificar um direito de acesso de controle.

Para obter mais informações e um exemplo de código que pode ser usado para definir direitos de acesso para um conjunto de propriedades, consulte [código de exemplo para definir permissões em um grupo de propriedades](example-code-for-setting-permissions-on-a-group-of-properties.md).

Para obter mais informações sobre como criar uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE para um conjunto de propriedades, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 