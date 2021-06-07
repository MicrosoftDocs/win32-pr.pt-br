---
title: Som
description: Som é o elemento de áudio da experiência do usuário.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 035f718494e5a0548324f3c5449c5e3ac3f49fa1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444537"
---
# <a name="sound"></a>Som

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

*Som* é o elemento de áudio da experiência do usuário. Quando usado adequadamente, o som pode ser uma forma efetiva de comunicação que estabelece uma relação não verbal e até mesmo emocional com seus usuários. Os sons podem ser usados sozinhos ou como um suplemento para a interface do usuário visual. Por exemplo, adicionar um efeito de som a uma notificação aumenta a probabilidade de que ela seja notada, especialmente se o usuário não estiver olhando para a tela quando um evento ocorrer.

![captura de tela da caixa de diálogo de som ](images/vis-sound-image1.png)

Na guia Sons do item do painel de controle de som, os usuários podem fazer alterações em seus sons do sistema.

Este artigo aborda o uso de sons em um programa como uma resposta a eventos e ações do usuário e a integração do controle de som de um programa com o Windows. Ele não abrange o uso de música ou fala.

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
-   **Marca.** O som pode ser associado a conteúdo específico para a marca de seu produto, aplicativo ou serviço. O Windows usa o som dessa maneira para a inicialização do sistema operacional.
-   **Entretenimento.** O som é comumente usado para aprimorar produtos de entretenimento e tornar qualquer produto mais envolvente. Por exemplo, a maioria dos jogos, aplicativos de treinamento e produtos de consumidor usa som para animar os usuários e aprimorar sua experiência.

Determinados sons podem atender a várias dessas finalidades ao mesmo tempo. O som de Inicialização do Windows, por exemplo, indica que o processo de inicialização foi concluído e que a área de trabalho está pronta para uso. Ele também fornece uma forma poderosa de identidade visual do produto e, até mesmo, envolve momentaneamente os usuários.

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

**Um erro comum é que os sons para eventos críticos precisam ser altos e chamativas para chamar a atenção do usuário.** Isso não é verdade, porque o som é realmente destinado a ser um meio complementar de comunicação. No caso de uma mensagem de erro crítica, sua apresentação (talvez em uma caixa de diálogo modal), seu ícone (um ícone de erro) e seu texto e tom se combinam para comunicar a natureza do erro. Um som de erro efetivo pode ser ligeiramente mais baixo do que o som típico do Windows, mas não precisa ser significativamente mais intenso.

### <a name="characteristics-of-windows-sounds"></a>Características dos sons do Windows

Além dessa chamada geral para minimalismo, o som modernos do Windows usa sons claros, puros e frios, com um esmaecimento suave e esmaecimento ("bordas") suaves para evitar efeitos repentinos, jarring e percussivos. Eles são projetados para se sentir sutis, ofensivos e consoantes. Os sons do Windows usam eco, reverb e equalização para obter uma sensação natural e ambiente.

O esquema de som padrão para Windows geralmente não usa sons instrumentais ou reconhecíveis todos os dias que são muito específicos ou músicais. Exemplos de sons que ele evita são instrumentos instrumentais, como instrumentações ou instrumentos instrumentais, sons de animais, ruídos ambientais, fala, vozes, efeitos de som parecidos com o filme ou outros sons de humanos. Além disso, os sons do Windows não devem ser percebidos como música (ou seja, com várias notas). Isso faz com que o Windows pareça funcionalmente diferente de outros tipos de sons.

Como os sons do Windows foram projetados profissionalmente para ter as características desejáveis e atrair um público amplo, considere usar esses sons do Windows integrados sempre **que apropriado.**

### <a name="designing-your-own-sounds"></a>Projetando seus próprios sons

Se você precisa criar seus próprios sons, projete-os para ter as características descritas anteriormente. Se esforça para fazer com que eles complementem suas tarefas ou eventos associados.

