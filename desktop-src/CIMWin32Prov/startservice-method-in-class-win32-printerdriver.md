---
description: O método StartService coloca o serviço no estado iniciado.
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Método StartService da classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe5afb79f2c5d74f2e9a68093cb98ac0b8597d767a747c8bd66b766ba72dd00f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752376"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a>Método StartService da classe Win32 \_ PrinterDriver

O método **StartService** coloca o serviço no estado iniciado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para valores diferentes daqueles listados na lista a seguir, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Serviço iniciado com êxito.

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
| MOF<br/>                      | <dl> <dt>\_Impressora. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[**\_PrinterDriver Win32**](win32-printerdriver.md)
</dt> </dl>

 

