---
description: Esta seção fornece informações de classe de WMI e de página de referência.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: Classes WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786171"
---
# <a name="wmi-classes"></a>Classes WMI

Esta seção fornece informações de classe de WMI e de página de referência. Para obter mais informações sobre como recuperar dados de classe ou instância, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md). A lista a seguir lista, descreve e fornece links para informações específicas da classe WMI. Para obter mais informações e exemplos de código de script do uso de classes WMI para obter uma variedade de dados de hardware e sistema operacional, consulte [tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md). Para obter exemplos em C++, consulte [exemplos de aplicativos WMI C++](wmi-c---application-examples.md). [Conectar-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md) mostra como obter dados remotos. Você também pode usar o PowerShell para acessar objetos WMI; para obter uma lista de classes WMI que incluem exemplos de código do PowerShell, consulte [aqui](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).



| Seção                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classes do sistema WMI](wmi-system-classes.md)               | Classes predefinidas que são incluídas em cada namespace no núcleo Instrumentação de Gerenciamento do Windows (WMI). Você pode reconhecer uma classe de sistema WMI porque o nome começa com um sublinhado duplo ( \_ \_ ). Essas classes fornecem grande parte da funcionalidade básica para o WMI. As classes do sistema WMI são semelhantes à finalidade das tabelas do sistema no SQL Server. |
| [Classes MSFT](msft-classes.md)                           | Outras classes da Microsoft que oferecem os meios para manipular vários recursos do sistema operacional, como eventos remotos e extensões de política. As classes de [solução de problemas do WMI](wmi-troubleshooting.md) são classes MSFT que fornecem dados sobre as operações do WMI.                                                                                               |
| [Classes CIM](cimclas.md)                                 | Classes [*de esquema de modelo CIM (CIM)*](gloss-c.md) . Se você quiser escrever suas próprias classes WMI, poderá herdar de uma ou mais dessas classes. As [classes WMI Win32](/windows/desktop/CIMWin32Prov/win32-provider) herdam das classes CIM.                                                                          |
| [Classes de consumidor padrão](standard-consumer-classes.md) | Um conjunto de consumidores de eventos do WMI que disparam uma ação após o recebimento de um evento arbitrário. Para obter mais informações, consulte [monitorando eventos](monitoring-events.md).                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Exemplos de código do centro de scripts de classes WMI

Os seguintes exemplos de código do centro de scripts afetam várias classes WMI em vários namespaces.



| Link                                                                                                                                      | Descrição                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gerenciador de WMI de GUI e gerador de ajuda do método WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Script de exemplo que fornece um Gerenciador de WMI de GUI e o gerador de ajuda do método WMI.                                                                                                                                                        |
| [NameSpaces WMI de pesquisa do Gerenciador WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Permite que os usuários pesquisem classes em todos os namespaces disponíveis nos computadores especificados. Este exemplo é a linha de comando versão do exemplo do Gerenciador WMI do GUI e pode ser considerado uma extensão da lista de Get-WmiObject. |
| [Ferramenta de administração de sistema do Windows Arposh](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | O AWSA foi criado com o administrador do sistema em mente. A solução de problemas do Windows requer uma vasta gama de ferramentas e conhecimento. O AWSA reúne essas ferramentas em um local central e adiciona funcionalidade adicional.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Convenções de nomenclatura para classes e propriedades WMI

Os nomes de propriedade devem estar em conformidade com a sintaxe de formato MOF (MOF) definida pelo protocolo DTMF (Distributed Management Task Force). Os caracteres do identificador inicial devem estar entre as letras de a a z e o caractere de sublinhado ( \_ ). Todos os caracteres adicionais devem estar entre as letras de a a z, o caractere de sublinhado e os numerais de 0 a 9. Para obter mais informações, consulte a seção uso Unicode da [especificação CIM versão 2,2](https://www.dmtf.org/standards/cim).

As palavras de reserva do SQL não devem ser usadas em nomes de classe e propriedade. Para obter uma lista completa das palavras de reserva do SQL e para obter mais informações, consulte a seção de diretrizes da [especificação CIM versão 2,2](https://www.dmtf.org/standards/cim).

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Convenções de documento para uma página de referência de classe WMI

Esta seção identifica e descreve as convenções de documento para uma página de referência de classe WMI.

Uma página de referência típica contém um bloco de sintaxe, uma tabela de métodos e uma lista de propriedades.

-   Bloco de sintaxe

    Uma versão simplificada do código MOF que inclui o nome da classe, a classe pai (se houver) e as propriedades de classe, em ordem alfabética, com tipos de dados.

-   Tabela de métodos

    Se uma classe tiver métodos, os métodos serão listados na tabela imediatamente após o bloco de sintaxe. Cada método implementado é vinculado a uma página de referência.

-   Lista de propriedades

    Cada propriedade de classe é listada com um tipo de dados, tipo de acesso (somente leitura ou leitura/gravação), qualificadores e uma descrição da propriedade.

## <a name="syntax-block"></a>Bloco de sintaxe

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>Tabela de métodos



| Métodos do Win32 \_ XYZ | Descrição                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | Breve descrição do que o método faz. |



 

## <a name="properties-list"></a>Lista de propriedades

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>ABC
</dt> <dd>

Tipo de dados: **UInt16**

Tipo de acesso: mostra se você tem acesso de leitura/gravação ou somente leitura a essa propriedade.

Qualificadores: se presente, mostra os qualificadores para a propriedade. Por exemplo, **chave**, **substituição**.

Descreve a propriedade e fornece informações de herança para a propriedade. Por exemplo, essa propriedade é herdada de ** \_ CIM* XYZ * * *. Há um link para a classe pai se a Microsoft fornecer uma implementação dessa classe. No entanto, as classes CIM não estão disponíveis.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>particular
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Tipo de acesso: Somente leitura

Descrição da propriedade.

</dd> </dl>

## <a name="remarks"></a>Comentários

Fornece mais informações sobre a classe, se aplicável. Também fornece informações de derivação, se aplicável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de WMI](wmi-reference.md)
</dt> </dl>

 

 
