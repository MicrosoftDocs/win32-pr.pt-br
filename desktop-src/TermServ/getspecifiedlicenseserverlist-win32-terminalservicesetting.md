---
title: Método GetSpecifiedLicenseServerList da classe Win32_TerminalServiceSetting dados
description: Recupera a lista de servidores de licença especificados.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- Método GetSpecifiedLicenseServerList Serviços de Área de Trabalho Remota
- Método GetSpecifiedLicenseServerList Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método GetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 359d348dc759534d1f3ca070f443f4207aa8ddba0c73ab989d0fa8c0ab5397fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033746"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Método GetSpecifiedLicenseServerList da classe Win32 \_ TerminalServiceSetting

Recupera a lista de servidores de licença especificados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SpecifiedLSList* \[ out\]
</dt> <dd>

Uma matriz de cadeia de caracteres que recebe a lista de servidores de licença. Se não houver servidores de licença, essa matriz estará vazia.

</dd> </dl>

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

[**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