Entenda que a criação de sons originais é difícil de fazer bem, especialmente para sons destinados a um público amplo. O som pode ser um elemento de design polarizador. Para cada usuário que adora um som, haverá muitos que o desagradam.

**Projete os sons do programa como um grupo para parecer que eles são variações relacionadas em um tema.** A experiência auditiva do programa deve ser coordenada com sua experiência visual. Além disso, o "tom" dos sons deve ser coordenado com [o tom do texto](text-style-tone.md). Considere como o texto com um tom natural e agradável pode ser prejudicado quando acompanhado por sons agressivos e alarmes.

**Se você fizer apenas quatro coisas...**

1.  Use som com restrição, certifique-se de que haja um benefício geral claro do usuário. Em caso de dúvida, não use som.
2.  Use os sons do Windows integrados sempre que apropriado.
3.  Se você criar seus próprios sons, certifique-se de que eles tenham as características de som desejáveis e como uma aparência completa, como variações de um tema.
4.  Não presuma que os sons precisam ser altos e dissonantes para obter a atenção do usuário.

## <a name="usage-patterns"></a>Padrões de uso

Os sons têm vários padrões de uso:



|     Uso de som                                                                                                                                                                 |  Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Conclusão da ação**<br/> o Sonic notifica os usuários quando uma ação de longa execução iniciada pelo usuário é concluída com êxito. <br/>                             | ![captura de tela da caixa de diálogo de download de arquivo ](images/vis-sound-image2.png)<br/> Neste exemplo, a caixa de diálogo reproduz um som para notificar os usuários de que o download foi concluído.<br/>                                                                                                                                                                                                                                      |
| **Falha na ação**<br/> o Sonic notifica os usuários quando uma ação de longa execução iniciada pelo usuário falha. <br/>                                                 | ![captura de tela da mensagem disco de backup não acessível ](images/vis-sound-image3.png)<br/> Neste exemplo, o Windows desempenha um som para notificar os usuários de que a operação de backup falhou.<br/>                                                                                                                                                                                                                                  |
| **Evento de sistema importante**<br/> o Sonic alerta os usuários de eventos importantes do sistema ou de status que exigem atenção imediata. <br/>                      | ![captura de tela de mensagem de bateria fraca ](images/vis-sound-image4.png)<br/> Neste exemplo, os usuários são alertados de que sua bateria fraca requer atenção imediata.<br/>                                                                                                                                                                                                                                                      |
| **CONHECIMENTO**<br/> o Sonic notifica os usuários de informações potencialmente úteis e relevantes. <br/>                                                                 | Como essas informações geralmente não exigem atenção imediata, um som FYI fornece comentários sutis sem interromper o fluxo do usuário. <br/> ![captura de tela da mensagem de entrada do Live Messenger ](images/vis-sound-image5.png)<br/> Neste exemplo, um som é reproduzido quando um contato entra em um serviço de mensagens instantâneas.<br/>                                                                                 |
| **Efeito de som**<br/> o Sonic fornece comentários às interações do usuário. <br/>                                                                            | Fornece comentários sonoros reais ou com estilo adequado para a interação. os efeitos sonoros costumam soar como se o usuário estivesse manipulando um objeto físico real. às vezes, chamado de Foley. <br/> ![captura de tela da janela que está sendo minimizada ](images/vis-sound-image6.png)<br/> Neste exemplo, o efeito de som de janela minimizar parece que um objeto do mundo real está sendo reduzido em tamanho.<br/> |
| **Sons de identidade visual**<br/> um som fornecido para aprimorar a experiência do usuário, embora o impacto emocional e, como um efeito colateral, promover a marca do produto. <br/> | Os sons de identidade visual são melhores quando sincronizados com eventos visuais, especialmente transições de interface do usuário, como a exibição de uma janela de programa. as marcas de som verdadeiro indicam a fonte de bens, semelhante a uma palavra registrada ou logotipo, e são relativamente incomuns. <br/> ![captura de tela do ícone de inicialização do Windows ](images/vis-sound-image7.png)<br/> Neste exemplo, a inicialização do Windows é uma experiência de transição com marca.<br/>      |



 

