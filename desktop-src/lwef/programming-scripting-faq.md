---
title: Perguntas frequentes sobre programação de scripts
description: Perguntas frequentes sobre programação de scripts
ms.assetid: 84078c5b-7b04-48fa-9d0a-d95393c323eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dec468eb5147968ca0db774f081212a78cf40d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004774"
---
# <a name="programming-scripting-faq"></a>Perguntas frequentes sobre programação de scripts

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

### <a name="when-i-use-microsoft-visual-basic-or-other-development-tools-for-scripting-microsoft-agent-i-do-not-see-all-the-properties-and-events-used-in-your-samples-how-do-i-access-them"></a>Quando uso o Microsoft Visual Basic (ou outras ferramentas de desenvolvimento) para gerar scripts no Microsoft Agent, não vejo todas as propriedades e os eventos usados em seus exemplos. Como fazer acessá-los?

A maioria dos eventos, métodos e propriedades com suporte pelo controle do Microsoft Agent é exposta somente em tempo de execução. Consulte [programação do controle do Microsoft Agent](programming-the-microsoft-agent-control.md) para obter mais informações.

### <a name="the-map-tag-or-some-other-tag-doesnt-seem-to-work"></a>A marca de mapa (ou alguma outra marca) não parece funcionar.

Algumas marcas incluem cadeias de caracteres entre aspas. Para algumas linguagens de programação, como Microsoft Visual Basic e Visual Basic Scripting Edition, talvez seja necessário usar duas aspas para designar o parâmetro da marca ou concatenar um caractere de aspas duplas como parte da cadeia de caracteres. O último é mostrado neste Visual Basic exemplo:

Agent1. Characters ("gênio"). Fale "é \\ map =" + Chr (34) + "texto falado" \_ + Chr (34) + "=" + Chr (34) + "texto de balão" + Chr (34) + " \\ ."

Para a programação C, C++ e Java, preceda as barras invertidas e aspas duplas com uma barra invertida. Por exemplo:

BSTR bszSpeak = SysAllocString (L "é \\ \\ map = \\ " texto falado \\ "= \\ " texto de balão \\ " \\ \\ ");

pCharacter->falar (bszSpeak,......);

> [!Note]  
> O Microsoft Agent não oferece suporte a todas as marcas especificadas no Microsoft Speech API. Além disso, o suporte para alguns parâmetros pode depender do mecanismo de conversão de texto em fala instalado. Para obter mais informações, consulte [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md).

 

### <a name="i-dont-seem-to-get-requeststart-and-requestcomplete-events-in-my-script-or-program"></a>Não parece obter eventos RequestStart e RequestComplete em meu script (ou programa).

Isso pode ser causado por um dos seguintes problemas:

-   Sua linguagem de programação não dá suporte total a controles ActiveX. Verifique sua documentação para garantir que ela dê suporte à interface e aos eventos do ActiveX para objetos ActiveX.
-   Em uma página da Web com script, não foi possível instalar ou carregar outro controle. Verifique se todos os outros controles estão instalados e carregando corretamente sem o Microsoft Agent.
-   Em uma página da Web com script com quadros, você tem a `<OBJECT>` marca para o controle do Microsoft Agent em uma página e os eventos com script em outra página. Os eventos são enviados somente para a página que hospeda o controle.

### <a name="i-am-using-the-microsoft-agent-control-with-other-activex-controls-on-my-webpage-and-i-dont-seem-to-get-any-events"></a>Estou usando o controle de agente da Microsoft com outros controles ActiveX na minha página da Web, e não parece ter nenhum evento.

Verifique se os outros controles estão instalados corretamente. Se outro controle ActiveX falhar em registrar-se corretamente, o controle do Microsoft Agent poderá receber seus eventos.

### <a name="what-programming-languages-can-i-use-to-program-the-microsoft-agent-control"></a>Quais linguagens de programação posso usar para programar o Microsoft Agent Control?

O Microsoft Agent deve ser compatível com qualquer linguagem que dê suporte à interface do ActiveX. Ele inclui exemplos de código para Visual Basic, VBScript, JScript, C/C++ e Java.

### <a name="can-i-access-the-parameters-returned-from-microsoft-agent-using-jscript"></a>Posso acessar os parâmetros retornados do Microsoft Agent usando o JScript?

