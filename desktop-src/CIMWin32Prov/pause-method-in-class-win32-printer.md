---
description: Pausa a fila de impressão.
ms.assetid: 0f425318-a7c0-4bba-bb44-e7635fa3ca03
ms.tgt_platform: multiple
title: Método Pause da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8122f98956b9bdc49f6d4ed11055a22aee660473a79860f9d00d4684f6cf3c7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929636"
---
# <a name="pause-method-of-the-win32_printer-class"></a>Método Pause da classe de \_ impressora Win32

O método **Pause** [WMI da classe](/windows/desktop/WmiSdk/retrieving-a-class) pausa a fila de impressão. Nenhum trabalho pode ser impresso até que a fila seja retomada.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Sucesso

</dd> <dt>

**5**
</dt> <dd>

Acesso negado

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

[**\_Impressora Win32**](win32-printer.md)
</dt> <dt>

[**Método Resume**](resume-method-in-class-win32-printer.md)
</dt> </dl>

 

