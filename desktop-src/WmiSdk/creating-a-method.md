---
description: Para criar um método WMI, defina os parâmetros de entrada e saída para o método.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Criando um método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689f69518f440e7c1983a92fbf86877c5c6dd2149ce2b31b8459aa08b9e94c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612526"
---
# <a name="creating-a-wmi-method"></a>Criando um método WMI

Para criar um método WMI, defina os parâmetros de entrada e saída para o método. Os parâmetros de entrada e saída são representados por um [**\_ \_ parâmetro**](--parameters.md)especial de classe do sistema WMI. Para obter mais informações, consulte [chamando um método](calling-a-method.md) e [escrevendo um provedor de método](writing-a-method-provider.md).

As seções a seguir são discutidas neste tópico:

-   [Criando um método de classe WMI no MOF](#creating-a-wmi-class-method-in-mof)
-   [Criando um método de classe WMI em C++](#creating-a-wmi-class-method-in-c)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>Criando um método de classe WMI no MOF

No WMI, os métodos de provedor geralmente são ações distintas relacionadas ao objeto que a classe representa. Em vez de alterar o valor de uma propriedade para executar uma ação, um método deve ser criado. Por exemplo, você pode habilitar ou desabilitar um centro de informações de rede (NIC) que é representado pelo [**Win32 \_ adaptador**](/windows/desktop/CIMWin32Prov/win32-networkadapter) usando os métodos [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) e [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) . Embora essas ações possam ser representadas como uma propriedade de leitura/gravação, o design recomendado é criar um método. Como alternativa, se você quiser tornar um Estado ou valor visível para a classe, a abordagem recomendada é criar uma propriedade de leitura/gravação em vez de um método. No **Win32 \_ adaptador**, a propriedade **netativad** torna o estado do adaptador visível, mas as alterações entre os Estados são executadas pelos métodos **Enable** ou **Disable** .

Declarações de classe podem incluir a declaração de um ou mais métodos. Você pode optar por herdar os métodos de uma classe pai ou implementar suas próprias. Se você optar por implementar seus próprios métodos, deverá declarar o método e marcar o método com marcas de qualificador específicas.

O procedimento a seguir descreve como declarar um método em uma classe que não herda de uma classe base.

**Para declarar um método**

1.  Defina o nome do seu método entre as chaves de uma declaração de classe, seguida por quaisquer qualificadores.

    O exemplo de código a seguir descreve a sintaxe de um método.

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  Quando terminar, insira seu código de formato MOF (MOF) no repositório WMI com uma chamada para o compilador MOF.

    Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).

A lista a seguir define os elementos da declaração do método.

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Operador**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

Vincula um provedor específico à sua descrição de classe. O valor do qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) é o nome do provedor, que informa ao WMI onde o código que dá suporte ao seu método reside. Um provedor também deve marcar com o qualificador **dinâmico** qualquer classe que tenha instâncias dinâmicas. Por outro lado, não use o qualificador **dinâmico** para marcar uma classe que contém uma instância estática com métodos **implementados** .

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementado**
</dt> <dd>

Declara que você implementará um método, em vez de herdar a implementação do método da classe pai. Por padrão, o WMI propaga a implementação da classe pai para uma classe derivada, a menos que a classe derivada forneça uma implementação. Omitir o qualificador **implementado** indica que o método não tem nenhuma implementação nessa classe. Se você redeclarar um método sem o qualificador **implementado** , o WMI ainda pressupõe que você não vai implementar esse método e invoca a implementação do método de classe pai quando chamado. Dessa forma, a redeclaração de um método em uma classe derivada sem anexar o qualificador **implementado** é útil somente quando você adiciona ou remove um qualificador de ou para o método.

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType
</dt> <dd>

Descreve o valor que o método retorna. O valor de retorno para um método deve ser um objeto booliano, numérico, **Char**, **cadeia de caracteres**, [DateTime](datetime.md)ou esquema. Você também pode declarar o tipo de retorno como [void](void.md), indicando que o método não retorna nada. No entanto, você não pode declarar uma matriz como um tipo de valor de retorno.

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName
</dt> <dd>

Define o nome do método. Cada método deve ter um nome exclusivo. O WMI não permite que dois métodos com o mesmo nome e assinaturas diferentes existam em uma classe ou em uma hierarquia de classe. Como tal, você também não pode sobrecarregar um método.

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection
</dt> <dd>

