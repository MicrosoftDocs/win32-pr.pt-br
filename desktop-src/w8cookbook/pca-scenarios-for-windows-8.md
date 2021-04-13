---
title: Cenários do assistente de compatibilidade de programas para o Windows 8
description: Cenários do assistente de compatibilidade de programas para o Windows 8
ms.assetid: C61BF746-63EE-4F4E-81D3-52947FD4954D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebada2ca5115d24f260808a1c9ae899963184a8
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104560640"
---
# <a name="program-compatibility-assistant-scenarios-for-windows-8"></a>Cenários do assistente de compatibilidade de programas para o Windows 8

## <a name="platforms"></a>Plataformas

**Clientes** -Windows XP Windows \| Vista Windows 7 Windows \| \| 8  

## <a name="description"></a>Descrição

O PCA (Assistente de compatibilidade de programa) é um recurso do Windows 8 que ajuda os usuários finais a executar aplicativos de desktop projetados para versões anteriores do Windows. O Windows 8 tem uma ótima compatibilidade de aplicativos interna que permite que aplicativos projetados para o Windows 7 ou versões anteriores do Windows funcionem muito bem no Windows 8 automaticamente. No entanto, há um pequeno número de aplicativos que podem ter problemas de execução sem intervenção.

Quando um usuário executa um aplicativo, o PCA rastreia o aplicativo e identifica os sintomas de determinados problemas de compatibilidade conhecidos no Windows 8. Quando detecta qualquer sintoma de problema, ele fornece ao usuário uma oportunidade de aplicar uma correção recomendada que ajudará a executar o aplicativo melhor no Windows 8.

## <a name="scenarios"></a>Cenários

O PCA rastreia aplicativos para um conjunto de problemas de compatibilidade conhecidos no Windows 8. O PCA rastreia os problemas, identifica as correções e fornece uma caixa de diálogo para o usuário com instruções para aplicar uma correção recomendada. O usuário pode decidir aplicar as correções recomendadas ou optar por não fazer nada e cancelar a recomendação. Se o usuário cancelar, o PCA não rastreará mais esse aplicativo.

O PCA geralmente aplica um dos três modos de compatibilidade do Windows – Windows XP SP3, Windows Vista SP2 ou Windows 7, dependendo de quando o programa (ou sua configuração) foi criado. O PCA usa os \_ atributos de data de vinculação e de subsistema do programa e as seções de TRUSTINFO e compatibilidade do manifesto do arquivo executável para determinar quais dos modos é relevante e aplica o Windows XP SP3 (inclui privilégio administrativo), Windows Vista SP2 ou Windows 7, respectivamente. Um glossário no final do documento lista cada um dos modos de compatibilidade que o PCA aplica e sua descrição.

Para todos os cenários listados abaixo, o PCA rastreia os aplicativos por uma segunda vez após a aplicação de uma correção. Se o aplicativo continuar a falhar da mesma maneira mesmo após a aplicação de uma correção de compatibilidade, o PCA reverterá a correção. O PCA interromperá permanentemente o rastreamento do aplicativo específico que falhou.

Embora o PCA acompanhe muitos problemas potenciais, nem todos os problemas realmente causarão falhas de aplicativo. O PCA recomenda correções apenas em situações em que há uma alta probabilidade de que a falha do aplicativo seja devido a motivos de compatibilidade do Windows. As seções a seguir se expandem em cada um dos cenários do PCA desenvolvidos no Windows 8. Cada seção descreve o cenário do problema e as recomendações que o PCA fornece para permitir que o aplicativo continue funcionando corretamente no Windows 8.

Para saber mais sobre as alterações de compatibilidade no Windows 8, consulte os outros tópicos no *manual de compatibilidade do Windows 8*.

Os cenários que o PCA acompanha e recomenda correções são:

-   Falha na instalação ou desinstalação do aplicativo
-   Falha na execução do aplicativo com uma mensagem de verificação de versão do Windows
-   Falha ao iniciar o aplicativo devido a um privilégio administrativo
-   Falha do aplicativo devido a problemas de memória específicos
-   Falha do aplicativo devido a arquivos do sistema incompatíveis
-   Falha do aplicativo devido a erros sem tratamento no Windows de 64 bits
-   O aplicativo falha ao tentar excluir arquivos não Windows protegidos
-   O aplicativo falha ao tentar modificar os arquivos do Windows
-   O aplicativo falha devido ao uso de modos de cor de 8 ou 16 bits
-   O aplicativo falha devido a problemas de exibição e gráficos
-   Falha do aplicativo ao declarar reconhecimento de DPI
-   Falha do aplicativo devido a recursos do Windows ausentes
-   O aplicativo falha devido a drivers não assinados no Windows 8 de 64 bits
-   Acompanhamento de aplicativos instalados por meio de configurações de compatibilidade
-   O aplicativo falha ao iniciar instaladores ou atualizadores
-   Instaladores de aplicativo que precisam ser executados com privilégio administrativo
-   Miniaplicativos do painel de controle herdados que precisam ser executados com privilégio administrativo

