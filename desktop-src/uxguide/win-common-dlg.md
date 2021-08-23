---
title: Caixas de diálogo comuns
description: o Microsoft Windows caixas de diálogo comuns consiste nas caixas de diálogo abrir arquivo, salvar arquivo, abrir pasta, localizar e substituir, imprimir, configurar página, fonte e cor.
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9ddd0bf5af0a609c07550ec91e7482ce35270c85b81d553d4a5e262db6ed3683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935578"
---
# <a name="common-dialogs"></a>Caixas de diálogo comuns

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

o Microsoft Windows caixas de diálogo comuns consiste nas caixas de diálogo abrir arquivo, salvar arquivo, abrir pasta, localizar e substituir, imprimir, configurar página, fonte e cor.

## <a name="open-file"></a>Abrir arquivo

![captura de tela da caixa de diálogo aberta ](images/win-common-dlg-image1.png)

O arquivo aberto é otimizado para localizar rapidamente os itens a serem usados com um programa.

## <a name="save-file"></a>Salvar arquivo

![captura de tela da caixa de diálogo Salvar como ](images/win-common-dlg-image2.png)

Salvar arquivo fecha o loop salvando um arquivo com seus metadados.

## <a name="open-folder"></a>Abrir Pasta

![captura de tela da caixa de diálogo procurar arquivos/pastas ](images/win-common-dlg-image3.png)

Abrir pasta é especificamente para escolher pastas.

## <a name="find-and-replace"></a>Localizar e substituir

![captura de tela das caixas de diálogo Localizar e substituir ](images/win-common-dlg-image4.png)

A opção Localizar permite que os usuários pesquisem cadeias de caracteres de texto, enquanto a versão de substituição permite que os usuários substituam correspondências por outra cadeia de caracteres.

## <a name="print"></a>Imprimir

![captura de tela da caixa de diálogo Imprimir ](images/win-common-dlg-image5.png)

A impressão permite que os usuários selecionem o que imprimir, o número de cópias a serem impressas e a sequência de agrupamento, juntamente com a capacidade de escolher e configurar impressoras.

## <a name="page-setup"></a>Configuração de página

![captura de tela da caixa de diálogo Configurar página ](images/win-common-dlg-image6.png)

A configuração de página permite que os usuários selecionem o tamanho e a origem do papel, a orientação da página e as margens.

## <a name="font"></a>Fonte

![captura de tela da caixa de diálogo fonte ](images/win-common-dlg-image7.png)

Fonte exibe as fontes e os tamanhos de pontos das fontes instaladas disponíveis.

## <a name="color"></a>Color

![captura de tela da caixa de diálogo Editar cores ](images/win-common-dlg-image8.png)

A cor permite que os usuários selecionem uma cor, seja por meio de um conjunto predefinido de cores ou escolhendo uma cor "personalizada".

## <a name="design-concepts"></a>Conceitos de design

Usando as caixas de diálogo comuns, você ajuda a fornecer aos usuários uma experiência consistente em diferentes programas. Além disso, usando as caixas de diálogo comuns, você também ajuda a fornecer uma experiência eficiente e agradável aos usuários.

Você pode melhorar significativamente a experiência dos usuários com essas caixas de diálogo escolhendo os padrões mais apropriados para:

-   Valores de entrada (exemplos: pastas padrão, nomes de arquivo padrão).
-   Opções selecionadas (exemplos: impressora selecionada, opções de impressão).
-   Exibições (exemplos: mostrando imagens no modo de exibição de miniatura, mostrando imagens sem nomes de arquivos, classificando por data, larguras de coluna).
-   Apresentação (exemplos: tamanho da janela, localização e conteúdo).

Você deve determinar os padrões iniciais e os padrões subsequentes. Os valores padrão iniciais são determinados pelo seu programa e com base no uso esperado do usuário de destino, enquanto os padrões subsequentes são baseados no uso real. O uso anterior é o melhor indicador de uso futuro.

Os padrões do seu programa são eficientes? Monitore o número de etapas que os usuários precisam executar para realizar as tarefas mais comuns. Se os usuários precisarem repetir as mesmas etapas potencialmente desnecessárias toda vez que executarem uma tarefa, os valores padrão poderão ser aprimorados.

**Se você fizer apenas uma coisa...**

Forneça aos usuários uma experiência eficiente e agradável selecionando os padrões iniciais e subsequentes apropriados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

