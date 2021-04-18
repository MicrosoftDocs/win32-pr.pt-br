---
title: Método SetTimeZoneRedirection da classe Win32_TerminalServiceSetting
description: O método SetTimeZoneRedirection define a propriedade TimeZoneRedirection, que permite que o computador cliente redirecione suas configurações de fuso horário para a sessão de Serviços de Área de Trabalho Remota.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetTimeZoneRedirection
- Método SetTimeZoneRedirection Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetTimeZoneRedirection
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
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766940"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Método SetTimeZoneRedirection da classe Win32 \_ TerminalServiceSetting

O método **SetTimeZoneRedirection** define a propriedade **TimeZoneRedirection** , que permite que o computador cliente redirecione suas configurações de fuso horário para a sessão de serviços de área de trabalho remota.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TimeZoneRedirection* \[ no\]
</dt> <dd>

O novo valor para a propriedade **TimeZoneRedirection** .

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Desabilita a propriedade **TimeZoneRedirection** . Nenhum redirecionamento de fuso horário ocorre.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilita a propriedade **TimeZoneRedirection** . O fuso horário do cliente é redirecionado para o fuso horário da sessão.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

Por padrão, o fuso horário para a sessão de Serviços de Área de Trabalho Remota é o mesmo que o fuso horário do servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Os computadores cliente não podem redirecionar informações de fuso horário.

Se o redirecionamento de fuso horário estiver desabilitado, as novas sessões herdarão o fuso horário do servidor. Quando uma sessão é reconectada, a sessão retém o fuso horário que tinha antes de se desconectar.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

