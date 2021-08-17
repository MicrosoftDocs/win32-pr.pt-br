---
title: Cenários do assistente de compatibilidade de programa para Windows 8
description: Cenários do assistente de compatibilidade de programa para Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63fbd912e14ac682ffe820ad140b2cad6a487dfbac833aa419c53389a9339ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852509"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Cenários do assistente de compatibilidade de programa para Windows 8

## <a name="platforms"></a>Plataformas

**clientes** -Windows XP \| Windows Vista \| Windows 7 \| Windows 8  

## <a name="description"></a>Descrição

o PCA (assistente de compatibilidade de programa) é um recurso do Windows 8 que ajuda os usuários finais a executar aplicativos de desktop projetados para versões anteriores do Windows. o Windows 8 tem uma excelente compatibilidade de aplicativo interna que permite que aplicativos criados para Windows 7 ou versões anteriores do Windows funcionem bem no Windows 8 automaticamente. No entanto, há um pequeno número de aplicativos que podem ter problemas de execução sem intervenção.

Quando um usuário executa um aplicativo, o PCA rastreia o aplicativo e identifica os sintomas de determinados problemas de compatibilidade conhecidos no Windows 8. Quando ele detecta problemas de problema, ele fornece ao usuário uma oportunidade de aplicar uma correção recomendada que ajudará a executar o aplicativo melhor no Windows 8.

## <a name="scenarios"></a>Cenários

O PCA rastreia aplicativos para um conjunto de problemas de compatibilidade conhecidos no Windows 8. O PCA rastreia os problemas, identifica as correções e fornece uma caixa de diálogo para o usuário com instruções para aplicar uma correção recomendada. O usuário pode decidir aplicar as correções recomendadas ou optar por não fazer nada e cancelar a recomendação. Se o usuário cancelar, o PCA não rastreará mais esse aplicativo.

o PCA geralmente aplica um dos três modos de compatibilidade Windows – Windows XP SP3, Windows Vista SP2 ou Windows 7, dependendo de quando o programa (ou sua configuração) foi criado. o PCA usa os \_ atributos de data de vinculação e de subsistema do programa e as seções de TRUSTINFO e compatibilidade do manifesto do arquivo executável para determinar quais dos modos é relevante e se aplica Windows XP SP3 (inclui privilégio administrativo), Windows Vista SP2 ou Windows 7, respectivamente. Um glossário no final do documento lista cada um dos modos de compatibilidade que o PCA aplica e sua descrição.

Para todos os cenários listados abaixo, o PCA rastreia os aplicativos por uma segunda vez após a aplicação de uma correção. Se o aplicativo continuar a falhar da mesma maneira mesmo após a aplicação de uma correção de compatibilidade, o PCA reverterá a correção. O PCA interromperá permanentemente o rastreamento do aplicativo específico que falhou.

Embora o PCA acompanhe muitos problemas potenciais, nem todos os problemas realmente causarão falhas de aplicativo. o PCA recomenda correções apenas em situações em que há uma alta probabilidade de que a falha do aplicativo seja devida a Windows motivos de compatibilidade. As seções a seguir se expandem em cada um dos cenários do PCA desenvolvidos no Windows 8. Cada seção descreve o cenário do problema e as recomendações que o PCA fornece para permitir que o aplicativo continue funcionando corretamente no Windows 8.

para saber mais sobre as alterações de compatibilidade no Windows 8, consulte os outros tópicos no guia de *compatibilidade do Windows 8*.

Os cenários que o PCA acompanha e recomenda correções são:

-   Falha na instalação ou desinstalação do aplicativo
-   falha na execução do aplicativo com uma mensagem de verificação de versão Windows
-   Falha ao iniciar o aplicativo devido a um privilégio administrativo
-   Falha do aplicativo devido a problemas de memória específicos
-   Falha do aplicativo devido a arquivos do sistema incompatíveis
-   O aplicativo falha devido a erros sem tratamento no Windows de 64 bits
-   o aplicativo falha ao tentar excluir arquivos não Windows protegidos
-   falha do aplicativo ao tentar modificar Windows arquivos
-   O aplicativo falha devido ao uso de modos de cor de 8 ou 16 bits
-   O aplicativo falha devido a problemas de exibição e gráficos
-   Falha do aplicativo ao declarar reconhecimento de DPI
-   falha do aplicativo devido a recursos de Windows ausentes
-   O aplicativo falha devido a drivers não assinados em Windows 8 de 64 bits
-   Acompanhamento de aplicativos instalados por meio de configurações de compatibilidade
-   O aplicativo falha ao iniciar instaladores ou atualizadores
-   Instaladores de aplicativo que precisam ser executados com privilégio administrativo
-   Miniaplicativos do painel de controle herdados que precisam ser executados com privilégio administrativo

Cada um desses cenários é expandido abaixo:

