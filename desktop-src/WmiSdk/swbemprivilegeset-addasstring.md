---
description: Você pode usar o método AddAsString do objeto SWbemPrivilegeSet para adicionar um privilégio a uma coleção SWbemPrivilegeSet usando uma cadeia de caracteres de privilégio.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. AddAsString (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772988"
---
# <a name="swbemprivilegesetaddasstring-method"></a>Método SWbemPrivilegeSet. AddAsString

Você pode usar o método **AddAsString** do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) para adicionar um privilégio a uma coleção **SWbemPrivilegeSet** usando uma cadeia de caracteres de privilégio. Use este método para adicionar um privilégio ou para habilitar um privilégio para objetos [**SWbemSecurity**](swbemsecurity.md) . Consulte [executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strPrivilege* 
</dt> <dd>

Obrigatórios. Uma das cadeias de caracteres de privilégio. Para obter uma lista completa dessas cadeias de caracteres e as constantes do WMI associadas, consulte [**constantes de privilégio**](privilege-constants.md). Cada cadeia de caracteres de privilégio representa um privilégio específico. Por exemplo, para adicionar o privilégio que usa para desligar um sistema de computador, use a cadeia de caracteres **SeShutdownPrivilege** .

</dd> <dt>

*bIsEnabled* \[ adicional\]
</dt> <dd>

Valor booliano que habilita ou desabilita esse privilégio. O valor padrão é **True**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, esse método retornará um objeto [**SWbemPrivilege**](swbemprivilege.md) que representa o novo privilégio. Caso contrário, um objeto nulo será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **AddAsString** , o objeto **Err** pode conter o código de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir cria uma nova porta para um servidor de impressão usando o [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport). O **SeLoadDriverPrivilege** é necessário para esta operação. Consulte [executando operações privilegiadas](executing-privileged-operations.md).


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



Um exemplo de código usando esse método também é descrito no tópico [**SWbemPrivilegeSet**](swbemprivilegeset.md) .

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

[**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md)
</dt> <dt>

[**SWbemPrivilegeSet. Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilégio**](privilege-constants.md)
</dt> <dt>

[Executando operações privilegiadas](executing-privileged-operations.md)
</dt> <dt>

[Executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

