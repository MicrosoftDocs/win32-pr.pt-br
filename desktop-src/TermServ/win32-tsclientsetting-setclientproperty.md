---
title: Método SetClientProperty da classe Win32_TSClientSetting
description: O método SetClientProperty define a propriedade LPTPortMapping, COMPortMapping, AudioMapping, ClipboardMapping, DriveMapping ou WindowsPrinterMapping para a classe .
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Método SetClientProperty Serviços de Área de Trabalho Remota
- Método SetClientProperty Serviços de Área de Trabalho Remota , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Serviços de Área de Trabalho Remota , método SetClientProperty
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017a771022e0f5edc7d4abe22501fc8dfadc006e01ed2642f95f9c39f101eef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127012"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a>Método SetClientProperty da classe \_ Win32 TSClientSetting

O **método SetClientProperty** define a propriedade **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping,** **DriveMapping** ou **WindowsPrinterMapping** para a classe .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PropertyName* \[ Em\]
</dt> <dd>

Especifica a propriedade do cliente que o método está configurando.

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**


</dt> <dd>

O método está definindo a **propriedade AudioMapping.**

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**


</dt> <dd>

O método está definindo a **propriedade ClipboardMapping.**

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**


</dt> <dd>

O método está definindo a **propriedade COMPortMapping.**

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**


</dt> <dd>

O método está definindo a **propriedade DriveMapping.**

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**


</dt> <dd>

O método está definindo a **propriedade LPTPortMapping.**

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**


</dt> <dd>

O método está definindo a **propriedade PNPRedirection.**

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**


</dt> <dd>

O método está definindo a **propriedade WindowsPrinterMapping.**

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

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a propriedade do cliente especificada não estiver sob controle de política de grupo ou se a configuração de propriedade não estiver qualificada para substituição pelo servidor.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

