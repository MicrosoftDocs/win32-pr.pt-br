---
description: O ICE35 valida que os componentes que contêm arquivos compactados armazenados em um arquivo de gabinete não estão definidos para execução da origem. Com o Windows Installer 2,0 ou posterior, essa restrição foi removida.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922019"
---
# <a name="ice35"></a>ICE35

O ICE35 valida que os componentes que contêm arquivos compactados armazenados em um [arquivo de gabinete](cabinet-files.md) não estão definidos para execução da origem. Com o Windows Installer 2,0 ou posterior, essa restrição foi removida.

ICE35 consulta a coluna de gabinete da [tabela de mídia](media-table.md) para determinar quais arquivos são compactados e armazenados em um arquivo de gabinete. Ele consulta a [tabela de arquivos](file-table.md) para determinar quais componentes contêm esses arquivos. Por fim, ele verifica a [tabela de componentes](component-table.md) para determinar se os bits de execução da origem estão definidos na coluna atributos.

## <a name="result"></a>Resultado

O ICE35 posta uma mensagem de erro se houver um arquivo compactado armazenado em um arquivo de gabinete pertencente a um componente com o conjunto de bits msidbComponentAttributesSourceOnly na coluna atributos da [tabela de componentes](component-table.md). Com o Windows Installer 2,0 ou posterior, isso é alterado de um erro para uma mensagem de aviso. Um pacote que dá suporte apenas a Windows Installer 2,0 e posteriores tem a \_ Propriedade PID PageCount do fluxo de informações de resumo definida como um valor de pelo menos 200.

O ICE35 posta a mensagem de aviso se houver um arquivo compactado armazenado em um arquivo de gabinete pertencente a um componente com o conjunto de bits msidbComponentAttributesOptional na coluna atributos da [tabela de componentes](component-table.md). Esta mensagem de aviso foi removida com Windows Installer 2,0 e posterior.

Se vários arquivos em um componente estiverem em um arquivo de gabinete, o ICE35 relatará erros para cada arquivo que tem a execução do conjunto de bits de origem.

## <a name="example"></a>Exemplo

O ICE35 relata os erros e avisos a seguir para o exemplo mostrado usando uma versão anterior à Windows Installer versão 2,0.



| Erro de ICE35                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRO: o componente Component3 não pode ser executado somente da origem, porque seu arquivo de membro ' arquivo3 ' está compactado. | Há um arquivo compactado armazenado em um arquivo de gabinete e esse arquivo pertence a um componente com o conjunto de bits SourceOnly na coluna atributos da [tabela de componentes](component-table.md). Para corrigir esse erro, altere os 2 bits inferiores do valor de atributos Component2's para "00", ou seja, somente local, ou remova Arquivo4 do arquivo CAB.<br/>                                                                                                                                                                         |
| ERRO: o componente Component3 não pode ser executado somente da origem, porque seu arquivo de membro ' arquivo3 ' está compactado. | Há um arquivo compactado armazenado em um arquivo de gabinete e esse arquivo pertence a um componente com o conjunto de bits SourceOnly na coluna atributos da [tabela de componentes](component-table.md). Como os arquivos em um componente não precisam ter origem na mesma mídia, o ICE35 relata erros para cada arquivo no componente que está em um gabinete.<br/> Para corrigir esse erro, altere os 2 bits inferiores do valor de atributos Component2's para "00", ou seja, somente local, ou remova Arquivo4 do arquivo CAB.<br/> |



 

[Tabela de mídia](media-table.md) (parcial)



| DiskID | LastSequence | Gabinete   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ | Sequência |
|-------|-------------|----------|
| Arquivo1 | Component1  | 1        |
| Arquivo2 | Component2  | 2        |
| Arquivo3 | Component2  | 3        |
| Arquivo4 | Component3  | 4        |
| Arquivo5 | Component3  | 5        |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Atributos |
|------------|------------|
| Component1 | 0          |
| Component2 | 2          |
| Component3 | 1          |



 

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | ícone\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

Observe que os arquivos também podem ser marcados como compactados usando a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) do [fluxo de informações de resumo](summary-information-stream.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




