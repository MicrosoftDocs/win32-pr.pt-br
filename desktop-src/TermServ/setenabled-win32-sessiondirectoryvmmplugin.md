---
title: Método SetEnabled da classe Win32_SessionDirectoryVMMPlugin classe
description: Habilita ou desabilita o plug-in.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- Método SetEnabled Serviços de Área de Trabalho Remota
- Método SetEnabled Serviços de Área de Trabalho Remota , Win32_SessionDirectoryVMMPlugin classe
- Win32_SessionDirectoryVMMPlugin classe Serviços de Área de Trabalho Remota , método SetEnabled
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d33b7a5255e5dc59624e7aa540246ed08e56003b1e9917b86dfe90137db5b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118851473"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetEnabled da classe \_ SessionDirectoryVMMPlugin do Win32

Habilita ou desabilita o plug-in.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Habilitado* \[ Em\]
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

 

 