**Falha na instalação ou desinstalação do aplicativo**

Um dos tipos mais comuns de falhas de aplicativo ocorre durante a instalação do aplicativo. Os programas de instalação mais antigos normalmente falham de duas maneiras:

-   o programa de instalação não está ciente dos recursos do controle de conta de usuário (UAC) no Windows 8, portanto, ele pode não ser executado com os privilégios totais necessários para fazer alterações no sistema nas áreas protegidas do Windows 8
-   o programa de instalação verifica a versão do Windows e bloqueia a execução se a versão for maior que a esperada

Essas condições de falha são dois dos tipos mais comuns de falhas de compatibilidade na instalação. o PCA, com a ajuda de vários outros componentes do Windows, como o UAC, detecta programas de instalação na inicialização e os acompanha no final da instalação. se o programa de instalação não conseguir adicionar arquivos ou adicionar uma entrada válida na parte "adicionar remover programas" do painel de controle de Windows, o PCA considerará que a instalação falhou.

Nesse caso, o PCA recomenda um modo de compatibilidade apropriado para o aplicativo. o modo de compatibilidade permite que o programa de instalação seja executado no modo de Windows ele foi projetado para o e também garante que o aplicativo seja executado com privilégios administrativos. o PCA aplica o modo de compatibilidade RUNASADMIN juntamente com o modo de compatibilidade do Windows XP, Windows Vista ou Windows 7 apropriado. O usuário, no final da instalação com falha, verá uma caixa de diálogo com a recomendação do PCA:

![falha do aplicativo ao instalar ou desinstalar a caixa de diálogo](images/pcafigure1.png)

Em seguida, o usuário pode optar por:

-   Execute o programa usando as configurações de compatibilidade (opção recomendada), após a qual o PCA aplicará a configuração recomendada (modo de compatibilidade), reinicie o programa de instalação e acompanhe-o até que a instalação seja concluída com êxito
-   Indicar que o programa foi instalado corretamente; nesse caso, o PCA não adicionará nenhuma configuração e interromperá o controle da configuração
-   Clique em fechar, caso em que o PCA não adicionará nenhuma configuração e interromperá o acompanhamento dessa configuração

o mesmo mecanismo é usado para ajudar a desinstalação do aplicativo quando um usuário tenta desinstalar o aplicativo na seção ' adicionar/remover programas ' no Windows ou no atalho do desinstalador do aplicativo.

**falha na execução do aplicativo com uma mensagem de verificação de versão Windows**

uma das falhas de compatibilidade mais comuns no tempo de execução do aplicativo é devido à verificação de versão Windows. muitos aplicativos, após a inicialização, verificam a versão do Windows; Se eles não reconhecerem a versão, eles se bloquearão mesmo que o aplicativo possa ter sido executado sem problemas.

Em geral, essas verificações são associadas a duas condições que o PCA rastreia:

O aplicativo exibe uma caixa de mensagem que avisa o usuário. Veja um exemplo abaixo:

![falha na execução do aplicativo com uma caixa de diálogo de verificação de versão do Windows](images/pcafigure2.png)

-   O aplicativo termina imediatamente ou falha

Se o PCA identificar essas duas condições para um aplicativo, ele fornecerá uma recomendação ao usuário. O PCA permitirá que o usuário execute novamente o aplicativo com as configurações de compatibilidade. o PCA aplicará o modo de compatibilidade do Windows XP, Windows Vista ou Windows 7 apropriado com base no aplicativo. Como em qualquer um dos cenários, o usuário pode informar ao PCA que o aplicativo foi executado corretamente ou recusar as configurações recomendadas clicando no botão fechar. Uma caixa de diálogo de exemplo é fornecida abaixo:

![o aplicativo não é executado com uma caixa de diálogo de opção de mensagem de verificação de versão do Windows](images/pcafigure3.png)

**Falha na inicialização ou execução do aplicativo devido a privilégio administrativo**

Alguns aplicativos precisam de privilégio administrativo para executar e executar sua funcionalidade. no entanto, no Windows 8, semelhante ao Windows 7 e Windows Vista, os aplicativos são executados em níveis de privilégio mais baixos por padrão devido ao UAC. aplicativos mais recentes projetados para o Windows Vista e superior geralmente declaram o nível de privilégio que precisam ser executados em usando a seção TRUSTINFO do manifesto EXE. No entanto, os aplicativos mais antigos geralmente falham de duas maneiras:

-   O aplicativo exibe uma mensagem para o usuário que requer privilégio administrativo, como no exemplo abaixo:

![o aplicativo não é iniciado ou executado devido à caixa de diálogo de privilégio administrativo](images/pcafigure4a.png)

-   O aplicativo termina imediatamente ou falha

