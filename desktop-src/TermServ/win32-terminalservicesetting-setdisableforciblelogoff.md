---
title: Método SetDisableForcibleLogoff da classe Win32_TerminalServiceSetting
description: Método SetDisableForcibleLogoff da classe Win32_TerminalServiceSetting – não há suporte para esse método.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetDisableForcibleLogoff
- Método SetDisableForcibleLogoff Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetDisableForcibleLogoff
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103704"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a>Método SetDisableForcibleLogoff da classe Win32 \_ TerminalServiceSetting

Não há suporte para o método.

**Windows Vista e Windows Server 2008:** Habilita ou desabilita se um administrador que fez logon no console pode ser forçado a fazer logoff.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DisableForcibleLogoff* \[ no\]
</dt> <dd>

Sinalizador desabilitando ou habilitando a propriedade **DisableForcibleLogoff** , que determina se um administrador que está conectado ao console pode ser forçado a fazer logoff.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Desabilite a propriedade. O administrador conectado pode ser forçado a fazer logoff.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilite a propriedade. Não é possível efetuar logoff forçado do administrador conectado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna êxito em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Fim do suporte do cliente<br/>    | Windows Vista<br/>                                                                |
| Fim do suporte do servidor<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





