---
description: A criação de uma classe derivada no WMI é muito semelhante à criação de uma classe base. Assim como com uma classe base, você deve primeiro definir a classe derivada e, em seguida, registrar a classe derivada com wMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Criando uma classe derivada de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cddc2b381346b2765e836bb3606cc06845280c41a7505b872098f383ac0409c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374866"
---
# <a name="creating-a-wmi-derived-class"></a>Criando uma classe derivada de WMI

A criação de uma classe derivada no WMI é muito semelhante à criação de uma classe base. Assim como com uma classe base, você deve primeiro definir a classe derivada e, em seguida, registrar a classe derivada com wMI. A principal diferença é que você deve primeiro localizar a classe pai da qual deseja derivar. Para obter mais informações, consulte [Escrevendo um provedor de classe](writing-a-class-provider.md) e escrevendo um provedor de [instância](writing-an-instance-provider.md).

A maneira recomendada de criar classes para um provedor está em arquivos Managed Object Format (MOF). Várias classes derivadas relacionadas entre si devem ser agrupadas em um arquivo MOF, juntamente com quaisquer classes base das quais derivam propriedades ou métodos. Se você colocar cada classe em um arquivo MOF separado, cada arquivo deverá ser compilado antes que o provedor possa funcionar corretamente.

Depois de criar sua classe, você deve excluir todas as instâncias de sua classe antes de executar qualquer uma das seguintes atividades em sua classe derivada:

-   Altere a classe pai da classe derivada.
-   Adicionar ou remover propriedades.
-   Alterar tipos de propriedade.
-   Adicionar ou remover [**qualificadores de**](key-qualifier.md) chave **ou** indexados.
-   Adicionar ou remover [**qualificadores Singleton,**](standard-wmi-qualifiers.md) **Dynamic** ou [**Abstract.**](standard-qualifiers.md)

> [!Note]  
> Para adicionar, remover ou modificar uma propriedade ou qualificador, chame [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) ou [**SWbemObject.Put \_**](swbemobject-put-.md) e desmarque o parâmetro de sinalizador como "modo de força". O [**qualificador**](standard-qualifiers.md) Abstract só poderá ser usado se a classe pai for abstrata.

 

Ao declarar sua classe derivada, observe as seguintes regras e restrições:

-   A classe pai da classe derivada já deve existir.

    A declaração da classe pai pode aparecer no mesmo arquivo MOF que a classe derivada ou em um arquivo diferente. Se a classe pai for desconhecida, o compilador gerará um erro em tempo de executar.

-   Uma classe derivada pode ter apenas uma única classe pai.

    O WMI não dá suporte a várias heranças. No entanto, uma classe pai pode ter muitas classes derivadas.

-   Você pode definir índices para classes derivadas, mas o WMI não usa esses índices.

    Portanto, especificar um índice em uma classe derivada não melhora o desempenho de consultas para instâncias da classe derivada. Você pode melhorar o desempenho de uma consulta em uma classe derivada especificando propriedades indexadas para a classe pai da classe derivada.

-   As definições de classe derivadas podem ser mais complexas e podem incluir recursos como aliases, qualificadores e tipo de qualificador.

    Para obter mais informações, consulte [Criando um alias](creating-an-alias.md) e [adicionando um qualificador](adding-a-qualifier.md).

-   Se você quiser alterar um qualificador, altere o valor padrão de uma propriedade de classe base ou, mais fortemente, digite uma propriedade de objeto de referência ou inserida de uma classe base, você deverá declarar toda a classe base novamente.
-   O número máximo de propriedades que você pode definir em uma classe WMI é 1024.

> [!Note]  
> As classes não podem ser alteradas durante a execução de provedores. Você deve interromper a atividade, alterar a classe e, em seguida, reiniciar o serviço Windows Management. Atualmente, não é possível detectar uma alteração de classe.

 

Assim como na classe base, o uso mais comum dessa técnica será pelos aplicativos cliente. No entanto, um provedor também pode criar uma classe derivada. Para obter mais informações, consulte [Criando uma classe base e](creating-a-base-class.md) escrevendo um provedor de [classe](writing-a-class-provider.md).

O exemplo de código neste tópico requer que a instrução \# include a seguir seja compilada corretamente.


```C++
#include <wbemidl.h>
```



O procedimento a seguir descreve como criar uma classe derivada usando C++.

**Para criar uma classe derivada usando C++**

1.  Localize a classe base com uma chamada para [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

    O exemplo de código a seguir mostra como localizar a classe base Example.

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  Crie um objeto derivado da classe base com uma chamada para [**IWbemClassObject::SpawnDerivedClass.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)

    O exemplo de código a seguir mostra como criar um objeto de classe derivada.

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  Estabeleça um nome para a classe definindo a propriedade do sistema **\_ \_ CLASS** com uma chamada para o [**método IWbemClassObject::P ut.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)

    O exemplo de código a seguir mostra como atribuir um nome à classe derivada.

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  Crie propriedades adicionais [**com IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    O exemplo de código a seguir mostra como criar propriedades adicionais.

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  Salve a nova classe chamando [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    O exemplo de código a seguir mostra como salvar a nova classe derivada.

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

O exemplo de código a seguir combina os exemplos de código discutidos no procedimento anterior para descrever como criar uma classe derivada usando a API WMI.


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



O procedimento a seguir descreve como definir uma classe derivada usando o código MOF.

**Para definir uma classe derivada usando o código MOF**

1.  Defina sua classe derivada com a palavra-chave **Class,** seguida pelo nome da classe derivada e o nome da classe pai separada por dois-pontos.

    O exemplo de código a seguir descreve uma implementação de uma classe derivada.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  Ao concluir, compile o código MOF com o compilador MOF.

    Para obter mais informações, consulte [Compilando arquivos MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma classe](creating-a-class.md)
</dt> </dl>

 

 



