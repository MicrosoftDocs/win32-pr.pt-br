---
description: Agenda o Autochk a ser executado na unidade de disco representada pelo LogicalDisk do Win32 \_ na próxima reinicialização se o bit sujo estiver definido.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Método ScheduleAutoChk da classe Win32_LogicalDisk
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
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920248"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Método ScheduleAutoChk da classe do \_ LogicalDisk do Win32

O método de classe **ScheduleAutoChk** agenda o Autochk para ser executado na unidade de disco representada [**pelo \_ LogicalDisk do Win32**](win32-logicaldisk.md) na próxima reinicialização se o bit sujo estiver definido.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LogicalDisk* \[ no\]
</dt> <dd>

Especifica a lista de unidades a serem agendadas para autochk na próxima reinicialização. A sintaxe da cadeia de caracteres consiste na letra da unidade seguida por dois-pontos para o disco lógico, por exemplo: "C:"

> [!Note]  
> Sempre verifique a validade das letras da unidade na matriz do *LogicalDisk* quando os dados vierem de uma fonte desconhecida ou uma fonte na qual você não confia.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se for bem-sucedido e algum outro valor se ocorrer qualquer outro erro. Os valores são listados na lista a seguir. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Sem erro** (0)
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

Esse método só é aplicável a essas instâncias de disco lógico que representam um disco físico no computador. Esse método não é aplicável a unidades lógicas mapeadas.

## <a name="examples"></a>Exemplos

Os exemplos do VBScript e do PowerShell a seguir agendam Autochk.exe para serem executados na unidade C na próxima vez em que o computador for reinicializado.


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
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Disco \_ lógico do Win32**](win32-logicaldisk.md)
</dt> </dl>

 

