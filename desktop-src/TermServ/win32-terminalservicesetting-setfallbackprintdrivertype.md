---
title: Método SetFallbackPrintDriverType da classe Win32_TerminalServiceSetting
description: O método SetFallbackPrintDriverType define a propriedade FallbackPrintDriverType para a classe.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetFallbackPrintDriverType
- Método SetFallbackPrintDriverType Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetFallbackPrintDriverType
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
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009690"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Método SetFallbackPrintDriverType da classe Win32 \_ TerminalServiceSetting

O método **SetFallbackPrintDriverType** define a propriedade **FallbackPrintDriverType** para a classe.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FallbackPrintDriverType* \[ no\]
</dt> <dd>

Define a propriedade **FallbackPrintDriverType** que permite ou nega novas conexões serviços de área de trabalho remota.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Nenhum driver de fallback.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Melhor estimativa.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Melhor estimativa. Se nenhuma correspondência for encontrada, fallback para Hewlett-Packard PCL (linguagem de controle de impressora).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**Beta**


</dt> <dd>

Melhor estimativa. Se nenhuma correspondência for encontrada, fallback para o PostScript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**quatro**


</dt> <dd>

Melhor estimativa. Se nenhuma correspondência for encontrada, mostre os drivers PS e PCL.

</dd> </dl> </dd> </dl>

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

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

