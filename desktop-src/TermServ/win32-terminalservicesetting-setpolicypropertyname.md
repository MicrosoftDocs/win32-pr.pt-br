---
title: Método SetPolicyPropertyName da classe Win32_TerminalServiceSetting dados
description: O método SetPolicyPropertyName define a propriedade DeleteTempFolders, UseTempFolders ou Help para a classe .
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Método SetPolicyPropertyName Serviços de Área de Trabalho Remota
- Método SetPolicyPropertyName Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método SetPolicyPropertyName
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a9009a05cb1c8de210c3e274af0e8c21297e9e01ed28dbc0c01d38edc06fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769976"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a>Método SetPolicyPropertyName da classe Win32 \_ TerminalServiceSetting

O **método SetPolicyPropertyName** define a **propriedade DeleteTempFolders**, **UseTempFolders** ou **Help** para a classe .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PropertyName* \[ Em\]
</dt> <dd>

Especifica a propriedade de política que o método está configurando.

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**


</dt> <dd>

O método está definindo a **propriedade DeleteTempFolders.**

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**


</dt> <dd>

O método está definindo a **propriedade UseTempFolders.**

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>**Ajuda**


</dt> <dd>

O método está definindo a **propriedade Ajuda.**

**Observação**  **Não há** suporte para a Ajuda

</dd> </dl> </dd> <dt>

*Valor* \[ Em\]
</dt> <dd>

Valor que indica se a propriedade especificada pelo parâmetro *PropertyName* deve ser habilitada ou desabilitada.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Desabilite a propriedade .

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilita a propriedade .

</dd> </dl> </dd> </dl>

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

