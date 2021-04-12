---
title: Método SetServiceLocation da classe Win32_SessionDirectoryVMMPlugin
description: Define o local do serviço para o plug-in.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetServiceLocation
- Método SetServiceLocation Serviços de Área de Trabalho Remota, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota, método SetServiceLocation
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499503"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetServiceLocation da classe Win32 \_ SessionDirectoryVMMPlugin

Define o local do serviço para o plug-in.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sServiceLocation* \[ no\]
</dt> <dd>

O local do serviço que o plug-in deve contatar.

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

 

 





