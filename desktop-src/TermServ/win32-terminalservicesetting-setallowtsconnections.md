---
title: Método SetAllowTSConnections da classe Win32_TerminalServiceSetting
description: O método SetAllowTSConnections permite ou nega novas conexões de área de trabalho remota. Esse método modificará a propriedade AllowTSConnections da classe de forma adequada.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetAllowTSConnections
- Método SetAllowTSConnections Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455852"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Método SetAllowTSConnections da classe Win32 \_ TerminalServiceSetting

O método **SetAllowTSConnections** permite ou nega novas conexões de área de trabalho remota. Esse método modificará a propriedade **AllowTSConnections** da classe de forma adequada.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AllowTSConnections* \[ no\]
</dt> <dd>

Especifica se são permitidas novas conexões de área de trabalho remota. Deve ser um dos valores a seguir.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Não são permitidas novas conexões. Se o parâmetro *ModifyFirewallException* for 1, a exceção de firewall área de trabalho remota será desabilitada.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Novas conexões são permitidas. Se o parâmetro *ModifyFirewallException* for 1, a exceção de firewall área de trabalho remota será habilitada.

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[ no\]
</dt> <dd>

Especifica se a configuração de exceção do firewall para Área de Trabalho Remota será modificada para o estado especificado pelo parâmetro *AllowTSConnections* . Deve ser um dos valores a seguir.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Não modifique a configuração de exceção do firewall.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Modifique a configuração de exceção do firewall.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna êxito em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="remarks"></a>Comentários

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

 

