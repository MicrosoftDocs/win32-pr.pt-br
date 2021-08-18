---
title: Método RemoteControl da classe Win32_TSRemoteControlSetting
description: O método RemoteControl define a propriedade LevelOfControl.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoteControl
- Método RemoteControl Serviços de Área de Trabalho Remota, classe Win32_TSRemoteControlSetting
- Classe Win32_TSRemoteControlSetting Serviços de Área de Trabalho Remota, método RemoteControl
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73de3f92171f688a9c0dc611552a061a3f2de7bf573fa41dab8606395eafe228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769416"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a>Método RemoteControl da classe Win32 \_ TSRemoteControlSetting

O método **RemoteControl** define a propriedade **LevelOfControl** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LevelOfControl* \[ no\]
</dt> <dd>

Novo valor para a propriedade **LevelOfControl** , que especifica se a sessão será exibida apenas pelo usuário remoto ou exibida e controlada por meio de um teclado e mouse. Para obter mais informações, consulte a seção Comentários. Os valores a seguir têm suporte.

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** (0)


</dt> <dd>

O controle remoto está desabilitado.

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)


</dt> <dd>

O usuário do controle remoto tem controle total da sessão do usuário, com a permissão do usuário.

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)


</dt> <dd>

O usuário do controle remoto tem controle total da sessão do usuário; a permissão do usuário não é necessária.

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)


</dt> <dd>

O usuário do controle remoto pode exibir a sessão remotamente, com a permissão do usuário; o usuário remoto não pode controlar ativamente a sessão.

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)


</dt> <dd>

O usuário do controle remoto pode exibir a sessão remotamente, mas não controlar ativamente a sessão; a permissão do usuário não é necessária.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="remarks"></a>Comentários

O controle total de uma sessão significa que o usuário remoto pode controlar ativamente a sessão do usuário com um teclado e um mouse.

Quando um usuário tenta estabelecer uma conexão de controle remoto, o sistema exibe uma mensagem para o cliente remoto, solicitando permissão para exibir ou participar ativamente na sessão remota.

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

[**\_TSRemoteControlSetting Win32**](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

