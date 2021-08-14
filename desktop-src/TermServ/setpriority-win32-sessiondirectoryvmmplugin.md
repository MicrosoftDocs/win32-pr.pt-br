---
title: Método SetPriority da classe Win32_SessionDirectoryVMMPlugin classe
description: Define a prioridade do plug-in.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- Método SetPriority Serviços de Área de Trabalho Remota
- Método SetPriority Serviços de Área de Trabalho Remota , Win32_SessionDirectoryVMMPlugin classe
- Win32_SessionDirectoryVMMPlugin classe Serviços de Área de Trabalho Remota , método SetPriority
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfe18b5998a1b8576cbd1a8f3c793e355469cfeff44f585dcb167a3b154803a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987736"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetPriority da classe \_ SessionDirectoryVMMPlugin do Win32

Define a prioridade do plug-in.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Prioridade* \[ Em\]
</dt> <dd>

A prioridade do plug-in. Quanto maior o valor, maior a prioridade do plug-in. A prioridade é zero por padrão.

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

 

 