Sim, mas atualmente a única maneira de fazer isso é usando a `<SCRIPT LANGUAGE="JScript" FOR="*object*" EVENT="event()">` sintaxe. Embora essa sintaxe tenha suporte para o Microsoft Internet Explorer, outros navegadores não dão suporte a ela, portanto, convém evitar o uso do JScript para essa parte do script de sua página.

### <a name="can-microsoft-agent-be-used-with-speech-recognition-or-speech-synthesis-text-to-speech-or-tts-engines-other-than-those-supplied-by-microsoft"></a>O Microsoft Agent pode ser usado com mecanismos de reconhecimento de fala ou de síntese de fala (conversão de texto em fala ou TTS) diferentes daqueles fornecidos pela Microsoft?

Sim, desde que o mecanismo dê suporte às interfaces do Microsoft Speech API (SAPI) 4,0 exigidas pelo Microsoft Agent. Verifique com o fornecedor do mecanismo. Para obter detalhes completos sobre as interfaces SAPI exigidas pelo Microsoft Agent, consulte [requisitos de suporte do mecanismo de fala](speech-engine-support-requirements.md).

### <a name="my-page-includes-html-object-tags-for-microsoft-agent-the-lernout--hauspie-truvoice-tts-engine-and-the-microsoft-command-and-control-speech-recognition-engine-but-not-all-the-components-install"></a>Minha página inclui marcas de objeto HTML para o Microsoft Agent, o mecanismo Lernout & Hauspie TruVoice TTS e o mecanismo de reconhecimento de fala de comando e controle da Microsoft, mas nem todos os componentes são instalados.

Normalmente, o problema pode ser corrigido atualizando a página. Como uma prática geral, é melhor especificar primeiro a marca de controle do Microsoft Agent `<OBJECT>` , depois o mecanismo de reconhecimento de fala de Lernout & Hauspie, em seguida, o comando e controlar o mecanismo.

### <a name="after-calling-the-moveto-method-my-character-seems-to-freeze-even-though-i-have-return-animations-assigned-to-moving-state-animations"></a>Depois de chamar o método MoveTo, meu caractere parece congelar, embora eu tenha animações de retorno atribuídas à movimentação de animações de estado.

Quando você joga uma animação, os serviços de animação continuam a exibir seu último quadro até que outra animação seja chamada. Portanto, você deve reproduzir outra animação depois de chamar [**MoveTo**](moveto-method.md). Se você tiver definido uma animação de **retorno** para a animação do estado **móvel** , o servidor a executará primeiro.

### <a name="when-i-query-the-characters-pitch-property-it-returns-a-value-of--1"></a>Quando eu consulta a propriedade Pitch do caractere, ela retorna um valor de-1.

Isso ocorre se o caractere tiver sido compilado usando a propriedade de densidade padrão de um mecanismo de fala; ou seja, a inclinação não foi alterada quando o caractere foi compilado.

### <a name="when-my-code-attempts-to-set-the-tts-mode-id-for-a-text-to-speech-engine-i-get-the-following-error-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Quando meu código tenta definir a ID do modo TTS para um mecanismo de conversão de texto em fala, obtenho o seguinte erro: uma chamada de saída não pode ser feita porque o aplicativo está expedindo uma chamada de entrada síncrona.

Para definir a propriedade TTSModeID, você deve ter Speech.dll instalado. Normalmente, isso é uma parte do código de instalação do mecanismo de fala. Você também pode instalar isso instalando o painel de controle do objeto de fala, disponível na página de downloads do Microsoft Agent.

### <a name="when-i-retry-loading-a-character-that-failed-to-load-the-call-fails-with-a-character-already-loaded-error"></a>Ao tentar carregar novamente um caractere que falhou ao ser carregado, a chamada falha com um erro "caractere já carregado".

O controle do Microsoft Agent não descarrega um objeto Character (libere a referência) quando seu arquivo de caractere associado não for carregado. Se você quiser tentar carregar o caractere novamente, deverá chamar [**Unload**](unload-method.md) explicitamente antes de chamar [**Load**](load-method.md) da segunda vez. Se você tentar isso a partir de um script de página da Web, também precisará preceder a chamada **Unload** com uma instrução On Error continue Next ou a chamada **Unload** também falhará. (Observe que o JScript não tem o erro retomar a próxima instrução.)