Se o PCA identificar essas duas condições para um aplicativo, ele fornecerá uma recomendação ao usuário. O PCA permitirá que o usuário execute novamente o aplicativo com privilégios administrativos (o PCA aplica o modo de compatibilidade RUNASHIGHEST). O usuário receberá um prompt do UAC quando o aplicativo for executado novamente. Como em qualquer um dos cenários, o usuário pode optar por executar novamente com a configuração recomendada ou recusar as configurações recomendadas clicando em fechar. Uma caixa de diálogo de exemplo é fornecida abaixo:

![o aplicativo falha ao iniciar ou executar devido à caixa de diálogo de opção de privilégio administrativo](images/pcafigure5.png)

**Falha do aplicativo devido a problemas de memória específicos**

Alguns aplicativos falham devido a um problema de memória bem conhecido. O aplicativo faz referência a uma DLL da memória e, em seguida, chama uma função para executar o código na mesma DLL. Isso causa uma falha imediata do aplicativo. embora esse problema não seja devido a Windows 8 alterações de compatibilidade, é um problema relativamente comum visto em uma ampla variedade de aplicativos. O PCA acompanha esse problema para dar aos usuários a oportunidade de executar seu aplicativo de forma mais confiável.

Para esses aplicativos, o PCA aplica automaticamente o modo de compatibilidade PINDLL silenciosamente. O modo de compatibilidade invocado pelo PCA impede que o aplicativo libere a DLL da memória. Portanto, a chamada de função para a DLL pelo aplicativo funcionará, impedindo que o aplicativo falhe e permitindo que ele continue a funcionar corretamente.

**Falha do aplicativo devido a arquivos do sistema incompatíveis**

alguns aplicativos projetados para o Windows XP e anterior incluem cópias de Windows DLLs do sistema junto com seus instaladores. quando esses aplicativos são instalados, o aplicativo tem uma cópia mais antiga da dll em sua própria pasta, bem como a versão mais recente da dll que está nas pastas do sistema Windows.

no Windows Vista e posterior, essa condição pode fazer com que o aplicativo falhe ao tentar carregar a dll local, já que essa DLL não funcionará bem com o restante das DLLs do sistema Windows atuais. Como o aplicativo geralmente não está ciente das versões mais recentes dessa DLL, ele não funciona corretamente.

quando o PCA detecta que a dll não foi carregada corretamente, ele aplicará uma configuração de compatibilidade que permite ao Windows carregar a versão mais recente da DLL da pasta do sistema Windows para que o aplicativo possa ser executado corretamente.

No final da primeira execução com falha do aplicativo, os usuários verão a caixa de diálogo do PCA que os notifica da configuração aplicada, como abaixo:

![falha do aplicativo devido à caixa de diálogo arquivos do sistema incompatíveis](images/pcafigure6.png)

**O aplicativo falha devido a erros sem tratamento no Windows de 64 bits**

na versão de 64 bits do Windows 8, uma nova exceção foi habilitada para o mecanismo de retorno de chamada do loop de mensagem. embora essa exceção tenha sido introduzida pela primeira vez no Windows 7, ela não era obrigatória para lidar com esse erro. no Windows 8, os aplicativos que usam loops de mensagem devem lidar com essa nova exceção. Caso contrário, eles falharão. aplicativos projetados para versões mais antigas do Windows podem não estar cientes dessa exceção e, portanto, talvez não manipulem esse erro (exceção) corretamente.

O PCA detecta aplicativos que falham devido a esse erro sem tratamento e aplica automaticamente o modo de compatibilidade DISABLEUSERCALLBACKEXCEPTION para o aplicativo. Depois que a configuração for aplicada ao final da execução, o usuário será notificado como abaixo. O aplicativo obterá o modo na próxima execução e poderá evitar esse erro.

![falha do aplicativo devido a erros sem tratamento na caixa de diálogo do Windows de 64 bits](images/pcafigure7.png)

**o aplicativo falha ao tentar excluir arquivos não Windows protegidos**

alguns aplicativos projetados para o Windows XP e anterior pressupõem que eles normalmente são executados com privilégios administrativos completos. como um curso de comportamento normal do aplicativo, eles podem tentar excluir arquivos não Windows protegidos (em arquivos de programas ou pastas de Windows). Quando a operação de exclusão falha, muitos aplicativos podem falhar.

O PCA detecta esses aplicativos que falham ao excluir arquivos protegidos e falhas e fornece uma recomendação ao usuário. O PCA permitirá que o usuário execute novamente o aplicativo com as configurações de compatibilidade. Como em qualquer um dos cenários, o usuário pode informar ao PCA que o aplicativo foi executado corretamente ou recusar as configurações recomendadas clicando no botão fechar. Nesse caso, o PCA aplica o modo de compatibilidade VIRTUALIZEDELETE. Uma caixa de diálogo de exemplo é fornecida abaixo:

