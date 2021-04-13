---
description: Instrumentação de Gerenciamento do Windows (WMI) define um conjunto de propriedades do sistema que estão associadas a todas as classes e instâncias de classes.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Propriedades do sistema WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165318"
---
# <a name="wmi-system-properties"></a>Propriedades do sistema WMI

Instrumentação de Gerenciamento do Windows (WMI) define um conjunto de propriedades do sistema que estão associadas a todas as classes e instâncias de classes. Assim como acontece com as classes do sistema, os nomes das propriedades do sistema começam com um sublinhado duplo, distinguindo-os das propriedades criadas por aplicativos ou provedores que não devem começar com um sublinhado simples ou duplo. Outra maneira de identificar uma propriedade do sistema é usar o método [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .

As propriedades do sistema estão disponíveis a qualquer momento, mas os valores podem ser **nulos**. **NULL** indica que uma propriedade não se aplica a um objeto específico. No entanto, as propriedades do sistema podem não estar disponíveis o tempo todo para todas as classes ou instâncias.

## <a name="system-properties"></a>Propriedades do Sistema

A lista a seguir descreve as propriedades do sistema WMI. Os exemplos fornecidos são obtidos das propriedades do sistema da classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , que é descrita na parte inferior deste tópico.

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Classes**
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Tipo de acesso: somente leitura para instâncias; leitura/gravação para classes

O nome da classe.

Exemplo: Win32 \_ OptionalFeature

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivação**
</dt> <dd>

Tipo de dados: matriz de **\_ cadeia de caracteres CIM**

Tipo de acesso: somente leitura para instâncias e classes

Hierarquia de classes da classe ou instância atual. O primeiro elemento é a classe pai imediata, o próximo é seu pai e assim por diante; o último elemento é a classe base.

Exemplo: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dinastia**
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Tipo de acesso: Somente leitura

Nome da classe de nível superior da qual a classe ou instância é derivada. Quando essa classe ou instância é a classe de nível superior, os valores de **\_ \_ dinastia** e **\_ \_ classe** são os mesmos.

Exemplo: CIM \_ ManagedSystemElement

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**
</dt> <dd>

Tipo de dados: **CIM \_ sint32**

Tipo de acesso: Somente leitura

Valor que é usado para distinguir entre classes e instâncias. Esse valor é **a \_ \_ classe WBEM genus** (1) para classes e **a \_ \_ instância do WBEM genus** (2) para instâncias e eventos.

Exemplo: 2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Tipo de acesso: Somente leitura

Nome do [*namespace*](gloss-n.md) da classe ou instância.

Exemplo: raiz \\ cimv2

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Multi-Path**
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Tipo de acesso: Somente leitura

Caminho completo para a classe ou instância — incluindo servidor e namespace.

Exemplo: \\ \\ meuservidor \\ raiz \\ cimv2: Win32 \_ OptionalFeature. Name = "TelnetClient"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Contagem de propriedades \_**
</dt> <dd>

Tipo de dados: **CIM \_ sint32**

Tipo de acesso: Somente leitura

Número de propriedades não do sistema definidas para a classe ou instância.

Exemplo: 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Tipo de acesso: Somente leitura

Caminho relativo para a classe ou instância.

Exemplo: Win32 \_ OptionalFeature. Name = "TelnetClient"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Servidor**
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Tipo de acesso: Somente leitura

Nome do servidor que fornece a classe ou instância.

Exemplo: meuservidor

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Super**
</dt> <dd>

Tipo de dados **: \_ cadeia de caracteres CIM**

Tipo de acesso: Somente leitura

Nome da classe pai imediata da classe ou instância.

Exemplo: CIM \_ LogicalElement

</dd> </dl>

O código do PowerShell a seguir recupera as propriedades da classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , que inclui as propriedades do sistema.


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



O exemplo de código anterior retorna o seguinte:


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
