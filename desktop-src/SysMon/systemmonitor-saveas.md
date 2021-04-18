---
title: Método SystemMonitor. SaveAs
description: Salva os valores do contador no modo de exibição de gráfico em um arquivo de log.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- Método SaveAs SysMon
- Método SaveAs SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771791"
---
# <a name="systemmonitorsaveas-method"></a>Método SystemMonitor. SaveAs

Salva os valores do contador no modo de exibição de gráfico em um arquivo de log.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do arquivo* \[ no\]
</dt> <dd>

Caminho do arquivo de log. Você pode especificar o caminho como um caminho absoluto, relativo ou UNC. A extensão do nome do arquivo de log deve ser. tsv ou. htm. Se uma pasta no caminho não existir, o SYSMON a criará. Se o arquivo existir, o arquivo será substituído. O SYSMON aplica as ACLs padrão do diretório pai.

</dd> <dt>

*filetype* \[ no\]
</dt> <dd>

Formato dos dados do contador salvos no arquivo de log. Você pode especificar [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) ou **SysmonFileType.sysmonFileTsv**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Somente os dados do contador visíveis no modo de exibição de gráfico são salvos (para o número real de pontos de dados salvos, consulte [**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. relog**](systemmonitor-relog.md)
</dt> </dl>

 

 





