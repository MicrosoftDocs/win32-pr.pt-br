---
title: Método TimeLimit da classe Win32_TSSessionSetting classe
description: Define o tempo máximo alocado para o tipo de limite de sessão especificado.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Método TimeLimit Serviços de Área de Trabalho Remota
- Método TimeLimit Serviços de Área de Trabalho Remota , Win32_TSSessionSetting classe
- Win32_TSSessionSetting classe Serviços de Área de Trabalho Remota método , TimeLimit
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
ms.openlocfilehash: 7f49451b1f6b7b2e63079d0bebbcd0dbb43b76352ae3609ce4138b771a01e03e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137549"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a>Método TimeLimit da classe Win32 \_ TSSessionSetting

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

*SessionLimitType* \[ Em\]
</dt> <dd>

Especifica o tipo de propriedade de limite de sessão que o método está definindo.

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**


</dt> <dd>

O método está definindo a **propriedade ActiveSessionLimit.**

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**


</dt> <dd>

O método está definindo a **propriedade DisconnectedSessionLimit.**

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**


</dt> <dd>

O método está definindo a **propriedade IdleSessionLimit.**

</dd> </dl> </dd> <dt>

*ValueLimit* \[ Em\]
</dt> <dd>

O novo tempo máximo, em milissegundos, para a propriedade especificada pelo *parâmetro SessionLimitType.* O valor zero indica que não há nenhum limite de sessão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna Êxito em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

## <a name="remarks"></a>Comentários

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

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> </dl>

 

