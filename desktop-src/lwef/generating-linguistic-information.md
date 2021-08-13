---
title: Gerando informações linguísticas
description: Gerando informações linguísticas
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a068153863236b7096b67a976bbcf0654af9c75df87d2f527027830a4df33eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479268"
---
# <a name="generating-linguistic-information"></a>Gerando informações linguísticas

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Depois de gravar um novo arquivo de som ou carregar um arquivo de som existente, você pode gerar informações phoneéticas e de quebra de palavras inserindo texto que corresponda ao seu arquivo de som na caixa Representação de **Texto.** Em seguida, **escolha o comando Gerar Informações** Linguísticas no menu Editar ou na barra de ferramentas.  O editor de som exibe uma mensagem de progresso e começa a processar o arquivo de som. Quando termina de gerar informações linguísticas, ele exibe um mapeamento de rótulos de palavra e phoneme para o arquivo de som em caixas na caixa **Representação de** Áudio. Observe que o **comando Gerar Informações Linguísticas** permanece desabilitado até que você insira uma representação de texto para o arquivo de som.

![Captura de tela que mostra os painéis 'Representação de Texto' e 'Representação de Áudio' na Ferramenta de Edição de Som de Informações Linguísticas da Microsoft.](images/f3listlabel.gif)

Se o editor não produzir um conjunto aceitável de rótulos de palavra ou phoneme, escolha o **comando Gerar Informações Linguísticas** novamente. Se o editor não gerar nenhuma informação linguística, verifique sua representação de texto para garantir que todas as palavras sejam ordenadas e escritas corretamente e que você não tenha espaços desnecessários em torno da pontuação. Em seguida, escolha **o comando Gerar Informações Linguísticas** novamente. Você pode editar a representação de  texto selecionando texto na caixa de texto Representação de Texto e usando os comandos Recortar, Copiar e **Colar** no **menu** Editar.  Se você não tiver certeza das palavras que o arquivo de  som inclui, poderá reproduzir o arquivo de som escolhendo Reproduzir no **menu** Editar ou na barra de ferramentas do editor. Se o editor ainda não conseguir produzir rótulos linguísticos, tente gravar o arquivo de som novamente. Uma gravação de baixa qualidade, especialmente com ruído excessivo em segundo plano, provavelmente reduzirá a probabilidade de gerar informações linguísticas razoáveis.

Você também pode criar manualmente suas próprias informações linguísticas selecionando parte da representação de áudio e escolhendo Inserir **Phoneme** ou **Inserir Palavra** **no** menu Editar. Esses comandos também estarão disponíveis se você clicar com o botão direito do mouse na seleção.

Para ver como as informações linguísticas podem ser usadas  para animação de caracteres de sincronização com o Microsoft Agent, escolha o botão Reproduzir na barra de ferramentas e o editor reproduzirá seu arquivo de som, animando uma imagem de amostra de boca com base nas informações de rótulo geradas.

Você pode alterar a exibição do rótulo phoneme para mostrar as atribuições de IPA (Alfabeto Phoneético Internacional) escolhendo o comando **Phoneme Label Display** no **menu** Editar e, em seguida, o comando IPA. Isso exibe o valor de byte para o phoneme. Para voltar aos nomes descritivos, escolha o comando Exibição de Rótulo do **Phoneme** novamente e escolha **Nome**.

### <a name="playing-a-sound-file"></a>Como tocar um arquivo de som

Você pode reproduzir arquivos Windows de som padrão ou arquivos de som aprimorados linguisticamente escolhendo o comando **Reproduzir** no **menu** Áudio ou na barra de ferramentas do editor. Os **comandos Pausar** **e** Parar permitem pausar ou parar de tocar o arquivo de som. Conforme você reproduz o arquivo, a imagem de boca de exemplo é animada para mostrar como as informações de sincronização podem ser usadas por um caractere do Microsoft Agent.