Contém qualificadores que descrevem se um parâmetro é um parâmetro de entrada, um parâmetro de saída ou ambos. Não use o mesmo nome de parâmetro mais de uma vez como um parâmetro de entrada ou mais de uma vez como um parâmetro de saída. Se o mesmo nome de parâmetro aparecer com os qualificadores [**in**](standard-qualifiers.md) e **out** , a funcionalidade será conceitualmente a mesma que usar os qualificadores **in** e **out** em um único parâmetro. No entanto, ao usar declarações separadas, os parâmetros de entrada e saída devem ser exatamente os mesmos em todos os outros aspectos, incluindo o número e o tipo de qualificadores de [**ID**](standard-wmi-qualifiers.md) , e o qualificador deve ser o mesmo e declarado explicitamente para ambos. É altamente recomendável usar os qualificadores **in** e **out** dentro de uma declaração de parâmetro único.

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**
</dt> <dd>

Contém o qualificador de [**ID**](standard-wmi-qualifiers.md) que identifica exclusivamente a posição de cada parâmetro na sequência de parâmetros no método. Por padrão, o compilador MOF marca automaticamente os parâmetros com um qualificador de **ID** . O compilador marca o primeiro parâmetro com um valor de 0 (zero), o segundo parâmetro com um valor de 1 (um) e assim por diante. Se necessário, você pode declarar explicitamente a sequência de ID em seu código MOF.

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType
</dt> <dd>

Descreve o tipo de dados que o método pode aceitar. Você pode definir um tipo de parâmetro como qualquer valor de dados MOF, incluindo uma matriz, objeto de esquema ou referência. Ao usar uma matriz como parâmetro, use a matriz como desassociada ou com um tamanho explícito.

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName
</dt> <dd>

Contém o nome do parâmetro. Você também pode optar por definir o valor padrão do parâmetro neste ponto. Os parâmetros sem valores iniciais permanecem não atribuídos.

</dd> </dl>

O exemplo de código a seguir descreve a lista de parâmetros e qualificadores.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

O exemplo de código a seguir descreve como usar uma matriz em um parâmetro do MOF.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

O exemplo de código a seguir descreve como usar um objeto de esquema como um valor de parâmetro e de retorno.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

O exemplo de código a seguir descreve como incluir duas referências: uma para uma instância da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e outra para uma instância de um tipo de objeto desconhecido.

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a>Criando um método de classe WMI em C++

O procedimento a seguir descreve como criar um método de classe WMI programaticamente.

**Para criar um método de classe WMI programaticamente**

1.  Crie a classe à qual o método pertencerá.

    Você deve primeiro ter uma classe para posicionar o método no antes de criar o método.

2.  Recupere duas classes filhas da classe System [**\_ \_ Parameters**](--parameters.md) usando [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

    Use a primeira classe filho para descrever os parâmetros in e a segunda para descrever os parâmetros out. Se necessário, você pode executar uma única recuperação seguida de uma chamada para o método [**IWbemClassObject:: clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .

3.  Escreva os parâmetros in na primeira classe e os parâmetros out para a segunda classe, usando uma ou mais chamadas para [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Ao descrever os parâmetros para um método, observe as seguintes regras e restrições:

    -   Trate os \[ parâmetros in e out \] como entradas separadas, um no objeto que contém os parâmetros in e um no objeto que contém os parâmetros out.
    -   Além dos \[ qualificadores de saída, \] os qualificadores restantes devem ser exatamente iguais.
    -   Especifique os qualificadores de [**ID**](standard-wmi-qualifiers.md) , começando em 0 (zero), um para cada parâmetro.

        A ordem dos parâmetros de entrada ou saída é estabelecida pelo valor do qualificador de [**ID**](standard-wmi-qualifiers.md) em cada parâmetro. Todos os argumentos de entrada devem preceder quaisquer argumentos de saída. Alterar a ordem dos parâmetros de entrada e saída do método ao atualizar um provedor de métodos existente pode fazer com que os aplicativos que chamam o método falhem. Adicione novos parâmetros de entrada ao final dos parâmetros existentes em vez de inseri-los na sequência que já está estabelecida.

        Certifique-se de não deixar nenhuma lacuna na sequência de qualificador de [**ID**](standard-wmi-qualifiers.md) .

    -   Coloque o valor de retorno na classe out-Parameters como uma propriedade chamada **ReturnValue**.

        Isso identifica a propriedade como o valor de retorno do método. O tipo CIM dessa propriedade é o tipo de retorno do método. Se o método tiver um tipo de retorno de void, não terá uma propriedade **ReturnValue** . Além disso, a propriedade **ReturnValue** não pode ter um qualificador de [**ID**](standard-wmi-qualifiers.md) como os argumentos do método. A atribuição de um qualificador de **ID** à propriedade **ReturnValue** produz um erro de WMI.

    -   Expresse todos os valores de parâmetro padrão para a propriedade na classe.

4.  Coloque os dois objetos de [**\_ \_ parâmetros**](--parameters.md) na classe pai com uma chamada para [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

    Uma única chamada para [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) pode posicionar os dois objetos de [**\_ \_ parâmetros**](--parameters.md) na classe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma classe](creating-a-class.md)
</dt> </dl>

 

 