No entanto, talvez você não precise incluir o código para repetir o carregamento de um caractere imediatamente quando o arquivo falhar ao ser carregado. O Microsoft Internet Explorer e o componente de servidor do Microsoft Agent tentam tentar novamente várias vezes, portanto, as chances de que sua repetição resulte em uma carga bem-sucedida sejam remotas. Uma estratégia melhor é aguardar (definir um temporizador) alguns segundos antes de tentar novamente.

### <a name="how-can-i-install-microsoft-agent-as-part-of-my-application-or-from-my-web-server"></a>Como posso instalar o Microsoft Agent como parte do meu aplicativo ou do meu servidor Web?

Você pode instalar o agente do site da Microsoft, incluindo seu *CLSID em uma marca de objeto HTML*. No entanto, se desejar incluir e instalar o agente do seu próprio programa de instalação de aplicativo ou de seu próprio servidor, você deverá baixar o arquivo de gabinete de autoinstalação do Microsoft Agent, baixando-o da página de downloads. Ao baixar, escolha a opção salvar em vez de executar do navegador. Sempre que esse arquivo for executado, ele instalará automaticamente o Microsoft Agent no computador de destino. Portanto, você pode especificar o arquivo em seu script de instalação.

Não tente instalar o Microsoft Agent copiando seus vários. DLLs e tentando registrá-la por conta própria. A tentativa de instalar o agente por outros meios significa que não há suporte para executar seu arquivo de gabinete de autoinstalação.

O sistema de destino também deve incluir versões recentes do MSVCRT.DLL (VC + + Runtime), REGSVR32.EXE (ferramenta de registro incluída no Microsoft VC + +) e COM. A melhor maneira de garantir que as versões corretas estejam instaladas é exigir que o Microsoft Internet Explorer 3, 2 ou posterior esteja instalado. No entanto, você também pode licenciar esses requisitos de tempo de execução. (Para a versão mais recente do COM, acesse a atualização DCOM do site da Microsoft.)

O Microsoft Agent 2,0 não será instalado no Microsoft Windows 2000, pois esta versão do sistema operacional já inclui o Agent.

### <a name="can-i-use-the-visual-basic-setup-wizard-to-install-microsoft-agent"></a>Posso usar o assistente de instalação do Visual Basic para instalar o Microsoft Agent?

Embora você possa criar seu próprio programa de instalação usando o Visual Basic (VB), não é possível usar o assistente de instalação do Visual Basic para fazer isso. Para instalar o agente do VB, você pode usar o comando do Shell, especificando o arquivo de gabinete de instalação automática do Microsoft Agent.

### <a name="how-do-i-install-microsoft-agent-on-windows-2000"></a>Como fazer instalar o Microsoft Agent no Windows 2000?

O Microsoft Agent 2,0 não é instalado no Windows 2000 porque já está incluído como parte do sistema operacional.

### <a name="agentsvr-crashes-when-speak-is-called-with-a-wav-file"></a>AgentSvr falha quando a fala é chamada com um arquivo WAV.

Isso pode ocorrer quando o caractere usa o TTS para saída falada e, em seguida, muda para usar um arquivo WAV. O texto não foi fornecido no primeiro parâmetro do método Speak.

Para evitar a falha, inclua um caractere de espaço no primeiro parâmetro do método Speak, mesmo que você não tenha nenhuma saída de texto.

### <a name="even-though-i-have-already-installed-the-agent-language-component-dll-for-a-particular-language-i-still-got-an-error-that-the-component-is-missing-when-i-set-the-characters-language-to-that-language"></a>Embora eu já tenha instalado o componente de linguagem do agente (DLL) para um idioma específico, ainda tenho um erro de que o componente está ausente quando eu defini o idioma do caractere para esse idioma.

Isso geralmente acontece quando você tem aplicativos de agente como o Microsoft Office 2000 aberto ao instalar o componente de idioma do agente. Feche todos os aplicativos e tente novamente. Se o problema persistir, reinicie o computador e você poderá definir a ID do idioma agora.