## <a name="guidelines"></a>Diretrizes

### <a name="usage"></a>Uso

-   **Use o som com o retentor** Verifique se há um benefício geral de usuário claro. Concentre-se em sons que mantêm os usuários informados, é provável que eles alterem seu comportamento ou forneçam comentários úteis. Em caso de dúvida, não use som.
-   **Selecione o som e suas características com base em como ele está sendo usado.** Para obter uma descrição de cada padrão de uso, consulte a tabela na seção anterior.
-   **Para notificações e comentários, não use som como o único método de comunicação.** Em vez disso, use o som como um método suplementar para reforçar visuais ou indicações de texto. Isso garante que os usuários possam ver as informações se não conseguirem ouvir o som.
-   **Não produza sons altos ou inversos com frequência.** Fazer isso é desnecessário e resulta em uma experiência de usuário ruim. Quanto mais vezes um som for reproduzido, menos invasivo deverá ser. Os sons não precisam ser altos ou se esduram para atrair a atenção.
-   **Não emita sinais sonoros.** O aviso sonoro não é apropriado para programas modernos. Os sinais sonoros não podem ter significados específicos atribuídos a eles e os usuários não podem controlá-los.
    -   **Exceção:** Funções críticas do sistema podem emitir um aviso para alertar os usuários de situações em que eles devem participar imediatamente, como energia de bateria criticamente baixa.

### <a name="playback"></a>Reprodução

-   **Não repita um som mais de duas vezes consecutivamente.**
-   **Para uma sequência consecutiva de eventos de som relacionados, reproduza um som somente no primeiro evento.** Evite usar vários sons, pois eles podem colidir uns com os outros ou resultar em uma experiência de usuário desagradável.

### <a name="sound-selection"></a>Seleção de som

-   **Escolha sons agradáveis.** Não use sons desagradáveis, alarmes, como repercussão, pane e interrupção.
-   **Use sons curtos** (menos de um segundo).
-   **Use sons que sejam aproximadamente o mesmo volume que o som típico do Windows.** Os usuários não gostam de desligar o volume ao iniciar um computador ou um programa, especialmente em ambientes públicos, como reuniões e apresentações. Os arquivos de som do Microsoft Windows estão localizados na pasta de mídia dentro da pasta do Windows.
-   **Não escolha sons que exijam localização.** Você pode conseguir isso usando sons que não usam fala ou que tenham significados ou connotações dependentes de cultura.

### <a name="windows-system-sounds"></a>Sons do sistema Windows

-   **Use os sons do sistema interno do Windows sempre que apropriado.**
-   **Escolha usar sons do sistema com base no seu significado associado, não apenas no próprio som.** Os sons do sistema devem ser usados de forma consistente.

### <a name="sound-design"></a>Design de som

Ao criar seus próprios sons:

-   **Crie sons com as características de som desejáveis.**
-   **Compor sons com a maioria das frequências de médio alcance a alta (600 Hz a 2 kHz).** Não use frequências baixas, pois elas viajam mais distantes, são mais difíceis de localizar e podem ser alarmantes.
-   **Defina a amplitude relativa de sons normais para o nível do som típico do Windows.** Os sons do Windows foram adequadamente redistribuídos para ambientes domésticos e de trabalho. Usar níveis diferentes para seus sons forçará os usuários a fazer ajustes de volume.
    -   Defina sons importantes como um pouco mais alto. Esses sons incluem conclusões de ação, falhas de ação e eventos importantes do sistema.
    -   Defina os sons que ocorrem com frequência para serem um pouco mais suaves. Isso inclui FYIs, sons de identidade visual e efeitos de som.
