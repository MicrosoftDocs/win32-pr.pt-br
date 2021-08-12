---
title: Método altermode da classe Win32_TerminalServiceSetting
description: O método Altermode define o tipo de licenciamento do servidor atual de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Método altermode Serviços de Área de Trabalho Remota
- Método altermode Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2812dd459e13922b1745e55355972092091b4fd9521bc41a46da40769c02021d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604035"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>Método altermode da classe Win32 \_ TerminalServiceSetting

O método **altermode** define o tipo de licenciamento do servidor atual de Host da Sessão da Área de Trabalho Remota (host da Sessão RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Licenciamento* \[ no\]
</dt> <dd>

O tipo de licenciamento a ser definido com base no modo de servidor Host da Sessão RD.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Servidor de Host da Sessão RD pessoal.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Área de trabalho remota para administração.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Por dispositivo/por estação. Válido para servidores de aplicativos.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Por Usuário. Válido para servidores de aplicativos.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

