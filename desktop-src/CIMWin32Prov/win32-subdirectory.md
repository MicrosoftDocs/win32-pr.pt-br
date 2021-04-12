---
description: A \_ classe WMI de associação de subdiretório Win32 relaciona um diretório (pasta) e um de seus subdiretórios (subpastas).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Classe Win32_SubDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089454"
---
# <a name="win32_subdirectory-class"></a>\_Classe de subdiretório Win32

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação de **\_ subdiretório Win32** relaciona um diretório (pasta) e um de seus subdiretórios (subpastas).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe de **\_ subdiretório Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ subdiretório Win32** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ diretório Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório WMI Win32 \_ ")
</dt> </dl>

Referência à instância que representa as propriedades do diretório pai (pasta) nesta associação.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ diretório Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório WMI Win32 \_ ")
</dt> </dl>

Referência à instância que representa a parte de subdiretório (subpasta) da associação.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ subdiretório Win32** é derivada do [**\_ componente CIM**](cim-component.md).

Para retornar uma coleção de subpastas para uma pasta, crie uma consulta de associação que defina *ResultRole* como *PartComponent*. Isso indica que todos os itens na coleção retornada devem desempenhar a função de um PartComponent, ou subpasta, do objeto Folder. Para retornar a pasta pai de uma pasta, defina *ResultRole* como *GroupComponent*.

A classe de **\_ subdiretório Win32** funciona apenas no nível do sistema de arquivos imediatamente acima ou imediatamente abaixo da pasta especificada.

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir retorna uma lista de todas as subpastas na pasta C: \\ scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
