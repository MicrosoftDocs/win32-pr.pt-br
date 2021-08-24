---
description: Esta seção fornece informações de página de referência e classe WMI.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: WMI Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1da15af60f1d1a32d652c8776e20ef36d65c1ff158dc6ac7465886361c5862c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757506"
---
# <a name="wmi-classes"></a>WMI Classes

Esta seção fornece informações de página de referência e classe WMI. Para obter mais informações sobre como recuperar dados de classe ou instância, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md). A lista a seguir lista, descreve e fornece links para informações específicas da classe WMI. Para obter mais informações e exemplos de código de script do uso de classes WMI para obter uma variedade de dados de hardware e sistema operacional, consulte [Tarefas WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md). Para exemplos em C++, consulte [Exemplos de aplicativo WMI C++.](wmi-c---application-examples.md) [Conectar-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md) mostra como obter dados remotos. Você também pode usar o PowerShell para acessar objetos WMI; para ver uma lista de classes WMI que incluem exemplos de código do PowerShell, consulte [aqui](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).



| Seção                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classes do sistema WMI](wmi-system-classes.md)               | Classes predefinidas incluídas em cada namespace no núcleo Windows WMI (Instrumentação de Gerenciamento de Dados). Você pode reconhecer uma classe de sistema WMI porque o nome começa com um sublinhado duplo ( \_ \_ ). Essas classes fornecem grande parte da funcionalidade básica para o WMI. As classes do sistema WMI são semelhantes para as tabelas do sistema no SQL servidor. |
| [MSFT Classes](msft-classes.md)                           | Outras classes da Microsoft que oferecem os meios para manipular vários recursos do sistema operacional, como eventos remotos e extensões de política. As [classes de solução de problemas do WMI](wmi-troubleshooting.md) são classes MSFT que fornecem dados sobre operações WMI.                                                                                               |
| [CIM Classes](cimclas.md)                                 | [*classes de esquema modelo CIM (CIM).*](gloss-c.md) Se você quiser escrever suas próprias classes WMI, poderá herdar de uma ou mais dessas classes. As classes [Win32 do](/windows/desktop/CIMWin32Prov/win32-provider) WMI herdam das classes CIM.                                                                          |
| [Classes de consumidor padrão](standard-consumer-classes.md) | Um conjunto de consumidores de eventos WMI que disparam uma ação após o recebimento de um evento arbitrário. Para obter mais informações, consulte [Monitoramento de eventos](monitoring-events.md).                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Exemplos de código do WMI Class Scripting Center

Os exemplos de código do Centro de Script a seguir afetam várias classes WMI em vários namespaces.



| Link                                                                                                                                      | Descrição                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gui WMI Explorer e Gerador de Ajuda do Método WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Script de exemplo que fornece um Explorador WMI de GUI e o Gerador de Ajuda do Método WMI.                                                                                                                                                        |
| [WMI Explorer Search WMI NameSpaces](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Permite que os usuários pesquisem classes em todos os namespaces disponíveis nos computadores especificados. Este exemplo é a linha de comando da amostra do WMI Explorer da GUI e pode ser considerada uma extensão de Get-WmiObject -List. |
| [Ferramenta de administração Windows sistema do Arp tool](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | A AWSA foi criada com o Administrador do Sistema em mente. A solução Windows problemas requer uma ampla gama de ferramentas e conhecimento. A AWSA reúne essas ferramentas em um local central e adiciona funcionalidade adicional.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Convenções de nomensão para classes e propriedades WMI

Os nomes de propriedade devem estar em conformidade com a sintaxe Managed Object Format (MOF) definida pela DTMF (Distributed Management Task Force). Os caracteres iniciais do identificador devem ser das letras a a z e do caractere de sublinhado ( \_ ). Todos os caracteres adicionais devem ser das letras a a z, do caractere de sublinhado e dos numerais de 0 a 9. Para obter mais informações, consulte a seção Uso de Unicode da [Especificação CIM Versão 2.2](https://www.dmtf.org/standards/cim).

SQL palavras de reserva não devem ser usadas em nomes de classe e propriedade. Para obter uma lista completa das SQL palavras e para obter mais informações, consulte a seção Diretrizes da Especificação [CIM Versão 2.2](https://www.dmtf.org/standards/cim).

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Convenções de documento para uma página de referência de classe WMI

Esta seção identifica e descreve as convenções de documento para uma página de referência de classe WMI.

Uma página de referência típica contém um bloco de sintaxe, uma tabela de métodos e uma lista de propriedades.

-   Bloco de sintaxe

    Uma versão simplificada do código MOF que inclui o nome da classe, a classe pai (se alguma) e as propriedades da classe, em ordem alfabética, com tipos de dados.

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



| Métodos Xyz do Win32 \_ | Descrição                                |
|--------------------|--------------------------------------------|
| *Somemethod*       | Breve descrição do que o método faz. |



 

## <a name="properties-list"></a>Lista de propriedades

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>Abc
</dt> <dd>

Tipo de dados: **uint16**

Tipo de acesso: mostra se você tem acesso de leitura/gravação ou somente leitura a essa propriedade.

Qualificadores: se presente, mostra os qualificadores para a propriedade . Por exemplo, **Chave**, **Substituir**.

Descreve a propriedade e fornece informações de herança para a propriedade . Por exemplo, essa propriedade é herdada de **CIM \_* xyz***. Haverá um link para a classe pai se a Microsoft fornece uma implementação dessa classe. No entanto, as classes CIM não estão disponíveis.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>Def
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Tipo de acesso: Somente leitura

Descrição da propriedade.

</dd> </dl>

## <a name="remarks"></a>Comentários

Fornece mais informações sobre a classe , se aplicável. Também fornece informações de derivação, se aplicável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de WMI](wmi-reference.md)
</dt> </dl>

 

 
