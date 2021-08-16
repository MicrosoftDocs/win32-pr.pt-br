---
description: Representa um namespace WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace classe
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
ms.openlocfilehash: 4640570dd834b42652d04262b70ec84fac106d99f463ca22144e28ad388a0937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320764"
---
# <a name="__namespace-class"></a>\_\_Classe namespace

A **\_ \_ classe de sistema Namespace** representa um namespace WMI.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Membros

A **\_ \_ classe Namespace** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **\_ \_ classe Namespace** tem essas propriedades.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [ **Chave**](standard-qualifiers.md)
</dt> </dl>

Nome do namespace.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\_ \_ classe Namespace** é derivada de [**\_ \_ SystemClass,**](--systemclass.md)que não tem nenhuma propriedade.

Você pode usar **\_ \_ o Namespace** para identificar, criar e excluir namespaces filho dentro do namespace de trabalho atual para o qual você tem um [**objeto IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) A criação de uma nova instância **\_ \_ do Namespace em** qualquer namespace de trabalho cria um namespace filho dentro do namespace de trabalho. Por outro lado, a exclusão de uma instância do **\_ \_ Namespace** remove o namespace filho do namespace de trabalho. Observe que a exclusão de um namespace filho também exclui todas as suas classes e instâncias.

Enumerar instâncias dessa classe em qualquer namespace de trabalho fornece os namespaces filho disponíveis.

Por exemplo, dentro do \\ namespace raiz há duas instâncias do **\_ \_ Namespace**. Um tem sua **propriedade Name** definida como "Padrão", a outra tem **Nome** definido como "Cimv2". Essas instâncias representam o \\ padrão raiz e os \\ \\ \\ namespaces raiz cimv2, respectivamente.

## <a name="examples"></a>Exemplos

O exemplo Listar Todos os [Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) do WMI VBScript na Galeria do TechNet usa uma chamada recursiva para listar todas as instâncias da classe Namespace em \_ \_ um sistema.

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
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemClass**](--systemclass.md)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




