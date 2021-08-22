---
description: O ICE35 valida se os componentes que contêm arquivos compactados armazenados em um arquivo de gabinete não estão definidos para ser executados da origem. Com Windows Instalador 2.0 ou posterior, essa restrição foi removida.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee42f97a049b165d41fef7391f0031836865dbf7bafec6b1b5e2fb868e75a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528556"
---
# <a name="ice35"></a>ICE35

O ICE35 valida se os componentes que contêm arquivos compactados armazenados em um arquivo [de gabinete](cabinet-files.md) não estão definidos para ser executados da origem. Com Windows Instalador 2.0 ou posterior, essa restrição foi removida.

ICE35 consulta a coluna Gabinete da tabela [Mídia](media-table.md) para determinar quais arquivos são compactados e armazenados em um arquivo de gabinete. Ele consulta a tabela [Arquivo para](file-table.md) determinar quais componentes contêm esses arquivos. Por fim, ele verifica [a tabela Componente](component-table.md) para determinar se os bits run-from-source estão definidos na coluna Atributos.

## <a name="result"></a>Resultado

ICE35 postará uma mensagem de erro se houver um arquivo compactado armazenado em um arquivo de gabinete pertencente a um componente com o bit msidbComponentAttributesSourceOnly definido na coluna Atributos da tabela [Componente](component-table.md). Com Windows Instalador 2.0 ou posterior, isso é alterado de um erro para uma mensagem de aviso. Um pacote que dá suporte apenas ao Windows Installer 2.0 e posterior tem a propriedade PID PAGECOUNT do Fluxo de Informações resumidas definida como um valor de pelo menos \_ 200.

O ICE35 postará uma mensagem de aviso se houver um arquivo compactado armazenado em um arquivo de gabinete pertencente a um componente com o bit msidbComponentAttributesOptional definido na coluna Atributos da tabela [Componente](component-table.md). Essa mensagem de aviso foi removida com Windows Instalador 2.0 e posterior.

Se vários arquivos em um componente estão em um arquivo de gabinete, o ICE35 relata erros para cada arquivo que tem a executar do conjunto de bits de origem.

## <a name="example"></a>Exemplo

O ICE35 relata os seguintes erros e avisos para o exemplo mostrado usando uma versão anterior Windows Installer versão 2.0.



| Erro ICE35                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRO: Component Component3 não pode ser Somente Executar da Origem, porque seu arquivo de membro 'File3' é compactado. | Há um arquivo compactado armazenado em um arquivo de gabinete e esse arquivo pertence a um componente com o bit SourceOnly definido na coluna Atributos da [tabela Component](component-table.md). Para corrigir esse erro, altere os 2 bits inferiores do valor atributos do Component2 para "00", ou seja, Local somente ou remova File4 do arquivo CAB.<br/>                                                                                                                                                                         |
| ERRO: Component Component3 não pode ser Somente Executar da Origem, porque seu arquivo de membro 'File3' é compactado. | Há um arquivo compactado armazenado em um arquivo de gabinete e esse arquivo pertence a um componente com o bit SourceOnly definido na coluna Atributos da [tabela Component](component-table.md). Como os arquivos em um componente nem todos têm que se originar da mesma mídia, o ICE35 relata erros para cada arquivo no componente que está em um gabinete.<br/> Para corrigir esse erro, altere os 2 bits inferiores do valor atributos do Component2 para "00", ou seja, Local somente ou remova File4 do arquivo CAB.<br/> |



 

[Tabela de mídia](media-table.md) (parcial)



| DiskID | LastSequence | Armário   |
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



| Atalho  | Ícone\_ |
|-----------|--------|
| Atalho1 | Icon2  |



 

Observe que os arquivos também podem ser marcados como compactados usando a propriedade Resumo de Contagem de [**Palavras**](word-count-summary.md) do fluxo [De informações resumidas](summary-information-stream.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