![o aplicativo falha ao tentar excluir a caixa de diálogo arquivos não Windows protegidos](images/pcafigure8.png)

**o aplicativo falha ao tentar modificar Windows arquivos ou chaves do registro**

alguns aplicativos projetados para o Windows XP e anterior pressupõem que eles normalmente são executados com privilégios administrativos completos. como um curso de comportamento normal do aplicativo, eles podem tentar modificar, excluir ou gravar Windows arquivos protegidos (em arquivos de programas ou pastas Windows) ou chaves do registro de propriedade de Windows. Quando qualquer uma das operações de gravação, exclusão ou modificação de um arquivo ou de uma chave de registro falha, muitos aplicativos podem falhar ou falhar incorretamente.

o PCA detecta esses aplicativos que falham ao gravar em arquivos protegidos do Windows ou chaves do registro e fornece uma recomendação ao usuário quando o aplicativo é encerrado. O PCA permitirá que o usuário execute novamente o aplicativo com as configurações de compatibilidade. Como em qualquer um dos cenários, o usuário pode informar ao PCA que o aplicativo foi executado corretamente ou recusar as configurações recomendadas clicando no botão fechar. Nesse caso, o PCA aplica o modo de compatibilidade WRPMITIGATION. Uma caixa de diálogo de exemplo é fornecida abaixo:

![falha do aplicativo ao tentar modificar os arquivos do Windows ou a caixa de diálogo de chaves do registro](images/pcafigure9.png)

**O aplicativo falha devido ao uso de modos de cor de 8 ou 16 bits**

como parte da releitura de Windows 8 para aplicativos da loja Windows, uma das principais alterações é que o Gerenciador de Janelas da Área de Trabalho (DWM) agora dará suporte apenas a cores de 32 bits no Windows 8. Os modos de cor inferior agora são simulados.

muitos aplicativos e jogos mais antigos projetados para o Windows XP ou antes de usar modos de cores de 8 ou 16 bits. Sem mitigação, esses aplicativos podem falhar ao serem executados em Windows 8. No entanto, quando esses aplicativos enumeram ou tentam usar qualquer um dos modos de cor de 8 ou 16 bits para exibição, o PCA identifica imediatamente o problema e com a ajuda do DWM, garante que o aplicativo funcionará corretamente com o modo de cores simulado.

Observe que isso acontece assim que o aplicativo solicita os modos de cor baixa e é transparente para o usuário. O usuário não precisa reiniciar o aplicativo para obter essa mitigação, pois essa correção é sempre necessária para garantir que o aplicativo funcione corretamente.

**Falha do aplicativo devido a problemas de gráficos e de exibição**

como Gerenciador de Janelas da Área de Trabalho (DWM) está sempre on no Windows 8, alguns aplicativos mais antigos do Windows XP poderão falhar se o aplicativo usar apis de gráficos de modo misto, como no uso de apis GDI e do DirectX para desenhar na tela (mais jogos mais antigos) e tentar usar o modo de tela inteira:

-   O DWM impedirá a pintura diretamente para a área de trabalho, e o jogo ou o aplicativo irá falhar ou desenhar uma tela preta na área de trabalho e nenhum dos elementos gráficos estará visível
-   nesses casos, quando o aplicativo é encerrado, Windows detecta que o aplicativo ou jogo tem um problema com o modo de tela inteira e aplica o modo de compatibilidade de DXMAXIMIZEDWINDOWEDMODE que permite que o aplicativo ou jogo seja executado em um modo de janela maximizado em vez de um modo de tela inteira
-   Depois que a configuração for aplicada ao final da execução, o usuário será notificado pelo PCA, como mostrado abaixo; o aplicativo obterá o modo de compatibilidade na próxima execução e poderá ser executado corretamente

![falha do aplicativo devido a uma caixa de diálogo de problemas de gráficos e de exibição](images/pcafigure10.png)

**Falha do aplicativo ao declarar reconhecimento de DPI**

