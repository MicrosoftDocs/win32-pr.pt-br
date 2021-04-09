---
description: Coloca o serviço representado pelo \_ objeto PrinterDriver do Win32 no estado parado.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Método StopService da classe Win32_PrinterDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010201"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a>Método StopService da classe Win32 \_ PrinterDriver

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca o serviço representado pelo [**objeto \_ PrinterDriver do Win32**](win32-printerdriver.md) no estado parado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para valores diferentes daqueles listados na lista a seguir, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Serviço parado com êxito.

</dd> <dt>

**1**
</dt> <dd>

Não há suporte para a solicitação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                        |
| parâmetro<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>           |
| MOF<br/>                      | <dl> <dt>\_Impressora. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[**\_PrinterDriver Win32**](win32-printerdriver.md)
</dt> </dl>

 

