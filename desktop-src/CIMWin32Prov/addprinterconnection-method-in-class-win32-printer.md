---
description: Fornece uma conexão com uma impressora existente na rede e a adiciona à lista de impressoras disponíveis.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Método AddPrinterConnection da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826216"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a>Método AddPrinterConnection da classe de \_ impressora Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AddPrinterConnection** fornece uma conexão a uma impressora existente na rede e a adiciona à lista de impressoras disponíveis.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ do no\]
</dt> <dd>

Nome amigável da impressora.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Sucesso

</dd> <dt>

**5**
</dt> <dd>

Acesso negado

</dd> <dt>

**1801**
</dt> <dd>

Nome de impressora inválido

</dd> <dt>

**1930**
</dt> <dd>

Driver de impressora incompatível

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo do PowerShell [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) instala todos os drivers de impressora de um servidor de impressão especificado.

O [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) exemplo do PowerShell lista impressoras compartilhadas em um computador remoto e oferece a você a capacidade de adicionar uma conexão de impressora do computador remoto ao seu.

O exemplo de código VBScript a seguir adiciona uma impressora local.


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>\_Impressora. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[Tarefas do WMI: impressoras e impressão](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**\_Impressora Win32**](win32-printer.md)
</dt> </dl>

 

