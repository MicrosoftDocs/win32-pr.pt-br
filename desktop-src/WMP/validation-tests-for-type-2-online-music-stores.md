---
title: Testes de validação para lojas online do tipo 2 de entrada
description: Este tópico descreve os testes que a Microsoft executará para validar sua loja online do Tipo 2. A Microsoft exige que você execute esses testes antes de enviar um candidato à versão. Sua loja online deve passar com êxito nesses testes para serem publicados.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player Lojas Online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2cb1b4d44b1bd3c6289311c6b276de7c75ed1bcd955431796a36d272811942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901238"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Testes de validação para lojas online do tipo 2 de entrada

Este tópico descreve os testes que a Microsoft executará para validar sua loja online do Tipo 2. A Microsoft exige que você execute esses testes antes de enviar um candidato à versão. Sua loja online deve passar com êxito nesses testes para serem publicados.

> [!Note]  
> Se o seu armazenamento for o Tipo 1 em vez do Tipo 2, você poderá usar este tópico como uma diretriz para entender o escopo do teste de certificação coberto para lojas do Tipo 1. Para o conjunto completo de testes para lojas do Tipo 1, entre em contato [com Suporte da Microsoft](https://support.microsoft.com/ph/7763#tab0).

 

Este tópico inclui as seções a seguir.

-   [Lista de verificação de teste](#test-checklist)
    -   [Preparação de passagem de teste](#test-pass-preparation)
-   [Ambiente de teste](#test-environment)
-   [Configuração](#configuration-and-setup)
    -   [Configurando um computador de teste](#setting-up-a-test-machine)
    -   [Configurando um armazenamento](#setting-up-a-store)
    -   [Criando uma conta](#creating-an-account)
    -   [Configurando a credencial Caching](#setting-up-credential-caching)
-   [Aquisição de conteúdo](#content-acquisition)
    -   [Conteúdo de streaming](#streaming-content)
    -   [Obtendo conteúdo](#obtaining-content)
    -   [Conteúdo de gravação](#burning-content)
    -   [Transferindo conteúdo](#transferring-content)
-   [Recursos da Loja](#store-features)
    -   [Gerenciando uma conta](#managing-an-account)
    -   [Gerenciando o Centro de Informações](#managing-the-info-center)
-   [Interação com o armazenamento](#store-interaction)
    -   [Ing to the Active Store](#yielding-to-the-active-store)
    -   [Impedindo que o armazenamento testado assumia o armazenamento ativo](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Acessando um armazenamento no modo High-Contrast armazenamento](#accessing-a-store-in-high-contrast-mode)
    -   [Proteger um armazenamento](#securing-a-store)

## <a name="test-checklist"></a>Lista de verificação de teste

Use a lista de verificação na tabela a seguir para validar sua loja online do Tipo 2 que você deseja colocar no quadro.



Teste

Windows XP

Windows Vista

Windows 7

Resultado (pass/fail/not applicable)

32

64

32

64

32

64

1. Verifique se o software é instalado.

2. Verifique se o software é desinstalado.

3. Verifique se o software não é executado na bandeja.

4. Verifique se a guia loja opera.

5. Verifique se o armazenamento tem uma opção para criar uma nova conta.

6. Verifique se a conta criada pode entrar.

7. Verifique se o armazenamento tem uma opção para salvar informações do usuário.

8. Verifique se o cache de credenciais está presente e funcionando.

9. Verifique se o usuário será solicitado a solicitar credenciais se eles não estão armazenados em cache.

10. Verifique se todos os tipos disponíveis de fluxo de conteúdo.

11. Verifique se o conteúdo é reproduzindo no Microsoft Windows Media Player.

12. Verifique se um preço calculado está correto.

13. Verifique se o conteúdo comprado foi baixado para a biblioteca.

14. Verifique se os metadados foram baixados para a compra.

15. Verifique se os direitos de uso de mídia estão corretos para a compra.

16. Verifique se o conteúdo comprado pode ser reproduzir.

17. Verifique se clicar no **botão Comprar** ou **Comprar** muda para a loja.

18. Verifique se o conteúdo comprado foi baixado.

19. Verifique se o conteúdo comprado pode ser gravado.

20. Verifique se a contagem de burn está decrementada.

21. Verifique se o conteúdo pode ser transferido para outro computador.

22. Verifique se o conteúdo é transferido para um dispositivo.

23. Verifique se a contagem de sincronização está decrementada.

24. Verifique se o histórico de compras rastreia as compras anteriores.

25. Verifique se uma compra anterior pode ser restaurada.

26. Verifique a funcionalidade de um armazenamento para gerenciar vários computadores.

27. Verifique se o Centro de Informações está desligado por padrão.

28. Verifique se o Centro de Informações tem informações de mídia na área agora em reprodução.

29. Verifique se os links navegam até o armazenamento.

30. Verifique se o armazenamento testado produz no armazenamento ativo.

31. Verifique se o armazenamento testado não assumirá o armazenamento atual.

32. Verifique se o armazenamento está acessível no modo de alto contraste.

33. Verifique se o armazenamento está seguro.



 

### <a name="test-pass-preparation"></a>Preparação de passagem de teste

Antes de executar uma aprovação de teste, você deve garantir que o armazenamento e as contas de teste estão prontos para teste. Você deve determinar as informações a seguir antes do início da passagem. Se você puder determinar as informações alguns dias antes da aprovação do teste, a passagem será executado com mais eficiência.

-   Determine as seguintes informações sobre contas de teste fornecidas pelo armazenamento:
    -   Contas e senhas funcionam para permitir que um usuário entre
    -   As contas são corretamente e adequadamente estruturadas para cada tipo de modo de negócios que a loja oferece
    -   As contas são válidas para todas as localidades a serem testadas ou existem contas para cada localidade se as contas não podem cruzar localidades
-   Determine quais localidades testar.
-   Determine quais idiomas testar.
-   Determine as seguintes informações sobre o ambiente de teste:

    -   Lojas ao vivo que funcionam com Windows XP, Windows Vista e Windows 7
    -   O armazenamento não ao vivo a ser testado
    -   Verifique se o armazenamento não ao vivo a ser testado está visível em todas as versões do sistema operacional e em todas as versões do Windows Media Player plataforma.

-   Determine as seguintes informações sobre o armazenamento a ser testado:

    -   Nome da loja
    -   Gráficos e rótulos de logotipo da guia da loja esperados
    -   A loja está em funcionamento para todas as versões do sistema operacional?
    -   Essa é uma nova versão da loja em teste?
    -   O armazenamento está em teste em um armazenamento tipo 1 ou Tipo 2?
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

-   Microsoft Windows Media Player 11 em Windows XP com Service Pack 3 (SP3) 32 bits e sistemas operacionais de 64 bits
-   Windows Media Player 11 nos sistemas operacionais Windows Vista 32 bits e 64 bits (32-bit Windows Media Player)
-   Microsoft Windows Media Player 12 em sistemas operacionais de Windows 7 32 bits e 64 bits (32-bit Windows Media Player)

embora você deva executar testes em todas as versões de sistema operacional e plataformas listadas, as versões de 32 bits do Windows Vista e Windows 7 são as versões de sistema operacional de prioridade. Você deve testar a instalação de qualquer software em todas as plataformas.

Capturas de tela neste tópico usam um repositório fictício, Proseware, para demonstrar o uso da interface do usuário.

## <a name="configuration-and-setup"></a>Configuração e instalação

As seções a seguir descrevem como configurar e configurar o teste de validação para o on-board a tipo 2 loja online.

### <a name="setting-up-a-test-machine"></a>Configurando um computador de teste

Execute as seguintes etapas para configurar um computador de teste:

1.  Aponte o computador de teste para os servidores de teste de conteúdo adicionando uma chave do Registro específica do repositório.
2.  Defina valores na caixa de diálogo **Opções regionais e de idioma** para as configurações adequadas de idioma e localidade. Para definir o idioma, selecione a guia **formatos** e, em seguida, selecione o idioma na caixa de combinação **formato atual** . Para definir a região, selecione a guia **local** e, em seguida, selecione a região na caixa de combinação **local atual** . Além disso, para lojas que exigem a instalação de um plug-in ou software personalizado específico para armazenamento, talvez seja necessário alterar a localidade do sistema para o idioma da localidade do repositório para facilitar a instalação. O instalador de software deve dar suporte a caracteres de byte único e duplo e deve ser executado em qualquer localidade. Você deve testar na localidade nativa. Para definir a localidade nativa, abra a caixa de diálogo **região e idioma** , selecione a guia **administrativo** e clique no botão **alterar localidade do sistema** , conforme mostrado na captura de tela a seguir. clicar nesse botão exibe a caixa de diálogo **região e idioma Configurações** . A caixa de combinação de **localidade do sistema atual** nessa caixa de diálogo altera a localidade do sistema.

    As capturas de tela a seguir mostram as guias nas quais você pode definir a região e o idioma:

    ![captura de tela da caixa de diálogo opções regionais e de idiomas](images/reg-lang-opt.png)

    ![captura de tela mostrando como alterar a localidade do sistema atual](images/reg-lang-settings.png)

3.  desative a exibição do centro de informações de um repositório definindo Windows Media Player para reproduzir uma visualização. a principal diferença entre as plataformas é que, no Windows Media Player 11, você começa clicando **agora em execução**, enquanto em Windows Media Player 12, você começa clicando com o botão direito do mouse na janela principal.

    a captura de tela a seguir mostra a sequência de opções de menu que desempenha uma visualização no Windows Media Player 11:

    ![captura de tela mostrando como reproduzir uma visualização no Windows Media Player 11](images/wmp11-visual.png)

    a captura de tela a seguir mostra a sequência de opções de menu que desempenha uma visualização no Windows Media Player 12:

    ![captura de tela mostrando como reproduzir uma visualização no Windows Media Player 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Configurando um repositório

Primeiro, execute as etapas a seguir para configurar um repositório e, em seguida, execute as etapas a seguir as etapas iniciais para verificar a configuração da loja:

1.  inicie o Windows Media Player e aguarde alguns segundos para adquirir o arquivo de AllServices.xml mais recente.
2.  para Windows XP e Windows Vista, para selecionar uma loja online, primeiro clique na guia que divide entre o modo de exibição de guia de mídia e a exibição de lojas online. Em seguida, no menu, clique em **procurar todas as lojas online** e selecione o repositório clicando em seu ícone na lista de lojas. para Windows 7, clique no botão no painel de navegação biblioteca que se divide entre o botão **guia de mídia** e o botão **lojas Online** . Em seguida, no menu, clique em **procurar todas as lojas online** e selecione o repositório clicando em seu ícone na lista de lojas.

    a captura de tela a seguir mostra como selecionar uma loja online no Windows Media Player 11:

    ![captura de tela mostrando como selecionar uma loja online no Windows Media Player 11](images/wmp11-set-store.png)

    a captura de tela a seguir mostra como selecionar uma loja Online no Windows Media Player 12:

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

    para Windows XP e Windows Vista com Windows Media Player 11, verifique se o nome e o ícone da loja estão visíveis em relação ao plano de fundo escuro Windows Media Player 11.

    para Windows 7 com Windows Media Player 12, verifique se o nome e o ícone da loja estão visíveis no painel de navegação biblioteca, no menu de contexto seletor de serviço.

    Verifique se o repositório está listado na parte superior da lista seletor de repositório no menu.

    > [!Note]  
    > Não haverá a opção **Adicionar serviço atual ao menu** se o repositório do tipo 2 for o repositório em destaque (padrão) para a região.

     

    a captura de tela a seguir mostra o menu que aparece quando você clica na guia no canto superior direito do Windows Media Player 11:

    ![captura de tela mostrando a guia armazenar no Windows Media Player 11](images/wmp11-verify-store.png)

    a captura de tela a seguir mostra o menu que aparece quando você clica no botão de divisão no canto inferior esquerdo do Windows Media Player 12:

    ![captura de tela mostrando a guia armazenar no Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Criando uma conta

**Para verificar a configuração da conta**

1.  Verifique se o repositório tem uma opção para criar uma nova conta e siga as instruções da loja para criar uma nova conta.

    a captura de tela a seguir realça um botão **criar nova conta** , como pode aparecer no Windows Media Player 11:

    ![captura de tela mostrando como verificar a configuração da conta do Windows Media Player 11](images/wmp11-verify-account.png)

    a captura de tela a seguir realça um botão **criar nova conta** , como pode aparecer no Windows Media Player 12:

    ![captura de tela mostrando como verificar a configuração da conta do Windows Media Player 12](images/wmp12-verify-account.png)

2.  Verifique se você pode entrar na conta que você criou.

### <a name="setting-up-credential-caching"></a>Configurando a credencial Caching

Primeiro, execute as seguintes etapas para configurar o cache de credenciais e execute as etapas a seguir as etapas iniciais para verificar a configuração de caching de credencial:

1.  Na página de entrada, insira as credenciais e selecione a opção para salvar as informações do usuário.
2.  Verifique se a página de entrada tem uma caixa de seleção que permite ao usuário armazenar em cache as credenciais.
3.  O cache de credenciais opcional é um ponto de segurança importante. O cache automático de credenciais pode expor informações de identificação pessoal de usuários que entram em um computador compartilhado ou público. Você deve proteger as informações do cliente oferecendo uma caixa de seleção que processa o cache opcional.

**Para verificar o cache de credenciais**

1.  Verifique se o repositório tem uma caixa de seleção para uma opção **salvar minhas informações de usuário** .

    1.  Feche Windows Media Player.
    2.  reabra Windows Media Player e tente baixar algum conteúdo.

2.  Verifique se o cache de credenciais está presente e funcionando.

    1.  Saia da loja.
    2.  Feche Windows Media Player.
    3.  reabra Windows Media Player e tente baixar algum conteúdo.

3.  Verifique se as credenciais do usuário são solicitadas se elas não estiverem armazenadas em cache.

    Depois de sair e, em seguida, tentar usar a loja, as credenciais do cliente deverão ser solicitadas.

## <a name="content-acquisition"></a>Aquisição de conteúdo

Esta seção descreve as várias maneiras de adquirir conteúdo e como verificar se o conteúdo foi adquirido.

### <a name="streaming-content"></a>Conteúdo de streaming

Transmita todos os tipos de conteúdo disponíveis do repositório. Por exemplo, transmita o conteúdo de rádio, vídeo, áudio e visualizações.

**Para verificar o conteúdo de streaming**

1.  Verifique se todos os tipos de fluxo de conteúdo disponíveis.

2.  verifique se o conteúdo é reproduzido no Windows Media Player e não em outro jogador ou controle.

### <a name="obtaining-content"></a>Obtendo conteúdo

Primeiro, execute as etapas a seguir para comprar conteúdo e, em seguida, execute as etapas a seguir as etapas iniciais para verificar a compra e verificar se o conteúdo foi baixado:

1.  Iniciar Windows Media Player.
2.  Entre na conta de teste.
3.  Navegue até o conteúdo a ser comprado.
4.  Siga o procedimento específico do repositório para comprar conteúdo.

**Para verificar o conteúdo adquirido e baixado**

1.  Verifique se o preço calculado está correto.

    Verifique se o preço está correto, especialmente ao comprar várias partes de conteúdo ao mesmo tempo e verifique se as informações de saldo da conta foram atualizadas corretamente após a compra. Alguns conteúdos podem ser comprados como faixas únicas e apenas como álbuns. Verifique se o preço do álbum não é maior do que a soma das faixas individuais.

2.  Verifique se o conteúdo adquirido é baixado para a biblioteca.

    quando o download for concluído, navegue até o conteúdo baixado na biblioteca de Windows Media Player. O conteúdo baixado está localizado na biblioteca do usuário atual.

    -   para Windows XP e Windows Vista com o Windows Media Player 11, o conteúdo baixado aparece no painel de navegação da **biblioteca, em tabela dinâmica** e, em seguida, em **músicas**.
    -   para Windows 7 com Windows Media Player 12, o conteúdo baixado para a biblioteca de Windows Media Player aparece no painel de navegação Windows Media Player em **música**.

3.  Verifique se os metadados são baixados para a compra.

    verifique se as colunas a seguir aparecem na biblioteca de Windows Media Player (adicione-as se não):

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

    execute as seguintes etapas para comprar conteúdo no Windows XP e Windows Vista com o Windows Media Player 11:

    1.  Clique na guia **executando agora** .
    2.  No painel lista, posicione o ponteiro do mouse para focalizar a arte do álbum para mostrar o link **comprar** .
    3.  Clique em **comprar**.

    a captura de tela a seguir mostra o local do link **comprar** no Windows Media Player 11:

    ![captura de tela mostrando como comprar conteúdo no Windows Media Player 11](images/wmp11-verify-buy-play.png)

    execute as seguintes etapas para comprar conteúdo no Windows 7 com Windows Media Player 12:

    1.  Em modo de biblioteca, clique na guia **reproduzir** .
    2.  Na lista de reprodução, na arte do álbum, clique em **comprar**

    a captura de tela a seguir mostra como comprar conteúdo no Windows Media Player 12:

    ![captura de tela mostrando como comprar conteúdo no Windows Media Player 12](images/wmp12-verify-buy-play.png)

6.  Verifique se clicar em **comprar** ou **comprar** alterna para o repositório.

    o Windows Media Player deve mudar para o repositório na exibição de biblioteca e carregar a experiência de compra da loja.

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

a captura de tela a seguir mostra a **lista de gravação** no lado direito da tela e o botão **iniciar gravação** abaixo da **lista de gravação** no Windows Media Player 11:

![captura de tela mostrando como gravar conteúdo no Windows Media Player 11](images/wmp11-verify-burn.png)

a captura de tela a seguir mostra como a lista de gravação aparece no Windows Media Player 12 depois que você arrasta uma faixa para a lista de gravação e mostra o botão **iniciar gravação** na parte superior da guia **gravar** :

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

 

1.  Conexão um dispositivo com um relógio seguro. os exemplos incluem dispositivos que usam Windows DRM de mídia para dispositivos portáteis, como um Media Center portátil como o iRiver H10, o Zen criativo e assim por diante.
2.  No Windows Media Player, clique na **guia Sincronizar.**
3.  Arraste o conteúdo da biblioteca para a área **De sincronização na** **guia Sincronizar.**
4.  Clique no **botão Iniciar Sincronização.**

A captura de tela a seguir mostra a  Faixa 1 na **área** de lista Sincronização e mostra o botão Iniciar Sincronização Windows Media Player 11:

![captura de tela mostrando como transferir conteúdo no Windows Media Player 11](images/wmp11-verify-transfer.png)

A captura de tela a seguir mostra a  Faixa 1 na **área** de lista Sincronização e mostra o botão Iniciar Sincronização Windows Media Player 12:

![captura de tela mostrando como transferir conteúdo no Windows Media Player 12](images/wmp12-verify-transfer.png)

**Para verificar se o conteúdo comprado pode ser transferido para outro dispositivo**

1.  Verifique se o conteúdo comprado é transferido para o dispositivo, ao tocar o conteúdo no dispositivo. O conteúdo transferido também deve ter metadados apropriados.

2.  Verifique se a contagem de sincronização está decrementada.

    Navegue até a biblioteca e abra os direitos de uso de mídia para uma faixa transferida.

    Se o número de vezes que uma faixa pode ser sincronizada for limitado, verifique se esse número diminui quando a faixa é transferida.

## <a name="store-features"></a>Recursos da Loja

As seções a seguir descrevem como testar vários recursos de uma loja online no boarded.

### <a name="managing-an-account"></a>Gerenciando uma conta

Entre com uma conta que fez algumas compras e abra o histórico de compras.

**Para verificar o histórico de compras**

-   Verifique se o histórico de compras rastreia as compras anteriores.

Se o tipo de loja ou conta for compatível com esse recurso, tente restaurar uma compra excluída.

**Para verificar se as compras anteriores podem ser reacompaciadas**

-   Verifique se uma compra anterior pode ser restaurada.

Se o armazenamento dá suporte ao uso de vários computadores com a conta, verifique qualquer funcionalidade que esse recurso fornece.

**Para verificar o gerenciamento de vários computadores com uma única conta**

-   Verifique a funcionalidade do armazenamento para gerenciar vários computadores.

### <a name="managing-a-store-specific-account"></a>Gerenciando uma conta Store-Specific banco de dados

O armazenamento pode não ter tipos de conta, restrições ou conteúdo típicos. Por exemplo, uma loja que alugue vídeo de streaming precisaria de alguma interface do usuário para exibir aluguéis ativos e essa interface do usuário precisaria ser testada.

> [!Note]  
> Embora a Microsoft não possa certificar a funcionalidade de conta específica do armazenamento, para garantir uma boa experiência do cliente, você deve testar essa funcionalidade.

 

### <a name="managing-the-info-center"></a>Gerenciando o Centro de Informações

Primeiro, execute as seguintes etapas para se preparar para testar o estado padrão e, em seguida, execute a próxima etapa que segue as etapas iniciais para verificar se o Info Center está desligado por padrão:

1.  Reproduza algum conteúdo da loja.
2.  Alternar para o modo Agora Em reprodução. No Windows XP ou Windows Vista com Windows Media Player 11, clique na **guia Agora Em** reprodução. No Windows 7 com Windows Media Player 12, clique  no botão Alternar para Agora Em Reprodução no canto inferior direito.

**Para verificar se o Centro de Informações está desligado por padrão**

-   Verifique se o Centro de Informações está desligado por padrão.

Se a loja oferecer uma exibição do Info Center, reproduza algum conteúdo da loja e, enquanto o conteúdo estiver sendo reproduzindo, alternar para o modo Agora Reproduzindo e ativar o Info Center.

No Windows XP ou Windows Vista com Windows Media Player 11, clique com o botão direito do mouse na janela agora em reprodução e, em seguida, no menu de contexto, selecione Exibição do **Centro** de Informações .

A captura de tela a seguir mostra o menu de contexto Windows Media Player 11:

![captura de tela mostrando como acessar o centro de informações de uma loja no Windows Media Player 11](images/wmp11-info-center.png)

No Windows 7 com Windows Media Player 12, clique com o botão direito do mouse na janela agora em reprodução, no menu de contexto, selecione Visualizações e clique em Exibição do Centro de **Informações**.

A captura de tela a seguir mostra o menu de contexto Windows Media Player 12:

![captura de tela mostrando como acessar o centro de informações de uma loja no Windows Media Player 12](images/wmp12-info-center.png)

**Para verificar se o Info Center está funcional**

-   Verifique se o Info Center mostra informações de mídia na área agora em reprodução. A captura de tela a seguir mostra um exemplo dessas informações de mídia:

    ![captura de tela mostrando a funcionalidade do centro de informações de uma loja](images/media-information.png)

Se algum link de compra ou outros links aparecerem na página, clique nos links.

**Para verificar links na exibição do Info Center**

-   Verifique se os links mostram o armazenamento.

    O Windows Media Player deve alternar para o armazenamento em sua biblioteca.

## <a name="store-interaction"></a>Interação com o armazenamento

As seções a seguir descrevem como testar a interação entre as outras lojas e a loja que você está testando.

### <a name="yielding-to-the-active-store"></a>Ing to the Active Store

Alternar para um armazenamento diferente do armazenamento que está sendo testado.

**Para verificar o rendimento para o armazenamento ativo**

-   Verifique se o armazenamento testado produz no armazenamento ativo.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Impedindo que o armazenamento testado assumia o armazenamento ativo

-   Com outro armazenamento selecionado, feche Windows Media Player e reinicie o computador.
-   Iniciar Windows Media Player.

**Para verificar se o armazenamento testado não assumirá o controle**

-   Verifique se o armazenamento ativo mais recentemente aparece e se o armazenamento testado não aparece.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Acessando um armazenamento no modo High-Contrast armazenamento

Primeiro, habilita o modo de alto contraste pressionando LEFT SHIFT+LEFT ALT+PRINT SCREEN e, em seguida, execute as seguintes etapas para verificar a acessibilidade de alto contraste:

**Para verificar se o armazenamento está acessível no modo de alto contraste**

1.  Verifique se a interface do usuário de logoff está intacta e funcional.
2.  Verifique se todas as janelas e caixas de diálogo aparecem corretamente.
3.  Mídia de compra. Verifique se os botões de compra e download, gerenciadores de download, informações de preço e assim por diante estão visíveis.
4.  Verifique se você pode transmitir, gravar e sincronizar.
5.  Procure elementos de texto recortado e interface do usuário, texto que não é legível e outros defeitos visíveis.

### <a name="securing-a-store"></a>Proteger um armazenamento

Execute as seguintes etapas para verificar a segurança da conta:

**Para verificar a segurança da conta**

1.  Insira informações de conta malformadas na página de logoff e na caixa de diálogo e verifique se o armazenamento as rejeita.
2.  Entre, veja a página da conta e saia.
3.  Clique no botão Voltar Windows Media Player e verifique se você não vê as informações da conta de usuário anterior.

 

 




