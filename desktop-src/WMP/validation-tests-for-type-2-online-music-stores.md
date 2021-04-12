---
title: Testes de validação para armazenamentos online do tipo 2 de integração
description: Este tópico descreve os testes que a Microsoft executará para validar sua loja online do tipo 2. A Microsoft requer que você execute esses testes antes de enviar uma versão Release Candidate. Seu repositório online deve passar com êxito esses testes para serem publicados.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Lojas online do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364051"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Testes de validação para armazenamentos online do tipo 2 de integração

Este tópico descreve os testes que a Microsoft executará para validar sua loja online do tipo 2. A Microsoft requer que você execute esses testes antes de enviar uma versão Release Candidate. Seu repositório online deve passar com êxito esses testes para serem publicados.

> [!Note]  
> Se seu repositório for do tipo 1 em vez de tipo 2, você poderá usar este tópico como uma diretriz para entender o escopo do teste de certificação que é coberto para armazenamentos do tipo 1. Para obter o conjunto completo de testes para repositórios do tipo 1, entre em contato com [suporte da Microsoft](https://support.microsoft.com/ph/7763#tab0).

 

Este tópico inclui as seções a seguir.

-   [Lista de verificação de teste](#test-checklist)
    -   [Preparação de aprovação de teste](#test-pass-preparation)
-   [Ambiente de teste](#test-environment)
-   [Configuração](#configuration-and-setup)
    -   [Configurando um computador de teste](#setting-up-a-test-machine)
    -   [Configurando um repositório](#setting-up-a-store)
    -   [Criando uma conta](#creating-an-account)
    -   [Configurando o cache de credenciais](#setting-up-credential-caching)
-   [Aquisição de conteúdo](#content-acquisition)
    -   [Conteúdo de streaming](#streaming-content)
    -   [Obtendo conteúdo](#obtaining-content)
    -   [Gravando conteúdo](#burning-content)
    -   [Transferindo conteúdo](#transferring-content)
-   [Armazenar recursos](#store-features)
    -   [Gerenciando uma conta](#managing-an-account)
    -   [Gerenciando o centro de informações](#managing-the-info-center)
-   [Interação de armazenamento](#store-interaction)
    -   [Gerando para o repositório ativo](#yielding-to-the-active-store)
    -   [Impedir que o armazenamento testado assuma o armazenamento ativo](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Acessando um repositório no modo de High-Contrast](#accessing-a-store-in-high-contrast-mode)
    -   [Protegendo uma loja](#securing-a-store)

## <a name="test-checklist"></a>Lista de verificação de teste

Use a lista de verificação na tabela a seguir para validar sua loja online do tipo 2 que você deseja colocar no painel.



Teste

Windows XP

Windows Vista

Windows 7

Resultado (aprovado/reprovado/não aplicável)

32

64

32

64

32

64

1. Verifique se o software é instalado.

2. Verifique se o software é desinstalado.

3. Verifique se o software não é executado na bandeja.

4. Verifique se a guia loja Opera.

5. Verifique se o repositório tem uma opção para criar uma nova conta.

6. Verifique se a conta criada pode entrar.

7. Verifique se o repositório tem uma opção para salvar as informações do usuário.

8. Verifique se o cache de credenciais está presente e funcionando.

9. Verifique se as credenciais do usuário são solicitadas se elas não estiverem armazenadas em cache.

10. Verifique se todos os tipos de fluxo de conteúdo disponíveis.

11. Verifique se o conteúdo é reproduzido no Microsoft Windows Media Player.

12. Verifique se um preço calculado está correto.

13. Verifique se o conteúdo comprado foi baixado para a biblioteca.

14. Verifique se os metadados são baixados para a compra.

15. Verifique se os direitos de uso de mídia estão corretos para a compra.

16. Verifique se o conteúdo comprado pode ser executado.

17. Verifique se clicar no botão **comprar** ou **comprar** alterna para o repositório.

18. Verifique se o conteúdo comprado foi baixado.

19. Verifique se o conteúdo comprado pode ser gravado.

20. Verifique se a contagem de gravação foi decrementada.

21. Verifique se o conteúdo pode ser transferido para outro computador.

22. Verifique se o conteúdo é transferido para um dispositivo.

23. Verifique se a contagem de sincronização foi decrementada.

24. Verifique se o histórico de compras acompanha as compras anteriores.

25. Verifique se uma compra anterior pode ser restaurada.

26. Verifique a funcionalidade de um repositório para gerenciar vários computadores.

27. Verifique se o centro de informações está desativado por padrão.

28. Verifique se o centro de informações tem informações de mídia na área de execução.

29. Verifique se os links navegam para a loja.

30. Verifique se o armazenamento testado resulta no repositório ativo.

31. Verifique se o repositório testado não assume o armazenamento atual.

32. Verifique se o repositório está acessível no modo de alto contraste.

33. Verifique se o repositório é seguro.



 

### <a name="test-pass-preparation"></a>Preparação de aprovação de teste

Antes de executar uma aprovação de teste, você deve garantir que a loja e as contas de teste estejam prontas para teste. Você deve determinar as seguintes informações antes que a passagem seja iniciada. Se você puder determinar as informações de alguns dias antes da aprovação do teste, a passagem será executada com mais eficiência.

-   Determine as seguintes informações sobre as contas de teste que são fornecidas pela loja:
    -   Contas e senhas funcionam para permitir que um usuário entre
    -   As contas são financiadas corretamente e adequadamente para cada tipo de modo de negócios que a loja oferece
    -   As contas são válidas para que todas as localidades sejam testadas ou as contas existem para cada localidade se as contas não podem cruzar as localidades
-   Determine quais localidades testar.
-   Determine quais idiomas testar.
-   Determine as seguintes informações sobre o ambiente de teste:

    -   Lojas ao vivo que funcionam com o Windows XP, o Windows Vista e o Windows 7
    -   A loja não dinâmica a ser testada
    -   Verifique se a loja não dinâmica a ser testada está visível em todas as versões do sistema operacional e todas as versões da plataforma Windows Media Player.

-   Determine as seguintes informações sobre a loja a ser testada:

    -   Nome do repositório
    -   Elemento gráfico e rótulo do logotipo da guia de armazenamento esperado
    -   O armazenamento reside para todas as versões do sistema operacional?
    -   Esta é uma nova versão do Store em teste?
    -   O repositório está sendo testado em um armazenamento tipo 1 ou tipo 2?
    -   O tipo de loja foi alterado?

-   Determine em quais versões e plataformas do sistema operacional você planeja testar o armazenamento.
-   Determine se o instalador e o plug-in funcionam em todas as versões de sistema operacional e plataformas a serem testadas.
-   Determine se um documento de navegação é necessário.
-   Determine as seguintes informações sobre a mídia que a loja oferece:

    -   Formatos
    -   Algum software proprietário é necessário?
    -   Você deve testar todos os tipos de mídia ou apenas um subconjunto de tipos de mídia?

-   Determine as seguintes informações sobre os direitos de uso de mídia:

    -   A mídia de armazenamento tem proteção de conteúdo?
    -   Nesse caso, determine o tipo de proteção de conteúdo que a mídia tem.
    -   Nesse caso, determine o comportamento protegido esperado.
    -   Os direitos de uso de mídia incluem compartilhamento de computador para computador?
    -   Os direitos de sincronização
    -   Os direitos de gravação
    -   Os direitos de reprodução
    -   As datas de expiração, se houver

-   Determine se você tem mídia suficiente (um catálogo grande o suficiente) para fornecer um exemplo significativo.
-   Determine qual é a passagem de estágio: RC 0, Compliance e assim por diante.
-   Determine se a aprovação de teste é um tipo específico: regressão, fumaça e assim por diante.

## <a name="test-environment"></a>Ambiente de Teste

Você deve realizar testes nas seguintes configurações:

-   Microsoft Windows Media Player 11 no Windows XP com Service Pack 3 (SP3) 32 bits e sistemas operacionais de 64 bits
-   Sistemas operacionais Windows Media Player 11 no Windows Vista 32 bits e 64 bits (32 bits Windows Media Player)
-   Sistemas operacionais Microsoft Windows Media Player 12 no Windows 7 32-bit e 64-bit (32-bit Windows Media Player)

Embora seja necessário executar testes em todas as versões de sistema operacional e plataformas listadas, as versões de 32 bits do Windows Vista e do Windows 7 são as versões de sistema operacional de prioridade. Você deve testar a instalação de qualquer software em todas as plataformas.

Capturas de tela neste tópico usam um repositório fictício, Proseware, para demonstrar o uso da interface do usuário.

## <a name="configuration-and-setup"></a>Configuração e instalação

As seções a seguir descrevem como configurar e configurar o teste de validação para o on-board a tipo 2 loja online.

### <a name="setting-up-a-test-machine"></a>Configurando um computador de teste

Execute as seguintes etapas para configurar um computador de teste:

1.  Aponte o computador de teste para os servidores de teste de conteúdo adicionando uma chave do Registro específica do repositório.
2.  Defina valores na caixa de diálogo **Opções regionais e de idioma** para as configurações adequadas de idioma e localidade. Para definir o idioma, selecione a guia **formatos** e, em seguida, selecione o idioma na caixa de combinação **formato atual** . Para definir a região, selecione a guia **local** e, em seguida, selecione a região na caixa de combinação **local atual** . Além disso, para lojas que exigem a instalação de um plug-in ou software personalizado específico para armazenamento, talvez seja necessário alterar a localidade do sistema para o idioma da localidade do repositório para facilitar a instalação. O instalador de software deve dar suporte a caracteres de byte único e duplo e deve ser executado em qualquer localidade. Você deve testar na localidade nativa. Para definir a localidade nativa, abra a caixa de diálogo **região e idioma** , selecione a guia **administrativo** e clique no botão **alterar localidade do sistema** , conforme mostrado na captura de tela a seguir. Clicar nesse botão exibe a caixa de diálogo **configurações de região e idioma** . A caixa de combinação de **localidade do sistema atual** nessa caixa de diálogo altera a localidade do sistema.

    As capturas de tela a seguir mostram as guias nas quais você pode definir a região e o idioma:

    ![captura de tela da caixa de diálogo opções regionais e de idiomas](images/reg-lang-opt.png)

    ![captura de tela mostrando como alterar a localidade do sistema atual](images/reg-lang-settings.png)

3.  Desative a exibição do centro de informações de um repositório Configurando o Windows Media Player para reproduzir uma visualização. A principal diferença entre as plataformas é que, no Windows Media Player 11, você começa clicando **agora em execução**, enquanto no Windows Media Player 12, você começa clicando com o botão direito do mouse na janela principal.

    A captura de tela a seguir mostra a sequência de opções de menu que desempenha uma visualização no Windows Media Player 11:

    ![captura de tela mostrando como reproduzir uma visualização no Windows Media Player 11](images/wmp11-visual.png)

    A captura de tela a seguir mostra a sequência de opções de menu que desempenha uma visualização no Windows Media Player 12:

    ![captura de tela mostrando como reproduzir uma visualização no Windows Media Player 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Configurando um repositório

Primeiro, execute as etapas a seguir para configurar um repositório e, em seguida, execute as etapas a seguir as etapas iniciais para verificar a configuração da loja:

1.  Inicie o Windows Media Player e aguarde alguns segundos para adquirir o arquivo de AllServices.xml mais recente.
2.  Para o Windows XP e o Windows Vista, para selecionar uma loja online, primeiro clique na guia que divide entre o modo de exibição de guia de mídia e a exibição de lojas online. Em seguida, no menu, clique em **procurar todas as lojas online** e selecione o repositório clicando em seu ícone na lista de lojas. Para o Windows 7, clique no botão no painel de navegação biblioteca que se divide entre o botão **Guia de mídia** e o botão **lojas online** . Em seguida, no menu, clique em **procurar todas as lojas online** e selecione o repositório clicando em seu ícone na lista de lojas.

    A captura de tela a seguir mostra como selecionar uma loja online no Windows Media Player 11:

    ![captura de tela mostrando como selecionar uma loja online no Windows Media Player 11](images/wmp11-set-store.png)

    A captura de tela a seguir mostra como selecionar uma loja online no Windows Media Player 12:

    ![captura de tela mostrando como selecionar uma loja online no Windows Media Player 12](images/wmp12-set-store.png)

3.  Siga as instruções da loja para instalar qualquer software adicional necessário para usar a loja.

**Para verificar a configuração do repositório**

1.  Verifique se o software é instalado.

    Verifique se o plug-in OCX ou qualquer outro software da loja baixa e instala sem erros.

2.  Verifique se o software é desinstalado.

    Verifique se, no painel de controle, no item **programas e recursos** , o software que a loja instala aparece na lista **desinstalar ou alterar um programa** e verifique se você pode desinstalá-lo dessa lista sem erros.

3.  Verifique se o software não é executado na bandeja do sistema.

    Verifique se nenhum software da loja adiciona ícones à área de notificação do programa (na barra de tarefas à esquerda do relógio) antes do consentimento do cliente para baixar o software do repositório.

    A experiência básica de armazenamento não deve exigir a instalação de software adicional. Uma experiência de mídia básica, como mídia de streaming, deve estar disponível. Alguns armazenamentos instalam software adicional, como gerenciadores de download para uma experiência de mídia Premier; esses armazenamentos podem ter ícones na bandeja do sistema se os ícones representarem aplicativos separados do Windows Media Player.

4.  Verifique se a guia loja Opera.

    Verifique se a guia loja é alterada para indicar o repositório selecionado.

    Para o Windows XP e o Windows Vista com o Windows Media Player 11, verifique se o nome e o ícone da loja estão visíveis em relação ao plano de fundo do Windows Media Player 11 escuro.

    Para o Windows 7 com Windows Media Player 12, verifique se o nome e o ícone da loja estão visíveis no painel de navegação biblioteca, no menu de contexto seletor de serviço.

    Verifique se o repositório está listado na parte superior da lista seletor de repositório no menu.

    > [!Note]  
    > Não haverá a opção **Adicionar serviço atual ao menu** se o repositório do tipo 2 for o repositório em destaque (padrão) para a região.

     

    A captura de tela a seguir mostra o menu que aparece quando você clica na guia no canto superior direito do Windows Media Player 11:

    ![captura de tela mostrando a guia armazenar no Windows Media Player 11](images/wmp11-verify-store.png)

    A captura de tela a seguir mostra o menu que aparece quando você clica no botão dividir no canto inferior esquerdo do Windows Media Player 12:

    ![captura de tela mostrando a guia armazenar no Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Criando uma conta

**Para verificar a configuração da conta**

1.  Verifique se o repositório tem uma opção para criar uma nova conta e siga as instruções da loja para criar uma nova conta.

    A captura de tela a seguir destaca um botão **criar nova conta** , como pode aparecer no Windows Media Player 11:

    ![captura de tela mostrando como verificar a configuração da conta do Windows Media Player 11](images/wmp11-verify-account.png)

    A captura de tela a seguir destaca um botão **criar nova conta** , como pode aparecer no Windows Media Player 12:

    ![captura de tela mostrando como verificar a configuração da conta do Windows Media Player 12](images/wmp12-verify-account.png)

2.  Verifique se você pode entrar na conta que você criou.

### <a name="setting-up-credential-caching"></a>Configurando o cache de credenciais

Primeiro, execute as seguintes etapas para configurar o cache de credenciais e execute as etapas a seguir as etapas iniciais para verificar a configuração de caching de credencial:

1.  Na página de entrada, insira as credenciais e selecione a opção para salvar as informações do usuário.
2.  Verifique se a página de entrada tem uma caixa de seleção que permite ao usuário armazenar em cache as credenciais.
3.  O cache de credenciais opcional é um ponto de segurança importante. O cache automático de credenciais pode expor informações de identificação pessoal de usuários que entram em um computador compartilhado ou público. Você deve proteger as informações do cliente oferecendo uma caixa de seleção que processa o cache opcional.

**Para verificar o cache de credenciais**

1.  Verifique se o repositório tem uma caixa de seleção para uma opção **salvar minhas informações de usuário** .

    1.  Feche o Windows Media Player.
    2.  Reabra o Windows Media Player e tente baixar algum conteúdo.

2.  Verifique se o cache de credenciais está presente e funcionando.

    1.  Saia da loja.
    2.  Feche o Windows Media Player.
    3.  Reabra o Windows Media Player e tente baixar algum conteúdo.

3.  Verifique se as credenciais do usuário são solicitadas se elas não estiverem armazenadas em cache.

    Depois de sair e, em seguida, tentar usar a loja, as credenciais do cliente deverão ser solicitadas.

## <a name="content-acquisition"></a>Aquisição de conteúdo

Esta seção descreve as várias maneiras de adquirir conteúdo e como verificar se o conteúdo foi adquirido.

### <a name="streaming-content"></a>Conteúdo de streaming

Transmita todos os tipos de conteúdo disponíveis do repositório. Por exemplo, transmita o conteúdo de rádio, vídeo, áudio e visualizações.

**Para verificar o conteúdo de streaming**

1.  Verifique se todos os tipos de fluxo de conteúdo disponíveis.

2.  Verifique se o conteúdo é reproduzido no Windows Media Player e não em outro jogador ou controle.

### <a name="obtaining-content"></a>Obtendo conteúdo

Primeiro, execute as etapas a seguir para comprar conteúdo e, em seguida, execute as etapas a seguir as etapas iniciais para verificar a compra e verificar se o conteúdo foi baixado:

1.  Inicie o Windows Media Player.
2.  Entre na conta de teste.
3.  Navegue até o conteúdo a ser comprado.
4.  Siga o procedimento específico do repositório para comprar conteúdo.

**Para verificar o conteúdo adquirido e baixado**

1.  Verifique se o preço calculado está correto.

    Verifique se o preço está correto, especialmente ao comprar várias partes de conteúdo ao mesmo tempo e verifique se as informações de saldo da conta foram atualizadas corretamente após a compra. Alguns conteúdos podem ser comprados como faixas únicas e apenas como álbuns. Verifique se o preço do álbum não é maior do que a soma das faixas individuais.

2.  Verifique se o conteúdo adquirido é baixado para a biblioteca.

    Quando o download for concluído, navegue até o conteúdo baixado na biblioteca do Windows Media Player. O conteúdo baixado está localizado na biblioteca do usuário atual.

    -   Para o Windows XP e o Windows Vista com o Windows Media Player 11, o conteúdo baixado aparece no painel de navegação **da biblioteca, em tabela dinâmica** e, em seguida, em **músicas**.
    -   Para o Windows 7 com Windows Media Player 12, o conteúdo baixado para a biblioteca do Windows Media Player aparece no painel de navegação do Windows Media Player em **música**.

3.  Verifique se os metadados são baixados para a compra.

    Verifique se as colunas a seguir aparecem na biblioteca do Windows Media Player (adicione-as se não):

    -   Artista do álbum
    -   Título
    -   Título do álbum
    -   Provedor de conteúdo
    -   Gênero

    As colunas anteriores devem ser preenchidas. O conteúdo deve ter arte do álbum. No entanto, a arte do álbum não é necessária para passar no teste de validação.

4.  Verifique se os direitos de uso de mídia estão corretos para a compra.

    Para cada trilha baixada, clique com o botão direito do mouse na faixa e selecione **Propriedades** e selecione a guia **direitos de uso de mídia** .

    O repositório pode optar por proteger seu conteúdo com direitos de uso de mídia ou optar por não proteger o conteúdo. A guia **direitos de uso de mídia** reflete esse status listando as restrições ou informando que o conteúdo não está protegido. O repositório deve comunicar seu plano mais atual para direitos de uso de mídia. Você deve verificar os resultados reais em relação a esse comportamento esperado.

    As licenças de direitos de mídia devem ser previamente entregues. O cliente não deve ser solicitado a reproduzir o conteúdo ou passar por algum outro processo para obter a licença. Você deve comparar os direitos de uso de mídia específicos para o que a loja se comunica com o cliente, conforme apropriado. Os direitos devem ser transferíveis para pelo menos dois outros computadores. Os clientes devem ser capazes de gravar e sincronizar suas mídias.

    A captura de tela a seguir mostra os direitos de uso de mídia de um arquivo protegido:

    ![captura de tela mostrando os direitos de uso de mídia para um arquivo protegido](images/media-rights-protected.png)

    Se o conteúdo não estiver protegido, a guia **direitos de uso de mídia** indicará esse fato.

    A captura de tela a seguir mostra os direitos de uso de mídia de um arquivo desprotegido:

    ![captura de tela mostrando os direitos de uso de mídia para um arquivo desprotegido](images/media-rights-not-protected.png)

5.  Verifique se o conteúdo comprado é reproduzido.

    Verifique se o conteúdo baixado é reproduzido no Windows Media Player.

    Reproduzir qualquer conteúdo adquirido da loja e que resida na biblioteca local ou transmitir uma visualização.

    Execute as seguintes etapas para comprar o conteúdo no Windows XP e no Windows Vista com o Windows Media Player 11:

    1.  Clique na guia **executando agora** .
    2.  No painel lista, posicione o ponteiro do mouse para focalizar a arte do álbum para mostrar o link **comprar** .
    3.  Clique em **comprar**.

    A captura de tela a seguir mostra o local do link **comprar** no Windows Media Player 11:

    ![captura de tela mostrando como comprar conteúdo no Windows Media Player 11](images/wmp11-verify-buy-play.png)

    Execute as seguintes etapas para comprar o conteúdo no Windows 7 com o Windows Media Player 12:

    1.  Em modo de biblioteca, clique na guia **reproduzir** .
    2.  Na lista de reprodução, na arte do álbum, clique em **comprar**

    A captura de tela a seguir mostra como comprar conteúdo no Windows Media Player 12:

    ![captura de tela mostrando como comprar conteúdo no Windows Media Player 12](images/wmp12-verify-buy-play.png)

6.  Verifique se clicar em **comprar** ou **comprar** alterna para o repositório.

    O Windows Media Player deve alternar para o repositório na exibição de biblioteca e carregar a experiência de compra da loja.

    Em seguida, você deve continuar a comprar a faixa.

7.  Verifique se, depois de clicar em **comprar** ou **comprar**, o conteúdo é baixado.

    Verifique se os direitos de uso de mídia são apropriados para o conteúdo comprado e seus metadados e verifique se o roteiro é reproduzido. Em geral, esse método de compra deve ter os mesmos resultados que outros métodos.

### <a name="burning-content"></a>Gravando conteúdo

Primeiro, execute as seguintes etapas para gravar o conteúdo adquirido (copiar conteúdo adquirido em um CD ou DVD gravável) e, em seguida, execute as etapas que seguem as etapas iniciais para verificar se o conteúdo grava:

> [!Note]  
> Antes de gravar uma faixa adquirida, anote sua contagem de gravação para que você possa verificar se a contagem diminui depois de gravar a faixa.

 

1.  Clique na guia **gravar**
2.  Arraste as faixas adquiridas para a **lista de gravação**.
3.  Clique no botão **Iniciar gravação** .

A captura de tela a seguir mostra a **lista de gravação** no lado direito da tela e o botão **Iniciar gravação** abaixo da **lista de gravação** no Windows Media Player 11:

![captura de tela mostrando como gravar conteúdo no Windows Media Player 11](images/wmp11-verify-burn.png)

A captura de tela a seguir mostra como a lista de gravação aparece no Windows Media Player 12 depois que você arrasta uma faixa para a lista de gravação e mostra o botão **Iniciar gravação** na parte superior da guia **gravar** :

![captura de tela mostrando como gravar conteúdo no Windows Media Player 12](images/wmp12-verify-burn.png)

**Para verificar se o conteúdo comprado pode ser gravado**

1.  Verifique se o conteúdo comprado é gravado reproduzindo o CD ou DVD após a gravação ser concluída.

2.  Verifique se a contagem de gravação foi decrementada.

    Navegue até a biblioteca e abra os direitos de uso de mídia para um roteiro comprado que foi gravado.

    Se o número de vezes que um controle pode ser gravado for limitado, verifique se esse número diminui depois que a faixa é gravada.

### <a name="transferring-content"></a>Transferindo conteúdo

Transferir conteúdo para outro computador.

**Para verificar se o conteúdo comprado pode ser transferido para outro computador**

-   Se o repositório permitir a transferência de conteúdo para outro computador, transfira o conteúdo para pelo menos dois computadores.

Primeiro execute as seguintes etapas para sincronizar um dispositivo e transferir o conteúdo adquirido para esse dispositivo e, em seguida, execute as etapas a seguir as etapas iniciais para verificar se o conteúdo foi transferido:

> [!Note]  
> Antes de transferir uma faixa adquirida, anote sua contagem de sincronização para que você possa verificar se a contagem diminui depois de transferir a faixa.

 

1.  Conecte um dispositivo com um relógio seguro. Os exemplos incluem dispositivos que usam o DRM do Windows Media para dispositivos portáteis, como um Media Center portátil como o iRiver H10, o Zen criativo e assim por diante.
2.  No Windows Media Player, clique na guia **sincronizar** .
3.  Arraste conteúdo da biblioteca para a área de **lista de sincronização** na guia **sincronizar** .
4.  Clique no botão **Iniciar sincronização** .

A captura de tela a seguir mostra o Track 1 na área de **lista de sincronização** e mostra o botão **Iniciar sincronização** no Windows Media Player 11:

![captura de tela mostrando como transferir conteúdo no Windows Media Player 11](images/wmp11-verify-transfer.png)

A captura de tela a seguir mostra o Track 1 na área de **lista de sincronização** e mostra o botão **Iniciar sincronização** no Windows Media Player 12:

![captura de tela mostrando como transferir conteúdo no Windows Media Player 12](images/wmp12-verify-transfer.png)

**Para verificar se o conteúdo comprado pode ser transferido para outro dispositivo**

1.  Verifique se o conteúdo comprado é transferido para o dispositivo executando o conteúdo no dispositivo. O conteúdo transferido também deve ter metadados apropriados.

2.  Verifique se a contagem de sincronização foi decrementada.

    Navegue até a biblioteca e abra os direitos de uso de mídia para uma faixa transferida.

    Se o número de vezes que uma faixa pode sincronizar é limitado, verifique se esse número diminui quando a faixa é transferida.

## <a name="store-features"></a>Armazenar recursos

As seções a seguir descrevem como testar vários recursos de uma loja online integrada.

### <a name="managing-an-account"></a>Gerenciando uma conta

Entre com uma conta que tenha feito algumas compras e abra o histórico de compra.

**Para verificar o histórico de compra**

-   Verifique se o histórico de compras acompanha as compras anteriores.

Se o tipo de conta ou armazenamento der suporte a esse recurso, tente restaurar uma compra excluída.

**Para verificar se as compras anteriores podem ser readquiridas**

-   Verifique se uma compra anterior pode ser restaurada.

Se o armazenamento oferecer suporte ao uso de vários computadores com a conta, verifique todas as funcionalidades fornecidas por esse recurso.

**Para verificar o gerenciamento de vários computadores com uma única conta**

-   Verifique a funcionalidade do repositório para gerenciar vários computadores.

### <a name="managing-a-store-specific-account"></a>Gerenciando uma conta de Store-Specific

O repositório pode não ter tipos de conta, restrições ou conteúdo típicos. Por exemplo, uma loja que aluga o vídeo de streaming precisaria de alguma interface do usuário para exibir locações ativas e essa interface do usuário precisaria ser testada.

> [!Note]  
> Embora a Microsoft não possa certificar a funcionalidade de conta específica da loja, para garantir uma boa experiência do cliente, você deve testar essa funcionalidade.

 

### <a name="managing-the-info-center"></a>Gerenciando o centro de informações

Primeiro, execute as seguintes etapas para se preparar para testar o estado padrão e, em seguida, execute a próxima etapa que segue as etapas iniciais para verificar se o centro de informações está desativado por padrão:

1.  Reproduzir algum conteúdo da loja.
2.  Alterne para o modo de agora em execução. No Windows XP ou no Windows Vista com Windows Media Player 11, clique na guia **executando agora** . No Windows 7 com Windows Media Player 12, clique no botão **alternar para agora** no canto inferior direito.

**Para verificar se o centro de informações está desativado por padrão**

-   Verifique se o centro de informações está desativado por padrão.

Se a loja oferece uma exibição do centro de informações, jogue algum conteúdo da loja e, enquanto o conteúdo está em execução, alterne para o modo de execução e ative o centro de informações.

No Windows XP ou Windows Vista com Windows Media Player 11, clique com o botão direito do mouse na janela agora em execução e, no menu de contexto, selecione **exibição do centro de informações**.

A captura de tela a seguir mostra o menu de contexto no Windows Media Player 11:

![captura de tela mostrando como acessar o centro de informações de um repositório no Windows Media Player 11](images/wmp11-info-center.png)

No Windows 7 com Windows Media Player 12, clique com o botão direito do mouse na janela agora em execução, no menu de contexto, selecione **visualizações** e clique em **exibição do centro de informações**.

A captura de tela a seguir mostra o menu de contexto no Windows Media Player 12:

![captura de tela mostrando como acessar o centro de informações de um repositório no Windows Media Player 12](images/wmp12-info-center.png)

**Para verificar se o centro de informações está funcional**

-   Verifique se o centro de informações mostra informações de mídia na área de execução. A captura de tela a seguir mostra um exemplo dessas informações de mídia:

    ![captura de tela mostrando a funcionalidade do centro de informações de um repositório](images/media-information.png)

Se quaisquer links de compra ou outros links aparecerem na página, clique nos links.

**Para verificar os links na exibição do centro de informações**

-   Verifique se os links mostram o repositório.

    O Windows Media Player deve mudar para o repositório em sua biblioteca.

## <a name="store-interaction"></a>Interação de armazenamento

As seções a seguir descrevem como testar a interação entre as outras lojas e a loja que você está testando.

### <a name="yielding-to-the-active-store"></a>Gerando para o repositório ativo

Alternar para um repositório diferente do armazenamento que está sendo testado.

**Para verificar a concessão para o repositório ativo**

-   Verifique se o armazenamento testado resulta no repositório ativo.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Impedir que o armazenamento testado assuma o armazenamento ativo

-   Com outra loja selecionada, feche o Windows Media Player e reinicie o computador.
-   Inicie o Windows Media Player.

**Para verificar se o armazenamento testado não assume**

-   Verifique se o repositório ativo mais recentemente aparece e se o repositório testado não aparece.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Acessando um repositório no modo de High-Contrast

Primeiro, habilite o modo de alto contraste pressionando SHIFT esquerda + ALT esquerda + PRINT SCREEN e, em seguida, execute as seguintes etapas para verificar a acessibilidade de alto contraste:

**Para verificar se o repositório está acessível no modo de alto contraste**

1.  Verifique se a interface do usuário de logon está intacta e funcional.
2.  Verifique se todas as janelas e caixas de diálogo aparecem corretamente.
3.  Mídia de compra. Verifique se os botões de compra e download, os gerentes de download, as informações de preço e assim por diante estão visíveis.
4.  Verifique se você pode transmitir, gravar e sincronizar.
5.  Procure por texto recortado e elementos da interface do usuário, texto que não seja legível e outros defeitos visíveis.

### <a name="securing-a-store"></a>Protegendo uma loja

Execute as seguintes etapas para verificar a segurança da conta:

**Para verificar a segurança da conta**

1.  Insira informações de conta malformadas na página de logon e na caixa de diálogo e verifique se a loja a rejeita.
2.  Entre, exiba a página da conta e saia.
3.  Clique no botão voltar no Windows Media Player e verifique se você não vê as informações da conta de usuário anterior.

 

 




