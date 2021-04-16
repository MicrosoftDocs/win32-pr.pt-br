---
description: O a seguir lista os qualificadores padrão específicos ao WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Qualificadores WMI padrão
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782519"
---
# <a name="standard-wmi-qualifiers"></a>Qualificadores WMI padrão

O a seguir lista os qualificadores padrão específicos ao WMI.

<dt>

<span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Aditamento**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes

Indica que uma classe contém qualificadores corrigidos que estão localizados. O padrão é **true**.

A classe associada pode ser convertida. Para acessar a versão traduzida, use o identificador de localidade para construir um nome de namespace.

</dd> <dt>

<span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Ignorar \_ GetObject**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: métodos

Indica que a chamada de método deve passar diretamente para a chamada **ExecMethodAsync** do provedor, em vez do provedor, primeiro fazendo uma chamada para **GetObject** para validar o caminho do objeto. O padrão é **false**. Usar **bypass \_ GetObject** pode melhorar significativamente o desempenho.

Antes de usar **ignorar \_ GetObject**, certifique-se de que nenhuma das seguintes ações seja executada:

-   Derive uma classe da sua classe.
-   Substitua o método que tem o qualificador **\_ GetObject de bypass** .

A falha em seguir essas precauções pode resultar na invocação da implementação do método da classe pai em vez da classe filho. Para obter mais informações, consulte usando o \_ qualificador GetObject de bypass.

</dd> <dt>

<span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Chave CIM**
</dt> <dd>

Tipo de dados: **CIM \_ booliano**

Aplica-se a: Propriedades

Indica que a propriedade associada é uma propriedade de chave no CIM, mas não no WMI.

</dd> <dt>

<span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)
</dt> <dd>

Tipo de dados: **VT \_ BSTR**

Aplica-se a: Propriedades, métodos, parâmetros

Contém o texto que descreve o tipo de uma propriedade.

</dd> <dt>

<span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**
</dt> <dd>

Tipo de dados: **VT \_ BSTR**

Aplica-se a: classes

Indica que uma classe tem instâncias associadas a mais informações fornecidas dinamicamente por um provedor.

</dd> <dt>

<span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Preterido**
</dt> <dd>

Tipo de dados: **CIM \_ booliano**

Aplica-se a: Propriedades, classes

Indica que a propriedade foi substituída por outra propriedade.

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**
</dt> <dd>

Aplica-se a: classes, propriedades

O **UUID** da classe associada.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dinâmico**](dynamic-qualifier.md)
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes, propriedades

Indica uma classe cujas instâncias são criadas dinamicamente. O valor desse qualificador deve ser definido como **true**.

</dd> <dt>

<span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes, instâncias

Indica que uma instância contém valores fornecidos por provedores de propriedades dinâmicas. O padrão é **true**.

Você deve especificar esse qualificador em uma instância desse tipo. Somente o valor **true** é permitido.

</dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixado**
</dt> <dd>

Tipo de dados: **CIM \_ booliano**

Aplica-se a: instâncias

Indica que o valor dessa propriedade não pode ser alterado durante o tempo de vida da instância.

</dd> <dt>

<span id="ID"></span><span id="id"></span>**SESSÃO**
</dt> <dd>

Tipo de dados: **VT \_ i4**

Aplica-se a: Propriedades, parâmetros

Identifica e sequencia exclusivamente um parâmetro de propriedade ou método quando as instruções MOF são geradas automaticamente.

Esse qualificador é necessário apenas para parâmetros de método. Ao criar parâmetros para um método, os designers de classe devem começar com ID (0) para o primeiro parâmetro e usar cada inteiro sucessivo para cada parâmetro sucessivo. Se os qualificadores de **ID** forem omitidos involuntariamente, o compilador MOF gerará qualificadores de **ID** automaticamente.

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementado**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: métodos

Indica que um método tem uma implementação fornecida por um provedor.

</dd> <dt>

<span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**
</dt> <dd>

Tipo de dados: **VT \_ BSTR**

Aplica-se a: instâncias

Indica que uma instância contém valores fornecidos por um provedor de propriedades dinâmicas.

