---
title: Método SetFallbackPrintDriverType da Win32_TerminalServiceSetting classe
description: O método SetFallbackPrintDriverType define a propriedade FallbackPrintDriverType para a classe .
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Método SetFallbackPrintDriverType Serviços de Área de Trabalho Remota
- Método SetFallbackPrintDriverType Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39033a34c75ea94f365ae690b1ac6fe4cd61663e9cd6db19f2cd2c232bd8c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137859"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Método SetFallbackPrintDriverType da classe Win32 \_ TerminalServiceSetting

O **método SetFallbackPrintDriverType** define a **propriedade FallbackPrintDriverType** para a classe .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FallbackPrintDriverType* \[ Em\]
</dt> <dd>

Define a **propriedade FallbackPrintDriverType** que permite ou nega novas Serviços de Área de Trabalho Remota conexões.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Nenhum drivers de fallback.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Melhor suposição.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Melhor suposição. Se nenhuma corresponder for encontrada, fallback para Hewlett-Packard PCL (Printer Control Language).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Melhor suposição. Se nenhuma corresponder for encontrada, fallback para Postscript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Melhor suposição. Se nenhuma combinação for encontrada, mostre os drivers PS e PCL.

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

 