**Ok! Use as caixas de diálogo comuns para uma experiência de usuário consistente. Não crie seu próprio.** É especialmente difícil criar UIs personalizadas que navegam no namespace de forma correta e segura. Observe que você pode personalizar as caixas de diálogo comuns, se necessário.

para o Windows Vista, o arquivo aberto e o arquivo de salvamento têm uma nova arquitetura extensível para facilitar a exposição de funcionalidades adicionais. Esse mecanismo é flexível o suficiente para atender aos requisitos mínimos dos principais fornecedores de software independentes (ISVs), mas não ser quebrados por versões futuras do Windows.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   Quando apropriado, forneça alternativas mais diretas ou [sem janela restrita](glossary.md) . Permitir que os usuários:
    -   Abra os arquivos soltando-os em seu programa.
    -   Salve os arquivos usando seu nome e local atuais com um comando salvar.
    -   Localize a próxima ocorrência de uma cadeia de caracteres usando a tecla F3.
    -   Imprima uma cópia de um documento inteiro para a impressora padrão com um comando Print.
    -   Alterar fontes e atributos de fonte usando uma barra de ferramentas ou uma janela de paleta.
    -   Altere as cores usando uma barra de ferramentas ou uma janela de paleta.
-   Use os comandos a seguir para exibir caixas de diálogo comuns (fornecidas junto com suas [chaves de acesso](glossary.md)preferenciais):



| Caixa de diálogo comum          | Comando                                 |
|------------------------|-----------------------------------------|
| Abrir arquivo<br/>         | Abrir...<br/>                            |
| Salvar arquivo<br/>         | Salvar como...<br/>                         |
| Abrir Pasta<br/>       | Abrir pasta... ou escolha a pasta...<br/> |
| Localizar e Substituir<br/>  | Localizar... ou substituir...<br/>              |
| Imprimir<br/>             | Imprimir...<br/>                           |
| Configurar Página<br/>        | Configurar página...<br/>                      |
| Fonte<br/>              | Fonte... ou escolha a fonte...<br/>          |
| Color<br/>             | Cor... ou escolha cor...<br/>        |



 

-   Você pode usar comandos mais específicos, conforme apropriado. Exemplo: para exportar um arquivo, use o arquivo de exportação de comando em vez de salvar como.
-   Defina o título da caixa de diálogo para refletir o comando que o iniciou. Exemplo: se salvar arquivo for iniciado a partir de um comando Exportar arquivo, renomeie a caixa de diálogo para exportar o arquivo.

### <a name="open-file"></a>Abrir arquivo

-   Para a pasta padrão inicial, use uma pasta especializada (imagens, música, vídeos) conforme apropriado; caso contrário, use documentos.
-   Para pastas padrão subsequentes, use a última pasta aberta pelo usuário usando o programa.
-   Ao abrir arquivos de fotos, suprimir nomes de arquivo por padrão. Normalmente, as fotos são identificadas por suas miniaturas e seus nomes normalmente não são significativos.

### <a name="save-file"></a>Salvar arquivo

-   Para a pasta padrão inicial (se um novo arquivo estiver sendo salvo pela primeira vez), use a pasta especializada (imagens, música, vídeos) conforme apropriado; caso contrário, use documentos.
-   Para arquivos temporários, use a pasta temporária do usuário atual. Escolha nomes de arquivo simples, mas exclusivos. Exemplo: Use file0001. tmp em vez de ~ DF1A92. tmp.
    -   **Desenvolvedores:** Você pode obter a pasta temporária do usuário atual usando a função de API GetTempPath.
-   Para o nome de arquivo padrão inicial, use um nome padrão exclusivo com base em:
    -   O conteúdo do arquivo, se conhecido. Exemplo: as primeiras palavras em um documento.
    -   Um padrão escolhido pelo usuário. Exemplo: se o arquivo anterior tiver sido denominado "Havaí 1.jpg", escolha "Havaí 2.jpg" como o próximo arquivo.
    -   Um padrão genérico com base no tipo de arquivo. Exemplo: "Photo1.jpg".
-   Para os padrões subsequentes (se o arquivo já existir), use a pasta e o nome atuais do arquivo.
-   Ao salvar um arquivo, preserve sua data de criação. Se o programa salvar arquivos criando um arquivo temporário, excluir o original e renomear o arquivo temporário para o nome do arquivo original, certifique-se de copiar a data de criação do arquivo original.
-   Use salvar arquivo se o usuário selecionar o comando salvar sem especificar um nome de arquivo.

