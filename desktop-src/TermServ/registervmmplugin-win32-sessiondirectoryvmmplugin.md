---
title: Método RegisterVMMPlugin da classe Win32_SessionDirectoryVMMPlugin
description: Registra um novo plug-in do VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RegisterVMMPlugin
- Método RegisterVMMPlugin Serviços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método RegisterVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369426"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método RegisterVMMPlugin da classe Win32 \_ SessionDirectoryVMMPlugin

Registra um novo plug-in do VMM.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sname* \[ no\]
</dt> <dd>

O nome do plug-in.

</dd> <dt>

*sProvider* \[ no\]
</dt> <dd>

O nome do provedor de plug-in.

</dd> <dt>

*sServiceLocation* \[ no\]
</dt> <dd>

O local do serviço que o plug-in deve contatar.

</dd> <dt>

*sClassID* \[ no\]
</dt> <dd>

O identificador de classe do plug-in.

</dd> <dt>

*Prioridade* \[ do no\]
</dt> <dd>

A prioridade do plug-in. Quanto maior o valor, maior a prioridade do plug-in.

</dd> <dt>

*Habilitado* \[ no\]
</dt> <dd>

Indica se o plug-in está habilitado ou desabilitado. **True** se o plug-in estiver habilitado ou **false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SessionDirectoryVMMPlugin Win32**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





