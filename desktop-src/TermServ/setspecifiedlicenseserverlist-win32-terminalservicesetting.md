---
title: Método SetSpecifiedLicenseServerList da classe Win32_TerminalServiceSetting
description: Atualiza a lista de servidores de licença especificados, substituindo quaisquer servidores de licença especificados existentes.
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSpecifiedLicenseServerList
- Método SetSpecifiedLicenseServerList Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10fde34e490f26c287e63dcddae3c62761670bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784060"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Método SetSpecifiedLicenseServerList da classe Win32 \_ TerminalServiceSetting

Atualiza a lista de servidores de licença especificados, substituindo quaisquer servidores de licença especificados existentes.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SpecifiedLSList* \[ no\]
</dt> <dd>

Uma matriz de cadeia de caracteres que contém a nova lista de servidores de licença especificados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> <dt>

[**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





