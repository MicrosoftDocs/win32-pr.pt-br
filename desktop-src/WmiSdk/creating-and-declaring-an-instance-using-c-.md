---
description: Você pode criar uma instância em C++ por meio da interface IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Criando e declarando uma instância usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046c8c32944c7b726e09eade2701f8d35c9edb0363635eca2a16f7e3d630799a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568795"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>Criando e declarando uma instância usando C++

Você pode criar uma instância em C++ por meio da interface [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

Os exemplos de código neste tópico exigem que a instrução \# include a seguir seja compilada corretamente.


```C++
#include <wbemidl.h>
```



O procedimento a seguir descreve como criar uma instância de uma classe existente.

**Para criar uma instância de uma classe existente**

1.  Recupere a definição da classe existente chamando os métodos [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices::GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

    O exemplo de código a seguir mostra como usar os métodos [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) para obter um ponteiro para a interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) que fornece acesso à definição de classe.

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  Crie a nova instância chamando o [**método IWbemClassObject::SpawnInstance.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

    O exemplo de código a seguir mostra como criar uma nova instância e, em seguida, liberar a classe .

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  De definir valores para todas as propriedades que não herdam os valores definidos para a classe chamando o [**método IWbemClassObject::P ut.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)

    Cada instância de uma classe herda todas as propriedades definidas para a classe . No entanto, você poderá especificar valores de propriedade diferentes se escolher.

    Se a classe existente tiver uma propriedade de chave, você deverá definir a propriedade como **NULL** ou um valor exclusivo garantido. Se você definir a chave como **NULL** e a chave for uma cadeia de caracteres, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) ou [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) gerará internamente e atribuirá um GUID à chave. Dessa forma, especificar **NULL para** uma propriedade de chave permite criar uma instância exclusiva que não substituirá nenhuma instância anterior.

    O exemplo de código a seguir mostra como definir o [**valor da**](swbemrefreshableitem-index.md) propriedade Index da classe de instância de exemplo.

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  De definidos os valores para quaisquer qualificadores relevantes por meio de uma chamada para [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).

    O [**método GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) retorna um ponteiro para uma interface [**IWbemQualifierSet,**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) que usa para acessar os qualificadores de uma classe ou instância. Você poderá especificar valores diferentes para um qualificador definido para a classe se o tipo de qualificador de classe **for EnableOverride**. Não é possível modificar ou excluir um qualificador de classe com o tipo definido como **DisableOverride.** Para obter mais informações, consulte [Qualificador Flavors](qualifier-flavors.md).

    Como opção, você também pode definir qualificadores adicionais para sua classe de instância. Você pode definir qualificadores adicionais para a propriedade de instância ou instância que não precisam aparecer na declaração de classe.

5.  Salve a instância chamando o [**método IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices::P utInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

    O WMI salva a instância no namespace WMI atual. Assim, o caminho completo da instância depende do namespace , que normalmente é o padrão \\ raiz. Para este exemplo de código, o nome completo do caminho seria \\ \\ . \\ root \\ default:Example.Index="IX100".

    O exemplo de código a seguir mostra como salvar uma instância.

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Salvar a instância no WMI bloqueia várias das propriedades da instância.

Especificamente, você não pode executar nenhuma das seguintes operações por meio da API WMI após a existência de uma instância na infraestrutura WMI:

-   Altere a classe pai da classe à qual a instância pertence.
-   Adicionar ou remover propriedades.
-   Alterar tipos de propriedade.
-   Adicionar ou remover [**qualificadores de**](standard-qualifiers.md) chave **ou** indexados.
-   Adicionar ou remover [**qualificadores Singleton,**](standard-wmi-qualifiers.md) **Dynamic** ou [**Abstract.**](standard-qualifiers.md)

O exemplo de código a seguir combina os exemplos de código discutidos no procedimento anterior para mostrar como criar uma instância usando a API WMI.


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



