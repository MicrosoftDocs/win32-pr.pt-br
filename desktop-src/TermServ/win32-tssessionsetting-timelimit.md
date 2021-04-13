---
title: Método timelimite da classe Win32_TSSessionSetting
description: Define o tempo máximo alocado para o tipo de limite de sessão especificado.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método timelimite
- Método timelimite Serviços de Área de Trabalho Remota, classe Win32_TSSessionSetting
- Classe Win32_TSSessionSetting Serviços de Área de Trabalho Remota, método timelimite
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499247"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a>Método timelimite da classe Win32 \_ TSSessionSetting

Define o tempo máximo alocado para o tipo de limite de sessão especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SessionLimitType* \[ no\]
</dt> <dd>

Especifica o tipo de propriedade de limite de sessão que o método está configurando.

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**


</dt> <dd>

O método está definindo a propriedade **ActiveSessionLimit** .

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**


</dt> <dd>

O método está definindo a propriedade **DisconnectedSessionLimit** .

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**


</dt> <dd>

O método está definindo a propriedade **IdleSessionLimit** .

</dd> </dl> </dd> <dt>

*ValueLimit* \[ no\]
</dt> <dd>

O novo tempo máximo, em milissegundos, para a propriedade especificada pelo parâmetro *SessionLimitType* . O valor zero indica que não há limite de sessão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

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

[**\_TSSessionSetting Win32**](win32-tssessionsetting.md)
</dt> </dl>

 

