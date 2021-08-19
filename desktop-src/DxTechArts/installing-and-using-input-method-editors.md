---
title: Instalar e usar editores de método de entrada
description: este artigo oferece um tutorial sobre como instalar e usar o IME (Editor de método de entrada) Windows padrão.
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45a0da52d0e917186831de8c84f39ecee3d2583ac4a267fa2501c643e2f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153361"
---
# <a name="installing-and-using-input-method-editors"></a>Instalar e usar editores de método de entrada

este artigo oferece um tutorial sobre como instalar e usar o IME (Editor de método de entrada) Windows padrão.

-   [Instalando um editor de método de entrada](#installing-an-input-method-editor)
-   [IME para chinês simplificado](#simplified-chinese-ime)
-   [IME chinês tradicional](#traditional-chinese-ime)
-   [IME do japonês](#japanese-ime)
-   [IME coreano](#korean-ime)
-   [Requirements](#requirements)

## <a name="installing-an-input-method-editor"></a>Instalando um editor de método de entrada

As seções a seguir descrevem como instalar e usar IMEs (editores de método de entrada) para inserir caracteres complexos em quatro idiomas do leste asiático diferentes. Recursos exclusivos de cada idioma são discutidos.

Para implementar a funcionalidade do IME (editor de método de entrada) em um aplicativo, consulte [usando um editor de método de entrada em um jogo](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game).

por padrão, um IME não é instalado em sistemas Microsoft Windows XP. Para instalar o, conclua as etapas a seguir.

**Para instalar um IME**

1.  No painel de controle, abra opções regionais e de idioma.
2.  Na guia idiomas, marque a caixa de seleção instalar arquivos para idiomas do leste asiático.

    ![guia idiomas das opções regionais e de idioma](images/ime-1.png)

    Uma caixa de diálogo Instalar suporte ao idioma suplementar é exibida informando os requisitos de armazenamento dos arquivos de idioma.

    ![caixa de diálogo Instalar suporte a idioma suplementar](images/ime-install-lang-dialog.png)

3.  Clique em OK para fechar a caixa de diálogo.
4.  Clique em OK na guia idiomas.
5.  outra caixa de diálogo é exibida solicitando um disco de instalação Windows XP ou local de compartilhamento de rede onde os arquivos de suporte de idioma estão localizados. insira um disco Windows XP compact ou navegue até o local de rede apropriado e clique em OK. o Microsoft Windows instala os arquivos necessários e solicita que você reinicie o computador.
6.  Clique em Sim para reiniciar o computador.
7.  Após a reinicialização, abra o painel de controle opções regionais e de idiomas novamente.
8.  Na guia idiomas, clique em detalhes. A janela Serviços de texto e idiomas de entrada é exibida.

    ![janela Serviços ext e idiomas de entrada](images/ime-2.png)

9.  na guia Configurações, clique em adicionar. A janela Adicionar idioma de entrada é exibida.

    ![Adicionar janela de idioma de entrada](images/ime-3.png)

10. Selecione chinês (Taiwan) para idioma de entrada e Microsoft novo IME fonético 2002a para layout de teclado/IME.
11. Clique em OK. Agora você pode adicionar outros idiomas e IMEs de maneira semelhante.
12. Clique em adicionar novamente, selecione chinês (PRC) para idioma de entrada e chinês (simplificado)-Microsoft Pinyin IME 3,0 para layout de teclado/IME e clique em OK.
13. Clique em adicionar novamente, selecione japonês para idioma de entrada e Microsoft IME Standard 2002 ver. 8,1 para layout do teclado/IME e clique em OK.
14. Clique em adicionar novamente, selecione coreano para idioma de entrada e sistema de entrada coreano (IME 2002) para layout do teclado/IME e clique em OK. Na janela Serviços de texto e idiomas de entrada, a caixa de listagem serviços instalados agora deve conter os quatro IMEs adicionados recentemente.

    ![caixa de listagem de serviços instalados](images/ime-7.png)

15. Clique em OK para fechar a janela Serviços de texto e idiomas de entrada.
16. Clique em OK para fechar o painel de controle opções regionais e de idioma. a barra de tarefas Windows agora deve conter um indicador de localidade de entrada circulado em vermelho. A existência do indicador significa que mais de um idioma de entrada foi instalado no sistema.

    ![indicador de que significa que mais de um idioma de entrada foi instalado no sistema](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>IME para chinês simplificado

esta seção descreve como usar o IME do chinês simplificado (PinYin) com o Microsoft Bloco de notas para inserir alguns caracteres chineses.

1.  inicie o Bloco de notas (disponível no botão iniciar e, em seguida, selecione todos os programas e acessórios). digite alguns caracteres em Bloco de notas. Esses caracteres o ajudarão a visualizar a janela do IME mais tarde.

    ![Captura que mostra caracteres que ajudam a visualizar a janela I M mais tarde para chinês simplificado.](images/ime-sc1.png)

2.  com Bloco de notas como o aplicativo ativo, clique no indicador de localidade de entrada e selecione chinês (PRC). O indicador exibe alterações em CH para refletir que o novo idioma de entrada é chinês (PRC).

    ![Captura de tela que mostra o indicador de localidade de entrada para selecionar chinês (P R C).](images/ime-sc2.png)

3.  coloque o cursor em Bloco de notas. Pressione HOME no teclado para que o cursor esteja no início da linha. No teclado, digite "N" e, em seguida, "I". A figura a seguir mostra a aparência da exibição. O pequeno retângulo horizontal é a janela de leitura, que exibe a cadeia de caracteres de leitura atual. Atualmente, a cadeia de caracteres de leitura é "Ni" como resultado da digitação de "N" e "I".

    ![Captura de tela que mostra uma cadeia de caracteres de leitura com ' n' e ' i '.](images/ime-sc3.png)

4.  Digite "3". agora Bloco de notas tem a exibição a seguir. Como N + I + 3 é uma pronúncia completa em Pinyin chinês simplificado, o IME tem informações suficientes para prever o caractere que o usuário pode ter destinado a inserir. A janela de leitura desaparece porque você inseriu uma pronúncia completa. um caractere é exibido na parte superior do cursor de Bloco de notas. esse caractere não faz parte de Bloco de notas, em vez disso, é exibido em outra janela sobre Bloco de notas e oculta os caracteres existentes no Bloco de notas que estão abaixo. Essa nova janela é chamada de janela de composição, e a cadeia de caracteres nela é chamada de cadeia de caracteres de composição. A cadeia de caracteres de composição é sublinhada na exibição.

    ![Captura de tela que mostra uma janela de composição com uma cadeia de caracteres de composição de um caractere.](images/ime-sc4.png)

5.  Agora, digite "H", "A", "O", "3" para inserir outro caractere. Observe que a janela de leitura aparece quando "H" é digitada e desaparece quando "3" é digitado. Como mostrado abaixo, a cadeia de caracteres de composição agora contém dois caracteres.

    ![Captura de tela que mostra uma janela de composição com uma cadeia de caracteres de composição de dois caracteres.](images/ime-sc5.png)

6.  Pressione a seta para a esquerda no teclado uma vez. O cursor de composição move um caractere para a esquerda, no segundo caractere que você digitou. uma janela aparece na parte superior de Bloco de notas, conforme mostrado abaixo. Essa janela é chamada de janela candidata. Ele exibe uma lista de caracteres ou frases que correspondem à pronúncia que você digitou. Você pode selecionar a palavra desejada nas entradas na lista de candidatos. Neste exemplo, dois caracteres candidatos estão disponíveis com a mesma pronúncia.

    ![dois caracteres candidatos disponíveis com a mesma pronúncia](images/ime-sc6.png)

7.  Digite "2" para selecionar a segunda entrada. A janela candidata agora é fechada e a cadeia de caracteres de composição é atualizada com o caractere selecionado.

    ![Captura de tela que mostra uma cadeia de caracteres de composição atualizada com o caractere selecionado.](images/ime-sc7.png)

8.  Pressione ENTER. isso informa ao IME que a composição está concluída e que a cadeia de caracteres deve ser enviada ao Bloco de notas do aplicativo neste exemplo. a janela composição é fechada e os dois caracteres são enviados para Bloco de notas por meio do WM \_ CHAR. o sublinhado não existe na figura a seguir porque os dois caracteres mostrados fazem parte do texto em Bloco de notas. o texto existente "ABCDEFG" em Bloco de notas é movido para a direita porque mais dois caracteres foram inseridos. Agora você inseriu com êxito dois caracteres do chinês simplificado usando um IME.

    ![inserido com êxito dois caracteres do chinês simplificado usando um IME](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>IME chinês tradicional

esta seção descreve como usar o IME do chinês tradicional (novo fonético) com Bloco de notas para inserir alguns caracteres chineses.

1.  Inicie o Bloco de notas. digite alguns caracteres em Bloco de notas. Esses caracteres ajudarão você a visualizar melhor a janela do IME mais tarde.

    ![Captura de tela que mostra os caracteres que ajudam a visualizar melhor a janela de E/S mais tarde para chinês tradicional.](images/ime-tc1.png)

2.  Clique no indicador de localidade de entrada na barra Windows tarefas e selecione Chinês (Taiwan). O indicador exibe alterações no CH para refletir que o novo idioma de entrada é chinês (Taiwan).

    ![indicador de localidade de entrada para selecionar chinês (taiwan)](images/ime-tc2.png)

3.  Coloque o cursor em Bloco de notas. Pressione HOME no teclado para que o cursor seja no início da linha. No teclado, digite "S", em seguida, "U". A figura a seguir mostra a aparência da exibição. O retângulo vertical pequeno é a janela de leitura, que exibe a cadeia de caracteres de leitura atual. Conforme mostrado na figura a seguir, a cadeia de caracteres de leitura tem dois caracteres como resultado da digitação de "S" e "U".

    ![Captura de tela que mostra uma cadeia de caracteres de leitura com dois caracteres.](images/ime-tc3.png)

4.  Digite "3". Agora Bloco de notas tem a exibição a seguir. Como S+U+3 é uma pronúncia completa em chinês tradicional, o IME tem informações suficientes para prever o caractere que o usuário pode ter pretendido inserir. A janela de leitura desaparece porque você entrou em uma pronúncia completa. Um caractere é exibido na parte superior Bloco de notas cursor. Esse caractere não faz parte do Bloco de notas, em vez disso, é exibido em outra janela sobre Bloco de notas e oculta os caracteres existentes Bloco de notas que estão abaixo. Essa nova janela é chamada de janela de composição e a cadeia de caracteres é chamada de cadeia de caracteres de composição. A cadeia de caracteres de composição é sublinhada na exibição.

    ![Captura de tela que mostra uma janela de composição com uma cadeia de caracteres de composição sublinhada.](images/ime-tc4.png)

5.  Agora digite "C", "L" e "3" para inserir outro caractere. Observe que a janela de leitura aparece quando "C" é digitado e desaparece quando "3" é digitado. Conforme mostrado abaixo, a cadeia de caracteres de composição agora contém dois caracteres.

    ![Captura de tela que mostra uma janela de composição com uma cadeia de caracteres de composição e dois caracteres sublinhados.](images/ime-tc5.png)

6.  Digite a seta para baixo no teclado uma vez. Uma janela é exibida na parte superior Bloco de notas conforme mostrado abaixo. Essa janela é chamada de janela candidata. Ele exibe uma lista de caracteres ou frases que corresponderem à pronúncia que você digitou. Você pode selecionar a palavra pretendido nas entradas na lista de candidatos. Neste exemplo, três caracteres candidatos estão disponíveis com a mesma pronúncia.

    ![três caracteres candidatos disponíveis com a mesma pronúncia](images/ime-tc6.png)

7.  Digite "2" para selecionar a segunda entrada. A janela candidata agora é fechada e a cadeia de caracteres de composição é atualizada com o caractere selecionado.

    ![Captura de tela que mostra uma cadeia de caracteres de composição atualizada com um caractere selecionado.](images/ime-tc7.png)

8.  Pressione ENTER. Isso informa ao IME que a composição está concluída e que a cadeia de caracteres deve ser enviada ao aplicativo – Bloco de notas neste exemplo. A janela de composição é fechada e os dois caracteres são enviados para Bloco de notas por meio [**do WM \_ CHAR.**](/windows/desktop/inputdev/wm-char) O sublinhado foi embora na figura a seguir porque os dois caracteres mostrados fazem parte do texto em Bloco de notas. O texto existente "ABCDEFG" no Bloco de notas é movido para a direita porque mais dois caracteres foram inseridos. Agora você entrou com êxito dois caracteres chineses tradicionais usando um IME.

    ![entrou com êxito dois caracteres chineses tradicionais usando um ime](images/ime-tc8.png)

## <a name="japanese-ime"></a>IME japonês

Esta seção é um passo a passo do uso do IME japonês com Bloco de notas inserir alguns caracteres em japonês.

1.  Inicie o Bloco de notas. Digite alguns caracteres em Bloco de notas. Esses caracteres ajudarão você a visualizar melhor a janela do IME mais tarde.

    ![Captura de tela que mostra os caracteres que ajudam a visualizar melhor a janela de E/S mais tarde para japonês.](images/ime-j1.png)

2.  Com Bloco de notas como o aplicativo ativo, clique no indicador de localidade de entrada e selecione Japonês. O indicador exibe alterações no JP para refletir que o novo idioma de entrada é japonês.

    ![indicador de localidade de entrada para selecionar japonês](images/ime-j2.png)

3.  Coloque o cursor em Bloco de notas. Pressione HOME no teclado para que o cursor seja no início da linha. No teclado, digite "N", em seguida, "I". A figura a seguir mostra a aparência da exibição. Como N+I é uma pronúncia completa em japonês, o IME tem informações suficientes para prever o caractere que o usuário pode ter pretendido inserir. Um caractere é exibido na parte superior Bloco de notas cursor. Esse caractere não faz parte do Bloco de notas, em vez disso, é exibido em outra janela sobre Bloco de notas e oculta os caracteres existentes Bloco de notas que estão abaixo. Essa nova janela é chamada de janela de composição e a cadeia de caracteres é chamada de cadeia de caracteres de composição. A cadeia de caracteres de composição é sublinhada na exibição.

    ![Captura de tela que mostra uma cadeia de caracteres de composição com um caractere japonês sublinhado.](images/ime-j3.png)

4.  Agora digite "H", "O", "N", "G" e "O" para inserir mais dois caracteres. A cadeia de caracteres de composição agora contém quatro caracteres, conforme mostrado abaixo.

    ![Captura de tela que mostra uma cadeia de caracteres de composição com quatro caracteres em japonês sublinhados.](images/ime-j4.png)

5.  Pressione a Barra de Espaços. Isso instrui o IME a converter o texto inserido em cláusulas. Na figura abaixo, o IME converte a pronúncia "Nihongo" em uma cláusula escrita em Kanji que significa "Idioma japonês".

    ![ime converte a pronúncia do japonês](images/ime-j5.png)

6.  Pressione a seta para baixo no teclado uma vez. Uma janela é exibida na parte superior Bloco de notas conforme mostrado abaixo. Essa janela é chamada de janela candidata. Ele exibe uma lista de cláusulas que corresponderem à pronúncia que você digitou. Você pode selecionar a palavra pretendido na lista de candidatos. Neste exemplo, três caracteres candidatos estão disponíveis com a mesma pronúncia. Observe que a segunda entrada está realçada e a cadeia de caracteres de composição muda. Isso é causado pela digitação da seta para baixo, que informa ao IME para selecionar a entrada após aquela que foi exibida anteriormente.

    ![Captura de tela que mostra a janela candidata.](images/ime-j6.png)

7.  Digite "2" para selecionar a segunda entrada. A janela candidata agora é fechada e a cadeia de caracteres de composição é atualizada com o caractere selecionado.

    ![Captura de tela que mostra a cadeia de caracteres de composição atualizada com o caractere japonês selecionado.](images/ime-j7.png)

8.  Pressione ENTER. Isso informa ao IME que a composição está concluída e que a cadeia de caracteres deve ser enviada ao aplicativo – Bloco de notas neste exemplo. A janela de composição é fechada e os dois caracteres são enviados para Bloco de notas por meio [**do WM \_ CHAR.**](/windows/desktop/inputdev/wm-char) O sublinhado foi embora na figura a seguir porque os dois caracteres mostrados fazem parte do texto em Bloco de notas. O texto existente "ABCDEFG" no Bloco de notas é movido para a direita porque mais dois caracteres foram inseridos. Agora você entrou com êxito alguns caracteres em japonês usando um IME.

    ![entrou com êxito alguns caracteres em japonês usando um ime](images/ime-j8.png)

## <a name="korean-ime"></a>IME coreano

Esta seção descreve como usar o IME coreano com Bloco de notas inserir alguns caracteres coreanos.

1.  Inicie o Bloco de notas. Digite alguns caracteres em Bloco de notas. Esses caracteres ajudarão você a visualizar melhor a janela do IME mais tarde.

    ![caracteres que ajudam a visualizar melhor a janela do ime mais tarde](images/ime-k1.png)

2.  Com Bloco de notas como o aplicativo ativo, clique no indicador de localidade de entrada e selecione Coreano. O indicador exibe alterações no KO para refletir que o novo idioma de entrada é coreano.

    ![indicador de localidade de entrada para selecionar coreano](images/ime-k2.png)

3.  Coloque o cursor em Bloco de notas. Pressione HOME no teclado para que o cursor seja no início da linha e digite "G". A figura a seguir mostra a aparência da exibição. O elemento phonetic correspondente a "G" aparece Bloco de notas e é realçada com um cursor de bloco. Esse caractere realçado é chamado de cadeia de caracteres de composição. observe que, diferentemente do IME para outros idiomas, a cadeia de caracteres de composição é enviada para Bloco de notas e inserida à esquerda do texto existente assim que o usuário insere um único elemento fonético.

    ![Captura de tela que mostra uma cadeia de caracteres de composição com um caractere inserido à esquerda do texto existente.](images/ime-k3.png)

4.  Neste momento, a cadeia de caracteres de composição consiste em um caractere provisório porque quaisquer elementos fonéticos adicionais inseridos pelo usuário alteram a cadeia de composição em vigor. Agora, digite "K" e "S". Observe que o caractere provisório muda com cada pressionamento de tecla.

    ![Cadeia de caracteres de composição](images/ime-k4.png)

5.  Agora, pressione a tecla CTRL direita. Aparece uma janela candidata que lista os caracteres Hanja que você pode selecionar para a pronúncia inserida, G + K + S.

    ![Captura de tela que mostra uma janela candidata com uma lista de caracteres Hanja que você pode selecionar na parte inferior da janela.](images/ime-k5.png)

6.  Digite o número "1" para selecionar a primeira entrada na lista. A janela candidata é fechada e a cadeia de caracteres de composição é atualizada com o caractere selecionado.

    ![Cadeia de composição atualizada com o caractere selecionado](images/ime-k6.png)

7.  Digite "R", "N" e "R". Em seguida, pressione a tecla CTRL direita para inserir outro caractere.

    ![janela candidata](images/ime-k7.png)

8.  Digite "1" para selecionar a primeira entrada. Agora você inseriu com êxito dois caracteres coreanos usando um IME. os caracteres coreanos já fazem parte da cadeia de caracteres de texto em Bloco de notas.

    ![inserido com êxito dois caracteres coreanos usando um IME](images/ime-k8.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Sistema operacional**                | Windows XP                                                                                                 |
| **Espaço disponível no disco rígido**       | Pelo menos 230 MB                                                                                            |
| **Locais de arquivo de idioma estrangeiro** | Windows cd de instalação do XP ou local de rede com arquivos de instalação do Windows XP                |
| **Hora**                            | Cerca de dez minutos para instalar arquivos de idioma estrangeiro; cerca de dez minutos cada para examinar quatro IMEs diferentes. |



 

 

 
