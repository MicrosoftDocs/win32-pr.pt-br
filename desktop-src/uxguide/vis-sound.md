---
title: Som
description: Som é o elemento de áudio da experiência do usuário.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5569fe76578fdb79b30da7cbad95939773889b0d22de92b0af4babe966ec6390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348608"
---
# <a name="sound"></a>Som

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

*Som* é o elemento de áudio da experiência do usuário. Quando usado adequadamente, o som pode ser uma forma efetiva de comunicação que estabelece uma relação não verbal e até mesmo emocional com seus usuários. Os sons podem ser usados sozinhos ou como um suplemento para a interface do usuário visual. Por exemplo, adicionar um efeito de som a uma notificação aumenta a probabilidade de que ela seja notada, especialmente se o usuário não estiver olhando para a tela quando um evento ocorrer.

![captura de tela da caixa de diálogo de som ](images/vis-sound-image1.png)

Na guia Sons do item do painel de controle de som, os usuários podem fazer alterações em seus sons do sistema.

Este artigo aborda o uso de sons em um programa como uma resposta a eventos e ações do usuário e a integração do controle de som de um programa com Windows. Ele não abrange o uso de música ou fala.

**Observação:** Diretrizes [relacionadas a notificações e](mess-notif.md) [identidade visual](exper-branding.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir se você deve usar som, considere estas perguntas:

-   **Há um benefício claro do usuário ao usar som?** Como as desvantagens de usar o som podem superar facilmente os benefícios, use o som somente quando houver uma vantagem clara.
-   **O uso de som é apropriado?** O uso de som chama a atenção para coisas que são importantes para a atenção? Os usuários perderiam o som se ele estivesse ausente? Concentre-se em sons que mantêm os usuários informados, provavelmente alterarão seu comportamento ou fornecerão comentários úteis.
-   **O uso de som causa distração?** Há sons frequentes, barulhentos e barulhentos? É provável que os usuários reduzam o volume do sistema ou o volume do programa como resultado do uso do som?
-   **Você está usando o som como uma forma principal de comunicação?** Em muitos casos, como para usuários que têm algum nível de perda auditiva, o som não deve ser usado como o principal meio de comunicação. O som é mais eficaz como um suplemento para outros meios de comunicação (como texto ou visuais).
-   **Os principais usuários de TI são profissionais de TI?** O som geralmente é ineficaz para tarefas direcionadas aos profissionais de TI porque muitas de suas tarefas são executadas de forma autônoma. Além disso, o som não é dimensionado para eles imaginem executar centenas de tarefas por vez e obter sons quando eles são concluídos ou falham.

## <a name="design-concepts"></a>Conceitos de design

Normalmente, o som atinge qualquer ou todas as seguintes finalidades:

-   **Notificação.** O som pode ser associado a eventos específicos. Por exemplo, um som de "novo email" informa aos usuários quando o email chega sem interromper sua tarefa atual.
-   **Feedback.** O som pode fornecer comentários para ações específicas do usuário. Por exemplo, um som sutil que é reproduzindo quando você libera o controle deslizante no controle de volume fornece comentários sobre o nível da configuração atual.
-   **Marca.** O som pode ser associado a conteúdo específico para a marca de seu produto, aplicativo ou serviço. Windows usa som dessa maneira para a inicialização do sistema operacional.
-   **Entretenimento.** O som é comumente usado para aprimorar produtos de entretenimento e tornar qualquer produto mais envolvente. Por exemplo, a maioria dos jogos, aplicativos de treinamento e produtos de consumidor usa som para animar os usuários e aprimorar sua experiência.

Determinados sons podem atender a várias dessas finalidades ao mesmo tempo. O Windows de inicialização, por exemplo, indica que o processo de inicialização foi concluído e que a área de trabalho está pronta para uso. Ele também fornece uma forma poderosa de identidade visual do produto e, até mesmo, envolve momentaneamente os usuários.

Sons que não cumprem nenhuma dessas finalidades provavelmente devem ser eliminados.

### <a name="inappropriate-use-of-sound"></a>Uso inadequado de som

**Apesar dos benefícios do som, o uso apropriado do som requer uma grande pressão para fazer de outra forma, o que pode tornar um programa entediante e uma distração.** Os usuários desligarão completamente o som se se tornarem desaloquesados por sons frequentes, repetitivos, repetitivos, interruptivos e mal projetados; em parte, isso é porque, por sua própria natureza, o som exige atenção e é difícil de ignorar. Para ver dicas sobre como encontrar um equilíbrio razoável, confira as [Diretrizes de design de som.](#sound-design)

Como as desvantagens de usar o som podem superar facilmente os benefícios, use o som somente quando houver uma vantagem clara. **Em caso de dúvida, não use som.**

### <a name="make-sound-supplemental"></a>Tornar o som complementar

Mesmo que o som seja usado adequadamente, há muitas situações em que o som pode não ser eficaz para todos os usuários:

-   Alguns usuários podem trabalhar em um ambiente barulhento em que os sons não podem ser ouvido.
-   Alguns usuários podem trabalhar em um ambiente silencioso que exige que o som seja desligado ou definido em um volume baixo.
-   Alguns usuários podem ter deficiências auditivas ou perda.
-   O computador pode não ter alto-falantes.

Por esses motivos, o som usado para notificações e comentários nunca deve ser o único método de **comunicação,** mas deve complementar dicas visuais ou textuais.

### <a name="desirable-characteristics-of-sound"></a>Características desejáveis do som

Em geral, os sons devem ser:

-   frequência média a alta (600 Hertz \[ Hz \] a 2 quilohertz \[ kHz \] ).
-   short (menos de um segundo).
-   soft ou moderado em volume.
-   Significativo.
-   não é alarme ou jarring.
-   não verbais.
-   não repetitivo.

Com o som, menos é mais. **O efeito de som ideal é aquele que os usuários mal notam, mas eles perderiam se estivesse ausente.**

**Um erro comum é que os sons para eventos críticos precisam ser altos e chamativas para chamar a atenção do usuário.** Isso não é verdade, porque o som é realmente destinado a ser um meio complementar de comunicação. No caso de uma mensagem de erro crítica, sua apresentação (talvez em uma caixa de diálogo modal), seu ícone (um ícone de erro) e seu texto e tom se combinam para comunicar a natureza do erro. Um som de erro efetivo pode ser ligeiramente mais baixo do que o som Windows som típico, mas não precisa ser significativamente barulhento.

### <a name="characteristics-of-windows-sounds"></a>Características de Windows sons

Além dessa chamada geral para minimalismo, o som do Windows usa tons claros, puros e sons frios e arescos, com um esmaecimento suave e esmaecimento ("bordas" suaves) para evitar efeitos percussivos, repentinos e jargões. Eles são projetados para se sentir sutis, ofensivos e consoantes. Windows sons usam eco, reverb e equalização para obter uma sensação natural e ambiente.

O esquema de som padrão para Windows geralmente não usa sons instrumentais ou reconhecíveis todos os dias que são muito específicos ou músicais. Exemplos de sons que ele evita são instrumentos músicais, como instrumentos de música, sons de animais, ruídos ambientais, fala, vozes, efeitos de som parecidos com o filme ou outros sons de humanos. Além disso, Windows sons não devem ser percebidos como música (ou seja, com várias notas). Isso faz Windows parece funcionalmente diferente de outros tipos de sons.

Como os Windows foram projetados profissionalmente para ter as características desejáveis e apelam para um público amplo, considere usar esses sons Windows integrados sempre que **apropriado.**

### <a name="designing-your-own-sounds"></a>Projetando seus próprios sons

Se você precisa criar seus próprios sons, projete-os para ter as características descritas anteriormente. Se esforça para fazer com que eles complementem suas tarefas ou eventos associados.

Entenda que a criação de sons originais é difícil de fazer bem, especialmente para sons destinados a um público amplo. O som pode ser um elemento de design polarizador. Para cada usuário que adora um som, haverá muitos que o desagradam.

**Projete os sons do programa como um grupo para parecer que eles são variações relacionadas em um tema.** A experiência auditiva do programa deve ser coordenada com sua experiência visual. Além disso, o "tom" dos sons deve ser coordenado com [o tom do texto](text-style-tone.md). Considere como o texto com um tom natural e agradável pode ser prejudicado quando acompanhado por sons agressivos e alarmes.

**Se você fizer apenas quatro coisas...**

1.  Use som com restrição, certifique-se de que haja um benefício geral claro do usuário. Em caso de dúvida, não use som.
2.  Use os sons de Windows integrados sempre que apropriado.
3.  Se você criar seus próprios sons, certifique-se de que eles têm as características de som desejáveis e, como um todo, parecem variações em um tema.
4.  Não suponha que os sons precisem ser altos e barulhentos para chamar a atenção do usuário.

## <a name="usage-patterns"></a>Padrões de uso

Os sons têm vários padrões de uso:



|     Uso de som                                                                                                                                                                 |  Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Conclusão da ação**<br/> notifica os usuários quando uma ação iniciada pelo usuário de longa execução é concluída com êxito. <br/>                             | ![captura de tela da caixa de diálogo de download de arquivo ](images/vis-sound-image2.png)<br/> Neste exemplo, a caixa de diálogo reproduz um som para notificar os usuários de que o download foi concluído.<br/>                                                                                                                                                                                                                                      |
| **Falha de ação**<br/> notifica os usuários quando uma ação iniciada pelo usuário de longa execução falha. <br/>                                                 | ![captura de tela da mensagem de disco de backup não acessível ](images/vis-sound-image3.png)<br/> Neste exemplo, Windows um som para notificar os usuários de que a operação de backup falhou.<br/>                                                                                                                                                                                                                                  |
| **Evento importante do sistema**<br/> alerta os usuários sobre eventos ou status importantes do sistema que exigem atenção imediata. <br/>                      | ![captura de tela da mensagem de bateria fraca ](images/vis-sound-image4.png)<br/> Neste exemplo, os usuários são alertados de que sua bateria fraca requer atenção imediata.<br/>                                                                                                                                                                                                                                                      |
| **Fyi**<br/> notifica os usuários de informações potencialmente úteis e relevantes. <br/>                                                                 | Como essas informações geralmente não exigem atenção imediata, um som fyi fornece comentários sutis sem quebrar o fluxo do usuário. <br/> ![captura de tela da mensagem de login do Live Messenger ](images/vis-sound-image5.png)<br/> Neste exemplo, um som é reproduzindo quando um contato entrar em um serviço de mensagens instantâneas.<br/>                                                                                 |
| **Efeito de som**<br/> fornece comentários sobre interações do usuário. <br/>                                                                            | Fornece comentários de som reais ou com estilo apropriados para a interação. os efeitos de som geralmente soam como se o usuário manipulava um objeto físico do mundo real. às vezes chamado de ltda. <br/> ![captura de tela da janela que está sendo minimizada ](images/vis-sound-image6.png)<br/> Neste exemplo, o efeito de minimizar o som da janela parece que um objeto do mundo real está sendo reduzido em tamanho.<br/> |
| **Sons de identidade visual**<br/> um som fornecido para aprimorar a experiência do usuário apesar do impacto emocional e, como um efeito colateral, promover a marca do produto. <br/> | Os sons de identidade visual são melhores quando sincronizados com eventos visuais, especialmente transições de interface do usuário, como a exibição de uma janela do programa. marcas de som verdadeiras indicam a origem de bens, semelhantes a uma palavra ou logotipo de marca registrada, e são relativamente incomuns. <br/> ![captura de tela do ícone de inicialização do Windows ](images/vis-sound-image7.png)<br/> Neste exemplo, a Windows inicialização é uma experiência de transição de marca.<br/>      |



 

## <a name="guidelines"></a>Diretrizes

### <a name="usage"></a>Uso

-   **Use som com restrição,** certifique-se de que haja um benefício geral claro do usuário. Concentre-se em sons que mantêm os usuários informados, provavelmente alterarão seu comportamento ou fornecerão comentários úteis. Em caso de dúvida, não use som.
-   **Selecione o som e suas características com base em como ele está sendo usado.** Para ver uma descrição de cada padrão de uso, consulte a tabela na seção anterior.
-   **Para notificações e comentários, não use o som como o único método de comunicação.** Em vez disso, use o som como um método complementar para reforçar as missões visuais ou textuais. Isso garante que os usuários possam ver as informações se não puderem ouvir o som.
-   **Não toque som alto ou barulhento com frequência.** Isso é desnecessário e resulta em uma experiência de usuário ruim. Quanto mais frequentemente um som é tocado, menos obtusivo ele deve ser. Os sons não devem ser altos ou difíceis para chamar a atenção.
-   **Não emitir um aviso.** Os avisos não são apropriados para programas modernos. Os avisos não podem ter significados específicos atribuídos a eles e os usuários não podem controlá-los.
    -   **Exceção:** As funções críticas do sistema podem emitir um aviso para alertar os usuários de situações que eles devem participar imediatamente, como baixa capacidade da bateria.

### <a name="playback"></a>Reprodução

-   **Não repita um som mais de duas vezes consecutivamente.**
-   **Para uma sequência consecutiva de eventos de som relacionados, toque um som somente no primeiro evento.** Evite usar vários sons, pois eles podem colidir entre si ou, de outra forma, resultar em uma experiência do usuário não agradável.

### <a name="sound-selection"></a>Seleção de som

-   **Escolha sons divertidos.** Não use sons desagradados e alarmes, como vibração, falha e falha.
-   **Use sons curtos** (menos de um segundo).
-   **Use sons que são aproximadamente o mesmo volume que o som Windows típico.** Os usuários não têm a responsabilidade de desligar o volume ao iniciar um computador ou programa, especialmente em ambientes públicos, como reuniões e apresentações. Os arquivos Windows de som da Microsoft estão localizados na pasta Mídia dentro da pasta Windows dados.
-   **Não escolha sons que exigem localização.** Você pode fazer isso usando sons que não usam fala ou têm significados ou conotações culturalmente dependentes.

### <a name="windows-system-sounds"></a>Windows do sistema

-   **Use os sons do sistema Windows integrado sempre que apropriado.**
-   **Opte por usar sons do sistema com base no significado associado, não apenas no próprio som.** Os sons do sistema devem ser usados consistentemente.

### <a name="sound-design"></a>Design de som

Ao criar seus próprios sons:

-   **Crie sons com as características de som desejáveis.**
-   **Compor sons com frequências principalmente médias a altas (600 Hz a 2 kHz).** Não use frequências baixas porque elas vão mais longe, são mais difíceis de localizar e podem ser alarmes.
-   **De definir a amplitude relativa de sons normais para o nível do som Windows típico.** Os Windows som foram nivelados adequadamente para ambientes domésticos e de trabalho. Usar níveis diferentes para seus sons força os usuários a fazer ajustes de volume.
    -   Definir sons importantes para ser ligeiramente mais barulhentos. Esses sons incluem preenchimentos de ação, falhas de ação e eventos importantes do sistema.
    -   Definir sons que ocorrem com frequência para serem ligeiramente mais suaves. Isso inclui FYIs, sons de identidade visual e efeitos de som.
-   **Escolher parece consistente com o significado dos Windows sons.** Para criar uma versão personalizada de um Windows, preserve o mesmo tom e intervalo, mas altere a orquestração ou o timbre. Não atribua significados diferentes a sons com tomes e intervalos semelhantes aos Windows sons.
-   **Projete os sons para que seu programa pareça que eles são variações relacionadas em um tema.** A experiência auditiva do programa deve ser coordenada com sua experiência visual.
    -   **Transições de cena de design e transições de áudio juntas.** Por exemplo, se uma cena esmaecer gradualmente, qualquer som também deverá esmaecer gradualmente. Não transições visuais perfeitas fazendo transições de som abruptas.
-   **Os sons devem estar no formato de arquivo .wav.** É recomendável o formato PCM (pulse code modular) estéreo de 44,1 kHz de 16 bits. Se o tamanho do arquivo for importante, use formatos compactados ouural (mono), mas esteja ciente de que há uma perda de qualidade facilmente perceptível que pode refletir mal em seu aplicativo.

### <a name="mixing"></a>Mistura

-   **Não tem controles de volume ou mudo em seu programa.** Em vez disso, permitir que os usuários controlem as configurações relativas de volume entre aplicativos com o Windows de volume. Se o programa tiver um controle de volume, haverá vários locais em que os usuários ajustam suas configurações, o que pode levar a confusão.

    ![captura de tela do mixer de volume do Windows ](images/vis-sound-image8.png)

    O Windows volume permite que os usuários controlem a configuração de volume principal, bem como o volume para cada programa que está atualmente tocando áudio.

<!-- -->

-   **Exceção:** Se a finalidade principal se o programa for reprodução ou criação de áudio ou vídeo, poderá ser útil ter um controle de volume no programa. Use um controle deslizante para essa finalidade e forneça comentários imediatos quando o usuário alterar o volume.

### <a name="windows-integration"></a>integração do Windows

-   **registre os sons do seu programa no registro Windows sons.** isso permite que o mixer de volume Windows adicione um controle deslizante para o seu programa.
-   **Registre os eventos de som personalizados do programa.** isso permite que o Windows item do painel de controle de som exiba-os. Crie a seguinte chave para cada evento de som personalizado: HKEY \_ Current \_ user \| AppEvents \| Event Labels = Event \| Name.
-   **Não desconecta os sons dos eventos de som do programa.** Em vez disso, especifique os sons a serem reproduzidos usando entradas do registro. Isso permite que os usuários personalizem os eventos de som por meio do item do painel de controle de som.
    -   **Exceção:** Você pode optar por usar o compartilhamento de sons para identidade visual.
-   **Não forneça uma maneira para os usuários configurarem sons nas opções do seu programa.** em vez disso, use o item do painel de controle Windows sons para essa finalidade.
-   **Considere não atribuir sons a eventos que ocorrem com frequência por padrão.** Não exija que os usuários configurem seu caminho de uma experiência inicial irritante.

### <a name="directsound-programming-issues"></a>Problemas de programação do DirectSound

-   Para programas DirectSound que têm seu próprio controle de volume, **defina o volume do programa como 100 por padrão.** Isso maximiza o intervalo dinâmico do seu áudio.
-   **Não bloqueie outros eventos de som executando seu programa em modo exclusivo.** Isso pode impedir que outros programas funcionem corretamente. Por exemplo, o uso de modo exclusivo impede que um computador seja usado como um dispositivo de telefonia.

## <a name="text"></a>Texto

-   Não use a frase adaptador de som. Em vez disso, use a placa de som.
-   Use o dispositivo para se referir genericamente a palestrantes, fones de ouvido e microfones.
-   Use o controlador para se referir ao hardware de áudio que controla os dispositivos, como placas de som e chipsets.
-   Use a frase esquema de som para descrever uma coleção de sons para eventos de programas comuns, como logon ou recebimento de novos emails. Use a frase tema da área de trabalho para descrever uma coleção de elementos visuais e sons para a área de trabalho do computador.
-   Use o termo áudio para fazer referência ampla a fala, música e sons. Use o termo som para se referir mais estreitamente ao programa e Windows sons descritos neste artigo.

 

