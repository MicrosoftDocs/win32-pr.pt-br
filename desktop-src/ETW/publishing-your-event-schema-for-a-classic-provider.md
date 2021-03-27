---
description: Os provedores clássicos devem usar formato MOF (MOF) para publicar o layout de seus dados de evento. Os consumidores podem ler o layout publicado do WMI em tempo de execução e usá-lo para ler os dados do evento.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Publicando seu esquema de evento para um provedor clássico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296425"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>Publicando seu esquema de evento para um provedor clássico

Os provedores [clássicos](about-event-tracing.md) devem usar [formato MOF](../wmisdk/managed-object-format--mof-.md) (MOF) para publicar o layout de seus dados de evento. Os consumidores podem ler o layout publicado do WMI em tempo de execução e usá-lo para ler os dados do evento.

Se você usar o MOF para publicar o layout dos dados de evento no WMI, normalmente criará os três tipos de classes MOF a seguir no \\ namespace WMI raiz:

-   [Uma classe MOF de provedor](#provider-mof-classes)
-   [Uma ou mais classes MOF de evento](#event-mof-classes)
-   [Uma ou mais classes MOF de tipo de evento](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>Classes MOF do provedor

Se você publicar o layout dos dados do evento, deverá criar uma classe MOF que identifique seu provedor. Essa classe deve derivar da classe **EventTrace** MOF e deve estar vazia (sem propriedades ou métodos). A classe também deve incluir o qualificador **GUID** que identifica exclusivamente o provedor. Esse é o mesmo GUID que você usa ao chamar a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para registrar seu provedor.

## <a name="event-mof-classes"></a>Classes do evento MOF

Uma classe MOF de evento define uma classe de eventos que o provedor fornece. Essa classe deriva da classe MOF do provedor e deve estar vazia (sem propriedades ou métodos). A classe também deve incluir o qualificador **GUID** que identifica exclusivamente a classe de eventos que suas classes filhas definem. O provedor usa esse mesmo GUID ao definir o membro **GUID** da estrutura [**do \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

## <a name="event-type-mof-classes"></a>Classes MOF de tipo de evento

Uma classe de tipo de evento MOF define os dados de evento reais. Essa classe deriva de sua classe MOF de evento pai. Ao nomear a classe MOF do tipo de evento, a Convenção é usar o nome da classe MOF do evento no início do tipo de evento nome da classe MOF. Por exemplo, se o nome da classe MOF do evento for HWConfig e a classe MOF de tipo de evento representar informações de CPU, você deverá nomear o tipo de evento classe MOF, \_ CPU HWConfig.

Use o qualificador **EventType** na classe do tipo de evento MOF para identificar o tipo de evento. Se vários tipos de eventos usarem os mesmos dados de evento, eles poderão usar a mesma classe MOF. O provedor usa o mesmo valor de tipo de evento para identificar o evento ao definir o membro **Class. Type** da estrutura do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

A classe MOF de tipo de evento contém propriedades. A ordem dessas propriedades define o layout dos dados do evento. A tabela a seguir identifica os tipos de dados e qualificadores que você pode usar para definir as propriedades. Para obter mais informações sobre os qualificadores de classe e propriedade que você pode usar, consulte [qualificadores MOF de rastreamento de eventos](event-tracing-mof-qualifiers.md).



| Tipo de dados              | Qualificadores                        | Descrição                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**, **uint8**   | **Formato**                        | Declara um inteiro decimal de 1 byte. Para declarar um caractere ANSI, use o qualificador de **formato** e defina seu valor como "c".                                                                                                                                                                                                  |
| **sint16**, **UInt16** | **Formato**                        | Declara um inteiro decimal de 2 bytes. Para indicar que o número é um número hexadecimal, use o qualificador de **formato** . Por exemplo, Format ("x").                                                                                                                                                                               |
| **sint32**, **UInt32** | **Formato**                        | Declara um inteiro decimal de 4 bytes. Para indicar que o número é um número hexadecimal, use o qualificador de **formato** e defina seu valor como "x".                                                                                                                                                                                |
| **sint64**, **UInt64** | **Formato**                        | Declara um inteiro decimal de 8 bytes. Para indicar que o número é um número hexadecimal, use o qualificador de **formato** e defina seu valor como "x".                                                                                                                                                                                |
| **booleano**            |                                   | Declara um valor booliano. O consumidor do evento deve interpretar o valor como BOOL (inteiro de 4 bytes).                                                                                                                                                                                                                        |
| **char16**             |                                   | Declara um caractere largo. O consumidor de evento deve interpretar matrizes char16 em eventos de kernel como cadeias de caracteres largos. (Use o tamanho da matriz para copiar a cadeia de caracteres. Algumas cadeias de caracteres podem conter espaços nulos à esquerda.)                                                                                                      |
| **object**             | **Extensão**                     | Declara um blob binário. O qualificador de **extensão** indica o tipo de dados no BLOB.                                                                                                                                                                                                                              |
| **cadeia de caracteres**             | **Formato**, **StringTermination** | Declara um valor de cadeia de caracteres. Para indicar que a cadeia de caracteres é uma cadeia de caracteres largos, use o qualificador de **formato** e defina seu valor como "w". A cadeia de caracteres será considerada uma cadeia de caracteres ANSI se você não especificar o qualificador de **formato** . Para indicar como a cadeia de caracteres é encerrada, use o qualificador **StringTermination** . <br/> |



 

Para especificar uma matriz, você pode usar colchetes, \[ \] . Os colchetes podem incluir o tamanho da matriz. Por exemplo:

`[WmiDataId(1), read] uint8 MyGuid[16];`

Você também pode usar o qualificador **máximo** para especificar o tamanho de uma matriz. Por exemplo:

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

Se você incluir o tamanho da matriz entre colchetes, o compilador MOF gerará o qualificador máximo para você.

É importante que você use o qualificador de **Descrição** para cada propriedade. A descrição deve conter um nome de exibição que o consumidor possa usar ao exibir os valores de propriedade.

O exemplo a seguir mostra o conteúdo de um arquivo MOF que descreve um provedor, evento e classe de tipo de evento MOF.

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

Observe que os nomes de classe MOF do provedor, do evento e do tipo de evento devem ser exclusivos em todo o namespace. Para evitar conflitos de nomenclatura, você deve usar um nome exclusivo e descritivo para todos os nomes de classe. As propriedades de classe também devem ser descritivas e exclusivas em sua hierarquia de classe — uma classe filha que contém o mesmo nome de propriedade que uma classe pai substitui a propriedade da classe pai.

Depois de definir suas classes MOF, use o compilador MOF para gerar seu esquema de evento e adicioná-lo ao repositório CIM. Os consumidores podem ler o esquema do repositório e ler programaticamente os dados do evento. Para obter uma descrição completa da sintaxe do MOF e usar o compilador MOF (Mofcomp.exe) para adicionar suas classes MOF ao repositório CIM, consulte [formato MOF](../wmisdk/managed-object-format--mof-.md). Para obter informações sobre como usar Wbemtest.exe para acessar o repositório CIM, consulte [Instrumentação de gerenciamento do Windows](../wmisdk/wmi-start-page.md) (WMI).

## <a name="versioning-mof-class"></a>Classe MOF de controle de versão

Se você adicionar ou alterar uma classe MOF de tipo de evento, a Convenção será a versão da classe MOF de evento e de seu tipo de evento filho classes MOF. Para obter a versão da classe MOF do evento atual, acrescente \_ vn ao nome da classe, em que n é um número incremental começando em 0. Se esta for a primeira revisão para a classe, acrescente \_ V0 ao nome da classe. Você também deve adicionar o qualificador **EventVersion** à classe. Use o mesmo número de versão usado no nome de classe para o valor do qualificador **EventVersion** .

A nova versão da classe MOF de evento deve usar o mesmo nome e qualificador **GUID** da classe original. A nova classe pode opcionalmente adicionar o qualificador **EventVersion** . A classe MOF de evento que não contém o qualificador **EventVersion** é considerada a versão mais recente, ou se todas as versões da classe contiverem um qualificador **EventVersion** , a classe com o número de versão mais alto será considerada a versão mais recente. O provedor usa o membro **Class. Version** da estrutura [**de \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar a versão do evento incluído no rastreamento.

O exemplo a seguir mostra como fazer a versão de uma classe MOF de evento.

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
