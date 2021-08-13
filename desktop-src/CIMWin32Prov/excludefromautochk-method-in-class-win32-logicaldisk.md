---
description: Exclui os discos da operação de Autochk a serem executados na próxima reinicialização.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Método ExcludeFromAutochk da classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37171c594cb3a51b131220bb604234bcae108fa025ea6343da99fdc998a7dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676124"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Método ExcludeFromAutochk da classe do \_ LogicalDisk do Win32

O método **ExcludeFromAutochk** exclui discos da operação de **autochk** a serem executados na próxima reinicialização.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LogicalDisk* \[ no\]
</dt> <dd>

Lista de unidades que devem ser excluídas do **autochk** na próxima reinicialização. A sintaxe da cadeia de caracteres consiste na letra da unidade seguida por dois-pontos para o disco lógico.

Exemplo: "C:"

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) quando não ocorre nenhum erro. Os valores são listados na lista a seguir. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Erro-unidade remota** (1)
</dt> <dt>

**Erro-unidade removível** (2)
</dt> <dt>

**Erro-unidade não diretório raiz** (3)
</dt> <dt>

**Erro-unidade desconhecida** (4)
</dt> </dl>

## <a name="remarks"></a>Comentários

Se não for excluído, o **autochk** será executado no disco quando o bit sujo for definido para o disco. Observe que as chamadas para excluir discos não são cumulativas. Se for feita uma chamada para excluir alguns discos, a nova lista não será adicionada à lista de discos que já estão marcados para exclusão. A nova lista de discos substitui a lista anterior. Esse método só é aplicável a essas instâncias de disco lógico que representam um disco físico no computador. Ele não é aplicável a unidades lógicas mapeadas.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir garante que o Autochk.exe não será executado na unidade C na próxima vez em que o computador for reinicializado, mesmo que o "bit sujo" tenha sido definido na unidade C.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Disco \_ lógico do Win32**](win32-logicaldisk.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

