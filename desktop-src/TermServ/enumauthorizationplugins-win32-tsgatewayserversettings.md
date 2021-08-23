---
title: Método EnumAuthorizationPlugins da classe Win32_TSGatewayServerSettings
description: Enumera todos os plug-ins de autorização registrados.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnumAuthorizationPlugins
- Método EnumAuthorizationPlugins Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método EnumAuthorizationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40447b6befd3042c766b4bd312619563617119b114c329867bfc3ca0b3e7bfce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574626"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnumAuthorizationPlugins da classe Win32 \_ TSGatewayServerSettings

Enumera todos os plug-ins de autorização registrados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnumAuthorizationPlugins(
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

Uma matriz de **cadeia de caracteres** que recebe os nomes dos plug-ins de autorização registrados.

</dd> <dt>

*CLSIDs* \[ fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Uma matriz de **cadeia de caracteres** que recebe os CLSIDs dos plug-ins de autorização registrados.

</dd> <dt>

*Descrições* \[ do fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Uma matriz de **cadeia de caracteres** que recebe as descrições dos plug-ins de autorização registrados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