Você também pode reproduzir uma parte selecionada de um  arquivo de som arrastando uma seleção na Representação de Áudio ou clicando em um rótulo de palavra ou phoneme e escolhendo **Reproduzir**. Você pode estender uma seleção existente pressionando SHIFT e clicando ou pressionando SHIFT e arrastando para o novo local na Representação **de Áudio**.

### <a name="editing-linguistic-information"></a>Editando informações linguísticas

Você pode editar as informações linguísticas de um arquivo de várias maneiras. Por exemplo, você pode ajustar o limite de um rótulo de palavra ou phoneme movendo o ponteiro para a borda da caixa que define o intervalo do rótulo. Quando o ponteiro mudar para o ponteiro de movimentação de limite, arraste para a esquerda ou para a direita. O editor ajusta automaticamente o limite de palavra ou phoneme adjacente também.

![Captura de tela que mostra as edições das informações linguísticas de um arquivo.](images/f4listadj.gif)

Ajustar o limite de um rótulo de phoneme altera o tempo de um phoneme quando o áudio é reproduzindo. Para caracteres desenvolvidos para uso com o Microsoft Agent, alterar o limite do rótulo phoneme pode alterar o tempo ou a duração de uma imagem de boca mapeada para esse phoneme. Alterar o limite de um rótulo de palavra altera o tempo da aparência da palavra no balão de palavra do caractere.

Você também pode substituir uma atribuição de phoneme selecionando o rótulo phoneme e escolhendo Substituir **Phoneme** no **menu** Editar ou clicando com o botão direito do mouse no rótulo do phoneme e escolhendo Substituir **Phoneme** no menu pop-up. O editor exibe a caixa **de diálogo Substituir Phoneme** e realça a atribuição de phoneme atual do rótulo. Você pode escolher um phoneme de substituição selecionando um na lista **IPA** ou escolhendo outra entrada na **lista** Nome. Se mais de uma tradução de IPA estiver disponível para esse nome, escolha um item na **lista IPA.** Para inserir uma designação de IPA para um phoneme que pode não ser incluído diretamente na linguagem, digite seu valor hexatório ou vários valores hexatórios, concatenados com um caractere de a mais (+). Depois de selecionar as informações de phoneme de substituição, escolha **OK** e o editor substituirá o rótulo de phoneme selecionado.

![Captura de tela que mostra a caixa de diálogo "Substituir Phoneme", com "<SIL>" selecionado como o rótulo descritivo.](images/f5listphone.gif)

Da mesma forma, você pode substituir um rótulo de palavra clicando na caixa do rótulo e escolhendo  Substituir **Palavra** ou clicando com o botão direito do mouse na caixa do rótulo e escolhendo Substituir Palavra no menu pop-up. O editor exibe a caixa **de diálogo Substituir Palavra.** Insira a palavra de substituição e escolha **OK.**

![Captura de tela que mostra a caixa de diálogo 'Substituir Palavra' por 'som' inserida na caixa de texto 'Texto do Word'.](images/f6listrep.gif)

Para caracteres desenvolvidos para uso com o Microsoft Agent, substituir um rótulo de phoneme pode alterar a imagem de boca exibida quando o arquivo de som é reproduzido. Substituir uma palavra substitui o texto que aparece no balão de palavras do caractere quando o [**método Speak**](speak-method.md) é chamado.

Você também pode inserir um novo rótulo de phoneme ou uma palavra fazendo uma seleção na Representação de Áudio e escolhendo Inserir **Phoneme** ou **Inserir Palavra** no **menu** Editar ou clicando com o botão direito do mouse na seleção e escolhendo os comandos no menu pop-up.  Esses comandos ativas caixas de diálogo semelhantes às caixas de diálogo Substituir **Phoneme** e Substituir **Palavra,** exceto que o editor insere a nova palavra ou phoneme em vez de substituir as informações existentes.

Por fim, você pode excluir um phoneme ou uma palavra selecionando seu rótulo e escolhendo **Excluir Phoneme** ou **Excluir Palavra.** Isso remove suas informações linguísticas do arquivo.

 

 




