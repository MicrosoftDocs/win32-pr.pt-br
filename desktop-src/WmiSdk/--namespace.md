---
description: Representa um namespace WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: Classe __Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836948"
---
# <a name="__namespace-class"></a>\_\_Classe de namespace

A classe de sistema **\_ \_ namespace** representa um namespace WMI.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ namespace** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ namespace** tem essas propriedades.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](standard-qualifiers.md)
</dt> </dl>

Nome do namespace.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ \_ namespace** é derivada de [**\_ \_ SystemClass**](--systemclass.md), que não tem propriedades.

Você pode usar o **\_ \_ namespace** para identificar, criar e excluir namespaces filho no namespace de trabalho atual para o qual você tem um objeto [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . A criação de uma nova instância do **\_ \_ namespace** em qualquer namespace de trabalho cria um namespace filho dentro do namespace de trabalho. Por outro lado, a exclusão de uma instância do **\_ \_ namespace** remove o namespace filho do namespace de trabalho. Observe que a exclusão de um namespace filho também exclui todas as suas classes e instâncias.

Enumerar instâncias dessa classe dentro de qualquer namespace de trabalho fornece os namespaces filho disponíveis.

Por exemplo, dentro do \\ namespace raiz há duas instâncias de **\_ \_ namespace**. Uma tem sua propriedade **Name** definida como "padrão", a outra tem o **nome** definido como "Cimv2". Essas instâncias representam os \\ \\ namespaces raiz padrão \\ e \\ cimv2 raiz, respectivamente.

## <a name="examples"></a>Exemplos

O exemplo de VBScript [listar todos os namespaces WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) na galeria do TechNet usa uma chamada recursiva para listar todas as instâncias da \_ \_ classe namespace em um sistema.

O exemplo de código a seguir recupera todos os namespaces no PowerShell.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



O exemplo de código a seguir melhora o exemplo anterior e adiciona informações adicionais.


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemClass**](--systemclass.md)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




