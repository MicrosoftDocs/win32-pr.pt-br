---
title: Adicionando uma classe auxiliar a uma instância de objeto
description: Os exemplos de código a seguir mostram como usar ADSI e LDAP para adicionar dinamicamente uma classe auxiliar a uma instância de objeto existente.
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6b1f61bffe9081350949cccddc70fee83a568
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007368"
---
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a>Adicionando uma classe auxiliar a uma instância de objeto

Os exemplos de código a seguir mostram como usar ADSI e LDAP para adicionar dinamicamente uma classe auxiliar a uma instância de objeto existente. Os exemplos pressupõem que uma classe auxiliar chamada **Vehicle** é definida no esquema de Active Directory e que a classe **Vehicle** tem um atributo **Vin** .

Quando você adiciona dinamicamente uma classe auxiliar a uma instância de objeto, você deve especificar simultaneamente valores para quaisquer atributos **mustHave** obrigatórios na classe. Os exemplos a seguir mostram como fazer isso com o atributo "Vin", que é considerado obrigatório.

O exemplo de C++ a seguir é associado a um objeto e usa [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) para acrescentar a classe auxiliar à lista de classes na propriedade **objectClass** do objeto. Em seguida, o exemplo usa [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) para definir o valor do atributo **Vin** . Por fim, ele chama [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar as alterações no diretório.


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&var);
```



 

 