### <a name="when-i-use-the-ampersand--symbol-the-text-around-the-symbol-in-the-characters-word-balloons-is-truncated"></a>Quando uso o símbolo de "&" e comercial, o texto em volta do símbolo nos balões de palavras do caractere é truncado.

Este é um problema conhecido. Você pode contornar isso usando a marca de mapa. Por exemplo, para exibir "A & B" no balão de palavras do caractere, use "A \\ map =" e "=" && " \\ B" na instrução Speak.

### <a name="my-application-allows-users-to-change-the-default-character-and-when-they-do-the-program-crashes"></a>Meu aplicativo permite que os usuários alterem o caractere padrão e, quando fazem isso, o programa falha.

Há duas causas possíveis:

Se você alterar a ID do modo TTS do caractere padrão e permitir que o usuário altere o caractere padrão por meio de ShowDefaultCharacterProperties, AgentSvr falhará.

Esse problema foi corrigido nos sistemas operacionais Windows 2000 e Windows XP. Para evitar a falha em outras plataformas, você não deve permitir que o usuário altere o caractere padrão depois de alterar a ID do modo TTS do caractere padrão ou não usar o caractere padrão em seu aplicativo ou página da Web.

Se seu aplicativo não usar caracteres de agente fornecidos pela Microsoft, verifique se o caractere personalizado usa uma paleta com uma paleta completa de 256 cores. Para obter mais informações, consulte o documento criando caracteres para o Microsoft Agent.

### <a name="my-page-loads-the-agent-character-from-multiple-frames-with-ie-5-i-get-the-microsoft-agent-failed-to-load-error"></a>Minha página carrega o caractere do agente de vários quadros. Com o IE 5, obtenho um erro ao carregar o Microsoft Agent.

Esse é um problema conhecido com o IE 5. Houve uma alteração na forma como o navegador manipula um determinado evento, o que faz com que o script HTML comece a ser executado antes que AgentSvr seja iniciado. Para fazer com que sua página funcione com todas as versões do navegador, você precisa adicionar essa linha ao seu script:

AgentControl. Connected = true

que cria explicitamente uma conexão com o AgentSvr. Observe que você só precisa fazer isso se a página carregar o agente de vários quadros.

### <a name="when-my-application-tries-to-install-microsoft-agent-on-windows-2000-or-windows-xp-i-get-the-error-that-agent-is-not-compatible-with-windows-2000-or-windows-xp"></a>Quando meu aplicativo tenta instalar o Microsoft Agent no Windows 2000 (ou no Windows XP), obtenho o erro de que o Agent não é compatível com o Windows 2000 (ou Windows XP).

Uma versão anterior do arquivo de gabinete do componente principal do Agent MSAGENT.exe, quando executada no Windows 2000 (e no Windows XP), bloqueará a instalação e exibirá uma mensagem de erro imprecisa que o Agent não é compatível com a versão do sistema operacional que você está executando. Na verdade, os componentes principais do Microsoft Agent 2,0 são incluídos como parte do Windows 2000 (e do Windows XP) e já estão instalados por padrão por meio da instalação do Windows.

Nesta versão, a verificação é removida e o arquivo de instalação não exibe a mensagem de erro mencionada anteriormente no Windows 2000 (ou no Windows XP). Observe que essa é a única alteração no arquivo de instalação e não há nenhuma alteração de código para os componentes principais do agente. Portanto, você não será afetado por essa atualização se já tiver o Agent 2,0 instalado ou se seu site usar uma marca de objeto para disparar Downloads automáticos dos componentes principais do agente do armazenamento de objetos da Microsoft.

Se você incluir o arquivo de instalação do componente de núcleo do agente com seu aplicativo, ou se você publicar o arquivo de instalação no servidor, convém baixar essa atualização. Para fazer isso, clique aqui e selecione a opção "salvar este programa em disco". Você deve ter uma licença válida e de distribuição de agente atual para essas circunstâncias.

Como alternativa, você também pode contornar esse problema usando a opção silencioso ao instalar a versão anterior do arquivo de instalação do MSAGENT.exe. O comando do Shell é:

**MSAGENT.exe/q: a**

