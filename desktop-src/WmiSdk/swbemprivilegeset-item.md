---
description: O método item do objeto SWbemPrivilegeSet retorna um objeto SWbemPrivilege da coleção. O método item é o método padrão de um objeto SWbemPrivilegeSet.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827713"
---
# <a name="swbemprivilegesetitem-method"></a>Método SWbemPrivilegeSet. Item

O método **Item** do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) retorna um objeto [**SWbemPrivilege**](swbemprivilege.md) da coleção. O método **Item** é o método padrão de um objeto **SWbemPrivilegeSet** .

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obrigatórios. Uma das constantes do WMI do grupo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) . Essas constantes são essencialmente inteiros que representam privilégios específicos. Por exemplo, para obter o privilégio que permite que você desligue um sistema Windows, use a constante **wbemPrivilegeShutdown** ou o equivalente numérico de 23 (0x17).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o objeto [**SWbemPrivilege**](swbemprivilege.md) solicitado será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O privilégio especificado não existe.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir usa o método **Item**


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPRIVILEGESET CLSID<br/>                                                     |
| IID<br/>                      | ISWbemPrivilegeSet de IID \_<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[Executando operações privilegiadas](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilege**](swbemprivilege.md)
</dt> </dl>

 

 