O valor é passado para o provedor de propriedades como um argumento para o método [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Localidade**
</dt> <dd>

Tipo de dados: **VT \_ BSTR**

Aplica-se a: classes ou instâncias

Especifica o idioma de origem para uma classe ou instância. Para obter mais informações sobre valores de localidade, consulte [códigos de localidade](#locale-codes).

</dd> <dt>

<span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Aplica-se a: instâncias de namespace

Especifica um descritor de segurança para o namespace no formato [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Para obter mais informações, consulte [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md). A cadeia de caracteres SDDL é processada pelo WMI para estabelecer a segurança do namespace, mas não é armazenada como uma cadeia de caracteres. Se nenhum descritor de segurança for especificado, a segurança padrão será usada. Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Adicional**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: parâmetros

Indica que um parâmetro não é necessário e que tem um valor padrão com bom desempenho.

</dd> <dt>

<span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Direitos**
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Aplica-se a: Propriedades, métodos

Conjunto de valores usado para informar ao cliente quais privilégios são necessários para criar instâncias, preencher propriedades ou executar métodos. O padrão é **false**.

</dd> <dt>

<span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**
</dt> <dd>

Tipo de dados: **VT \_ BSTR**

Aplica-se a: Propriedades

Indica que uma propriedade de instância contém valores fornecidos por provedores de propriedades dinâmicas.

Você deve especificar esse qualificador nessa propriedade. O valor é passado para o provedor de propriedades como um argumento para [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Operador**
</dt> <dd>

Tipo de dados: **VT \_ BSTR**

Aplica-se a: classes

O valor desse qualificador é o nome do provedor dinâmico que fornece instâncias de classe e atualiza os dados da instância. Esse nome deve ser registrado com WMI criando uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) com a propriedade **Name** que contém esse nome. Quando esse qualificador é especificado em uma classe cujas instâncias são fornecidas dinamicamente, o qualificador **dinâmico** também deve ser especificado.

</dd> <dt>

<span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: instâncias de namespace

Se definido como **true**, **RequiresEncryption** marca um namespace para que os aplicativos e scripts cliente devam se conectar com a autenticação criptografada. O nível de autenticação deve ser definido para a **privacidade de PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C** em C++. Em script ou Visual Basic, o nível de autenticação deve ser definido como **WbemAuthenticationLevelPktPrivacy**. Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md). O qualificador é usado no [*MOF*](gloss-m.md) com o comando de pré-processador do namespace pragma.

Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md) ou [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md). Os níveis de autenticação de script são definidos em [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Único**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes

Designa uma classe que só pode ter uma instância do e que não contenha propriedades de chave.

Somente o valor **true** (padrão) é permitido.

</dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Auto-estática**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: métodos

Indica se um método pode ser chamado usando a definição de classe ou suas instâncias.

O método não pode ser invocado de uma instância.

</dd> <dt>

<span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Subtipo**
</dt> <dd>

Tipo de dados: **VT \_ BSTR**

Aplica-se a: Propriedades

Indica que uma propriedade do tipo **CIM \_ DateTime** representa um intervalo de tempo em vez de uma hora específica.

Para identificar a propriedade como um intervalo, o valor desse qualificador deve ser "Interval". Todos os outros valores para esse qualificador são reservados para uso futuro.

</dd> <dt>

<span id="UUID"></span><span id="uuid"></span>**PERSONALIZADO**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes

Identificador Universal exclusivo aplicado à classe.

</dd> <dt>

<span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes

O número de versão do objeto de classe. O padrão é **NULL**. O número de versão é incrementado quando são feitas alterações na classe.

</dd> <dt>

<span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Aplica-se a: Propriedades

Conjunto de valores que indica quais privilégios do sistema devem estar disponíveis e habilitados para uma operação de gravação bem-sucedida.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="locale-codes"></a>Códigos de localidade

Um código de localidade tem o formato "MS \_ <Three Digit Language ID> ". Por exemplo, a localidade inglês é MS \_ 409. A tabela a seguir lista as IDs de idioma.



| Idioma              | ID do idioma (hexadecimal) |
|-----------------------|---------------------------|
| Árabe                | 401                       |
| Português (Brasil)   | 416                       |
| Chinês (Simplificado)  | 804                       |
| Chinês (Tradicional) | 404                       |
| Tcheco                 | 405                       |
| Dinamarquês                | 406                       |
| Holandês                 | 413                       |
| Inglês (padrão)     | 409                       |
| Finlandês               | 40b                       |
| Francês                | 40c                       |
| Alemão                | 407                       |
| Grego                 | 408                       |
| Hebraico                | 40d                       |
| Húngaro             | 40e                       |
| Italiano               | 410                       |
| Japonês              | 411                       |
| Coreano                | 412                       |
| Norueguês             | 414                       |
| Polonês                | 415                       |
| Português (Portugal) | 816                       |
| Russo               | 419                       |
| Espanhol               | c0a                       |
| Sueco               | 41D                       |
| Turco               | 41f                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a>Usando o \_ qualificador GetObject de bypass

Usar o qualificador **\_ GetObject de bypass** em um método pode gerar resultados confusos.

O exemplo a seguir define as classes **Shape** e **Circle** . Observe que a classe **Circle** é derivada da classe **Shape** .


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



A seguinte chamada para **ExecMethod** usa um objeto **Circle** chamado "mycircle" para desenhar um círculo.


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



No cenário anterior, o WMI chama **GetObject**; descobre que "Shape. Name = ' mycircle '" é um **círculo**; e executa a implementação de **círculo** de **DrawIt**. No entanto, se você usar o qualificador **\_ GetObject de bypass** em **DrawIt**, o WMI não chamará **GetObject**, não descobrirá que "Shape. Name = ' mycircle '" é um **círculo** e executará a implementação de **forma** de **DrawIt** em vez da implementação de **Circle** de **DrawIt**.

A chamada a seguir para **ExecMethod** sempre invoca a implementação correta de **DrawIt**.


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Qualificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adicionando um qualificador](adding-a-qualifier.md)
</dt> </dl>

 

