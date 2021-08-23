---
title: Objeto LogFiles (Isysmon.h)
description: Use essa classe para gerenciar uma coleção de um ou mais arquivos de log que contêm dados do contador de desempenho. Para recuperar esse objeto, chame SystemMonitor. LogFiles.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- Objeto LogFiles SysMon
- Objeto LogFiles SysMon, descrito
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a0890acdf656c807ae3bcb275012bd56a4711a114547f750f04fd8d875fc68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883144"
---
# <a name="logfiles-object"></a>Objeto LogFiles

Use essa classe para gerenciar uma coleção de um ou mais arquivos de log que contêm dados do contador de desempenho.

Para recuperar esse objeto, chame [**SystemMonitor. LogFiles**](systemmonitor-logfiles.md).

## <a name="members"></a>Membros

O objeto **LogFiles** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **LogFiles** tem esses métodos.



| Método                                          | Descrição                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Agrega**](systemmonitor-logfiles-add.md)       | Adiciona uma instância de [**LogFileItem**](logfileitem.md) à coleção.<br/>      |
| [**Remover**](systemmonitor-logfiles-remove.md) | Remove uma instância de [**LogFileItem**](logfileitem.md) da coleção.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **LogFiles** tem essas propriedades.



| Propriedade                                                 | Descrição                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**Contagem**](systemmonitor-logfiles-count.md)<br/> | Recupera o número de instâncias [**LogFileItem**](logfileitem.md) na coleção.<br/>  |
| [**Item**](systemmonitor-logfiles-item.md)<br/>   | Recupera a instância [**LogFileItem**](logfileitem.md) especificada da coleção.<br/> |



 

## <a name="remarks"></a>Comentários

Para ter os contadores de desempenho de exibição SYSMON de um arquivo de log, defina [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) como [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Depois de adicionar os arquivos de log à coleção, use a coleção de [**contadores**](counters.md) para especificar os dados de contadores que você deseja ler dos arquivos de log. Observe que, se **SystemMonitor. DataSourceType** for definido como **DataSourceTypeConstants.sysmonLogFiles**, o SYSMON recriará os arquivos de log sempre que você adicionar um arquivo de log ou contador às respectivas coleções.

**antes do Windows Vista:** Você não poderá adicionar arquivos de log à [**coleção de arquivos de log**](systemmonitor-logfiles.md) se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for definido como [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Primeiro, defina **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonNullDataSource**, adicione os arquivos de log e contadores e, em seguida, defina **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonLogFiles**.

As propriedades [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) e [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) especificam o intervalo de valores de amostra dos arquivos de log para o grafo. Os grafos do SYSMON apenas uma exibição de dados do arquivo de log (a exibição de gráfico não rola como faz ao grafar a atividade atual do computador). Se os dados de amostra excederem o que pode ser mostrado em uma exibição de gráfico único, o SYSMON compacta os dados de amostra (cada ponto grafado representa a média de vários valores de amostra) para ajustar todos os dados de amostra dos arquivos de log no grafo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





