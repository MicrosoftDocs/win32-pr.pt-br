---
description: Cria um novo driver de impressora.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Método AddPrinterDriver da Win32_PrinterDriver classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14681c381f8c8b9abbc5b28ec763b959854e2303b9a0b87af762238f4e5a8d27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752796"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Método AddPrinterDriver da classe PrinterDriver win32 \_

O **método de classe AddPrinterDriver** cria um novo driver de impressora.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DriverInfo* \[ Em\]
</dt> <dd>

Uma instância da classe [**\_ PrinterDriver Win32**](win32-printerdriver.md) que representa o driver de impressora.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para valores diferentes daqueles listados na lista a seguir, consulte [**Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Êxito.

</dd> <dt>

**5**
</dt> <dd>

Acesso negado

</dd> <dt>

**87**
</dt> <dd>

O parâmetro está incorreto. Pode ocorrer quando o objeto não está preenchido corretamente ou quando o driver não pode ser encontrado no sistema. Como alternativa, o atributo name pode ser diferente do modelo especificado no arquivo .inf. Ou pode haver uma invertida ausente (" \\ ") em um atributo PathFile.

</dd> <dt>

**1797**
</dt> <dd>

O driver de impressora é desconhecido.

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> Ao usar o **método AddPrinterDriver,** você deve usar **SeLoadDriverPrivilege** para carregar ou descarregar um driver de dispositivo.

 

## <a name="examples"></a>Exemplos

O[exemplo de código](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) Instalar um Driver de Impressora não Encontrado em Drivers Cab VBScript instala uma impressora hipotética usando um driver de impressão não encontrado no Drivers.cab.

O exemplo de VBScript a seguir instala o driver de impressora para uma impressora Apple LaserWriter 8500.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ PrinterDriver**](win32-printerdriver.md)
</dt> </dl>

 

