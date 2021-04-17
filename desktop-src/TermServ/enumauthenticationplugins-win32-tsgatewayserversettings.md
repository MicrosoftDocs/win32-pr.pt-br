---
title: Método EnumAuthenticationPlugins da classe Win32_TSGatewayServerSettings
description: Enumera todos os plug-ins de autenticação registrados.
ms.assetid: a5c1859d-e20c-4c72-aef5-ef9941edf73e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnumAuthenticationPlugins
- Método EnumAuthenticationPlugins Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método EnumAuthenticationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthenticationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0cd9d059a79749f657c6191e68e7bcd08555cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779431"
---
# <a name="enumauthenticationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnumAuthenticationPlugins da classe Win32 \_ TSGatewayServerSettings

Enumera todos os plug-ins de autenticação registrados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnumAuthenticationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Plug-ins* \[ fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Uma matriz de **cadeia de caracteres** que recebe os nomes dos plug-ins de autenticação registrados.

</dd> <dt>

*CLSIDs* \[ fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Uma matriz de **cadeia de caracteres** que recebe os CLSIDs dos plug-ins de autenticação registrados.

</dd> <dt>

*Descrições* \[ do fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Uma matriz de **cadeia de caracteres** que recebe as descrições dos plug-ins de autenticação registrados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

