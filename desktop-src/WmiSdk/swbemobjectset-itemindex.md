---
description: Retorna o SWbemObject associado ao índice especificado na coleção.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: Método SWbemObjectSet. ItemIndex (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765636"
---
# <a name="swbemobjectsetitemindex-method"></a>Método SWbemObjectSet. ItemIndex

O método **ItemIndex** retorna o [**SWbemObject**](swbemobject.md) associado ao índice especificado na coleção. O índice indica a posição do elemento dentro da coleção. A numeração da coleção começa em zero.

## <a name="syntax"></a>Sintaxe


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lIndex* 
</dt> <dd>

Índice do item na coleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o objeto [**SWbemObject**](swbemobject.md) solicitado retornará.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método [**Item**](swbemobjectset-item.md) , o objeto **Err** pode conter um dos códigos de erro abaixo.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Foi especificado um parâmetro inválido. Esse erro será retornado se um número de índice negativo for fornecido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O item solicitado não foi encontrado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método **ItemIndex** permite que os scripts de clientes WMI e aplicativos escritos em qualquer linguagem uma maneira uniforme de manipular uma coleção como uma matriz. Esse método pode ser usado com coleções [**SWbemObjectSet**](swbemobjectset.md) . Consultas, como [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices. References**](swbemservices-referencesto.md), [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md) retornam coleções **SWbemObjectSet** . O método **ItemIndex** não funciona com coleções que não contêm [**SWbemObjects**](swbemobject.md), como [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)e [**SWbemQualifierSet**](swbemqualifierset.md).

**ItemIndex** também pode ser usado para obter a única instância de uma classe singleton.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir consulta uma coleção de todas as instâncias de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) , em seguida, exibe os nomes dos três primeiros processos.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



Há apenas uma instância do [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) para cada instalação do sistema operacional. A criação do caminho [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) para obter a única instância é estranha, portanto, os scripts normalmente enumeram o sistema **\_ operacional do Win32** , embora apenas uma instância esteja disponível. O exemplo de código VBScript a seguir mostra como usar o método **ItemIndex** para chegar a um **sistema \_ operacional Win32** sem usar um loop **for each** .


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



O exemplo de código VBScript a seguir obtém instâncias associadas ao sistema [**\_ operacional Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), como [**Win32 \_ SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



A saída de exemplo de código a seguir mostra as instâncias associadas ao sistema [**\_ operacional Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | ISWbemObjectSet de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

