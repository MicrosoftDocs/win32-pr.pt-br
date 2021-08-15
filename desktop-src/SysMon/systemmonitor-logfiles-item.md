---
title: Propriedade LogFiles.Item
description: Recupera a instância de LogFileItem especificada da coleção.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Propriedade de item SysMon
- Propriedade de item SysMon, classe LogFiles
- Classe LogFiles SysMon, propriedade Item
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2441575ec45c3d914fef80d5a7c6655b76597c094e319f5f0b01dbb62190e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882277"
---
# <a name="logfilesitem-property"></a>Propriedade LogFiles.Item

Recupera a instância [**de LogFileItem**](logfileitem.md) especificada da coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Valor da propriedade

[**Instância LogFileItem**](logfileitem.md) que corresponde ao valor de índice especificado.

## <a name="remarks"></a>Comentários

Essa é a propriedade padrão do [**objeto LogFiles.**](systemmonitor-logfiles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[arquivos de log](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**arquivos de log**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





