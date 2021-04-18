---
title: Método SetPromptForPassword da classe Win32_TSLogonSetting
description: O método SetPromptForPassword define a propriedade PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetPromptForPassword
- Método SetPromptForPassword Serviços de Área de Trabalho Remota, classe Win32_TSLogonSetting
- Classe Win32_TSLogonSetting Serviços de Área de Trabalho Remota, método SetPromptForPassword
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756798"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>Método SetPromptForPassword da classe Win32 \_ TSLogonSetting

O método **SetPromptForPassword** define a propriedade **PromptForPassword** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PromptForPassword* \[ no\]
</dt> <dd>

Sinalizador desabilitando ou habilitando a propriedade **PromptForPassword** .

<dt>

0
</dt> <dd>

Desabilita a solicitação de senha.

</dd> <dt>

1
</dt> <dd>

Habilita a solicitação de senha.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

<dl> <dt>

**False** (0)
</dt> <dt>

**Verdadeiro** (1)
</dt> </dl>

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

[**\_TSLogonSetting Win32**](win32-tslogonsetting.md)
</dt> </dl>

 

