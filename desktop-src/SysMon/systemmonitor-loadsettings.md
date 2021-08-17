---
title: Método SystemMonitor.LoadSettings
description: Adiciona os contadores no arquivo de modelo HTML ao Monitor do Sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Método LoadSettings SysMon
- Método LoadSettings SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método LoadSettings
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387bf2e42475d27f5440afb3fa0b945c910b3ac3bad610495936cd3a4a900bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882321"
---
# <a name="systemmonitorloadsettings-method"></a>Método SystemMonitor.LoadSettings

Adiciona os contadores no arquivo de modelo HTML ao Monitor do Sistema.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ConfiguraçõesFileName* \[ Em\]
</dt> <dd>

Cadeia de caracteres HTML que especifica os contadores a adicionar ao Monitor do Sistema.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para salvar os contadores atuais no Monitor do Sistema em um arquivo HTML, chame o [**método SystemMonitor.SaveAs.**](systemmonitor-saveas.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





