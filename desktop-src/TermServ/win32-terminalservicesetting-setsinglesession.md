---
title: Método SetSingleSession da classe Win32_TerminalServiceSetting
description: O método SetSingleSession define a propriedade SingleSession para a classe.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSingleSession
- Método SetSingleSession Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetSingleSession
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93fe070a2c820a1fe098d34c65a00a78b2bb9abecb85dd672ba048a99d7f565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755681"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a>Método SetSingleSession da classe Win32 \_ TerminalServiceSetting

O método **SetSingleSession** define a propriedade **SingleSession** para a classe.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SingleSession* \[ no\]
</dt> <dd>

Sinalizador desabilitando ou habilitando a propriedade **SingleSession** , que determina se os usuários estão limitados a uma ou mais sessões de serviços de área de trabalho remota.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Desabilite a propriedade.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilite a propriedade.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

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

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

