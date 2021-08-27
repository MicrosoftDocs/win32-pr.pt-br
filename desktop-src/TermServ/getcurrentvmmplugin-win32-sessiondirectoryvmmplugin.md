---
title: Método GetCurrentVMMPlugin da classe Win32_SessionDirectoryVMMPlugin
description: Obtém o plug-in de prioridade mais alta habilitado.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Método GetCurrentVMMPlugin Serviços de Área de Trabalho Remota
- Método GetCurrentVMMPlugin Serviços de Área de Trabalho Remota , Win32_SessionDirectoryVMMPlugin classe
- Win32_SessionDirectoryVMMPlugin classe Serviços de Área de Trabalho Remota , método GetCurrentVMMPlugin
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
ms.openlocfilehash: 4cc683275581aeb00c654a30e8c5aba7fd920f58248b480fc39caa96c885bb7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080106"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método GetCurrentVMMPlugin da classe \_ SessionDirectoryVMMPlugin do Win32

Obtém o plug-in de prioridade mais alta habilitado.

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

*sName* \[ out\]
</dt> <dd>

O nome do plug-in.

</dd> <dt>

*sProvider* \[ out\]
</dt> <dd>

O nome do provedor de plug-in.

</dd> <dt>

*sServiceLocation* \[ out\]
</dt> <dd>

O local de serviço que o plug-in deve contatar.

</dd> <dt>

*sClassID* \[ out\]
</dt> <dd>

O identificador de classe do plug-in.

</dd> <dt>

*Prioridade* \[ out\]
</dt> <dd>

A prioridade do plug-in. Quanto maior o valor, maior a prioridade do plug-in.

</dd> <dt>

*Habilitado* \[ out\]
</dt> <dd>

Indica se o plug-in está habilitado ou desabilitado. **True** se o plug-in estiver habilitado ou **false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SessionDirectoryVMMPlugin do Win32**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





