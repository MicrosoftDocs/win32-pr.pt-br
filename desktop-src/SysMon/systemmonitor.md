---
title: Objeto SystemMonitor (Isysmon. h)
description: Essa classe contém os métodos e as propriedades usadas para configurar o controle do monitor do sistema.
ms.assetid: 5a6195ee-ed89-4f5d-85dd-88cf4a9b5155
keywords:
- Objeto SystemMonitor SysMon
- Objeto SystemMonitor SysMon, descrito
topic_type:
- apiref
api_name:
- SystemMonitor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297f0e3e67134f911932aa7784396c244dc79f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762876"
---
# <a name="systemmonitor-object"></a>Objeto SystemMonitor

Essa classe contém os métodos e as propriedades usadas para configurar o controle do monitor do sistema.

## <a name="members"></a>Membros

O objeto **SystemMonitor** tem estes tipos de membros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

O objeto **SystemMonitor** tem esses eventos.



| Evento                                                         | Descrição                                                                                                                 |
|:--------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**OnCounterAdded**](systemmonitor-oncounteradded.md)        | Notifica quando um contador é adicionado à coleção de [**contadores**](counters.md) .<br/>                             |
| [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)   | Notifica você antes de um contador ser excluído da coleção de [**contadores**](counters.md) .<br/>                       |
| [**OnCounterSelected**](-systemmonitor-oncounterselected.md) | Notifica quando um contador é selecionado.<br/>                                                                         |
| [**AoClicarDuasVezes**](-systemmonitor-ondblclick.md)               | Notifica quando um usuário clica duas vezes na linha do gráfico, na barra de histograma ou no item de relatório com o botão esquerdo do mouse.<br/> |
| [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) | Notifica você quando os valores de exemplo para os contadores foram coletados.<br/>                                            |



 

### <a name="methods"></a>Métodos

O objeto **SystemMonitor** tem esses métodos.



| Método                                                       | Descrição                                                                                                                                                              |
|:-------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchLocking**](systemmonitor-batchinglock.md)           | Bloqueia o monitor do sistema para impedi-lo de amostragem de dados do contador do contador ou arquivo de log recém-adicionado.<br/>                                                   |
| [**BrowseCounters**](systemmonitor-browsecounters.md)       | Exibe a caixa de diálogo **Adicionar contador** .<br/>                                                                                                                      |
| [**ClearData**](systemmonitor-cleardata.md)                 | Limpa todos os campos de dados no controle.<br/>                                                                                                                        |
| [**CollectSample**](systemmonitor-collectsample.md)         | Obtém um valor para cada contador no objeto da coleção de **contadores** .<br/>                                                                                       |
| [**CopiarObjeto**](systemmonitor-copy.md)                           | Copia as configurações de Propriedade do controle, a lista de contadores e os dados do contador para a área de transferência como um objeto HTML.<br/>                                                |
| [**Exibirproperties**](systemmonitor-displayproperties.md) | Exibe a caixa de diálogo **Propriedades do grafo** .<br/>                                                                                                                 |
| [**GetLogViewRange**](systemmonitor-getlogviewrange.md)     | Recupera a data de início usada para recuperar valores de contadores dos arquivos de log.<br/>                                                                               |
| [**LoadSettings**](systemmonitor-loadsettings.md)           | Adiciona os contadores no arquivo de modelo HTML ao monitor do sistema.<br/>                                                                                            |
| [**Colar**](systemmonitor-paste.md)                         | Acrescenta a lista de contadores que foram copiados para a área de transferência para a coleção atual de contadores. <br/>                                                        |
| [**Relog**](systemmonitor-relog.md)                         | Registra novamente os dados do contador em um novo arquivo. Você também pode usar esse método para especificar um novo tipo de arquivo e reduzir o número de amostras contidas no arquivo de log.<br/> |
| [**Redefinir**](systemmonitor-reset.md)                         | Remove todos os objetos de [**comitem**](counteritem.md) do objeto da coleção **Counters** .<br/>                                                               |
| [**SaveAs**](systemmonitor-saveas.md)                       | Salva os valores do contador no modo de exibição de gráfico em um arquivo de log.<br/>                                                                                                     |
| [**ScaleToFit**](systemmonitor-scaletofit.md)               | Dimensionar valores do contador para caber no grafo.<br/>                                                                                                                     |
| [**SetLogViewRange**](systemmonitor-setlogviewrange.md)     | Define a data de início usada para recuperar valores de contadores dos arquivos de log.<br/>                                                                                    |
| [**UpdateGraph**](systemmonitor-updategraph.md)             | Atualiza o conteúdo das janelas de monitor do sistema.<br/>                                                                                                         |



 

