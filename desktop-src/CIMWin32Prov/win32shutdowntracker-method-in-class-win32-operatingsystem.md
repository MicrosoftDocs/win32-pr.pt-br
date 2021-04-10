---
description: O método Win32ShutdownTracker fornece o mesmo conjunto de opções de desligamento com suporte do método Win32Shutdown no sistema \_ operacional Win32, mas também permite que você especifique comentários, um motivo para o desligamento ou um tempo limite.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Método Win32ShutdownTracker da classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088962"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Método Win32ShutdownTracker da classe de sistema \_ operacional Win32

O método **Win32ShutdownTracker** fornece o mesmo conjunto de opções de desligamento com suporte do método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) no sistema [**\_ operacional Win32**](win32-operatingsystem.md), mas também permite que você especifique comentários, um motivo para o desligamento ou um tempo limite.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tempo limite* \[ no\]
</dt> <dd>

Tempo, em segundos, antes de o desligamento ocorrer. O valor padrão é 0 (zero).

</dd> <dt>

*Comentário* \[ no\]
</dt> <dd>

Mensagem a ser exibida na caixa de diálogo de desligamento que também é armazenada como um comentário na entrada do log de eventos.

</dd> <dt>

*ReasonCode* \[ no\]
</dt> <dd>

Motivo para iniciar o desligamento.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Conjunto de sinalizadores de bitmap para desligar o computador. Para forçar um comando, adicione o sinalizador Force (4) ao valor do comando. O uso da força em conjunto com o desligamento ou reinicialização em um computador remoto desliga imediatamente tudo (incluindo WMI, COM e assim por diante) ou reinicia o computador remoto. Isso resulta em um valor de retorno indeterminado.

<dt>

0 (0x0)
</dt> <dd>

Fazer logoff

</dd> <dt>

4 (0x4)
</dt> <dd>

Logoff forçado (0 + 4)

</dd> <dt>

1 (0x1)
</dt> <dd>

Desligar

</dd> <dt>

5 (0x5)
</dt> <dd>

Desligamento forçado (1 + 4)

</dd> <dt>

2 (0x2)
</dt> <dd>

Reboot

</dd> <dt>

6 (0x6)
</dt> <dd>

Reinicialização forçada (2 + 4)

</dd> <dt>

8 (0x8)
</dt> <dd>

Desligar

</dd> <dt>

12 (0xC)
</dt> <dd>

Desligamento forçado (8 + 4)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para códigos de erro, consulte [**constantes de erro WMI**](../wmisdk/wmi-error-constants.md) ou [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](../debug/system-error-codes.md).

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Outro** (1 a 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

O processo de chamada deve ter o privilégio de **\_ \_ nome de desligamento se** .

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir descreve como chamar **Win32ShutdownTracker**.


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
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

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[**Sistema \_ operacional Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
