---
title: Método SetMaxMonitors da classe Win32_TSClientSetting dados
description: Define a propriedade MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Método SetMaxMonitors Serviços de Área de Trabalho Remota
- Método SetMaxMonitors Serviços de Área de Trabalho Remota , Win32_TSClientSetting classe
- Win32_TSClientSetting classe Serviços de Área de Trabalho Remota , método SetMaxMonitors
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e91cc6a53bbec769236e5c1b462e7bdfe5859cc140a11366299a3eaab46e1777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987906"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a>Método SetMaxMonitors da classe \_ Win32 TSClientSetting

Define a **propriedade MaxMonitors.**

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaxMonitors* \[ Em\]
</dt> <dd>

Especifica o novo número máximo de monitores com suporte pelo servidor. O valor mínimo é 1 e o valor máximo é 10.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se as configurações de conexão do usuário são substituídos pelo servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





