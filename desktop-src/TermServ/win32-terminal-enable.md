---
title: Método Enable da classe Win32_Terminal
description: O método Enable desabilita ou habilita o terminal.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Habilitar método Serviços de Área de Trabalho Remota
- Habilitar método Serviços de Área de Trabalho Remota, classe Win32_Terminal
- Classe Win32_Terminal Serviços de Área de Trabalho Remota, método Enable
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
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369360"
---
# <a name="enable-method-of-the-win32_terminal-class"></a>Habilitar o método da \_ classe terminal do Win32

O método **Enable** desabilita ou habilita o terminal.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnableTerminal* \[ no\]
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

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Terminal do Win32 \_**](win32-terminal.md)
</dt> </dl>

 

