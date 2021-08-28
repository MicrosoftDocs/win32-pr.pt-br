---
description: Wilogutl.exe ajuda na análise de arquivos de log de uma instalação do Windows e exibe soluções sugeridas para erros encontrados em um arquivo de log.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9958b91513dccc32f3bfc82ff781f65f166c208
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883857"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe ajuda na análise de arquivos de log de uma instalação do Windows e exibe soluções sugeridas para erros encontrados em um arquivo de log.

Erros não críticos não são exibidos. Wilogutl.exe pode ser executado no modo silencioso ou com uma interface do usuário. A ferramenta gera relatórios como arquivos de texto na interface do usuário e nos modos silenciosos. Ele funciona melhor com arquivos de log Windows instalador detalhados, mas também funciona com logs não detalhados. Para obter mais informações, consulte [Registro em log.](logging.md)

Essa ferramenta só está disponível nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="syntax"></a>Syntax

**wilogutl.exe** *\[ &lt; opções de &gt; \] \[ <source file> \] \[ &lt; configuração &gt; \] \[ <report file directory> \]*

Você pode usar as linhas de comando a seguir para executar no modo silencioso.

**wilogutl /q /l c:** *\\ mymsilog.log* **/o** c *\\ outputdir \\*

**wilogutl /q /l** *c: \\ mymsilog.log*

## <a name="command-line-options"></a>Opções de Linha de Comando

Wilogutl.exe usa as seguintes opções de linha de comando sem maiúsculas e minúsculas. Um delimiter de traço pode ser usado no lugar de uma barra.



| Opção | Descrição                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nenhum   | É executado no modo de interface do usuário— sem opções de linha de comando.                                                                                                                                                   |
| /q     | Especifica o modo silencioso. Wilogutl.exe gera arquivos de relatório e não exibe uma interface do usuário.                                                                                            |
| /l     | Especifica o nome do arquivo de log a ser analisado. Essa opção é necessária ao usar o modo silencioso.                                                                                           |
| /o     | Especifica o diretório de saída para arquivos de relatório. Esse caminho de saída é usado somente durante a execução no modo silencioso. Se a opção não estiver presente, os relatórios serão colocados no diretório C: \\ WiLogResults. |



 

Quando executado no modo de interface do usuário, Wilogutl.exe exibe as caixas de diálogo a seguir.




