---
title: Método SetMaxXResolution da classe Win32_TSClientSetting
description: Define a propriedade MaxXResolution.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetMaxXResolution
- Método SetMaxXResolution Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetMaxXResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759a674e2b283d18caf1cc4d1b2f3e3ecae786dc76f9acc222f47dd8daf385de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000506"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a>Método SetMaxXResolution da classe Win32 \_ TSClientSetting

Define a propriedade **MaxXResolution** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaxXResolution* \[ no\]
</dt> <dd>

A nova resolução máxima de X com suporte do servidor. O valor mínimo é 200 e o valor máximo é 4096.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





