---
description: Cria um novo driver de impressora.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Método AddPrinterDriver da classe Win32_PrinterDriver
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
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370374"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Método AddPrinterDriver da classe Win32 \_ PrinterDriver

O método da classe **AddPrinterDriver** cria um novo driver de impressora.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DriverInfo* \[ no\]
</dt> <dd>

Uma instância da classe [**Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa o driver de impressora.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para valores diferentes daqueles listados na lista a seguir, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Êxito.

</dd> <dt>

**5**
</dt> <dd>

Acesso negado.

</dd> <dt>

**87**
</dt> <dd>

O parâmetro está incorreto. Pode ocorrer quando o objeto não está preenchido corretamente ou quando o driver não pode ser encontrado no sistema. Como alternativa, o atributo de nome pode ser diferente do modelo especificado no arquivo. inf. Ou, pode haver uma barra invertida ausente (" \\ ") em um atributo Pathfile.

</dd> <dt>

**1797**
</dt> <dd>

O driver de impressora é desconhecido.

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> Ao usar o método **AddPrinterDriver** , você deve usar **SeLoadDriverPrivilege** para carregar ou descarregar um driver de dispositivo.

 

## <a name="examples"></a>Exemplos

O exemplo de código de[instalação de um driver de impressora não encontrado nos drivers cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript instala uma impressora hipotética usando um driver de impressão não encontrado no Drivers.cab.

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
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>\_Impressora. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[**\_PrinterDriver Win32**](win32-printerdriver.md)
</dt> </dl>

 

