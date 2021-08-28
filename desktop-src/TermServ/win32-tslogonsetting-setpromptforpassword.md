---
title: Método SetPromptForPassword da classe Win32_TSLogonSetting dados
description: O método SetPromptForPassword define a propriedade PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Método SetPromptForPassword Serviços de Área de Trabalho Remota
- Método SetPromptForPassword Serviços de Área de Trabalho Remota , Win32_TSLogonSetting classe
- Win32_TSLogonSetting classe Serviços de Área de Trabalho Remota , método SetPromptForPassword
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
ms.openlocfilehash: 90ea5202b0cfdfb624a05240deb042a88a8c73c8ea994cd810e1d9680ac0ddc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769516"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>Método SetPromptForPassword da classe \_ TSLogonSetting do Win32

O **método SetPromptForPassword** define a **propriedade PromptForPassword.**

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PromptForPassword* \[ Em\]
</dt> <dd>

Sinalizar a desabilitação ou a habilitação da **propriedade PromptForPassword.**

<dt>

0
</dt> <dd>

Desabilita o prompt de senha.

</dd> <dt>

1
</dt> <dd>

Habilita o prompt de senha.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna Êxito em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

<dl> <dt>

**FALSE** (0)
</dt> <dt>

**TRUE** (1)
</dt> </dl>

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

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