### <a name="properties"></a>Propriedades

O objeto **SystemMonitor** tem essas propriedades.



| Propriedade                                                                                | Descrição                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aparência**](systemmonitor-appearance.md)<br/>                               | Recupera ou define a aparência do controle para incluir ou omitir os efeitos de exibição tridimensionais.<br/>                                                                                                                        |
| [**Fundo**](systemmonitor-backcolor.md)<br/>                                 | Recupera ou define a cor do plano de fundo das exibições de gráfico e relatório.<br/>                                                                                                                                                        |
| [**BackColorCtl**](systemmonitor-backcolorctl.md)<br/>                           | Recupera ou define a cor do plano de fundo do controle.<br/>                                                                                                                                                                       |
| [**BorderStyle**](systemmonitor-borderstyle.md)<br/>                             | Recupera ou define o estilo de borda do controle.<br/>                                                                                                                                                                           |
| [**ChartScroll**](systemmonitor-chartscroll.md)<br/>                             | Recupera ou define um valor que determina se o gráfico de linha rola na exibição.<br/>                                                                                                                                             |
| [**Contadores**](systemmonitor-counters.md)<br/>                                   | Recupera a coleção de objetos de [**coitem**](counteritem.md) .<br/>                                                                                                                                                      |
| [**DataPointCount**](systemmonitor-datapointcount.md)<br/>                       | Recupera ou define o número de pontos de dados exibidos em um grafo de linha.<br/>                                                                                                                                                       |
| [**DataSourceType**](systemmonitor-datasourcetype.md)<br/>                       | Recupera ou define a origem dos dados do contador de desempenho.<br/>                                                                                                                                                                |
| [**TipoDeExibição**](systemmonitor-displaytype.md)<br/>                             | Recupera ou define o tipo de grafo usado para grafar os dados do contador de desempenho.<br/>                                                                                                                                              |
| [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)<br/>             | Recupera ou define um valor que determina se o SYSMON usa o agrupamento de dígitos ao exibir valores numéricos.<br/>                                                                                                                      |
| [**EnableToolTips**](systemmonitor-enabletooltips.md)<br/>                       | Recupera ou define um valor que determina se uma dica de ferramenta é mostrada quando o mouse passa sobre um contador em uma das exibições de gráfico.<br/>                                                                                             |
| [**Fonte**](systemmonitor-font.md)<br/>                                           | Recupera ou define a fonte usada no controle.<br/>                                                                                                                                                                              |
| [**ForeColor**](systemmonitor-forecolor.md)<br/>                                 | Recupera ou define a cor do texto que aparece no controle.<br/>                                                                                                                                                         |
| [**GraphTitle**](systemmonitor-graphtitle.md)<br/>                               | Recupera ou define o título do grafo.<br/>                                                                                                                                                                                    |
| [**GridColor**](systemmonitor-gridcolor.md)<br/>                                 | Recupera ou define a cor das linhas de grade usadas no grafo.<br/>                                                                                                                                                             |
| [**Realce**](systemmonitor-highlight.md)<br/>                                 | Recupera ou define um valor que indica se os valores dos contadores selecionados são realçados no grafo.<br/>                                                                                                               |
| [**LogFileName**](systemmonitor-logfilename.md)<br/>                             | Obsoleto. Recupera ou define o nome de um arquivo de log a ser usado como a origem dos valores do contador exibidos no monitor do sistema.<br/>                                                                                                   |
| [**arquivos de log**](systemmonitor-logfilename.md)<br/>                                | Coleção de um ou mais arquivos de log a serem usados como a origem dos valores do contador exibidos no monitor do sistema.<br/>                                                                                                                  |
| [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)<br/>               | Recupera o carimbo de data/hora do valor do contador mais antigo de um contador em sua coleção de contadores que foi registrada nos arquivos de log.<br/>                                                                                           |
| [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)<br/>                 | Recupera o carimbo de data/hora do valor do contador mais recente de um contador em sua coleção de contadores que foi registrada nos arquivos de log.<br/>                                                                                             |
| [**LogViewStart**](systemmonitor-logviewstart.md)<br/>                           | Recupera ou define a data de início usada para recuperar valores de contadores dos arquivos de log.<br/>                                                                                                                                      |
| [**LogViewStop**](systemmonitor-logviewstop.md)<br/>                             | Recupera ou define a data de término usada para recuperar valores de contadores dos arquivos de log.<br/>                                                                                                                                        |
| [**ManualUpdate**](systemmonitor-manualupdate.md)<br/>                           | Recupera ou define um valor que indica se o conteúdo do monitor do sistema será atualizado manualmente ou automaticamente em intervalos especificados.<br/>                                                                           |
| [**MaximumScale**](systemmonitor-maximumscale.md)<br/>                           | Recupera ou define o valor máximo do eixo vertical (Y) do grafo.<br/>                                                                                                                                                   |
| [**MinimumScale**](systemmonitor-minimumscale.md)<br/>                           | Recupera ou define o valor mínimo do eixo vertical (Y) do grafo.<br/>                                                                                                                                                   |
| [**MonitorDuplicateInstances**](systemmonitor-monitorduplicateinstances.md)<br/> | Recupera ou define um valor que determina se várias instâncias de um contador podem ser monitoradas.<br/>                                                                                                                          |
| [**ReadOnly**](systemmonitor-readonly.md)<br/>                                   | Recupera ou define um valor que determina se um usuário pode modificar os valores de Propriedade do controle.<br/>                                                                                                                      |
| [**ReportValueType**](systemmonitor-reportvaluetype.md)<br/>                     | Recupera ou define um valor que determina se as exibições de histograma e relatório exibem o último valor amostrado durante o intervalo de amostragem ou um valor calculado da amostragem, como o valor médio ou mínimo do contador.<br/> |
| [**ShowHorizontalGrid**](systemmonitor-showhorizontalgrid.md)<br/>               | Recupera ou define um valor que determina se as linhas de grade horizontais são exibidas no grafo.<br/>                                                                                                                          |
| [**Conlegenda**](systemmonitor-showlegend.md)<br/>                               | Recupera ou define um valor que determina se a legenda é exibida.<br/>                                                                                                                                                   |
| [**ShowScaleLabels**](systemmonitor-showscalelabels.md)<br/>                     | Recupera ou define um valor que determina se os rótulos de escala são exibidos no eixo vertical do grafo.<br/>                                                                                                          |
| [**ShowTimeAxisLabels**](systemmonitor-showtimeaxislabels.md)<br/>               | Recupera ou define um valor que determina se o eixo horizontal (X) da exibição de gráfico contém rótulos.<br/>                                                                                                                      |
| [**MostrarBarraDeFerramentas**](systemmonitor-showtoolbar.md)<br/>                             | Recupera ou define um valor que determina se a barra de ferramentas é exibida no controle.<br/>                                                                                                                                   |
| [**ShowValueBar**](systemmonitor-showvaluebar.md)<br/>                           | Recupera ou define um valor que determina se a barra de valores (o conjunto de valores estatísticos abaixo do grafo) é exibida no controle.<br/>                                                                                 |
| [**ShowVerticalGrid**](systemmonitor-showverticalgrid.md)<br/>                   | Recupera ou define um valor que determina se as linhas de grade verticais são exibidas no grafo.<br/>                                                                                                                            |
| [**SqlDsnName**](systemmonitor-sqldsnname.md)<br/>                               | Recupera ou define o nome da fonte de dados ODBC.<br/>                                                                                                                                                                                 |
| [**SqlLogSetName**](systemmonitor-sqllogsetname.md)<br/>                         | Recupera ou define o nome amigável do conjunto de logs.<br/>                                                                                                                                                                          |
| [**TimeBarColor**](systemmonitor-timebarcolor.md)<br/>                           | Recupera ou define a cor da barra de tempo (a barra vertical que se move pela janela do grafo para indicar a passagem de cada intervalo de amostragem na exibição de gráfico de linha).<br/>                                                  |
| [**UpdateInterval**](systemmonitor-updateinterval.md)<br/>                       | Recupera ou define o período de tempo que o SYSMON espera antes da próxima vez que atualizar o gráfico ou relatório.<br/>                                                                                                                  |
| [**YAxisLabel**](systemmonitor-yaxislabel.md)<br/>                               | Recupera ou define o rótulo do eixo vertical (Y) do grafo.<br/>                                                                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





