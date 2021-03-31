---
title: Método LogFiles. Remove
description: Remove a instância LogFileItem especificada da coleção.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Remover o método SysMon
- Remover método SysMon, classe LogFiles
- Classe LogFiles SysMon, método remove
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645008"
---
# <a name="logfilesremove-method"></a>Método LogFiles. Remove

Remove a instância [**LogFileItem**](logfileitem.md) especificada da coleção.

## <a name="syntax"></a>Sintaxe


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

Índice de inteiro do arquivo de log a ser removido da coleção. O índice é baseado em um.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

**Antes do Windows Vista:** Você não poderá remover arquivos de log da [**coleção de arquivos de log**](systemmonitor-logfiles.md) se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for definido como sysmonLogFiles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[arquivos de log](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**arquivos de log**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





