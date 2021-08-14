---
title: Sintaxes para atributos no Active Directory Domain Services
description: Active Directory Domain Services definir um conjunto de sintaxes de atributo para especificar o tipo de dados contidos por um atributo.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Sintaxes para atributos Active Directory Domain Services Active Directory
- Atributos do Active Directory, sintaxes para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c324fef5267ce37b42ede66b618b33148d266ac52dd69662a15bbce6094951ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182834"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Sintaxes para atributos no Active Directory Domain Services

Active Directory Domain Services definir um conjunto de sintaxes de atributo para especificar o tipo de dados contidos por um atributo. As sintaxes predefinidos não aparecem realmente no diretório e você não pode adicionar novas sintaxes. Vários métodos podem ser usados para identificar a sintaxe de uma classe de atributo:

-   Os métodos [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs.GetEx,**](/windows/desktop/api/iads/nf-iads-iads-getex) [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put)e [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) usam a estrutura [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) para obter e definir os valores dos atributos de um objeto. O **membro vt** dessa estrutura é um **valor VARTYPE** que identifica o tipo de dados.
-   Os métodos das interfaces [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) usam um valor da [**enumeração ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) para especificar o tipo de dados.
-   Para especificar a sintaxe de uma nova classe de atributo, de definir os atributos [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) e [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) de [**um objeto attributeSchema.**](/windows/desktop/ADSchema/c-attributeschema) Se o valor de **oMSyntax** for 127, você também deverá definir o atributo [**oMObjectClass.**](/windows/desktop/ADSchema/a-omobjectclass) Para obter mais informações, consulte [Escolhendo uma sintaxe](choosing-a-syntax.md).

Para ver uma lista completa das sintaxes fornecidas pelo Active Directory Domain Services, incluindo o valor **CORRESPONDENTE VARTYPE** e [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) de cada sintaxe, consulte [Sintaxes](/windows/desktop/ADSchema/syntaxes).

 

 