outro problema de exibição típico com muitos aplicativos mais antigos ocorre quando Windows e o aplicativo é executado no modo de alto DPI, mas o aplicativo não declara seu reconhecimento de DPI alto por meio de seu manifesto EXE. Entre os problemas comuns que podem ocorrer devido a essa incompatibilidade nas configurações estão elementos de interface do usuário recortados ou texto e tamanho de fonte incorreto. Para obter mais detalhes sobre os problemas, consulte este link [aqui](/previous-versions//dd464660(v=vs.85)).

nesses casos, Windows detecta que o aplicativo tem reconhecimento de DPI alta e aplica o modo de compatibilidade de HIGHDPIAWARE ao aplicativo no final da primeira execução. O PCA irá informar o usuário sobre isso, conforme mostrado abaixo:

![o aplicativo falha ao declarar a caixa de diálogo reconhecimento de DPI](images/pcafigure11.png)

**falha do aplicativo devido a recursos de Windows ausentes**

alguns aplicativos dependem de Windows recursos que foram removidos desde Windows Vista. Quando esses aplicativos tentam carregar as DLLs ou os componentes COM ausentes, eles não funcionam.

o PCA detecta aplicativos quando tenta carregar os recursos de Windows ausentes e fornece uma recomendação para baixar esses componentes e instalá-los após a finalização do aplicativo. O usuário pode clicar em ' obter ajuda online ' para encontrar uma alternativa ou baixar o recurso e instalá-lo. Se necessário, o usuário pode optar por não fazer nada clicando em fechar.

![falha do aplicativo devido à caixa de diálogo de recursos do Windows ausente](images/pcafigure12.png)

**O aplicativo falha devido a drivers não assinados em Windows 8 de 64 bits**

o Windows de 64 bits exigiu drivers assinados digitalmente (arquivos SYS) desde Windows Vista. no entanto, os aplicativos mais antigos criados antes do lançamento do Windows Vista enviaram drivers que não foram assinados digitalmente. se esse driver não assinado estiver instalado, Windows não os carregará. em casos raros, é possível que Windows não seja iniciada se esses drivers estiverem marcados como drivers de tempo de inicialização.

Alguns aplicativos mais antigos instalam drivers que não são assinados no Windows de 64 bits. Qualquer dispositivo ou aplicativo que tente usar esse driver poderá falhar ou resultar em uma falha do sistema. Para evitar esse cenário, o PCA detecta aplicativos ao instalar drivers não assinados e desabilita o driver que está marcado como um driver de tempo de inicialização.

Ele também instrui o usuário a adquirir um driver assinado digitalmente para que o aplicativo funcione corretamente. A mensagem é mostrada como resultado da instalação do driver e, como resultado da instalação do aplicativo. Se outro aplicativo instalar o mesmo Driver, esse aplicativo também receberá a mesma mensagem.

![o aplicativo falha devido a drivers não assinados na caixa de diálogo do Windows 8 de 64 bits](images/pcafigure13.png)

**Acompanhamento de aplicativos instalados por meio de configurações de compatibilidade**

Quando um instalador falha, o PCA ajuda o instalador com vários modos de compatibilidade, dependendo do tipo de falha. Depois que o instalador for executado com as configurações de compatibilidade, o PCA acompanhará os atalhos adicionados pelo instalador. Isso é feito para controlar se os aplicativos que foram instalados também podem precisar das configurações de compatibilidade aplicadas ao instalador.

Quando um usuário inicia esse aplicativo, o PCA solicita que o usuário pergunte se o aplicativo funcionou corretamente. Se o usuário responder, ' Sim ', o PCA interromperá o rastreamento do aplicativo. Se o usuário responder ' não ', ele aplicará o mesmo modo de compatibilidade que foi aplicado ao instalador do aplicativo e executará novamente o aplicativo com o modo de compatibilidade aplicado.

**O aplicativo falha ao iniciar instaladores ou atualizadores**

Os aplicativos às vezes iniciam programas filhos que precisam ser executados como administradores. Normalmente, esse é o caso quando um aplicativo tenta iniciar seu software de atualizador para verificar e instalar novas atualizações para o aplicativo. Quando os aplicativos executam diretamente esses programas filho, o programa filho pode falhar ao ser iniciado porque o próprio aplicativo não tinha privilégios administrativos ou porque o programa filho não foi marcado corretamente para elevação com o manifesto do UAC.

O PCA rastreia esses erros e quando o aplicativo primário é fechado, ele aplica automaticamente o modo de compatibilidade ELEVATECREATEPROCESS que ajudará os programas filhos a serem executados corretamente. Quando o aplicativo iniciar o aplicativo filho em execuções subsequentes, o usuário verá uma caixa de diálogo do UAC para o programa filho.

Um exemplo da caixa de diálogo do PCA é mostrado abaixo:

![o aplicativo não consegue iniciar instaladores ou caixa de diálogo de atualizadores](images/pcafigure14.png)

**Instaladores de aplicativo que precisam ser executados com privilégio administrativo**

os instaladores de aplicativos de área de trabalho Windows exigem privilégios administrativos, pois gravam arquivos, pastas e entradas de registro em áreas do sistema protegidas. o Windows (UAC) tem lógica de detecção para identificar quando um instalador é executado e imediatamente solicita que o usuário forneça privilégios administrativos por meio da caixa de diálogo UAC. No entanto, em alguns casos, essa lógica não será capaz de determinar que um aplicativo era realmente um instalador e pode não obter privilégios administrativos. geralmente, eles são instaladores personalizados que não usam tecnologias de instalação bem conhecidas, como Windows Installer ou instalar o escudo.

Nesses casos, o PCA detecta que o instalador falhou ao gravar seus arquivos. No final, se a instalação com falha, a PCA fornecerá uma recomendação para aplicar as configurações de compatibilidade. Se o usuário optar por clicar em 'Executar Programa', o PCA aplicará o modo de compatibilidade RUNASADMIN e executará o instalador de novo. Se o usuário optar por fechar, nenhuma configuração será aplicada. Um exemplo de caixa de diálogo PCA é mostrado abaixo:

![Captura de tela que mostra um exemplo de uma caixa de diálogo para um instalador de aplicativo que precisa ser executado com privilégios administrativos.](images/pcafigure15.png)

Os applets Painel de Controle herdados que precisam ser executados com privilégios administrativos Os applets do painel de controle geralmente alteram as configurações do sistema e precisam da capacidade de executar o administrador de ad. No entanto, aqueles escritos antes Windows Vista não têm um manifesto EXE ou não têm a seção TRUSTINFO que declara o nível de privilégio necessário. Quando esses applets são executados, a PCA os detecta e, no final da primeira, fornece uma recomendação para executar com configurações administrativas. Se o usuário optar por clicar em 'Executar Programa', a PCA aplicará o modo de compatibilidade RUNASADMIN e executará o instalador de novo. Se o usuário optar por fechar, nenhuma configuração será aplicada. Um exemplo de caixa de diálogo PCA é mostrado abaixo:

![instaladores de aplicativo que precisam ser executados com a caixa de diálogo de privilégio administrativo](images/pcafigure16.png)

**Verificando as configurações recomendadas por meio dos comentários do usuário**

No final de cada um dos cenários (depois que o aplicativo for executado com as configurações de compatibilidade recomendadas), a PCA fará uma pergunta simples ao usuário:

![verificando as configurações recomendadas por meio da caixa de diálogo comentários do usuário](images/pcafigure17.png)

O usuário pode fornecer comentários se o aplicativo funcionou ou falhou com a configuração de compatibilidade. Esses dados serão enviados anonimamente para a Microsoft. Isso ajuda a garantir que essas correções possam ser internas no Windows 8 por meio de um processo de atualização do Windows, para que os futuros usuários do Windows 8 não possam mais encontrar a falha do aplicativo e a PCA não precise mais acompanhar o aplicativo para a falha.

**Acompanhamento de problemas que não têm recomendações**

Os aplicativos podem falhar de várias maneiras diferentes por motivos de compatibilidade. O PCA acompanha muito mais problemas de compatibilidade do que o que está listado nos cenários acima. Nesses casos, muitas vezes, a manifestação do problema depende do aplicativo. Isso significa que alguns aplicativos lidam com esses problemas normalmente e se recuperam dele, enquanto outros podem não. Portanto, para esses problemas, embora o PCA ainda rastreia o aplicativo, ele não fornece uma recomendação direta para uma correção.

Os problemas que a PCA rastreia que não têm uma configuração recomendada ou uma caixa de diálogo incluem aplicativos que:

-   Ter um runtime muito curto – Os aplicativos são executados por não mais de três segundos
-   Criar objetos de memória global sem privilégios administrativos
-   Ter um erro (exceção win32) na iniciação
-   Verificar se há privilégios administrativos (mas pode não falhar)
-   Usar codecs indeo (preterido do Windows Vista)
-   Tente gravar ou excluir chaves de locais de Registro protegidos, como HKLM
-   Falha ao iniciar

**Aplicando correções por meio da guia de compatibilidade e da solução de problemas de compatibilidade**

Conforme mencionado acima, os aplicativos podem falhar por vários motivos de compatibilidade. Nem todos eles têm uma recomendação PCA clara, pois as configurações dependem do aplicativo. No entanto, os usuários podem ir para a Solução de Problemas de Compatibilidade ou a guia Compatibilidade para aplicar determinadas correções comuns para tentar fazer com que seu aplicativo com falha funcione corretamente no Windows 8. Nesses casos, a PCA ainda acompanhará o aplicativo quanto a problemas de compatibilidade, antes e depois que a correção for aplicada. Depois que o aplicativo for executado com a correção aplicada, a PCA perguntará ao usuário se a correção funcionou. Depois que o usuário responder à pergunta, os dados serão enviados anonimamente por meio da telemetria para a Microsoft. Esses dados são coletados de muitos usuários e analisados, e as correções de qualificação são amplamente distribuídas para todos os Windows 8 usuários por meio Windows atualização.

**Usando a solução de problemas de compatibilidade**

A Solução de Problemas de Compatibilidade é um mecanismo no Windows que permite diagnosticar problemas com aplicativos e aplicar correções recomendadas para fazer com que eles funcionarem corretamente. Isso só é necessário quando o PCA não fornece nenhuma recomendação para o aplicativo.

A solução de problemas permite que os usuários andem e respondam a um conjunto de perguntas e, com base nas respostas, ele aplicará um conjunto de correções e permitirá que os usuários testem seus aplicativos e verifiquem as correções. Depois de verificadas, as correções serão aplicadas permanentemente aos aplicativos para fazê-los funcionar melhor Windows 8.

A interface do usuário da solução de problemas é mostrada abaixo para referência:

![usando a caixa de diálogo de solução de problemas de compatibilidade](images/pcafigure18.png)

Você pode iniciar a Solução de Problemas de Compatibilidade de duas maneiras:

**Na tela inicial:**

1.  Tipo: solução de problemas de compatibilidade
2.  Na seção de configurações, clique no lado "Executar programas feitos para a versão anterior do Windows"

  
**No azulão do aplicativo:**

1.  No tela inicial, clique com o botão direito do mouse no lado do aplicativo
2.  Clique em 'Abrir Local do Arquivo' (somente aplicativos da área de trabalho)
3.  Na faixa de opções do Explorer, clique na 'guia Aplicativo'
4.  Escolha "Solucionar problemas de compatibilidade"

  


**Usando a guia Compatibilidade**

Observe que isso é recomendado somente para usuários especialistas em tentar configurações de compatibilidade diferentes. Esse método não fornece nenhuma recomendação do tipo de correção a ser aplicada aos aplicativos. Espera-se que o usuário saiba quais correções podem ser aplicadas para fazer o aplicativo funcionar. Se você não tiver certeza das correções, use a Solução de Problemas de Compatibilidade para encontrar uma correção para o aplicativo.

Para acessar a guia Compatibilidade:

 **Na tela inicial:**

1.  Clique com o botão direito do mouse no lado do aplicativo
2.  Abrir local do arquivo (somente aplicativos da área de trabalho)

  
**Na faixa de opções do Explorer:**

1.  Clique em Propriedades
2.  Navegue até a guia Compatibilidade
3.  Selecione as correções de compatibilidade
4.  Executar o aplicativo de novo
    > [!Note]  
    > Você pode voltar ao mesmo lugar novamente para alterar ou remover as correções também. Você também pode aplicar as correções a todos os usuários no computador usando o botão fornecido na guia.

     

  


![usando a guia de compatibilidade](images/pcafigure19.png)

**Aplicativos com problemas de compatibilidade conhecidos**

Além dos cenários de detecção de problemas de runtime listados acima, a PCA também informará os usuários na inicialização do aplicativo se o aplicativo tiver problemas de compatibilidade conhecidos. A lista é armazenada no banco de dados de compatibilidade do aplicativo do sistema. Há dois tipos dessas mensagens:

-   **Mensagens de** bloco rígido — se o aplicativo for conhecido como incompatível e se permitir que o aplicativo seja executado resultará em um impacto grave no sistema (por exemplo, uma falha de Windows ou não conseguir inicializar após a instalação), uma mensagem de bloqueio conforme mostrado abaixo será exibida

![aplicativos com problemas de compatibilidade conhecidos – caixa de diálogo mensagens de bloco rígido](images/pcafigure20.png)

-   **Mensagens de bloco suave**— se o aplicativo tiver um problema de compatibilidade conhecido e não funcionar corretamente, essa mensagem será mostrada:

![aplicativos com problemas de compatibilidade conhecidos – caixa de diálogo mensagens de blocos suaves](images/pcafigure21.png)

Em ambos os casos, a opção "Obter ajuda Online" envia um relatório de Windows para obter uma resposta online da Microsoft e exibi-la para o usuário. Normalmente, as respostas apontarão o usuário para um dos três tipos de recursos:

-   Uma atualização do fornecedor do aplicativo
-   Site de um fornecedor de aplicativo para obter mais informações
-   Um artigo da Base de Dados de Conhecimento Microsoft para obter mais informações

**Telemetria para PCA**

Depois que o PCA resolver quaisquer problemas de aplicativo em um computador Windows 8 e receber todos os comentários do usuário, ele coletará dados anônimos sobre o aplicativo, o instalador, os problemas detectados e as configurações de compatibilidade aplicadas ao aplicativo e os enviará de volta à Microsoft. Esses dados são coletados de qualquer usuário que esteja disposto a fornecer esses dados anônimos (por meio do Programa de Aperfeiçoamento da Experiência do Usuário – CEIP). Depois que esses dados são coletados, as falhas e correções do aplicativo são analisadas e as correções são distribuídas para todo o ecossistema do Windows por meio do mecanismo de atualização do Windows para que qualquer usuário do aplicativo no futuro se benesse da correção automaticamente.

**Controles administrativos e gerenciamento de configurações de PCA**

Os administradores de IT podem controlar o comportamento da PCA de duas maneiras:

-   **Desligar PCA** – essa configuração permite que os administradores de IT desliguem os diálogos que o PCA mostra aos usuários; A PCA ainda acompanhará e detectará problemas e enviará telemetria de volta
-   **Desligar a telemetria do aplicativo** – essa configuração desativará qualquer coleta e envio de dados de telemetria pela PCA
    > [!Note]  
    > Se o CEIP estiver desligado, essa configuração não terá impacto.

     

**Projetando aplicativos para trabalhar com PCA**

Os desenvolvedores precisam garantir que seus aplicativos funcionem bem em todos os cenários de compatibilidade descritos acima. Os desenvolvedores devem testar e validar seus aplicativos para cada um dos cenários acima e garantir que não haja problemas de compatibilidade. Se os problemas de compatibilidade são identificados, os desenvolvedores devem fazer as correções em seus aplicativos necessárias para garantir que o problema de compatibilidade seja resolvido. Algumas das correções comuns que os desenvolvedores devem fazer incluem:

-   Eliminar Windows de versão do sistema operacional na instalação e no runtime
-   Elimine a verificação de privilégio (verificando o acesso do administrador); usar o manifesto EXE para declarar o nível certo de privilégio necessário
-   Verifique se Windows binários não são enviados dentro do instalador do aplicativo
-   Eliminar a escrita em áreas protegidas (registro, pastas) ou a escrita em arquivos protegidos
-   Assinar digitalmente todos os binários (exe, DLL, arquivos SYS)
-   Para instaladores, verifique se a entrada apropriada 'Adicionar/Remover programas' foi adicionada; no mínimo, essa entrada de metadados do aplicativo deve incluir o nome do aplicativo, o editor, a cadeia de caracteres de versão e o idioma com suporte. Isso indicará à PCA que o instalador foi concluído com êxito e também fornecerá uma maneira conveniente para os usuários desinstalarem o aplicativo

Garantir que a seção TRUSTINFO e COMPATIBILITY do manifesto do aplicativo (executável) seja atualizada, conforme listado no Guia de Compatibilidade do Windows 8, permitirá que a PCA saiba que o aplicativo foi projetado para Windows 8 e também garantirá que o aplicativo sempre seja executado na nativa sem nenhum modo de compatibilidade aplicado a ele.

Para garantir que o PCA considere o aplicativo a ser projetado para Windows 8:

-   Todos os EXEs (instalador ou runtime) devem ser manifestos para as seções TRUSTINFO e COMPATIBILITY para Windows 8
-   O instalador deve adicionar uma entrada 'Adicionar/Remover programas'

**Glossário**

Os modos de compatibilidade usados pelo PCA são listados abaixo com uma breve descrição do que o modo habilita.



| Mode                         | Descrição                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | Esse modo emula o comportamento Windows 7, incluindo o número de versão do sistema operacional 6.1                                                                   |
| WindowsVistaSP2              | Esse modo emula o comportamento Windows 7, incluindo o número de versão do sistema operacional 6.1                                                                   |
| WindowsXPSp3                 | Esse modo emula o comportamento Windows XP SP3, incluindo o número de versão do sistema operacional 5.1. Isso também inclui o modo RUNASHIGHEST                    |
| RUNASHIGHEST                 | Esse modo solicita que o usuário execute o aplicativo com o privilégio mais alto disponível. Os usuários com privilégios administrativos verão um prompt de elevação do UAC para o aplicativo |
| Runasadmin                   | Esse modo sempre solicita que o usuário execute o aplicativo com privilégios administrativos; aplicativos com esse modo sempre obterão o prompt de elevação do UAC                    |
| ELEVATECREATEPROCESS         | Esse modo faz com que os processos filho do aplicativo principal executem com privilégios administrativos; os processos filho obterão uma caixa de diálogo de elevação do UAC                          |
| PINDLL                       | Esse modo força uma DLL a ficar na memória para um aplicativo, mesmo que o aplicativo descarregue a DLL                                                                                |
| DISABLEUSERCALLBACKEXCEPTION | Esse modo intercepta as exceções de retorno de chamada do usuário e permite que o aplicativo continue sem precisar lidar com a exceção                                          |
| VIRTUALIZEDELETE             | Esse modo intercepta operações de exclusão em arquivos protegidos e impede que os aplicativos falham devido a exceções sem tratativas da operação de exclusão                   |
| WRPMITIGATION                | Esse modo retorna êxito quando um aplicativo tenta gravar, modificar ou excluir Windows arquivos protegidos ou entradas do Registro (sem realmente concluir a operação)  |
| DXMAXIMIZEDWINDOWEDMODE      | Esse modo identifica os aplicativos que vão para o modo de tela inteira e os redireciona para um modo de Janela maximizada                                                          |
| HIGHDPIAWARE                 | Esse modo permite que o restante do Windows saiba que o aplicativo tem alto conhecimento de DPI e ajuda a renderização adequada de elementos de interface do usuário, texto, fonte etc.                              |



 

 

 