Cada um desses cenários é expandido abaixo:

**Falha na instalação ou desinstalação do aplicativo**

Um dos tipos mais comuns de falhas de aplicativo ocorre durante a instalação do aplicativo. Os programas de instalação mais antigos normalmente falham de duas maneiras:

-   O programa de instalação não está ciente dos recursos do controle de conta de usuário (UAC) no Windows 8; Portanto, ele pode não ser executado com os privilégios totais necessários para fazer alterações no sistema nas áreas protegidas do Windows 8
-   O programa de instalação verifica a versão do Windows e bloqueia a execução se a versão for maior do que a esperada

Essas condições de falha são dois dos tipos mais comuns de falhas de compatibilidade na instalação. O PCA, com a ajuda de vários outros componentes do Windows, como o UAC, detecta programas de instalação na inicialização e os acompanha no final da instalação. Se o programa de instalação não conseguir adicionar arquivos ou adicionar uma entrada válida na parte "Adicionar remover programas" do painel de controle do Windows, o PCA considerará que a instalação falhou.

Nesse caso, o PCA recomenda um modo de compatibilidade apropriado para o aplicativo. O modo de compatibilidade permite que o programa de instalação seja executado no modo do Windows para o qual foi projetado e também garante que o aplicativo seja executado com privilégios administrativos. O PCA aplica o modo de compatibilidade RUNASADMIN juntamente com o modo de compatibilidade apropriado do Windows XP, do Windows Vista ou do Windows 7. O usuário, no final da instalação com falha, verá uma caixa de diálogo com a recomendação do PCA:

![falha do aplicativo ao instalar ou desinstalar a caixa de diálogo](images/pcafigure1.png)

Em seguida, o usuário pode optar por:

-   Execute o programa usando as configurações de compatibilidade (opção recomendada), após a qual o PCA aplicará a configuração recomendada (modo de compatibilidade), reinicie o programa de instalação e acompanhe-o até que a instalação seja concluída com êxito
-   Indicar que o programa foi instalado corretamente; nesse caso, o PCA não adicionará nenhuma configuração e interromperá o controle da configuração
-   Clique em fechar, caso em que o PCA não adicionará nenhuma configuração e interromperá o acompanhamento dessa configuração

O mesmo mecanismo é usado para ajudar a desinstalação do aplicativo quando um usuário tenta desinstalar o aplicativo na seção ' Adicionar/remover programas ' no Windows ou no atalho do desinstalador do aplicativo.

**Falha na execução do aplicativo com uma mensagem de verificação de versão do Windows**

Uma das falhas de compatibilidade mais comuns no tempo de execução do aplicativo é devido à verificação da versão do Windows. Muitos aplicativos, após a inicialização, verificam a versão do Windows; Se eles não reconhecerem a versão, eles se bloquearão mesmo que o aplicativo possa ter sido executado sem problemas.

Em geral, essas verificações são associadas a duas condições que o PCA rastreia:

O aplicativo exibe uma caixa de mensagem que avisa o usuário. Veja abaixo um exemplo:

![falha na execução do aplicativo com uma caixa de diálogo de verificação de versão do Windows](images/pcafigure2.png)

-   O aplicativo termina imediatamente ou falha

Se o PCA identificar essas duas condições para um aplicativo, ele fornecerá uma recomendação ao usuário. O PCA permitirá que o usuário execute novamente o aplicativo com as configurações de compatibilidade. O PCA aplicará o modo de compatibilidade apropriado do Windows XP, do Windows Vista ou do Windows 7 com base no aplicativo. Como em qualquer um dos cenários, o usuário pode informar ao PCA que o aplicativo foi executado corretamente ou recusar as configurações recomendadas clicando no botão fechar. Uma caixa de diálogo de exemplo é fornecida abaixo:

![o aplicativo não é executado com uma caixa de diálogo de opção de mensagem de verificação de versão do Windows](images/pcafigure3.png)

**Falha na inicialização ou execução do aplicativo devido a privilégio administrativo**

