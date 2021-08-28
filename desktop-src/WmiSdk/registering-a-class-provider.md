---
description: Para criar um provedor de classes WMI, você deve registrar a \_ \_ instância Win32Provider que representa seu provedor usando uma instância de \_ \_ ClassProviderRegistration.
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: Registrando um provedor de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16a28b489f2cfd01163d6b32c9a70c0d8a193a542197795d6d2b40de0e1baef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316478"
---
# <a name="registering-a-class-provider"></a>Registrando um provedor de classe

Para criar um provedor de classes WMI, você deve registrar a instância [**\_ \_ Win32Provider**](--win32provider.md) que representa seu provedor usando uma instância de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md). Como um objeto COM, seu provedor deve se registrar no sistema operacional e no WMI. O procedimento a seguir pressupõe que você já implementou o processo de registro conforme descrito em [registrando um provedor](registering-a-provider.md). Se o provedor armazenar a maioria dos dados no repositório WMI e se os dados forem atualizados somente na inicialização do WMI, registre sua classe como um provedor de classe Push. Se os dados que você está fornecendo mudam com frequência e são recuperados dinamicamente pelo seu código em cada solicitação do WMI, Registre seu provedor como um provedor de classe pull.

O procedimento a seguir descreve como registrar um provedor de classe Push.

**Para registrar um provedor de classe push**

-   Defina a propriedade **interactiontype** da instância [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) como 1.

    A criação de uma instância do [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) faz parte do processo de registro.

O procedimento a seguir descreve como registrar um provedor de classe pull.

**Para registrar um provedor de classe pull**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.
2.  Crie uma instância da classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) que descreve o conjunto de recursos do provedor.

    Na instância de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) :

    1.  Defina a propriedade **interactiontype** para indicar se o provedor é um provedor de Push ou pull.
    2.  Marque a classe com os qualificadores [**dinâmicos**](standard-wmi-qualifiers.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .

        O qualificador [**dinâmico**](standard-wmi-qualifiers.md) sinaliza que o WMI deve usar um provedor para recuperar as instâncias de classe. O qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) especifica o nome do provedor que o WMI deve usar.

    3.  Defina as propriedades **ResultSetQueries**, **ReferencedSetQueries** e **UnsupportedQueries** .

        Essas propriedades de consulta descrevem informações detalhadas sobre a classe com suporte.

Além de descrever os vários métodos com suporte de uma classe, a classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) também tem três propriedades que descrevem uma série de consultas. Quando usadas juntas, essas três propriedades descrevem todo o intervalo de classes fornecidas pelo provedor de classe. Cada propriedade de consulta contém uma instrução de seleção WQL, chamada de "consulta de esquema", para especificar os tipos de classes com suporte. Consultas de esquema especificam um nome de classe especial chamado meta \_ Class. A tabela a seguir lista as propriedades de consulta.



| Propriedade                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ResultSetQueries**     | Contém informações sobre o conjunto de resultados que o provedor fornece. O WMI usa as informações para determinar se deve invocar o provedor para atender a uma consulta de um aplicativo. Esta propriedade descreve o conjunto de todas as classes que o provedor pode fornecer ou um superconjunto das classes disponíveis, mas nunca um subconjunto. O WMI requer um provedor para especificar pelo menos uma consulta nesta propriedade.<br/> O exemplo a seguir mostra como definir **ResultSetQueries** quando um provedor fornece uma classe de associação que faz referência à classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> O exemplo a seguir mostra como especificar uma consulta geral quando um provedor fornece classes que fazem referência a outras classes desconhecidas.<br/> `SELECT * FROM meta_class`<br/> O exemplo a seguir mostra como definir **ResultSetQueries** quando um provedor fornece apenas subclasses, mas não a classe pai de uma determinada classe.<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> O exemplo a seguir mostra como usar a \_ \_ propriedade especial this e Set **ResultSetQueries** quando um provedor fornece todas as classes e subclasses.<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **ReferencedSetQueries** | Determina se o provedor deve ser ignorado em consultas de esquema em que as associações e referências estão sendo solicitadas. Provedores que podem fornecer classes de associação devem incluir pelo menos uma consulta em sua propriedade **ReferencedSetQueries** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **UnsupportedQueries**   | Contém informações sobre o conjunto de resultados que um provedor de classe não fornece. O WMI usa essa propriedade para subtrair do conjunto de classes implícitas por **ResultSetQueries**. Por exemplo, um provedor de classe pode especificar no suporte **ResultSetQueries** para todas as classes derivadas de MyClass e especificar em **UnsupportedQueries** a falta de suporte para uma classe derivada específica.<br/> Quanto mais informações o provedor puder registrar sobre seus recursos de processamento de consulta, mais rápido será executado. A inserção de uma ou mais consultas na propriedade **UnsupportedQueries** é uma maneira de ser específica e é particularmente importante quando um provedor se baseia em uma classe que não fornece. Quando uma solicitação é feita para uma classe que está listada em uma consulta na propriedade **UnsupportedQueries** , o WMI pode fornecer a própria classe ou invocar um provedor alternativo para fornecê-la.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Como o WMI não oferece suporte à cláusula OR, você deve criar uma consulta separada para cada classe.

As consultas a seguir são especificadas em **ResultSetQueries** quando um provedor de classe fornece MyClass1, MyClass2 e MyClass3.


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



Somente os administradores podem registrar ou excluir um provedor criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e do [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md).

 

