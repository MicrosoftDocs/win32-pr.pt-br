---
title: Método SetTimeZoneRedirection da classe Win32_TerminalServiceSetting
description: O método SetTimeZoneRedirection define a propriedade TimeZoneRedirection, que permite que o computador cliente redirecione suas configurações de fuso horário para a Serviços de Área de Trabalho Remota sessão.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Método SetTimeZoneRedirection Serviços de Área de Trabalho Remota
- Método SetTimeZoneRedirection Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método SetTimeZoneRedirection
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802cd4741f4ea30f378492075f69dfa21dfce54688fbc7ff9e72b957689d7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755637"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Método SetTimeZoneRedirection da classe Win32 \_ TerminalServiceSetting

O **método SetTimeZoneRedirection** define a propriedade **TimeZoneRedirection,** que permite que o computador cliente redirecione suas configurações de fuso horário para a Serviços de Área de Trabalho Remota sessão.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TimeZoneRedirection* \[ Em\]
</dt> <dd>

O novo valor para a **propriedade TimeZoneRedirection.**

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Desabilita a **propriedade TimeZoneRedirection.** Nenhum redirecionamento de fuso horário ocorre.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilita a **propriedade TimeZoneRedirection.** O fuso horário do cliente é redirecionado para o fuso horário da sessão.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retornará um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="remarks"></a>Comentários

Por padrão, o fuso horário da Serviços de Área de Trabalho Remota é o mesmo que o fuso horário do servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Os computadores cliente não podem redirecionar informações de fuso horário.

Se o redirecionamento de fuso horário estiver desabilitado, novas sessões herdarão o fuso horário do servidor. Quando uma sessão se reconecta, a sessão retém o fuso horário que tinha antes da desconexão.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