Alguns aplicativos precisam de privilégio administrativo para executar e executar sua funcionalidade. No entanto, no Windows 8, semelhante ao Windows 7 e ao Windows Vista, os aplicativos são executados em níveis de privilégio mais baixos por padrão devido ao UAC. Aplicativos mais recentes projetados para o Windows Vista e superior geralmente declaram o nível de privilégio que precisam ser executados em usando a seção TRUSTINFO do manifesto EXE. No entanto, os aplicativos mais antigos geralmente falham de duas maneiras:

-   O aplicativo exibe uma mensagem para o usuário que requer privilégio administrativo, como no exemplo abaixo:

![o aplicativo não é iniciado ou executado devido à caixa de diálogo de privilégio administrativo](images/pcafigure4a.png)

-   O aplicativo termina imediatamente ou falha

Se o PCA identificar essas duas condições para um aplicativo, ele fornecerá uma recomendação ao usuário. O PCA permitirá que o usuário execute novamente o aplicativo com privilégios administrativos (o PCA aplica o modo de compatibilidade RUNASHIGHEST). O usuário receberá um prompt do UAC quando o aplicativo for executado novamente. Como em qualquer um dos cenários, o usuário pode optar por executar novamente com a configuração recomendada ou recusar as configurações recomendadas clicando em fechar. Uma caixa de diálogo de exemplo é fornecida abaixo:

![o aplicativo falha ao iniciar ou executar devido à caixa de diálogo de opção de privilégio administrativo](images/pcafigure5.png)

**Falha do aplicativo devido a problemas de memória específicos**

Alguns aplicativos falham devido a um problema de memória bem conhecido. O aplicativo faz referência a uma DLL da memória e, em seguida, chama uma função para executar o código na mesma DLL. Isso causa uma falha imediata do aplicativo. Embora esse problema não seja devido a alterações de compatibilidade com o Windows 8, é um problema relativamente comum visto em uma ampla variedade de aplicativos. O PCA acompanha esse problema para dar aos usuários a oportunidade de executar seu aplicativo de forma mais confiável.

Para esses aplicativos, o PCA aplica automaticamente o modo de compatibilidade PINDLL silenciosamente. O modo de compatibilidade invocado pelo PCA impede que o aplicativo libere a DLL da memória. Portanto, a chamada de função para a DLL pelo aplicativo funcionará, impedindo que o aplicativo falhe e permitindo que ele continue a funcionar corretamente.

**Falha do aplicativo devido a arquivos do sistema incompatíveis**

Alguns aplicativos projetados para o Windows XP e anterior incluem cópias de DLLs de sistema do Windows junto com seus instaladores. Quando esses aplicativos são instalados, o aplicativo tem uma cópia mais antiga da DLL em sua própria pasta, bem como a versão mais recente da DLL que está nas pastas de sistema do Windows.

No Windows Vista e posterior, essa condição pode fazer com que o aplicativo falhe ao tentar carregar a DLL local, já que essa DLL não funcionará bem com o restante das DLLs de sistema atuais do Windows. Como o aplicativo geralmente não está ciente das versões mais recentes dessa DLL, ele não funciona corretamente.

Quando o PCA detecta que a DLL não foi carregada corretamente, ele aplica uma configuração de compatibilidade que permite que o Windows carregue a versão mais recente da DLL da pasta de sistema do Windows para que o aplicativo possa ser executado corretamente.

No final da primeira execução com falha do aplicativo, os usuários verão a caixa de diálogo do PCA que os notifica da configuração aplicada, como abaixo:

![falha do aplicativo devido à caixa de diálogo arquivos do sistema incompatíveis](images/pcafigure6.png)

**Falha do aplicativo devido a erros sem tratamento no Windows de 64 bits**

Na versão de 64 bits do Windows 8, uma nova exceção foi habilitada para o mecanismo de retorno de chamada de loop de mensagem. Embora essa exceção tenha sido introduzida pela primeira vez no Windows 7, ela não era obrigatória para lidar com esse erro. No Windows 8, os aplicativos que usam loops de mensagens devem lidar com essa nova exceção. Caso contrário, eles falharão. Aplicativos projetados para versões mais antigas do Windows podem não estar cientes dessa exceção e, portanto, talvez não manipulem esse erro (exceção) corretamente.

O PCA detecta aplicativos que falham devido a esse erro sem tratamento e aplica automaticamente o modo de compatibilidade DISABLEUSERCALLBACKEXCEPTION para o aplicativo. Depois que a configuração for aplicada ao final da execução, o usuário será notificado como abaixo. O aplicativo obterá o modo na próxima execução e poderá evitar esse erro.

![falha do aplicativo devido a erros sem tratamento na caixa de diálogo do Windows de 64 bits](images/pcafigure7.png)

