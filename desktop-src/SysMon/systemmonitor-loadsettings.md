---
title: Método SystemMonitor. Configurations
description: Adiciona os contadores no arquivo de modelo HTML ao monitor do sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Método LoadSettings SysMon
- Método LoadSettings SysMon, objeto SystemMonitor
- Objeto SystemMonitor Sysmon, método Configurations
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
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369641"
---
# <a name="systemmonitorloadsettings-method"></a>Método SystemMonitor. Configurations

Adiciona os contadores no arquivo de modelo HTML ao monitor do sistema.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SettingsFileName* \[ no\]
</dt> <dd>

Cadeia de caracteres HTML que especifica os contadores a serem adicionados ao monitor do sistema.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para salvar os contadores atuais no monitor do sistema em um arquivo HTML, chame o método [**SystemMonitor. SaveAs**](systemmonitor-saveas.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





