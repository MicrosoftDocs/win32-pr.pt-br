---
title: Habilitar o método da Win32_Terminal classe
description: O método Enable desabilita ou habilita o terminal.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Habilitar a Serviços de Área de Trabalho Remota
- Habilitar a Serviços de Área de Trabalho Remota , Win32_Terminal classe
- Win32_Terminal classe Serviços de Área de Trabalho Remota , habilitar método
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38bcc4f6eddbfb8a40a0c128d87f3c5bac6f7d214f14a43347a613db4cce3963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848162"
---
# <a name="enable-method-of-the-win32_terminal-class"></a>Habilitar método da classe Terminal Win32 \_

O **método Enable** desabilita ou habilita o terminal.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnableTerminal* \[ Em\]
</dt> <dd>

Sinalizador que desabilita ou habilita o terminal.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

O terminal está desabilitado.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

O terminal está habilitado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ Terminal**](win32-terminal.md)
</dt> </dl>

 