**O aplicativo falha ao tentar excluir arquivos não Windows protegidos**

Alguns aplicativos projetados para o Windows XP e anterior pressupõem que eles normalmente são executados com privilégios administrativos completos. Como um curso de comportamento normal do aplicativo, eles podem tentar excluir arquivos não Windows protegidos (seja em arquivos de programas ou pastas do Windows). Quando a operação de exclusão falha, muitos aplicativos podem falhar.

O PCA detecta esses aplicativos que falham ao excluir arquivos protegidos e falhas e fornece uma recomendação ao usuário. O PCA permitirá que o usuário execute novamente o aplicativo com as configurações de compatibilidade. Como em qualquer um dos cenários, o usuário pode informar ao PCA que o aplicativo foi executado corretamente ou recusar as configurações recomendadas clicando no botão fechar. Nesse caso, o PCA aplica o modo de compatibilidade VIRTUALIZEDELETE. Uma caixa de diálogo de exemplo é fornecida abaixo:

![o aplicativo falha ao tentar excluir a caixa de diálogo arquivos não Windows protegidos](images/pcafigure8.png)

**O aplicativo falha ao tentar modificar os arquivos do Windows ou as chaves do registro**

Alguns aplicativos projetados para o Windows XP e anterior pressupõem que eles normalmente são executados com privilégios administrativos completos. Como um curso de comportamento normal do aplicativo, eles podem tentar modificar, excluir ou gravar arquivos protegidos do Windows (em arquivos de programas ou pastas do Windows) ou chaves do registro pertencentes ao Windows. Quando qualquer uma das operações de gravação, exclusão ou modificação de um arquivo ou de uma chave de registro falha, muitos aplicativos podem falhar ou falhar incorretamente.

O PCA detecta esses aplicativos que não conseguem gravar em arquivos protegidos do Windows ou chaves do registro e fornece uma recomendação ao usuário quando o aplicativo é encerrado. O PCA permitirá que o usuário execute novamente o aplicativo com as configurações de compatibilidade. Como em qualquer um dos cenários, o usuário pode informar ao PCA que o aplicativo foi executado corretamente ou recusar as configurações recomendadas clicando no botão fechar. Nesse caso, o PCA aplica o modo de compatibilidade WRPMITIGATION. Uma caixa de diálogo de exemplo é fornecida abaixo:

![falha do aplicativo ao tentar modificar os arquivos do Windows ou a caixa de diálogo de chaves do registro](images/pcafigure9.png)

**O aplicativo falha devido ao uso de modos de cor de 8 ou 16 bits**

Como parte da releitura do Windows 8 para aplicativos da Windows Store, uma das principais alterações é que o Gerenciador de Janelas da Área de Trabalho (DWM) agora dará suporte apenas a cores de 32 bits no Windows 8. Os modos de cor inferior agora são simulados.

Muitos aplicativos e jogos mais antigos projetados para o Windows XP ou antes usam modos de cores de 8 ou 16 bits. Sem mitigação, esses aplicativos poderiam falhar ao serem executados no Windows 8. No entanto, quando esses aplicativos enumeram ou tentam usar qualquer um dos modos de cor de 8 ou 16 bits para exibição, o PCA identifica imediatamente o problema e com a ajuda do DWM, garante que o aplicativo funcionará corretamente com o modo de cores simulado.

Observe que isso acontece assim que o aplicativo solicita os modos de cor baixa e é transparente para o usuário. O usuário não precisa reiniciar o aplicativo para obter essa mitigação, pois essa correção é sempre necessária para garantir que o aplicativo funcione corretamente.

**Falha do aplicativo devido a problemas de gráficos e de exibição**

Como a Gerenciador de Janelas da Área de Trabalho (DWM) está sempre ativa no Windows 8, alguns aplicativos da era mais antigos do Windows XP poderão falhar se o aplicativo usar APIs de gráficos de modo misto, como no uso de APIs GDI e DirectX para desenhar na tela (jogos mais antigos) e tentar usar o modo de tela inteira:

-   O DWM impedirá a pintura diretamente para a área de trabalho, e o jogo ou o aplicativo irá falhar ou desenhar uma tela preta na área de trabalho e nenhum dos elementos gráficos estará visível
-   Nesses casos, quando o aplicativo é encerrado, o Windows detecta que o aplicativo ou jogo tem um problema com o modo de tela inteira e aplica o modo de compatibilidade de DXMAXIMIZEDWINDOWEDMODE que permite que o aplicativo ou jogo seja executado em um modo de janela Maximizado em vez de um modo de tela inteira
-   Depois que a configuração for aplicada ao final da execução, o usuário será notificado pelo PCA, como mostrado abaixo; o aplicativo obterá o modo de compatibilidade na próxima execução e poderá ser executado corretamente

