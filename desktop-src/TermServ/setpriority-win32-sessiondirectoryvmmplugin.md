---
title: Método setanteriority da classe Win32_SessionDirectoryVMMPlugin
description: Define a prioridade do plug-in.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método setanteriority
- Método setServiços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método setanteriority
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
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919132"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método setanteriority da classe Win32 \_ SessionDirectoryVMMPlugin

Define a prioridade do plug-in.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Prioridade* \[ do no\]
</dt> <dd>

A prioridade do plug-in. Quanto maior o valor, maior a prioridade do plug-in. A prioridade é zero por padrão.

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

 

 





