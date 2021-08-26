---
description: Exclui um nome de compartilhamento da lista de recursos compartilhados de um servidor, desconectando as conexões com o recurso compartilhado.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Método Delete da classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1331ce9dfa3309c1cfbd0ba0ddc3b4a0c96d431d524d8f0e74f7937c8cdb332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918466"
---
# <a name="delete-method-of-the-win32_share-class"></a>Método Delete da classe de \_ compartilhamento Win32

O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui um nome de compartilhamento da lista de recursos compartilhados de um servidor, desconectando as conexões com o recurso compartilhado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Nome inválido** (9)
</dt> <dt>

**Nível inválido** (10)
</dt> <dt>

**Parâmetro inválido** (21)
</dt> <dt>

**Compartilhamento duplicado** (22)
</dt> <dt>

**Caminho Redirecionado** (23)
</dt> <dt>

**Dispositivo ou diretório desconhecido** (24)
</dt> <dt>

**Nome de rede não encontrado** (25)
</dt> <dt>

**Outro** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

O método **delete** é um método Object e é usado em uma instância de uma classe.

Somente os membros do grupo local Administradores ou operadores de conta ou aqueles com a associação de grupo de operador de servidor, impressão ou comunicação podem executar o método com êxito. O operador Print só pode excluir filas de impressora. O operador de comunicação pode excluir somente filas de dispositivo de comunicação.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir exclui o compartilhamento especificado.


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



O exemplo de código do PowerShell a seguir exclui os compartilhamentos em branco.


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
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

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Compartilhamento do Win32 \_**](win32-share.md)
</dt> </dl>

 