| Nome | Descrição | 
|------|-------------|
| Windows Analisador de Log Detalhado do Instalador | A Windows de diálogo Analisador de Log Detalhado do Instalador permite que os usuários selecionem um arquivo de log para análise:<ul><li>O <strong>botão</strong> Abrir abre o arquivo Bloco de notas. A área de visualização pode ser usada para verificar se o arquivo de log correto foi selecionado.</li><li>O <strong>botão Analisar</strong> inicia a análise de arquivo de log e exibe a caixa de diálogo Exibição Detalhada do Arquivo de Log.</li></ul> | 
| Exibição detalhada do arquivo de log | A caixa de diálogo Exibição Detalhada do Arquivo de Log exibe informações de erro registradas. Use os <strong>botões Voltar</strong> <strong>e</strong> Próximo para navegar por vários erros. Para exibir erros não críticos, marque a caixa de seleção Mostrar <strong>Erros de Depuração</strong> Ignorados. A versão do instalador no computador usado para executar a instalação registrada é exibida. Se a instalação registrada em registro tiver sido executado com permissões elevadas, a <strong></strong> caixa de <strong></strong> seleção Instalação com privilégios elevados será marcada e as informações serão fornecidas nas caixas de texto Detalhes do Privilégio do Lado do Cliente e Detalhes do Privilégio do Lado do Servidor. <strong></strong> A caixa de diálogo Exibição Detalhada do Arquivo de Log contém os seguintes botões:<br /><ul><li><strong>Estados</strong> – mostra a caixa de diálogo Estados de Recurso e Componente.</li><li><strong>Propriedades</strong> – mostra a caixa de diálogo Propriedades.</li><li><strong>Políticas</strong> – mostra a caixa de diálogo Políticas.</li><li><strong>Log Anotado HTML –</strong> Mostrar log como arquivo HTML anotado.</li><li><strong>Salvar Resultados</strong> – salve arquivos de relatório no diretório especificado.</li><li><strong>Ajuda da mensagem de</strong> erro – mostrar a ajuda da mensagem de erro do instalador.</li><li><strong>Ajuda</strong> – mostre ajuda para o Windows do Instalador do Instalador de Log.</li><li><strong>Como ler um arquivo de log</strong> – mostrar o documento de ajuda do arquivo de log.</li></ul> | 
| Estados de recurso e componente | A <strong>caixa de diálogo Estados de Recurso</strong> e Componente exibe os estados de recursos e componentes:<ul><li>A <strong>coluna</strong> Recurso mostra o nome do recurso no pacote de instalação.</li><li>A <strong>coluna</strong> Componente mostra o nome do componente no pacote de instalação.</li><li>A <strong>coluna Instalado</strong> mostra o estado do recurso ou do componente no final da instalação.</li><li>A <strong>coluna</strong> Solicitação mostra a seleção do usuário durante a instalação do estado do recurso ou do componente.</li><li>A <strong>coluna</strong> Ação mostra a ação tomada pelo instalador para o recurso ou componente.</li></ul>Para obter mais informações, <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>consulte MsiGetComponentState</strong></a> e <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.<br /> | 
| Propriedades | A caixa de diálogo Propriedades Windows propriedades do <a href="properties.md">instalador</a> e seus valores no final da instalação. Você pode classificar as propriedades por nome ou por valor:<ul><li>A <strong>guia</strong> Cliente mostra propriedades e valores durante a parte do lado do cliente da instalação.</li><li>A <strong>guia</strong> Servidor mostra propriedades e valores durante a parte do servidor da instalação.</li><li>A <strong>guia Aninhada</strong> mostra as propriedades e os valores de <a href="concurrent-installations.md">qualquer Instalação Simultânea.</a></li></ul> | 
| Políticas | A caixa de diálogo Políticas exibe o conjunto <a href="system-policy.md">de Políticas do</a> Sistema após a instalação:<ul><li>Um valor de 0 (zero) definido para a política significa que a política não está habilitada.</li><li>Um valor de 1 (um) significa que a política está habilitada.</li><li>Um valor de ? (ponto de interrogação) significa que o valor da política não está registrado no log.</li></ul>Se você precisar de um valor de política que não está no log, tente usar o Regedit.exe para verificar as chaves do Registro no computador que está falhando na instalação.<br /> | 




 

## <a name="report-files"></a>Arquivos de relatório

Ao executar uma análise de  modo silencioso ou clicar no botão Salvar Resultados na caixa de diálogo Exibição detalhada do Arquivo de **Log,** a ferramenta analisador de instalação do instalador do Windows gera três arquivos de texto e um arquivo de log anotado em HTML.

A tabela a seguir identifica os nomes e o conteúdo nos arquivos de relatório.



| Nome                      | Descrição                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| logfilename \_summary.txt  | Resume o arquivo de log. Lista as informações exibidas pela caixa de diálogo Exibição Detalhada do Arquivo de Log e o primeiro erro.         |
| logfilename \_errors.txt   | Identifica o número de erros, os erros e as soluções recomendadas. Esse arquivo lista erros críticos e não críticos. |
| logfilename \_policies.txt | Identifica os nomes de política e os valores definidos no final da instalação como na caixa de diálogo Políticas.                       |
| detalhes \_logfilename.htm  | Um log anotado em HTML com uma legenda para a codificação de cores.                                                                      |



 

## <a name="return-values"></a>Valores de retorno

Se argumentos de linha de comando inválidos são passados para operações de modo silencioso, Wilogutl.exe não faz nada e o processo retorna um dos valores na tabela a seguir.



| Valor | Significado                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | Diretório de saída ruim especificado.                                      |
| 2     | Nome de arquivo de log ruim é especificado.                                         |
| 3     | Passou/q, mas está faltando a opção/l necessária para o nome do arquivo de log. |
| 4     | Passou em/l, mas não tem a opção necessária/q para o modo silencioso.        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> </dl>

 

 




