---
description: Inicia o depurador que está registrado atualmente para este processo.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Método AttachDebugger da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 86ec5e31afef484733381d94bfdfa48595401d963443c2ab407ee6166d5d0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959165"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a>Método AttachDebugger da \_ classe Process do Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** inicia o depurador que está atualmente registrado para esse processo.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida**
</dt> <dd>

0

Conclusão bem-sucedida.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

O usuário não tem acesso às informações solicitadas.

</dd> <dt>

**Privilégio insuficiente**
</dt> <dd>

3

O usuário não tem privilégios suficientes.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

8

Falha desconhecida.

</dd> <dt>

**demarcador não localizado**
</dt> <dd>

9

O caminho especificado não existe.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

21

O parâmetro especificado não é válido.

</dd> <dt>

**Outras**
</dt> <dd>

22 4294967295

</dd> </dl>

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

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 