![falha do aplicativo devido a uma caixa de diálogo de problemas de gráficos e de exibição](images/pcafigure10.png)

**Falha do aplicativo ao declarar reconhecimento de DPI**

Outro problema de exibição típico com muitos aplicativos mais antigos acontece quando o Windows e o aplicativo são executados no modo de alto DPI, mas o aplicativo não declara seu reconhecimento de DPI alto por meio de seu manifesto EXE. Entre os problemas comuns que podem ocorrer devido a essa incompatibilidade nas configurações estão elementos de interface do usuário recortados ou texto e tamanho de fonte incorreto. Para obter mais detalhes sobre os problemas, consulte este link [aqui](/previous-versions//dd464660(v=vs.85)).

Nesses casos, o Windows detecta que o aplicativo tem reconhecimento de DPI alta e aplica o modo de compatibilidade de HIGHDPIAWARE ao aplicativo no final da primeira execução. O PCA irá informar o usuário sobre isso, conforme mostrado abaixo:

![o aplicativo falha ao declarar a caixa de diálogo reconhecimento de DPI](images/pcafigure11.png)

**Falha do aplicativo devido a recursos do Windows ausentes**

Alguns aplicativos dependem de recursos do Windows que foram removidos desde o Windows Vista. Quando esses aplicativos tentam carregar as DLLs ou os componentes COM ausentes, eles não funcionam.

O PCA detecta aplicativos quando tenta carregar os recursos do Windows ausentes e fornece uma recomendação para baixar esses componentes e instalá-los após a finalização do aplicativo. O usuário pode clicar em ' obter ajuda online ' para encontrar uma alternativa ou baixar o recurso e instalá-lo. Se necessário, o usuário pode optar por não fazer nada clicando em fechar.

![falha do aplicativo devido à caixa de diálogo de recursos do Windows ausente](images/pcafigure12.png)

**O aplicativo falha devido a drivers não assinados no Windows 8 de 64 bits**

o Windows de 64 bits exigiu drivers assinados digitalmente (arquivos SYS) desde o Windows Vista. No entanto, os aplicativos mais antigos criados antes do lançamento do Windows Vista enviaram drivers que não foram assinados digitalmente. Se esse driver não assinado estiver instalado, o Windows não os carregará. Em casos raros, é possível que o Windows não seja iniciado se esses drivers estiverem marcados como drivers de tempo de inicialização.

Alguns aplicativos mais antigos instalam drivers que não são assinados em janelas de 64 bits. Qualquer dispositivo ou aplicativo que tente usar esse driver poderá falhar ou resultar em uma falha do sistema. Para evitar esse cenário, o PCA detecta aplicativos ao instalar drivers não assinados e desabilita o driver que está marcado como um driver de tempo de inicialização.

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

Os instaladores de aplicativos da área de trabalho do Windows exigem privilégios administrativos, pois gravam arquivos, pastas e entradas do registro em áreas do sistema protegidas. O Windows (UAC) tem lógica de detecção para identificar quando um instalador é executado e imediatamente solicita que o usuário forneça privilégios administrativos por meio da caixa de diálogo UAC. No entanto, em alguns casos, essa lógica não será capaz de determinar que um aplicativo era realmente um instalador e pode não obter privilégios administrativos. Geralmente, eles são instaladores personalizados que não usam tecnologias de instalação bem conhecidas, como Windows Installer ou instalar o escudo.

Nesses casos, o PCA detecta que o instalador falhou ao gravar seus arquivos. No final, se a instalação com falha, o PCA fornecerá uma recomendação para aplicar as configurações de compatibilidade. Se o usuário optar por clicar em ' Executar programa ', o PCA aplicará o modo de compatibilidade RUNASADMIN e executará novamente o instalador. Se o usuário optar por fechar, nenhuma configuração será aplicada. Uma caixa de diálogo do PCA de exemplo é mostrada abaixo:

![Captura de tela que mostra um exemplo de uma caixa de diálogo para um instalador de aplicativo que precisa ser executado com privilégios administrativos.](images/pcafigure15.png)

Os miniaplicativos do painel de controle herdados que precisam ser executados com os miniaplicativos do painel de controle de privilégio administrativo geralmente alteram as configurações do sistema e precisam da capacidade de executar o administrador do AD. No entanto, aqueles escritos antes do Windows Vista não têm um manifesto EXE ou não têm a seção TRUSTINFO que declara o nível de privilégio que eles exigem. Quando esses applets são executados, o PCA os detecta e, no final da primeira execução, fornece uma recomendação para executar com as configurações administrativas. Se o usuário optar por clicar em ' Executar programa ', o PCA aplicará o modo de compatibilidade RUNASADMIN e executará novamente o instalador. Se o usuário optar por fechar, nenhuma configuração será aplicada. Uma caixa de diálogo do PCA de exemplo é mostrada abaixo:

![instaladores de aplicativo que precisam ser executados com a caixa de diálogo de privilégio administrativo](images/pcafigure16.png)

**Verificando as configurações recomendadas por meio de comentários do usuário**

No final de cada um dos cenários (depois que o aplicativo é executado com as configurações de compatibilidade recomendadas), o PCA perguntará ao usuário uma pergunta simples:

![verificando as configurações recomendadas por meio da caixa de diálogo de comentários do usuário](images/pcafigure17.png)

O usuário poderá fornecer comentários se o aplicativo funcionou ou falhou com a configuração de compatibilidade. Esses dados serão enviados anonimamente para a Microsoft. Isso ajuda a garantir que essas correções possam ser criadas no Windows 8 por meio do processo do Windows Update, para que os usuários futuros do Windows 8 não encontrem mais a falha do aplicativo e o PCA não precise mais controlar o aplicativo para a falha.

**Controlando problemas que não têm recomendações**

Os aplicativos podem falhar de várias maneiras diferentes por motivos de compatibilidade. O PCA rastreia muito mais problemas de compatibilidade do que o que está listado nos cenários acima. Nesses casos, muitas vezes, a manifestação do problema depende do aplicativo. Isso significa que alguns aplicativos manipulam esses problemas normalmente e se recuperam, enquanto outros não podem. Portanto, para esses problemas, embora o PCA ainda acompanhe o aplicativo, ele não fornece uma recomendação direta para uma correção.

Os problemas que o PCA rastreia que não têm uma configuração recomendada ou uma caixa de diálogo incluem aplicativos que:

-   Ter um tempo de execução muito curto – os aplicativos são executados por no máximo três segundos
-   Criar objetos de memória global sem privilégios administrativos
-   Ter um erro (exceção Win32) na inicialização
-   Verificar o privilégio administrativo (mas pode não falhar)
-   Usar codecs Indeos (preteridos do Windows Vista)
-   Tente gravar ou excluir chaves de locais de registro protegidos, como HKLM
-   Falha na inicialização

**Aplicando correções por meio da guia compatibilidade e solução de problemas de compatibilidade**

Conforme mencionado acima, os aplicativos podem falhar por vários motivos de compatibilidade. Nem todas elas têm uma recomendação do PCA clara, pois as configurações dependem do aplicativo. No entanto, os usuários podem acessar a solução de problemas de compatibilidade ou a guia compatibilidade para aplicar determinadas correções comuns para tentar fazer com que seu aplicativo com falha funcione corretamente no Windows 8. Nesses casos, o PCA ainda acompanhará o aplicativo em busca de problemas de compatibilidade, antes e depois da correção ser aplicada. Depois que o aplicativo for executado com a correção aplicada, o PCA perguntará ao usuário se a correção funcionou. Depois que o usuário responde à pergunta, os dados são enviados anonimamente por meio da telemetria para a Microsoft. Esses dados são coletados de muitos usuários e analisados, e as correções qualificadas são amplamente distribuídas para todos os usuários do Windows 8 por meio do Windows Update.

**Usando a solução de problemas de compatibilidade**

O solucionador de problemas de compatibilidade é um mecanismo do Windows que permite diagnosticar problemas com aplicativos e aplicar correções recomendadas para que eles funcionem corretamente. Isso é necessário somente quando o PCA não fornece nenhuma recomendação para o aplicativo.

A solução de problemas permite que os usuários percorram e respondam a um conjunto de perguntas e, com base nas respostas, apliquem um conjunto de correções e permitam que os usuários testem seus aplicativos e verifiquem as correções. Depois de verificadas, as correções serão aplicadas permanentemente aos aplicativos para que funcionem melhor no Windows 8.

A interface do usuário da solução de problemas é mostrada abaixo para referência:

![usando a caixa de diálogo solução de problemas de compatibilidade](images/pcafigure18.png)

Você pode iniciar a solução de problemas de compatibilidade de duas maneiras:

**Na tela inicial:**

1.  Tipo: solução de problemas de compatibilidade
2.  Na seção Configurações, clique no bloco ' executar programas feitos para a versão anterior do Windows '

  
**No bloco do aplicativo:**

1.  Na tela iniciar, clique com o botão direito do mouse no bloco do aplicativo
2.  Clique em ' abrir local do arquivo ' (somente aplicativos da área de trabalho)
3.  Na faixa de para do Explorer, clique na ' guia do aplicativo '
4.  Escolha ' solução de problemas de compatibilidade '

  


**Usando a guia Compatibilidade**

Observe que isso é recomendado apenas para usuários que são especialistas na tentativa de configurações de compatibilidade diferentes. Esse método não fornece nenhuma recomendação do tipo de correção a ser aplicada aos aplicativos. Aqui, espera-se que o usuário saiba quais correções podem ser aplicadas para fazer o aplicativo funcionar. Se você não tiver certeza das correções, use a solução de problemas de compatibilidade para encontrar uma correção para o aplicativo.

Para acessar a guia Compatibilidade:

 **Na tela inicial:**

1.  Clique com o botão direito do mouse no bloco do aplicativo
2.  Abrir local do arquivo (somente aplicativos da área de trabalho)

  
**Na faixa de faixas do Explorer:**

1.  Clique em Propriedades
2.  Navegue até a guia Compatibilidade
3.  Selecionar as correções de compatibilidade
4.  Executar novamente o aplicativo
    > [!Note]  
    > Você pode voltar para o mesmo local novamente para alterar ou remover as correções também. Você também pode aplicar as correções a todos os usuários no computador usando o botão fornecido na guia.

     

  


![usando a guia Compatibilidade](images/pcafigure19.png)

**Aplicativos com problemas de compatibilidade conhecidos**

Além dos cenários de detecção de problemas de tempo de execução listados acima, o PCA também informa os usuários na inicialização do aplicativo se o aplicativo tiver problemas de compatibilidade conhecidos. A lista é armazenada no banco de dados de compatibilidade de aplicativos do sistema. Há dois tipos de mensagens:

-   **Mensagens de bloqueio rígido**— se o aplicativo for conhecido como incompatível e, se permitir que o aplicativo seja executado, resultará em um impacto grave no sistema (por exemplo, uma falha do Windows ou não poderá ser inicializado após a instalação), uma mensagem de bloqueio, conforme mostrado abaixo, será exibida

![aplicativos com problemas de compatibilidade conhecidos – caixa de diálogo mensagens de bloqueio físico](images/pcafigure20.png)

-   **Mensagens de bloqueio flexível**– se o aplicativo tiver um problema de compatibilidade conhecido e puder não funcionar corretamente, essa mensagem será mostrada:

![aplicativos com problemas de compatibilidade conhecidos – caixa de diálogo mensagens de bloqueio flexível](images/pcafigure21.png)

Em ambos os casos, a opção ' obter ajuda online ' envia um relatório de erros do Windows para obter uma resposta online da Microsoft e exibi-la para o usuário. Normalmente, as respostas apontarão o usuário para um dos três tipos de recursos:

-   Uma atualização do fornecedor do aplicativo
-   Um site do fornecedor do aplicativo para obter mais informações
-   Um artigo da base de dados de conhecimento Microsoft para obter mais informações

**Telemetria para o PCA**

Depois que o PCA solucionar qualquer problema de aplicativo em um computador com Windows 8 e obter todos os comentários do usuário, ele coletará dados anônimos sobre o aplicativo, o instalador, os problemas detectados e as configurações de compatibilidade aplicadas ao aplicativo e os enviará de volta à Microsoft. Esses dados são coletados de qualquer usuário que esteja disposto a fornecer esses dados anônimos (por meio do Programa de Aperfeiçoamento da Experiência do Usuário-CEIP). Depois que esses dados são coletados, as falhas e as correções do aplicativo são analisadas, e as correções são distribuídas para todo o ecossistema do Windows por meio do mecanismo de Windows Update, de forma que qualquer usuário do aplicativo no futuro se beneficie automaticamente da correção.

**Controles administrativos e gerenciando configurações do PCA**

Os administradores de ti podem controlar o comportamento do PCA de duas maneiras:

-   Desligar o **PCA** – essa configuração permite que os administradores de ti desativem as caixas de diálogo que o PCA mostra para os usuários; O PCA ainda acompanhará e detectará problemas e enviará telemetria de volta
-   Desligar a **telemetria do aplicativo** – essa configuração desativará qualquer coleção e envio de dados de telemetria pelo PCA
    > [!Note]  
    > Se o CEIP estiver desativado, essa configuração não terá nenhum impacto.

     

**Criando aplicativos para trabalhar com o PCA**

Os desenvolvedores precisam garantir que seus aplicativos funcionarão bem em todos os cenários de compatibilidade descritos acima. Os desenvolvedores devem testar e validar seus aplicativos para cada um dos cenários acima e garantir que não haja nenhum problema de compatibilidade. Se forem identificados problemas de compatibilidade, os desenvolvedores devem fazer correções em seus aplicativos necessários para garantir que o problema de compatibilidade seja resolvido. Algumas das correções comuns que os desenvolvedores devem fazer incluem:

-   Eliminar verificações de versão do sistema operacional Windows na instalação e no tempo de execução
-   Eliminar verificação de privilégios (verificando o acesso de administrador); Use o manifesto EXE para declarar o nível certo de privilégio necessário
-   Verifique se os binários do Windows não foram enviados no instalador do aplicativo
-   Elimine a gravação em áreas protegidas (registro, pastas) ou gravação de arquivos protegidos
-   Assinar digitalmente todos os binários (arquivos EXE, DLL, SYS)
-   Para instaladores, verifique se a entrada apropriada de ' Adicionar/remover programas ' foi adicionada; no mínimo, essa entrada de metadados de aplicativo deve incluir o nome do aplicativo, o editor, a cadeia de caracteres de versão e o idioma com suporte. Isso indicará ao PCA que o instalador foi concluído com êxito e também fornecerá uma maneira conveniente para que os usuários desinstalem o aplicativo

Garantir que a seção TRUSTINFO e compatibilidade do manifesto do aplicativo (executável) seja atualizada conforme listado no manual de compatibilidade do Windows 8 permitirá que o PCA saiba que o aplicativo foi projetado para o Windows 8 e também garantirá que o aplicativo sempre seja executado nativamente sem nenhum modo de compatibilidade aplicado a ele.

Para garantir que o PCA considere o aplicativo a ser projetado para o Windows 8:

-   Todos os EXEs (instalador ou tempo de execução) devem ser manifestados para as seções de TRUSTINFO e compatibilidade do Windows 8
-   O instalador deve adicionar uma entrada ' Adicionar/remover programas '

**Glossário**

Os modos de compatibilidade usados pelo PCA são listados abaixo com uma breve descrição do que o modo habilita.



| Mode                         | Descrição                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows7RTM                  | Esse modo emula o comportamento comum do Windows 7, incluindo o número de versão do sistema operacional 6,1                                                                   |
| WindowsVistaSP2              | Esse modo emula o comportamento comum do Windows 7, incluindo o número de versão do sistema operacional 6,1                                                                   |
| WindowsXPSp3                 | Esse modo emula o comportamento comum do Windows XP SP3, incluindo o número de versão do sistema operacional 5,1. Isso também inclui o modo RUNASHIGHEST                    |
| RUNASHIGHEST                 | Esse modo solicita que o usuário execute o aplicativo com o privilégio mais alto disponível. Os usuários com privilégios administrativos verão um prompt de elevação do UAC para o aplicativo |
| RUNASADMIN                   | Esse modo sempre solicita que o usuário execute o aplicativo com privilégios administrativos; aplicativos com esse modo sempre receberão a solicitação de elevação do UAC                    |
| ELEVATECREATEPROCESS         | Esse modo faz com que os processos filho do aplicativo principal sejam executados com privilégios administrativos; os processos filho receberão uma caixa de diálogo de elevação do UAC                          |
| PINDLL                       | Esse modo força uma DLL a ficar na memória de um aplicativo, mesmo que o aplicativo descarregue a DLL                                                                                |
| DISABLEUSERCALLBACKEXCEPTION | Esse modo intercepta as exceções de retorno de chamada do usuário e permite que o aplicativo continue sem a necessidade de lidar com a exceção                                          |
| VIRTUALIZEDELETE             | Esse modo intercepta as operações de exclusão nos arquivos protegidos e impede que os aplicativos falhem devido a exceções sem tratamento da operação de exclusão                   |
| WRPMITIGATION                | Esse modo retorna êxito quando um aplicativo tenta gravar, modificar ou excluir arquivos protegidos do Windows ou entradas de registro (sem realmente concluir a operação)  |
| DXMAXIMIZEDWINDOWEDMODE      | Esse modo identifica os aplicativos que entram no modo de tela inteira e os redireciona para um modo de janela Maximizado                                                          |
| HIGHDPIAWARE                 | Esse modo permite que o restante do Windows saiba que o aplicativo tem reconhecimento de DPI alta e ajuda a renderização adequada de elementos da interface do usuário, texto, fonte, etc.                              |



 

 

 