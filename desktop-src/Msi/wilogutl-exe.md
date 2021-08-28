---
description: Wilogutl.exe ajuda na análise de arquivos de log de uma instalação do Windows Installer e exibe soluções sugeridas para erros encontrados em um arquivo de log.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6734b22afa6aa5d464f3d6b01555e54f240e006b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476022"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe ajuda na análise de arquivos de log de uma instalação do Windows Installer e exibe soluções sugeridas para erros encontrados em um arquivo de log.

Os erros não críticos não são exibidos. Wilogutl.exe pode ser executado no modo silencioso ou com uma interface do usuário (IU). A ferramenta gera relatórios como arquivos de texto na interface do usuário e nos modos silenciosos. ele funciona melhor com arquivos de log Windows Installer detalhados, mas também funciona com logs não detalhados. Para obter mais informações, consulte [Logging](logging.md).

essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintaxe

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

Você pode usar as linhas de comando a seguir para executar no modo silencioso.

**Wilogutl/q/l** *c: \\ mymsilog. log* **/o** *c \\ OutputDir \\*

**Wilogutl/q/l** *c: \\ mymsilog. log*

## <a name="command-line-options"></a>Opções de Linha de Comando

Wilogutl.exe usa as seguintes opções de linha de comando sem diferenciação de maiúsculas e minúsculas. Um delimitador de traço pode ser usado no lugar de uma barra.



| Opção | Descrição                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| none   | É executado no modo de interface do usuário — sem opções de linha de comando.                                                                                                                                                   |
| /q     | Especifica o modo silencioso. Wilogutl.exe gera arquivos de relatório e não exibe uma interface do usuário.                                                                                            |
| /l     | Especifica o nome do arquivo de log a ser analisado. Essa opção é necessária ao usar o modo silencioso.                                                                                           |
| /o     | Especifica o diretório de saída para arquivos de relatório. Esse caminho de saída é usado somente quando executado no modo silencioso. Se a opção não estiver presente, os relatórios serão colocados no diretório C: \\ WiLogResults. |



 

Quando executado no modo de interface do usuário, Wilogutl.exe exibe as caixas de diálogo a seguir.




