---
title: Gerando informações linguísticas
description: Gerando informações linguísticas
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23fb99a5139e287e07e353791ce776b8a04dd8d2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104549946"
---
# <a name="generating-linguistic-information"></a>Gerando informações linguísticas

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Depois de gravar um novo arquivo de som ou carregar um arquivo de som existente, você pode gerar informações fonéticas e de quebra de palavras digitando o texto que corresponde ao arquivo de som na caixa **representação de texto** . Em seguida, escolha o comando **gerar informações linguísticas** no menu **Editar** ou na barra de ferramentas. O editor de som exibe uma mensagem de progresso e começa a processar o arquivo de som. Quando termina de gerar informações linguísticas, ele exibe um mapeamento dos rótulos Word e fonema para o arquivo de som em caixas na caixa **representação de áudio** . Observe que o comando **gerar informações linguísticas** permanece desabilitado até que você insira uma representação de texto para o arquivo de som.

![Captura de tela que mostra os painéis ' representação de texto ' e ' representação de áudio ' na ferramenta de edição de som linguístico de informações da Microsoft.](images/f3listlabel.gif)

Se o editor não produzir um conjunto aceitável de rótulos Word ou fonema, escolha o comando **gerar informações linguísticas** novamente. Se o editor não gerar informações linguísticas, verifique sua representação de texto para garantir que todas as palavras sejam corretamente ordenadas e escritas e que você não tenha espaços desnecessários em volta de pontuação. Em seguida, escolha o comando **gerar informações linguísticas** novamente. Você pode editar a representação de texto selecionando texto na caixa de texto **representação de texto** e usando os comandos **recortar**, **copiar** e **colar** no menu **Editar** . Se você não tiver certeza das palavras que o arquivo de som inclui, poderá reproduzir o arquivo de som escolhendo **reproduzir** no menu **Editar** ou na barra de ferramentas do editor. Se o editor ainda não produzir rótulos lingüísticos, tente gravar o arquivo de som novamente. Uma gravação de baixa qualidade, especialmente com ruído excessivo de fundo, provavelmente reduzirá a probabilidade de gerar informações linguísticas razoáveis.

Você também pode criar manualmente suas próprias informações linguísticas selecionando parte da representação de áudio e escolhendo **Inserir fonema** ou **Inserir o Word** no menu **Editar** . Esses comandos também estarão disponíveis se você clicar com o botão direito do mouse dentro da seleção.

Para ver como as informações linguísticas poderiam ser usadas para a animação de caracteres de sincronização de Lip com o Microsoft Agent, escolha o botão **reproduzir** na barra de ferramentas e o editor irá reproduzir o arquivo de som, animando uma imagem de boca de exemplo com base nas informações de rótulo geradas.

Você pode alterar a exibição do rótulo de fonema para mostrar as atribuições de IPA (alfabeto internacional fonético) escolhendo o comando de **exibição do rótulo fonema** no menu **Editar** e, em seguida, o comando IPA. Isso exibe o valor de byte para o fonema. Para alterar de volta para os nomes descritivos, escolha o comando de **exibição do rótulo fonema** novamente e escolha **nome**.

### <a name="playing-a-sound-file"></a>Reproduzindo um arquivo de som

Você pode reproduzir arquivos de som padrão do Windows ou arquivos de som com uma melhoria linguística escolhendo o comando **reproduzir** no menu de **áudio** ou na barra de ferramentas do editor. Os comandos **Pause** e **Stop** permitem que você pause ou pare de reproduzir o arquivo de som. À medida que você executa o arquivo, a imagem de boca de exemplo anima para mostrar como as informações de sincronização de Lip podem ser usadas por um caractere do Microsoft Agent.

Você também pode reproduzir uma parte selecionada de um arquivo de som arrastando uma seleção na **representação de áudio** ou clicando em um rótulo de Word ou fonema e, em seguida, escolhendo **reproduzir**. Você pode estender uma seleção existente pressionando SHIFT e clicando, ou pressionando SHIFT e arrastando para o novo local na **representação de áudio**.

### <a name="editing-linguistic-information"></a>Editando informações linguísticas

Você pode editar as informações linguísticas de um arquivo de várias maneiras. Por exemplo, você pode ajustar um limite de rótulo de palavra ou fonema movendo o ponteiro para a borda da caixa que define o intervalo do rótulo. Quando o ponteiro muda para o ponteiro de movimentação de limite, arraste para a esquerda ou para a direita. O editor ajusta automaticamente o limite de palavra ou fonema adjacente também.

![Captura de tela que mostra edições para as informações linguísticas de um arquivo.](images/f4listadj.gif)

Ajustar o limite de um rótulo de fonema altera o tempo de um fonema quando o áudio é reproduzido. Para os caracteres desenvolvidos para uso com o Microsoft Agent, alterar o limite do rótulo de fonema pode alterar o tempo ou a duração de uma imagem de boca mapeada para esse fonema. Alterar o limite de um rótulo de palavra altera o tempo da aparência da palavra no balão de palavras do caractere.

Você também pode substituir uma atribuição de fonema selecionando o rótulo de fonema e escolhendo **substituir fonema** no menu **Editar** ou clicando com o botão direito do mouse no rótulo fonema e escolhendo **replace fonema** no menu pop-up. O editor exibe a caixa de diálogo **substituir fonema** e realça a atribuição de fonema atual do rótulo. Você pode escolher um fonema de substituição selecionando um na lista **IPA** ou escolhendo outra entrada na lista **nome** . Se mais de uma tradução IPA estiver disponível para esse nome, escolha um item na lista **IPA** . Para inserir uma designação de IPA para um fonema que pode não ser incluído diretamente na linguagem, digite seu valor hex ou vários valores hexadecimais, concatenados com um caractere de adição (+). Depois de selecionar as informações de fonema de substituição, escolha **OK** e o editor substituirá o rótulo de fonema selecionado.

![Captura de tela que mostra a caixa de diálogo ' substituir fonema ', com ' <SIL> ' selecionado como o rótulo descritivo.](images/f5listphone.gif)

Da mesma forma, você pode substituir um rótulo de palavra clicando na caixa do rótulo e escolhendo **substituir palavra** ou clicando com o botão direito do mouse na caixa do rótulo e escolhendo **substituir palavra** no menu pop-up. O editor exibe a caixa de diálogo **substituir palavra** . Insira a palavra substituta e escolha **OK**.

![Captura de tela que mostra a caixa de diálogo ' substituir palavra ' com ' som ' digitado nas caixas de texto ' texto do Word '.](images/f6listrep.gif)

Para os caracteres desenvolvidos para uso com o Microsoft Agent, substituir um rótulo de fonema pode alterar a imagem de boca exibida quando o arquivo de som é reproduzido. Substituir uma palavra substitui o texto que aparece no balão de palavras do caractere quando o método [**Speak**](speak-method.md) é chamado.

Você também pode inserir um novo rótulo ou palavra do fonema fazendo uma seleção na **representação de áudio** e escolhendo **Inserir fonema** ou **inserir palavra** no menu **Editar** ou clicando com o botão direito do mouse na seleção e escolhendo os comandos no menu pop-up. Esses comandos trazem caixas de diálogo semelhantes às caixas de diálogo **replace fonema** e **replace Word** , exceto que o editor insere a nova palavra ou o fonema em vez de substituir as informações existentes.

Por fim, você pode excluir um fonema ou uma palavra selecionando seu rótulo e escolhendo **excluir fonema** ou **excluir o Word**. Isso remove suas informações linguísticas do arquivo.

 

 




