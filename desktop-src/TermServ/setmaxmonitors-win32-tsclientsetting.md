---
title: Método SetMaxMonitors da classe Win32_TSClientSetting
description: Define a propriedade MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetMaxMonitors
- Método SetMaxMonitors Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetMaxMonitors
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
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769377"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a>Método SetMaxMonitors da classe Win32 \_ TSClientSetting

Define a propriedade **MaxMonitors** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaxMonitors* \[ no\]
</dt> <dd>

Especifica o novo número máximo de monitores com suporte no servidor. O valor mínimo é 1 e o valor máximo é 10.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se as configurações de conexão do usuário forem substituídas pelo servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

 