-   **Escolha sons consistentes com o significado dos sons do Windows.** Para criar uma versão personalizada de um som do Windows, preserve o mesmo Tom e intervalo, mas altere a orquestração ou timbre. Não atribua diferentes significados a sons com timbres e intervalos semelhantes como sons do Windows.
-   **Crie os sons para o seu programa se sentirem como variações relacionadas a um tema.** A experiência de auditoria do programa deve ser coordenada com sua experiência visual.
    -   **Crie transições de cena e transições de áudio juntas.** Por exemplo, se uma cena esmaecer gradualmente, qualquer som também deverá desaparecer gradualmente. Não arruinar transições visuais suaves tendo transições de som abruptas.
-   **Os sons devem estar no formato de arquivo. wav.** O formato PCM (modulação de código de pulso) não compactado estéreo de 16 bits de 44,1 kHz é recomendado. Se o tamanho do arquivo for importante, use os formatos de arquivos compactados ou monaural (mono), mas lembre-se de que há uma perda de qualidade facilmente discernida que pode refletir incorretamente em seu aplicativo.

### <a name="mixing"></a>Mixa

-   **Não têm controles de volume ou sem áudio em seu programa.** Em vez disso, permita que os usuários controlem as configurações de volume relativas entre aplicativos com o mixer de volume do Windows. Se o seu programa tiver um controle de volume, haverá vários locais em que os usuários ajustam suas configurações, o que pode levar à confusão.

    ![captura de tela do mixer de volume do Windows ](images/vis-sound-image8.png)

    O mixer de volume do Windows permite que os usuários controlem a configuração do volume principal, bem como o volume de cada programa que está reproduzindo áudio no momento.

<!-- -->

-   **Exceção:** Se o principal objetivo se o seu programa for reprodução de áudio ou vídeo ou criação, pode ser útil ter um controle de volume no programa. Use um controle deslizante para essa finalidade e forneça comentários imediatos quando o usuário alterar o volume.

### <a name="windows-integration"></a>Integração do Windows

-   **Registre os sons do seu programa no registro de sons do Windows.** Isso permite que o mixer de volume do Windows adicione um controle deslizante para o seu programa.
-   **Registre os eventos de som personalizados do programa.** Isso permite que o item do painel de controle de som do Windows os exiba. Crie a seguinte chave para cada evento de som personalizado: HKEY \_ Current \_ user \| AppEvents \| Event Labels = Event \| Name.
-   **Não desconecta os sons dos eventos de som do programa.** Em vez disso, especifique os sons a serem reproduzidos usando entradas do registro. Isso permite que os usuários personalizem os eventos de som por meio do item do painel de controle de som.
    -   **Exceção:** Você pode optar por usar o compartilhamento de sons para identidade visual.
-   **Não forneça uma maneira para os usuários configurarem sons nas opções do seu programa.** Em vez disso, use o item do painel de controle de sons do Windows para essa finalidade.
-   **Considere não atribuir sons a eventos que ocorrem com frequência por padrão.** Não exija que os usuários configurem seu caminho de uma experiência inicial irritante.

### <a name="directsound-programming-issues"></a>Problemas de programação do DirectSound

-   Para programas DirectSound que têm seu próprio controle de volume, **defina o volume do programa como 100 por padrão.** Isso maximiza o intervalo dinâmico do seu áudio.
-   **Não bloqueie outros eventos de som executando seu programa em modo exclusivo.** Isso pode impedir que outros programas funcionem corretamente. Por exemplo, o uso de modo exclusivo impede que um computador seja usado como um dispositivo de telefonia.

## <a name="text"></a>Text

-   Não use a frase adaptador de som. Em vez disso, use a placa de som.
-   Use o dispositivo para se referir genericamente a palestrantes, fones de ouvido e microfones.
-   Use o controlador para se referir ao hardware de áudio que controla os dispositivos, como placas de som e chipsets.
-   Use a frase esquema de som para descrever uma coleção de sons para eventos de programas comuns, como logon ou recebimento de novos emails. Use a frase tema da área de trabalho para descrever uma coleção de elementos visuais e sons para a área de trabalho do computador.
-   Use o termo áudio para fazer referência ampla a fala, música e sons. Use o termo som para se referir mais estreitamente aos sons do programa e do Windows descritos neste artigo.

 

