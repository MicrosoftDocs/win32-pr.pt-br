---
description: A maneira recomendada para criar uma nova classe base WMI para um provedor WMI é em um arquivo formato MOF (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Criando uma classe base WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780279f00eea403b330400c490da75adfa097406796cd0b14f15f9861411bfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071506"
---
# <a name="creating-a-wmi-base-class"></a>Criando uma classe base WMI

A maneira recomendada para criar uma nova classe base WMI para um provedor WMI é em um arquivo formato MOF (MOF). Você também pode criar uma classe base usando a [API com para o WMI](com-api-for-wmi.md). Embora você possa criar uma classe base ou derivada no script, sem que um provedor forneça dados para a classe e suas subclasses, a classe não é útil.

As seções a seguir são discutidas neste tópico:

-   [Criando uma classe base usando o MOF](#creating-a-base-class-using-mof)
-   [Criando uma classe base com C++](#creating-a-base-class-with-c)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-a-base-class-using-mof"></a>Criando uma classe base usando o MOF

As classes WMI geralmente dependem da herança. Antes de criar uma classe base, verifique as classes de modelo CIM (CIM) disponíveis na[DMTF](https://www.dmtf.org/)(Distributed Management Task Force).

Se muitas classes derivadas usarem as mesmas propriedades, coloque essas propriedades e métodos em sua classe base. O número máximo de propriedades que você pode definir em uma classe WMI é 1024.

Ao criar uma classe base, observe a seguinte lista de diretrizes para nomes de classe:

-   Use letras maiúsculas e minúsculas.
-   Inicie um nome de classe com uma letra.
-   Não use um sublinhado à esquerda ou à direita.
-   Defina todos os caracteres restantes como letras, dígitos ou sublinhados.
-   Use uma Convenção de nomenclatura consistente.

    Embora não seja necessário, uma boa Convenção de nomenclatura para uma classe é dois componentes Unidos por um sublinhado. Quando possível, um nome de fornecedor deve criar a primeira metade do nome e um nome de classe descritivo deve ser a segunda parte.

> [!Note]  
> Classes não podem ser alteradas durante a execução de provedores. você deve interromper a atividade, alterar a classe e reiniciar o serviço de gerenciamento de Windows. Atualmente, não é possível detectar uma alteração de classe.

 

No MOF, crie uma classe base, nomeando-a com a palavra-chave **Class** , mas não indicando uma classe pai.

**Para criar uma classe base usando o código MOF**

1.  Use a palavra-chave **Class** com o nome da nova classe, seguida por um par de chaves e um ponto-e-vírgula. Adicione Propriedades e métodos para a classe entre as chaves. O exemplo de código a seguir é fornecido.

    O exemplo de código a seguir mostra como uma classe base deve ser definida.

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    O exemplo de código a seguir mostra uma definição incorreta de uma classe base.

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  Adicione qualquer [*qualificador*](gloss-q.md) de classe antes da palavra-chave class para modificar a maneira como a classe é usada. Coloque os qualificadores entre colchetes. Para obter mais informações sobre qualificadores para modificar classes, consulte [qualificadores WMI](wmi-qualifiers.md). Use o qualificador **abstract** para indicar que você não pode criar uma instância dessa classe diretamente. Classes abstratas são geralmente usadas para definir propriedades ou métodos que serão usados por várias classes derivadas. Para obter mais informações, consulte [criando uma classe derivada](creating-a-derived-class.md).

    O exemplo de código a seguir define a classe como abstrata e define o provedor que fornecerá os dados. O [*tipo*](gloss-f.md) de qualificador **ToSubClass** indica que as informações no qualificador de **provedor** são herdadas por classes derivadas.

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  Adicione as propriedades e os métodos para a classe dentro de colchetes antes do nome da propriedade ou do método. Para obter mais informações, consulte [adicionando uma propriedade](adding-a-property.md) e [criando um método](creating-a-method.md). Você pode modificar essas propriedades e métodos usando qualificadores MOF. Para obter mais informações, consulte [adicionando um qualificador](adding-a-qualifier.md).

    O exemplo de código a seguir mostra como modificar propriedades e métodos com qualificadores MOF.

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  Salve o arquivo MOF com uma extensão. mof.
5.  Registre a classe com WMI executando [**Mofcomp.exe**](mofcomp.md) no arquivo.

    **mofcomp.exe** *newmof. mof*

    Se você não usar a opção **-N** ou o \# [**namespace pragma**](pragma-namespace.md) do comando de pré-processador para especificar um namespace, as classes MOF compiladas serão armazenadas no \\ namespace root padrão no repositório. Para obter mais informações, consulte [**Mofcomp**](mofcomp.md).

O exemplo de código a seguir combina os exemplos de código MOF discutidos no procedimento anterior e mostra como criar uma classe base no \\ namespace raiz cimv2 usando o MOF.

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

Para obter mais informações, consulte [criando uma classe derivada](creating-a-derived-class.md) para obter um exemplo de uma classe dinâmica derivada desta classe base.

## <a name="creating-a-base-class-with-c"></a>Criando uma classe base com C++

Criar uma classe base usando a API do WMI é principalmente uma série de comandos Put que definem a classe e registram a classe com o WMI. A principal finalidade dessa API é permitir que aplicativos cliente criem classes base. No entanto, você também pode fazer com que um provedor Use essa API para criar uma classe base. Por exemplo, se você acreditar que o código MOF para seu provedor não será instalado corretamente, você poderá instruir seu provedor para criar automaticamente as classes corretas no repositório do WMI. Para obter mais informações sobre provedores, consulte [escrevendo um provedor de classe](writing-a-class-provider.md).

> [!Note]  
> Classes não podem ser alteradas durante a execução de provedores. você deve interromper a atividade, alterar a classe e reiniciar o serviço de gerenciamento de Windows. Atualmente, não é possível detectar uma alteração de classe.

 

O código requer a seguinte referência para compilar corretamente.


```C++
#include <wbemidl.h>
```



Você pode criar uma nova classe base programaticamente usando a [API com para o WMI](com-api-for-wmi.md).

**Para criar uma nova classe base com a API do WMI**

1.  Recupere uma definição para a nova classe chamando o método [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) com o parâmetro *strObjectPath* definido como um valor **nulo** .

    O exemplo de código a seguir mostra como recuperar uma definição para uma nova classe.

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  Estabeleça um nome para a classe definindo a propriedade do sistema de **\_ \_ classe** com uma chamada para o método [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    O exemplo de código a seguir mostra como nomear a classe definindo a propriedade do sistema de **\_ \_ classe** .

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  Crie a propriedade ou propriedades de chave chamando [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    O exemplo de código a seguir descreve como criar a propriedade [**index**](swbemrefreshableitem-index.md) , que é rotulada como uma propriedade de chave na etapa 4.

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  Anexe o qualificador padrão da [**chave**](standard-qualifiers.md) à propriedade de chave chamando primeiro o método [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) e, em seguida, o método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    O exemplo de código a seguir mostra como anexar o qualificador de [**chave**](standard-qualifiers.md) padrão à propriedade de chave.

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  Crie outras propriedades da classe com [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    O exemplo de código a seguir descreve como criar propriedades adicionais.

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  Registre a nova classe chamando [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Como não é possível definir chaves e índices depois de registrar uma nova classe, verifique se você definiu todas as suas propriedades antes de chamar [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    O exemplo de código a seguir descreve como registrar uma nova classe.

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

O exemplo de código a seguir combina os exemplos de código discutidos no procedimento anterior e mostra como criar uma classe base usando a API do WMI.


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma classe](creating-a-class.md)
</dt> </dl>

 

 



