---
title: Instalar e usar editores de método de entrada
description: Este artigo oferece um tutorial sobre como instalar e usar o IME (editor de método de entrada) padrão do Windows.
ms.assetid: 0dc430ce-bed4-8d02-f45e-4eefb0ad0369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6018b3a387a12409f9e46d0392bbd60015af29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756779"
---
# <a name="installing-and-using-input-method-editors"></a>Instalar e usar editores de método de entrada

Este artigo oferece um tutorial sobre como instalar e usar o IME (editor de método de entrada) padrão do Windows.

-   [Instalando um editor de método de entrada](#installing-an-input-method-editor)
-   [IME para chinês simplificado](#simplified-chinese-ime)
-   [IME chinês tradicional](#traditional-chinese-ime)
-   [IME do japonês](#japanese-ime)
-   [IME coreano](#korean-ime)
-   [Requirements](#requirements)

## <a name="installing-an-input-method-editor"></a>Instalando um editor de método de entrada

As seções a seguir descrevem como instalar e usar IMEs (editores de método de entrada) para inserir caracteres complexos em quatro idiomas do leste asiático diferentes. Recursos exclusivos de cada idioma são discutidos.

Para implementar a funcionalidade do IME (editor de método de entrada) em um aplicativo, consulte [usando um editor de método de entrada em um jogo](/windows/desktop/DxTechArts/using-an-input-method-editor-in-a-game).

Por padrão, um IME não é instalado em sistemas do Microsoft Windows XP. Para instalar o, conclua as etapas a seguir.

**Para instalar um IME**

1.  No painel de controle, abra opções regionais e de idioma.
2.  Na guia idiomas, marque a caixa de seleção instalar arquivos para idiomas do leste asiático.

    ![guia idiomas das opções regionais e de idioma](images/ime-1.png)

    Uma caixa de diálogo Instalar suporte ao idioma suplementar é exibida informando os requisitos de armazenamento dos arquivos de idioma.

    ![caixa de diálogo Instalar suporte a idioma suplementar](images/ime-install-lang-dialog.png)

3.  Clique em OK para fechar a caixa de diálogo.
4.  Clique em OK na guia idiomas.
5.  Outra caixa de diálogo é exibida solicitando um disco de instalação do Windows XP ou um local de compartilhamento de rede onde os arquivos de suporte ao idioma estão localizados. Insira um disco do Windows XP Compact ou navegue até o local de rede apropriado e clique em OK. O Microsoft Windows instala os arquivos necessários e solicita que você reinicie o computador.
6.  Clique em Sim para reiniciar o computador.
7.  Após a reinicialização, abra o painel de controle opções regionais e de idiomas novamente.
8.  Na guia idiomas, clique em detalhes. A janela Serviços de texto e idiomas de entrada é exibida.

    ![janela Serviços ext e idiomas de entrada](images/ime-2.png)

9.  Na guia Configurações, clique em Adicionar. A janela Adicionar idioma de entrada é exibida.

    ![Adicionar janela de idioma de entrada](images/ime-3.png)

10. Selecione chinês (Taiwan) para idioma de entrada e Microsoft novo IME fonético 2002a para layout de teclado/IME.
11. Clique em OK. Agora você pode adicionar outros idiomas e IMEs de maneira semelhante.
12. Clique em adicionar novamente, selecione chinês (PRC) para idioma de entrada e chinês (simplificado)-Microsoft Pinyin IME 3,0 para layout de teclado/IME e clique em OK.
13. Clique em adicionar novamente, selecione japonês para idioma de entrada e Microsoft IME Standard 2002 ver. 8,1 para layout do teclado/IME e clique em OK.
14. Clique em adicionar novamente, selecione coreano para idioma de entrada e sistema de entrada coreano (IME 2002) para layout do teclado/IME e clique em OK. Na janela Serviços de texto e idiomas de entrada, a caixa de listagem serviços instalados agora deve conter os quatro IMEs adicionados recentemente.

    ![caixa de listagem de serviços instalados](images/ime-7.png)

15. Clique em OK para fechar a janela Serviços de texto e idiomas de entrada.
16. Clique em OK para fechar o painel de controle opções regionais e de idioma. A barra de tarefas do Windows agora deve conter um indicador de localidade de entrada circulado em vermelho. A existência do indicador significa que mais de um idioma de entrada foi instalado no sistema.

    ![indicador de que significa que mais de um idioma de entrada foi instalado no sistema](images/ime-8.png)

## <a name="simplified-chinese-ime"></a>IME para chinês simplificado

Esta seção descreve como usar o IME do chinês simplificado (PinYin) com o bloco de notas da Microsoft para inserir alguns caracteres chineses.

1.  Inicie o bloco de notas (disponível no botão Iniciar e, em seguida, selecione todos os programas e acessórios). Digite alguns caracteres no bloco de notas. Esses caracteres o ajudarão a visualizar a janela do IME mais tarde.

    ![Captura que mostra caracteres que ajudam a visualizar a janela I M mais tarde para chinês simplificado.](images/ime-sc1.png)

2.  Com o bloco de notas como o aplicativo ativo, clique no indicador de localidade de entrada e selecione chinês (PRC). O indicador exibe alterações em CH para refletir que o novo idioma de entrada é chinês (PRC).

    ![Captura de tela que mostra o indicador de localidade de entrada para selecionar chinês (P R C).](images/ime-sc2.png)

3.  Coloque o cursor no bloco de notas. Pressione HOME no teclado para que o cursor esteja no início da linha. No teclado, digite "N" e, em seguida, "I". A figura a seguir mostra a aparência da exibição. O pequeno retângulo horizontal é a janela de leitura, que exibe a cadeia de caracteres de leitura atual. Atualmente, a cadeia de caracteres de leitura é "Ni" como resultado da digitação de "N" e "I".

    ![Captura de tela que mostra uma cadeia de caracteres de leitura com ' n' e ' i '.](images/ime-sc3.png)

4.  Digite "3". Agora o bloco de notas tem a exibição a seguir. Como N + I + 3 é uma pronúncia completa em Pinyin chinês simplificado, o IME tem informações suficientes para prever o caractere que o usuário pode ter destinado a inserir. A janela de leitura desaparece porque você inseriu uma pronúncia completa. Um caractere é exibido na parte superior do cursor do bloco de notas. Esse caractere não faz parte do bloco de notas, em vez disso, é exibido em outra janela acima do bloco de notas e oculta os caracteres existentes no bloco de notas que estão abaixo. Essa nova janela é chamada de janela de composição, e a cadeia de caracteres nela é chamada de cadeia de caracteres de composição. A cadeia de caracteres de composição é sublinhada na exibição.

    ![Captura de tela que mostra uma janela de composição com uma cadeia de caracteres de composição de um caractere.](images/ime-sc4.png)

5.  Agora, digite "H", "A", "O", "3" para inserir outro caractere. Observe que a janela de leitura aparece quando "H" é digitada e desaparece quando "3" é digitado. Como mostrado abaixo, a cadeia de caracteres de composição agora contém dois caracteres.

    ![Captura de tela que mostra uma janela de composição com uma cadeia de caracteres de composição de dois caracteres.](images/ime-sc5.png)

6.  Pressione a seta para a esquerda no teclado uma vez. O cursor de composição move um caractere para a esquerda, no segundo caractere que você digitou. Uma janela aparece na parte superior do bloco de notas, conforme mostrado abaixo. Essa janela é chamada de janela candidata. Ele exibe uma lista de caracteres ou frases que correspondem à pronúncia que você digitou. Você pode selecionar a palavra desejada nas entradas na lista de candidatos. Neste exemplo, dois caracteres candidatos estão disponíveis com a mesma pronúncia.

    ![dois caracteres candidatos disponíveis com a mesma pronúncia](images/ime-sc6.png)

7.  Digite "2" para selecionar a segunda entrada. A janela candidata agora é fechada e a cadeia de caracteres de composição é atualizada com o caractere selecionado.

    ![Captura de tela que mostra uma cadeia de caracteres de composição atualizada com o caractere selecionado.](images/ime-sc7.png)

8.  Pressione ENTER. Isso informa ao IME que a composição foi concluída e a cadeia de caracteres deve ser enviada ao bloco de notas do aplicativo neste exemplo. A janela composição é fechada e os dois caracteres são enviados ao bloco de notas por meio do WM \_ Char. O sublinhado não existe na figura a seguir porque os dois caracteres mostrados fazem parte do texto no bloco de notas. O texto existente "ABCDEFG" no bloco de notas é movido para a direita porque mais dois caracteres foram inseridos. Agora você inseriu com êxito dois caracteres do chinês simplificado usando um IME.

    ![inserido com êxito dois caracteres do chinês simplificado usando um IME](images/ime-sc8.png)

## <a name="traditional-chinese-ime"></a>IME chinês tradicional

Esta seção descreve como usar o IME do chinês tradicional (novo fonético) com o bloco de notas para inserir alguns caracteres chineses.

1.  Inicie o Bloco de notas. Digite alguns caracteres no bloco de notas. Esses caracteres o ajudarão a visualizar a janela do IME mais tarde.

    ![Captura de tela que mostra caracteres que ajudam a visualizar a janela I M mais adiante para chinês tradicional.](images/ime-tc1.png)

2.  Clique no indicador de localidade de entrada na barra de tarefas do Windows e selecione chinês (Taiwan). O indicador exibe alterações em CH para refletir que o novo idioma de entrada é chinês (Taiwan).

    ![indicador de localidade de entrada para selecionar chinês (Taiwan)](images/ime-tc2.png)

3.  Coloque o cursor no bloco de notas. Pressione HOME no teclado para que o cursor esteja no início da linha. No teclado, digite "S" e, em seguida, "U". A figura a seguir mostra a aparência da exibição. O pequeno retângulo vertical é a janela de leitura, que exibe a cadeia de caracteres de leitura atual. Conforme mostrado na figura a seguir, a cadeia de caracteres de leitura tem dois caracteres como resultado da digitação de "S" e "U".

    ![Captura de tela que mostra uma cadeia de caracteres de leitura com dois caracteres.](images/ime-tc3.png)

4.  Digite "3". Agora o bloco de notas tem a exibição a seguir. Como S + U + 3 é uma pronúncia completa no chinês tradicional, o IME tem informações suficientes para prever o caractere que o usuário pode ter destinado a inserir. A janela de leitura desaparece porque você inseriu uma pronúncia completa. Um caractere é exibido na parte superior do cursor do bloco de notas. Esse caractere não faz parte do bloco de notas, em vez disso, é exibido em outra janela acima do bloco de notas e oculta os caracteres existentes no bloco de notas que estão abaixo. Essa nova janela é chamada de janela de composição, e a cadeia de caracteres nela é chamada de cadeia de caracteres de composição. A cadeia de caracteres de composição é sublinhada na exibição.

    ![Captura de tela que mostra uma janela de composição com uma cadeia de caracteres de composição sublinhada.](images/ime-tc4.png)

5.  Agora, digite "C", "L" e "3" para inserir outro caractere. Observe que a janela de leitura aparece quando "C" é digitado e desaparece quando "3" é digitado. Como mostrado abaixo, a cadeia de caracteres de composição agora contém dois caracteres.

    ![Captura de tela que mostra uma janela de composição com uma cadeia de caracteres de composição e dois caracteres sublinhados.](images/ime-tc5.png)

6.  Digite a seta para baixo no teclado uma vez. Uma janela aparece na parte superior do bloco de notas, conforme mostrado abaixo. Essa janela é chamada de janela candidata. Ele exibe uma lista de caracteres ou frases que correspondem à pronúncia que você digitou. Você pode selecionar a palavra desejada nas entradas na lista de candidatos. Neste exemplo, três caracteres candidatos estão disponíveis com a mesma pronúncia.

    ![três caracteres candidatos disponíveis com a mesma pronúncia](images/ime-tc6.png)

7.  Digite "2" para selecionar a segunda entrada. A janela candidata agora é fechada e a cadeia de caracteres de composição é atualizada com o caractere selecionado.

    ![Captura de tela que mostra uma cadeia de caracteres de composição atualizada com um caractere selecionado.](images/ime-tc7.png)

8.  Pressione ENTER. Isso informa ao IME que a composição foi concluída e a cadeia de caracteres deve ser enviada ao bloco de notas do aplicativo neste exemplo. A janela composição é fechada e os dois caracteres são enviados ao bloco de notas por meio do [**WM \_ Char**](/windows/desktop/inputdev/wm-char). O sublinhado não existe na figura a seguir porque os dois caracteres mostrados fazem parte do texto no bloco de notas. O texto existente "ABCDEFG" no bloco de notas é movido para a direita porque mais dois caracteres foram inseridos. Agora você inseriu com êxito dois caracteres chineses tradicionais usando um IME.

    ![inserido com êxito dois caracteres chineses tradicionais usando um IME](images/ime-tc8.png)

## <a name="japanese-ime"></a>IME do japonês

Esta seção é um passo a passo de como usar o IME do japonês com o bloco de notas para inserir alguns caracteres japoneses.

1.  Inicie o Bloco de notas. Digite alguns caracteres no bloco de notas. Esses caracteres o ajudarão a visualizar a janela do IME mais tarde.

    ![Captura de tela que mostra caracteres que ajudam a visualizar a janela I M mais tarde para japonês.](images/ime-j1.png)

2.  Com o bloco de notas como o aplicativo ativo, clique no indicador de localidade de entrada e selecione japonês. O indicador exibe alterações em JP para refletir que o novo idioma de entrada é japonês.

    ![indicador de localidade de entrada para selecionar japonês](images/ime-j2.png)

3.  Coloque o cursor no bloco de notas. Pressione HOME no teclado para que o cursor esteja no início da linha. No teclado, digite "N" e, em seguida, "I". A figura a seguir mostra a aparência da exibição. Como N + I é uma pronúncia completa em Japonês, o IME tem informações suficientes para prever o caractere que o usuário pode ter destinado a inserir. Um caractere é exibido na parte superior do cursor do bloco de notas. Esse caractere não faz parte do bloco de notas, em vez disso, é exibido em outra janela acima do bloco de notas e oculta os caracteres existentes no bloco de notas que estão abaixo. Essa nova janela é chamada de janela de composição, e a cadeia de caracteres nela é chamada de cadeia de caracteres de composição. A cadeia de caracteres de composição é sublinhada na exibição.

    ![Captura de tela que mostra uma cadeia de caracteres de composição com um caractere japonês sublinhado.](images/ime-j3.png)

4.  Agora, digite "H", "O", "N", "G" e "O" para inserir mais dois caracteres. A cadeia de caracteres de composição agora contém quatro caracteres, como mostrado abaixo.

    ![Captura de tela que mostra uma cadeia de caracteres de composição com quatro caracteres japoneses sublinhados.](images/ime-j4.png)

5.  Pressione a barra de espaço. Isso instrui o IME a converter o texto inserido em cláusulas. Na figura abaixo, o IME converte a pronúncia "Nihongo" em uma cláusula escrita em kanji que significa "idioma japonês".

    ![o IME converte a pronúncia japonesa](images/ime-j5.png)

6.  Pressione a seta para baixo no teclado uma vez. Uma janela aparece na parte superior do bloco de notas, conforme mostrado abaixo. Essa janela é chamada de janela candidata. Ele exibe uma lista de cláusulas que correspondem à pronúncia que você digitou. Você pode selecionar a palavra desejada na lista de candidatos. Neste exemplo, três caracteres candidatos estão disponíveis com a mesma pronúncia. Observe que a segunda entrada é realçada e a cadeia de caracteres de composição é alterada. Isso é causado pela digitação da seta para baixo, que informa ao IME para selecionar a entrada após aquela que foi exibida anteriormente.

    ![Captura de tela que mostra a janela candidata.](images/ime-j6.png)

7.  Digite "2" para selecionar a segunda entrada. A janela candidata agora é fechada e a cadeia de caracteres de composição é atualizada com o caractere selecionado.

    ![Captura de tela que mostra a cadeia de caracteres de composição atualizada com o caractere japonês selecionado.](images/ime-j7.png)

8.  Pressione ENTER. Isso informa ao IME que a composição foi concluída e a cadeia de caracteres deve ser enviada ao bloco de notas do aplicativo neste exemplo. A janela composição é fechada e os dois caracteres são enviados ao bloco de notas por meio do [**WM \_ Char**](/windows/desktop/inputdev/wm-char). O sublinhado não existe na figura a seguir porque os dois caracteres mostrados fazem parte do texto no bloco de notas. O texto existente "ABCDEFG" no bloco de notas é movido para a direita porque mais dois caracteres foram inseridos. Agora você inseriu com êxito alguns caracteres japoneses usando um IME.

    ![alguns caracteres japoneses foram inseridos com êxito usando um IME](images/ime-j8.png)

## <a name="korean-ime"></a>IME coreano

Esta seção descreve como usar o IME coreano com o bloco de notas para inserir alguns caracteres coreanos.

1.  Inicie o Bloco de notas. Digite alguns caracteres no bloco de notas. Esses caracteres o ajudarão a visualizar a janela do IME mais tarde.

    ![caracteres que ajudam a visualizar a janela IME mais tarde](images/ime-k1.png)

2.  Com o bloco de notas como o aplicativo ativo, clique no indicador de localidade de entrada e selecione coreano. O indicador exibe alterações em KO para refletir que o novo idioma de entrada é coreano.

    ![indicador de localidade de entrada para selecionar coreano](images/ime-k2.png)

3.  Coloque o cursor no bloco de notas. Pressione HOME no teclado para que o cursor esteja no início da linha e, em seguida, digite "G". A figura a seguir mostra a aparência da exibição. O elemento fonético correspondente a "G" aparece no bloco de notas e é realçado com um cursor de bloco. Esse caractere realçado é chamado de cadeia de caracteres de composição. Observe que, diferentemente do IME para outros idiomas, a cadeia de caracteres de composição é enviada ao bloco de notas e inserida à esquerda do texto existente assim que o usuário insere um único elemento fonético.

    ![Captura de tela que mostra uma cadeia de caracteres de composição com um caractere inserido à esquerda do texto existente.](images/ime-k3.png)

4.  Neste momento, a cadeia de caracteres de composição consiste em um caractere provisório porque quaisquer elementos fonéticos adicionais inseridos pelo usuário alteram a cadeia de composição em vigor. Agora, digite "K" e "S". Observe que o caractere provisório muda com cada pressionamento de tecla.

    ![Cadeia de caracteres de composição](images/ime-k4.png)

5.  Agora, pressione a tecla CTRL direita. Aparece uma janela candidata que lista os caracteres Hanja que você pode selecionar para a pronúncia inserida, G + K + S.

    ![Captura de tela que mostra uma janela candidata com uma lista de caracteres Hanja que você pode selecionar na parte inferior da janela.](images/ime-k5.png)

6.  Digite o número "1" para selecionar a primeira entrada na lista. A janela candidata é fechada e a cadeia de caracteres de composição é atualizada com o caractere selecionado.

    ![Cadeia de composição atualizada com o caractere selecionado](images/ime-k6.png)

7.  Digite "R", "N" e "R". Em seguida, pressione a tecla CTRL direita para inserir outro caractere.

    ![janela candidata](images/ime-k7.png)

8.  Digite "1" para selecionar a primeira entrada. Agora você inseriu com êxito dois caracteres coreanos usando um IME. Os caracteres coreanos já fazem parte da cadeia de texto no bloco de notas.

    ![inserido com êxito dois caracteres coreanos usando um IME](images/ime-k8.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Sistema operacional**                | Windows XP                                                                                                 |
| **Espaço disponível no disco rígido**       | Pelo menos 230 MB                                                                                            |
| **Locais de arquivo de idioma estrangeiro** | CD de instalação do Windows XP ou local de rede com arquivos de instalação do Windows XP                |
| **Hora**                            | Cerca de dez minutos para instalar arquivos de idioma estrangeiro; cerca de dez minutos cada para examinar quatro IMEs diferentes. |



 

 

 
