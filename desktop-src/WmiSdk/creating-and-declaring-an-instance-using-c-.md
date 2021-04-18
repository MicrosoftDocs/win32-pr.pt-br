---
description: Você pode criar uma instância em C++ por meio da interface IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Criando e declarando uma instância usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761512"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>Criando e declarando uma instância usando C++

Você pode criar uma instância em C++ por meio da interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

Os exemplos de código neste tópico exigem a seguinte \# instrução include para serem compiladas corretamente.


```C++
#include <wbemidl.h>
```



O procedimento a seguir descreve como criar uma instância de uma classe existente.

**Para criar uma instância de uma classe existente**

1.  Recupere a definição da classe existente chamando os métodos [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

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

    

2.  Crie a nova instância chamando o método [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

    O exemplo de código a seguir mostra como criar uma nova instância e, em seguida, liberar a classe.

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Defina valores para todas as propriedades que não herdam os valores definidos para a classe chamando o método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    Cada instância de uma classe herda todas as propriedades que são definidas para a classe. No entanto, você pode especificar valores de propriedade diferentes se escolher.

    Se a classe existente tiver uma propriedade de chave, você deverá definir a propriedade como **NULL** ou um valor exclusivo garantido. Se você definir a chave como **NULL** e a chave for uma cadeia de caracteres, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) ou [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) gerará internamente e atribuirá um GUID à chave. Dessa forma, especificar **NULL** para uma propriedade de chave permite criar uma instância exclusiva que não substituirá nenhuma instância anterior.

    O exemplo de código a seguir mostra como definir o valor da propriedade [**index**](swbemrefreshableitem-index.md) da classe de instância de exemplo.

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

    

4.  Defina os valores para quaisquer qualificadores relevantes por meio de uma chamada para [**IWbemClassObject:: Getqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).

    O método [**Getqualifierset**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) retorna um ponteiro para uma interface [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , que usa para acessar os qualificadores para uma classe ou instância. Você pode especificar valores diferentes para um qualificador definido para a classe se o tipo de qualificador de classe for **EnableOverride**. Você não pode modificar ou excluir um qualificador de classe com o tipo definido como **DisableOverride**. Para obter mais informações, consulte [qualificadores de tipos](qualifier-flavors.md).

    Como opção, você também pode definir qualificadores adicionais para sua classe de instância. Você pode definir qualificadores adicionais para a propriedade instância ou instância que não precisam aparecer na declaração de classe.

5.  Salve a instância chamando o método [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    O WMI salva a instância no namespace WMI atual. Como tal, o caminho completo da instância depende do namespace, que normalmente é o \\ padrão raiz. Para este exemplo de código, o nome do caminho completo seria \\ \\ . \\ raiz \\ padrão: example. index = "IX100".

    O exemplo de código a seguir mostra como salvar uma instância do.

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Salvar a instância em bloqueios de WMI reduz várias das propriedades da instância.

Especificamente, você não pode executar nenhuma das seguintes operações por meio da API do WMI depois que existe uma instância dentro da infraestrutura do WMI:

-   Altere a classe pai da classe à qual a instância pertence.
-   Adicionar ou remover propriedades.
-   Alterar tipos de propriedade.
-   Adicionar ou remover qualificadores **indexados** ou de [**chave**](standard-qualifiers.md) .
-   Adicionar ou remover qualificadores [**singleton**](standard-wmi-qualifiers.md), **dinâmico** ou [**abstrato**](standard-qualifiers.md) .

O exemplo de código a seguir combina os exemplos de código discutidos no procedimento anterior para mostrar como criar uma instância usando a API do WMI.


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



 

 



