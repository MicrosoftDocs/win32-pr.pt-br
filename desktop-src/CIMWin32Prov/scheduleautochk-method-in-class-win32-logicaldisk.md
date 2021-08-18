---
description: Agenda o Autochk a ser executado na unidade de disco representada pelo LogicalDisk do Win32 na próxima reinicialização se \_ o bit sujo estiver definido.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Método ScheduleAutoChk da Win32_LogicalDisk classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7e4920bdded79a7f63cbe7beaf28a70837ad7a47c2b28a1e37d83208b4f4e6f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588186"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Método ScheduleAutoChk da classe LogicalDisk do Win32 \_

O método de classe **ScheduleAutoChk** agenda o Autochk a ser executado na unidade de disco representada pelo [**\_ LogicalDisk do Win32**](win32-logicaldisk.md) na próxima reinicialização se o bit sujo estiver definido.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LogicalDisk* \[ Em\]
</dt> <dd>

Especifica a lista de unidades a ser agendada para o Autochk na próxima reinicialização. A sintaxe de cadeia de caracteres consiste na letra da unidade seguida por dois-pontos para o disco lógico, por exemplo: "C:"

> [!Note]  
> Sempre verifique a validade das letras da unidade na matriz *LogicalDisk* quando os dados vêm de uma fonte desconhecida ou de uma fonte em que você não confia.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará um valor de 0 (zero) se for bem-sucedido e algum outro valor se qualquer outro erro ocorrer. Os valores são listados na lista a seguir. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Nenhum erro** (0)
</dt> <dt>

**Erro – Unidade Remota** (1)
</dt> <dt>

**Erro – Unidade Removível** (2)
</dt> <dt>

**Erro – Unidade não diretório raiz** (3)
</dt> <dt>

**Erro – Unidade Desconhecida** (4)
</dt> </dl>

## <a name="remarks"></a>Comentários

Esse método só é aplicável a instâncias de disco lógico que representam um disco físico no computador. Esse método não é aplicável a unidades lógicas mapeadas.

## <a name="examples"></a>Exemplos

Os exemplos de VBScript e PowerShell a seguir Autochk.exe para executar na unidade C na próxima vez que o computador reinicializar.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LogicalDisk do Win32 \_**](win32-logicaldisk.md)
</dt> </dl>

 