### <a name="file-types-lists"></a>Listas de tipos de arquivo

**Observação:** As listas de tipos de arquivo são usadas por arquivo aberto e arquivo de salvamento para determinar os tipos de arquivos exibidos e a extensão de arquivo padrão.

-   Se a lista de tipos de arquivo for curta (cinco ou menos), ordene a lista por probabilidade de uso. Se a lista for longa (seis ou mais), use uma ordem alfabética para facilitar a localização dos tipos.
-   Para salvar arquivo, inclua todas as variações das extensões de arquivo com suporte, mesmo se não forem comuns, e coloque a extensão mais comum primeiro. A lógica de manipulação de arquivo examina essa lista para determinar se o usuário forneceu uma extensão de arquivo com suporte. Exemplo: se uma lista de tipos de arquivo JPEG incluir apenas .jpg e. jpeg, o arquivo Test. jpe poderá ser salvo como test.jpe.jpg.
-   Para salvar arquivo, o tipo de arquivo padrão inicial é o mais provável escolhido pelo usuário de destino. O padrão subsequente é o tipo atual do arquivo.
-   Para o arquivo aberto, o tipo de arquivo padrão inicial é o mais provável escolhido pelo usuário de destino. O padrão subsequente deve ser o último tipo de arquivo usado.
-   Para abrir arquivo, inclua uma entrada "todos os arquivos" como o primeiro item se os usuários puderem abrir qualquer tipo de arquivo ou se precisar ver todos os arquivos em uma pasta ao mesmo tempo. Considere fornecer outros filtros meta, como "todas as imagens", "todas as músicas" e "todos os vídeos". Coloque-os imediatamente após "todos os arquivos".
-   Use o formato "nome do tipo de arquivo ( \* . EXT1; \* . ext2). " O nome do tipo de arquivo deve ser o nome do tipo de arquivo registrado, que pode ser exibido no item do painel de controle opções de pasta. Exemplo: "documento HTML ( \*.htm; \*.html). "
    -   **Exceção:** Para meta-filtros, remova a lista de extensão de arquivo para eliminar a desordem. Exemplos: "todos os arquivos", "todas as imagens", "todas as músicas" e "todos os vídeos".
-   Use a [capitalização de estilo de frase](glossary.md) para os nomes de tipo de arquivo e minúsculas para as extensões de tipo de arquivo.

### <a name="open-folder"></a>Abrir Pasta

-   **Para novos programas, use a caixa de diálogo abrir arquivos no modo "escolher pastas".** isso requer o Windows Vista ou posterior, portanto, use a caixa de diálogo abrir pasta para programas que são executados em versões anteriores do Windows.
    -   **Desenvolvedores:** Você pode usar a caixa de diálogo abrir arquivos no modo "escolher pastas" usando o \_ sinalizador FOS PICKFOLDERS.

### <a name="font"></a>Fonte

-   Se necessário, você pode filtrar a lista de fontes para mostrar apenas as fontes disponíveis para seu programa.

### <a name="persistence"></a>Persistência

-   Considere tornar os seguintes valores persistentes para usar como padrões subsequentes:
    -   Valores de entrada (exemplos: pastas padrão, nomes de arquivo padrão).
    -   Opções selecionadas (exemplos: impressora selecionada, opções de impressão).
    -   Exibições (exemplos: mostrando imagens no modo de exibição de miniatura, mostrando imagens sem nomes de arquivos, classificando por data, larguras de coluna).
    -   Apresentação (exemplos: tamanho da janela, localização e conteúdo).

**Exceção:** Não faça esses valores persistirem em caixas de diálogo comuns quando seu uso for, de modo que os usuários têm a probabilidade muito mais desejados de iniciar completamente.

-   Ao determinar os valores padrão, considere o que os usuários de destino têm mais probabilidade de se desejarem com base nos cenários importantes. Além disso, considere cenários em uma instância de programa, em várias instâncias (consecutivas ou simultâneas) e em vários documentos. Não faça com que os valores persistam em circunstâncias que provavelmente não são úteis.
    -   **Exemplo:** Para um aplicativo típico baseado em documento, é útil usar as configurações persistentes abrir arquivo e salvar arquivo em uma instância do programa e em instâncias consecutivas, mas manter as instâncias simultâneas independentes. Dessa forma, os usuários podem trabalhar com eficiência com vários documentos de cada vez.
-   Faça as configurações persistirem em uma base por programa por usuário.

 

