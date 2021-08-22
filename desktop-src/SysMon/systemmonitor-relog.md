---
title: Método SystemMonitor. relog
description: Registra novamente os dados do contador em um novo arquivo. Você também pode usar esse método para especificar um novo tipo de arquivo e reduzir o número de amostras contidas no arquivo de log.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Método relog. SysMon
- Método relog SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73025a352ba3ec2e9ed113c59a7e04f98084495da834f83bf052c697833dd13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881723"
---
# <a name="systemmonitorrelog-method"></a>Método SystemMonitor. relog

Registra novamente os dados do contador em um novo arquivo. Você também pode usar esse método para especificar um novo tipo de arquivo e reduzir o número de amostras contidas no arquivo de log.

## <a name="syntax"></a>Sintaxe


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do arquivo* \[ no\]
</dt> <dd>

Caminho do arquivo de log. Você pode especificar o caminho como um caminho absoluto, relativo ou UNC. A extensão do nome do arquivo de log deve ser. blg,. tsv ou .csv. Se uma pasta no caminho não existir, o SYSMON a criará. Se o arquivo existir, o arquivo será substituído. O SYSMON aplica as ACLs padrão do diretório pai.

</dd> <dt>

*filetype* \[ no\]
</dt> <dd>

Formato dos dados do contador salvos no arquivo de log. Você pode especificar [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysMonFileCsv** ou **SysmonFileType.sysmonFileTsv**.

</dd> <dt>

*Filtrar* \[ no\]
</dt> <dd>

Número de amostras dos arquivos de log antigos a serem salvos no novo arquivo de log. Especifique 1 para salvar todas as amostras dos arquivos antigos nos novos arquivos. Especifique 2 para salvar um de cada dois exemplos do arquivo antigo. Especifique 3 para salvar um de cada três amostras do arquivo antigo. E assim por diante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método usa os arquivos de log contidos na coleção [**SystemMonitor. LogFiles**](systemmonitor-logfiles.md) para repetir os dados do contador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. SaveAs**](systemmonitor-saveas.md)
</dt> </dl>

 

 





