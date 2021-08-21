---
title: Definindo permissões em operações de objeto filho
description: Permissões, como Criar Filho e Excluir Filho, também podem ser concedidas ou negadas para operações em todos os subobjetos ou subobjetos de uma classe específica.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Definindo permissões no AD de Operações de Objeto Filho
- objetos AD , filho, definindo permissões em operações de objeto filho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f136119d5e61ea312748d5cd64cabb8c0aee0b651d8b192519dc2d74e2045cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024764"
---
# <a name="setting-permissions-on-child-object-operations"></a>Definindo permissões em operações de objeto filho

Permissões, como Criar Filho e Excluir Filho, também podem ser concedidas ou negadas para operações em todos os subobjetos ou subobjetos de uma classe específica.

O procedimento a seguir pode ser usado para definir permissões para um tipo de subobjeto específico.

**Para definir permissões para um tipo de subobjeto específico**

1.  De definir [**a propriedade IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT** ou **ADS \_ ACETYPE ACCESS \_ \_ DENIED \_ OBJECT**.
2.  De definir [**a propriedade IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o GUID da classe de objeto. Essa é a **propriedade schemaIDGUID** do objeto classSchema que define a classe de objeto . Se a **propriedade ObjectType** for **NULL,** a ACE se aplicará a subobjetos de qualquer classe.
3.  De definir [**a propriedade IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS FLAG OBJECT TYPE \_ \_ \_ \_ PRESENT.**

Para obter mais informações e um procedimento para criar uma ACE, consulte [Definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE que controla operações de objeto filho, consulte Código de exemplo para definir uma ACE em [um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 