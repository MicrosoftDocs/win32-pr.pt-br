---
title: Método LogFiles. Add
description: Adiciona um arquivo de log à coleção.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Adicionar método SysMon
- Adicionar método SysMon, classe LogFiles
- Classe LogFiles SysMon, método Add
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085605"
---
# <a name="logfilesadd-method"></a>Método LogFiles. Add

Adiciona um arquivo de log à coleção.

## <a name="syntax"></a>Sintaxe


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do caminho* \[ no\]
</dt> <dd>

Caminho para o arquivo de log. Você pode especificar o caminho como um caminho absoluto, relativo ou UNC. A extensão do nome do arquivo de log deve ser. csv,. tsv ou. blg.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve usar a ferramenta Logman.exe ou o snap-in do MMC Perfmon. msc para gerar os arquivos de log que você adiciona a essa coleção. Para Perfmon. msc, os logs de contador estão localizados em **logs e alertas de desempenho**. Para obter detalhes sobre como usar Logman.exe ou Perfmon. msc, pesquise logman ou usando o desempenho, respectivamente, no **centro de ajuda e suporte**.

**Antes do Windows Vista:** Você não poderá adicionar arquivos de log à [**coleção de arquivos de log**](systemmonitor-logfiles.md) se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for definido como [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Primeiro, defina **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonNullDataSource**, adicione os arquivos de log e contadores e, em seguida, defina **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonLogFiles**.

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

 

 





