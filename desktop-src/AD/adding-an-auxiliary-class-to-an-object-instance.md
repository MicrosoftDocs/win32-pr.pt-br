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
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a><span data-ttu-id="7d99b-103">Adicionando uma classe auxiliar a uma instância de objeto</span><span class="sxs-lookup"><span data-stu-id="7d99b-103">Adding an Auxiliary Class to an Object Instance</span></span>

<span data-ttu-id="7d99b-104">Os exemplos de código a seguir mostram como usar ADSI e LDAP para adicionar dinamicamente uma classe auxiliar a uma instância de objeto existente.</span><span class="sxs-lookup"><span data-stu-id="7d99b-104">The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance.</span></span> <span data-ttu-id="7d99b-105">Os exemplos pressupõem que uma classe auxiliar chamada **Vehicle** é definida no esquema de Active Directory e que a classe **Vehicle** tem um atributo **Vin** .</span><span class="sxs-lookup"><span data-stu-id="7d99b-105">The examples assume that an auxiliary class named **vehicle** is defined in the Active Directory schema, and that the **vehicle** class has a **vin** attribute.</span></span>

<span data-ttu-id="7d99b-106">Quando você adiciona dinamicamente uma classe auxiliar a uma instância de objeto, você deve especificar simultaneamente valores para quaisquer atributos **mustHave** obrigatórios na classe.</span><span class="sxs-lookup"><span data-stu-id="7d99b-106">When you dynamically add an auxiliary class to an object instance, you must simultaneously specify values for any mandatory **mustHave** attributes in the class.</span></span> <span data-ttu-id="7d99b-107">Os exemplos a seguir mostram como fazer isso com o atributo "Vin", que é considerado obrigatório.</span><span class="sxs-lookup"><span data-stu-id="7d99b-107">The following examples show how to do this with the "vin" attribute, which is assumed to be mandatory.</span></span>

<span data-ttu-id="7d99b-108">O exemplo de C++ a seguir é associado a um objeto e usa [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) para acrescentar a classe auxiliar à lista de classes na propriedade **objectClass** do objeto.</span><span class="sxs-lookup"><span data-stu-id="7d99b-108">The following C++ example binds to an object, and uses [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) to append the auxiliary class to the list of classes in the object's **objectClass** property.</span></span> <span data-ttu-id="7d99b-109">Em seguida, o exemplo usa [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) para definir o valor do atributo **Vin** .</span><span class="sxs-lookup"><span data-stu-id="7d99b-109">Then the example uses [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put) to set the value of the **vin** attribute.</span></span> <span data-ttu-id="7d99b-110">Por fim, ele chama [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar as alterações no diretório.</span><span class="sxs-lookup"><span data-stu-id="7d99b-110">Finally, it calls [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>


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



 

 