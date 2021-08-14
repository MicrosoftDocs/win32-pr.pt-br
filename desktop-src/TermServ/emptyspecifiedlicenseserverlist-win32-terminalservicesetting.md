---
title: Método EmptySpecifiedLicenseServerList da classe Win32_TerminalServiceSetting dados
description: Remove todos os servidores de licença da lista de servidores de licença especificados.
ms.assetid: de1633ca-3f0b-4540-8b45-44303a4e72fe
ms.tgt_platform: multiple
keywords:
- Método EmptySpecifiedLicenseServerList Serviços de Área de Trabalho Remota
- Método EmptySpecifiedLicenseServerList Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método EmptySpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.EmptySpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 580287460e4d703f24c4186f6a98a0e69412736a8b621f8f58cc0dc5ec0179df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353979"
---
# <a name="emptyspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Método EmptySpecifiedLicenseServerList da classe Win32 \_ TerminalServiceSetting

Remove todos os servidores de licença da lista de servidores de licença especificados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EmptySpecifiedLicenseServerList();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> <dt>

[**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





