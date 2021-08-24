---
title: Gerenciamento de esquema
description: O componente do provedor de exemplo ADSI define as classes de esquema \ 0034; Organizational Unit \ 0034; e \ 0034; Usuário \ 0034; e gerencia essas classes de esquema da seguinte maneira.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- ADSI de gerenciamento de esquema
- ADSI de gerenciamento de esquema
- Gerenciando esquemas ADSI
- esquemas, gerenciando ADSI
- Gerenciando um esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddb8fcc3d29dce27ac2b74c9c8e79d1cef2f9d2a23307e9b7626861ed3e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770477"
---
# <a name="schema-management"></a>Gerenciamento de esquema

O componente do provedor de exemplo ADSI define as classes de esquema "Organizational Unit" e "user" e gerencia essas classes de esquema da seguinte maneira.

A classe de esquema "Organizational Unit" é representada por um objeto de contêiner ADs e pode conter outras "unidades organizacionais" e "usuários". O objeto contêiner dá suporte às interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). A classe de esquema "user" é representada por um objeto Active Directory genérico e não contém outros tipos de objetos. No componente de provedor de exemplo, o objeto de usuário é implementado como um objeto de Active Directory genérico que dá suporte às interfaces **IUnknown**, **IDispatch** e **IADs**. Lembre-se de que o objeto de usuário, nesse caso, não oferece suporte à interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .

O componente de provedor de exemplo também deve implementar o objeto de namespace ADs, que dá suporte às interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

A figura a seguir mostra os detalhes do esquema que representa as duas classes de esquema de componente de provedor de exemplo.

![esquema de componente do provedor de exemplo ADSI](images/dssmsch.png)

Lembre-se de que, na figura anterior, a classe de esquema "Organizational Unit" define três propriedades: "Description", "headcounts" e "ID". A classe de esquema "user" define quatro propriedades: "ID", "Name", "PhoneNumber" e "title". A propriedade "ID" é compartilhada por ambas as classes de esquema. Cada propriedade é definida pelo objeto de sintaxe "String" ou "Integer".

> [!Note]  
> Os objetos de sintaxe não estão presentes na primeira versão do componente de provedor de exemplo. No entanto, na maioria das implementações de esquema ADSI da Microsoft, os objetos de sintaxe são incluídos no objeto de contêiner de esquema, assim como os objetos de classe de esquema e propriedade. Por esse motivo, eles são mostrados aqui.

 

Esse componente de provedor torna os dados de esquema acessíveis para o aplicativo cliente ADSI na forma de objetos de classe ADs, objetos de propriedade ADs e objetos de sintaxe ADs, tudo dentro de um objeto contêiner de classe de esquema, para que os dados de esquema possam ser recuperados em tempo de execução.

O ADsPaths para os objetos de contêiner de classe de esquema definidos para o componente de provedor de exemplo são "Sample://Seattle/schema" e "Sample://Toronto/schema". Neste exemplo, o conteúdo dos esquemas é idêntico.

 

 