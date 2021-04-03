---
title: Método GetCurrentVMMPlugin da classe Win32_SessionDirectoryVMMPlugin
description: Obtém o plug-in de prioridade mais alta que está habilitado.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetCurrentVMMPlugin
- Método GetCurrentVMMPlugin Serviços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método GetCurrentVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824779"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método GetCurrentVMMPlugin da classe Win32 \_ SessionDirectoryVMMPlugin

Obtém o plug-in de prioridade mais alta que está habilitado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sname* \[ fora\]
</dt> <dd>

O nome do plug-in.

</dd> <dt>

*sProvider* \[ fora\]
</dt> <dd>

O nome do provedor de plug-in.

</dd> <dt>

*sServiceLocation* \[ fora\]
</dt> <dd>

O local do serviço que o plug-in deve contatar.

</dd> <dt>

*sClassID* \[ fora\]
</dt> <dd>

O identificador de classe do plug-in.

</dd> <dt>

*Prioridade* \[ do fora\]
</dt> <dd>

A prioridade do plug-in. Quanto maior o valor, maior a prioridade do plug-in.

</dd> <dt>

*Habilitado* \[ fora\]
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

 

 





