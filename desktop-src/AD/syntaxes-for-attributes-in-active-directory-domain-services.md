---
title: Sintaxes para atributos em Active Directory Domain Services
description: Active Directory Domain Services definir um conjunto de sintaxes de atributo para especificar o tipo de dados contidos em um atributo.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Sintaxes para atributos de Active Directory Domain Services Active Directory
- Atributos Active Directory, sintaxes para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084430"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Sintaxes para atributos em Active Directory Domain Services

Active Directory Domain Services definir um conjunto de sintaxes de atributo para especificar o tipo de dados contidos em um atributo. As sintaxes predefinidas não aparecem na verdade no diretório, e você não pode adicionar novas sintaxes. Vários métodos podem ser usados para identificar a sintaxe de uma classe de atributo:

-   Os métodos [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs. GetEx**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put)e [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) usam a estrutura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) para obter e definir os valores dos atributos de um objeto. O membro **VT** dessa estrutura é um valor **VarType** que identifica o tipo de dados.
-   Os métodos das interfaces [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) usam um valor da enumeração [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) para especificar o tipo de dados.
-   Para especificar a sintaxe de uma nova classe de atributo, defina os atributos [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) e [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) de um objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Se o valor de **oMSyntax** for 127, você também deverá definir o atributo [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) . Para obter mais informações, consulte [escolhendo uma sintaxe](choosing-a-syntax.md).

Para obter uma lista completa das sintaxes fornecidas pelo Active Directory Domain Services, incluindo o valor de **VarType** e [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) correspondente de cada sintaxe, consulte [sintaxes](/windows/desktop/ADSchema/syntaxes).

 

 