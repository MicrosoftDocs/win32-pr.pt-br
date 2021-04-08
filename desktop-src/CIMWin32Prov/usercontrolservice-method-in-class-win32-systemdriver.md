---
description: Tenta enviar um código de controle definido pelo usuário para um serviço gerenciado por um driver de sistema.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Método UserControlService da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920530"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a>Método UserControlService da \_ classe SystemDriver Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tenta enviar um código de controle definido pelo usuário para um serviço gerenciado por um driver de sistema.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ControlCode* \[ no\]
</dt> <dd>

Especifica os valores definidos (de 128 a 255) que fornecem comandos de controle específicos para um usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se a solicitação **UserControlService** tiver sido aceita, 1 (uma) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.

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

[**Systemdrive do Win32 \_**](win32-systemdriver.md)
</dt> </dl>

 