O mesmo se aplica aos componentes de idioma do agente que foram originalmente lançados em outubro de 1998. Houve uma verificação que impediria que os componentes árabe, francês, alemão, Hebraico, italiano, japonês, coreano, chinês simplificado, espanhol e chinês tradicional sejam instalados no Windows 2000 (e no Windows XP). As versões mais recentes desses arquivos de instalação, juntamente com os 19 idiomas adicionais, foram adicionados em março de 2000, não contêm essa verificação e serão instaladas com êxito no Windows 2000 (e no Windows XP).

### <a name="my-customized-character-exhibits-some-unexpected-behavior-with-its-transparency-color-on-windows-2000-and-windows-xp"></a>Meu caractere personalizado exibe algum comportamento inesperado com sua cor de transparência no Windows 2000 (e no Windows XP).

Esse é um problema conhecido para caracteres criados com uma paleta com menos de 256 cores. Problemas com esses caracteres incluem a cor de transparência mostrada em segundo plano, texto de balão transparente, borda de balão transparente ou plano de fundo de balão transparente. Observe que esses caracteres podem fazer com que seus aplicativos falhem quando carregados na caixa de diálogo Seletor de caracteres do agente ou na galeria do assistente de Microsoft Office. Seus caracteres personalizados devem usar uma paleta completa com 256 cores. Você pode usar a paleta de exemplo fornecida para caracteres do assistente do Office como um ponto de partida com uma paleta de cores 256 completa.

### <a name="the-character-does-not-use-the-british-english-tts-engine-even-though-i-have-set-its-language-id-to-british-english-h0809"></a>O caractere não usa o mecanismo de TTS em inglês britânico, embora tenha definido sua ID de idioma como inglês britânico &h0809.

Primeiro, verifique se você tem todos os componentes necessários instalados — componentes principais do agente, os binários de tempo de execução SAPI e um mecanismo de TTS em inglês britânico SAPI4 compatível, como o mecanismo TTS3000 britânico em inglês, disponível para download na página de downloads do agente. Se o seu caractere ainda não estiver usando o mecanismo de TTS em inglês britânico, é provável que você também tenha um mecanismo de TTS inglês americano instalado. Como o inglês britânico e o inglês americano compartilham o mesmo idioma principal (inglês) e inglês americano é o padrão, o Agent escolherá o primeiro mecanismo de TTS do inglês americano disponível, conforme retornado pelo SAPI. Para usar um mecanismo de TTS em inglês britânico, use a propriedade TTSModeID do caractere em vez disso. Por exemplo, o TTSModeID para a voz masculina de inglês britânico TTS3000 é {227A0E41-A92A-11d1-B17B-0020AFED142E}. No Microsoft Visual Basic você pode usar esse mecanismo definindo o TTSModeID da Merlin da seguinte maneira:

AgentControl. Characters ("Merlin"). TTSModeID = {227A0E41-A92A-11d1-B17B-0020AFED142E}

### <a name="when-the-characters-volume-is-set-to-zero-using-the-speech-tag-vol0-it-either-has-no-effects-or-crashes-the-agentsvr"></a>Quando o volume do caractere é definido como zero usando a marca de fala \\ vol = 0 \\ , ele não tem nenhum efeito ou cai Agentsvr.

Esse é um problema conhecido. Nos sistemas operacionais Windows 95, Windows 98 e Windows me, o volume do caractere não é alterado, mas permanecerá no nível definido anteriormente. Nas plataformas Windows NT 4,0, Windows 2000 e Windows XP, isso fará com que o AgentSvr falhe, mesmo quando um mecanismo de TTS não estiver instalado. Como o intervalo do volume do caractere, de 0 (silêncio) a 65535 (volume máximo), é grande e a diferença entre níveis sucessivos não é mais discernida, a solução fácil é definir o volume como 1 em vez de 0 quando você deseja que a voz do caractere seja inaudível.

### <a name="my-customized-characters-return-animation-does-not-play-correctly-after-the-movedown-moveleft-moveright-andor-moveup-animations"></a>A animação de retorno do meu caractere personalizado não é reproduzida corretamente após as animações MoveDown, MoveLeft, MoveRight e/ou MoveUp.

Certifique-se de que uma animação de fala simples seja atribuída ao estado de fala. Por exemplo, você pode usar um único quadro que consiste na posição neutra do caractere com sobreposições de boca.

 

 