| Nome | Descrição | 
|------|-------------|
| Windows Analisador detalhado de log do instalador | a Windows Installer caixa de diálogo analisador de Log detalhado permite que os usuários selecionem um arquivo de Log para análise:<ul><li>o botão <strong>abrir</strong> abre o arquivo em Bloco de notas. A área de visualização pode ser usada para verificar se o arquivo de log correto foi selecionado.</li><li>O botão <strong>analisar</strong> começa a análise do arquivo de log e exibe a caixa de diálogo exibição detalhada do arquivo de log.</li></ul> | 
| Exibição detalhada do arquivo de log | A caixa de diálogo exibição do arquivo de log detalhado exibe informações de erro registradas. Use os botões <strong>voltar</strong> e <strong>Avançar</strong> para navegar por vários erros. Para exibir erros não críticos, marque a caixa de seleção <strong>mostrar erros de depuração ignorados</strong> . A versão do instalador no computador usado para executar a instalação registrada é exibida. Se a instalação registrada tiver sido executada com permissões elevadas, a caixa de seleção <strong>instalação elevada</strong> será marcada e as informações serão fornecidas nas caixas de texto <strong>detalhes do privilégio do lado do cliente</strong> e detalhes de <strong>privilégio do lado do servidor</strong> . A caixa de diálogo exibição detalhada do arquivo de log contém os seguintes botões:<br /><ul><li><strong>Estados</strong> – mostra a caixa de diálogo de recursos e Estados de componentes.</li><li><strong>Propriedades</strong> – mostre a caixa de diálogo Propriedades.</li><li><strong>Políticas</strong> – mostrar a caixa de diálogo políticas.</li><li>Log <strong>anotado em HTML</strong> -Mostrar log como arquivo HTML anotado.</li><li><strong>Salvar resultados</strong> – salvar arquivos de relatório no diretório especificado.</li><li><strong>Mensagem de erro ajuda</strong> -mostrar ajuda da mensagem de erro do instalador.</li><li><strong>ajuda</strong> -mostrar ajuda para o Windows Installer Setup Log Analyzer.</li><li><strong>Como ler um arquivo de log</strong> -mostrar o documento de ajuda do arquivo de log.</li></ul> | 
| Estados de recursos e componentes | A caixa de diálogo Estados de recursos <strong>e componentes</strong> exibe os Estados dos recursos e componentes:<ul><li>A coluna <strong>recurso</strong> mostra o nome do recurso no pacote de instalação.</li><li>A coluna <strong>componente</strong> mostra o nome do componente no pacote de instalação.</li><li>A coluna <strong>instalado</strong> mostra o estado do recurso ou componente no final da instalação.</li><li>A coluna <strong>solicitação</strong> mostra a seleção do usuário durante a instalação para o estado do recurso ou componente.</li><li>A coluna <strong>ação</strong> mostra a ação realizada pelo instalador para o recurso ou componente.</li></ul>Para obter mais informações, consulte <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> e <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.<br /> | 
| Propriedades | a caixa de diálogo propriedades mostra Windows Installer <a href="properties.md">propriedades</a> e seus valores no final da instalação. Você pode classificar as propriedades por nome ou por valor:<ul><li>A guia <strong>cliente</strong> mostra Propriedades e valores durante a parte do lado do cliente da instalação.</li><li>A guia <strong>servidor</strong> mostra Propriedades e valores durante a parte do servidor da instalação.</li><li>A guia <strong>aninhada</strong> mostra as propriedades e os valores de qualquer <a href="concurrent-installations.md">instalação simultânea</a>.</li></ul> | 
| Políticas | A caixa de diálogo políticas exibe o conjunto de <a href="system-policy.md">políticas do sistema</a> após a instalação:<ul><li>Um valor de 0 (zero) definido para a política significa que a política não está habilitada.</li><li>Um valor de 1 (um) significa que a política está habilitada.</li><li>Um valor de? (ponto de interrogação) significa que o valor da política não é registrado no log.</li></ul>Se você precisar de um valor de política que não esteja no log, tente usar Regedit.exe para verificar as chaves do registro no computador que está falhando na instalação.<br /> | 




 

## <a name="report-files"></a>Arquivos de relatório

ao executar uma análise de modo silencioso ou clicar no botão **salvar resultados** na caixa de diálogo **exibir arquivo de log detalhado** , a ferramenta Windows Installer Setup Analyzer gera três arquivos de texto e um arquivo de Log anotado em HTML.

A tabela a seguir identifica os nomes e o conteúdo nos arquivos de relatório.



| Nome                      | Descrição                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| LogFileName \_summary.txt  | Resume o arquivo de log. Lista as informações exibidas pela caixa de diálogo exibição detalhada do arquivo de log e o primeiro erro.         |
| LogFileName \_errors.txt   | Identifica o número de erros, os erros e as soluções recomendadas. Esse arquivo lista os erros críticos e não críticos. |
| LogFileName \_policies.txt | Identifica os nomes de política e os valores definidos no final da instalação como na caixa de diálogo políticas.                       |
| detalhes \_logfilename.htm  | Um log anotado em HTML com uma legenda para a codificação de cores.                                                                      |



 

## <a name="return-values"></a>Valores de retorno

Se argumentos de linha de comando inválidos forem passados para operações de modo silencioso, o Wilogutl.exe não fará nada e o processo retornará um dos valores na tabela a seguir.



| Valor | Significado                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | Diretório de saída inválidos especificado.                                      |
| 2     | Nome de arquivo de log inadequado especificado.                                         |
| 3     | Passou/q, mas está faltando a opção/l necessária para o nome do arquivo de log. |
| 4     | Passou em/l, mas não tem a opção necessária/q para o modo silencioso.        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> </dl>

 

 




