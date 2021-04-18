---
title: Som
description: O som é o elemento de áudio da experiência do usuário.
ms.assetid: 2a276370-eff9-4844-b008-eba9ae5ac395
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 664d78d00cf75dae8f43717db07290a26574f0c6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556331"
---
# <a name="sound"></a>Som

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

O *som* é o elemento de áudio da experiência do usuário. Quando usado adequadamente, o som pode ser uma forma eficaz de comunicação que estabelece uma relação não verbal e mesmo emocional com seus usuários. Os sons podem ser usados sozinhas ou como um suplemento para a interface do usuário visual. Por exemplo, adicionar um efeito de som a uma notificação aumenta a probabilidade de que ele seja notado, especialmente se o usuário não estiver olhando para a tela quando ocorrer um evento.

![captura de tela da caixa de diálogo som ](images/vis-sound-image1.png)

Na guia sons do item do painel de controle de som, os usuários podem fazer alterações em seus sons do sistema.

Este artigo aborda o uso de sons em um programa como resposta a eventos e ações do usuário e a integração do controle de som de um programa com o Windows. Ele não cobre o uso de música ou fala.

**Observação:** As diretrizes relacionadas a [notificações](mess-notif.md) e [identidade visual](exper-branding.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir se você deve usar o som, considere estas perguntas:

-   **Há um benefício de usuário claro para usar som?** Como as desvantagens do uso de som podem superar facilmente os benefícios, use o som somente quando houver uma vantagem clara.
-   **O uso do som é apropriado?** O uso de som soa a atenção para as coisas que são dignas de atenção? Os usuários perderam o som se estivessem ausentes? Concentre-se em sons que mantêm os usuários informados, é provável que eles alterem seu comportamento ou forneçam comentários úteis.
-   **O uso de som parece confuso?** Há sons frequentes, dissonantes? Os usuários provavelmente reduzirão o volume do sistema ou o volume do programa como resultado do seu uso de som?
-   **Você está usando som como uma forma primária de comunicação?** Em muitos casos, como para usuários que têm algum nível de perda de audição, o som não deve ser usado como o principal meio de comunicação. O som é mais eficaz como um suplemento para outros meios de comunicação (como texto ou visuais).
-   **Os principais usuários de destino são profissionais de ti?** Normalmente, o som é ineficaz para tarefas direcionadas a profissionais de ti, pois muitas de suas tarefas são executadas de forma autônoma. Além disso, o som não é dimensionado para eles, imagine a execução de centenas de tarefas por vez e receba sons quando eles forem concluídos ou falharem.

## <a name="design-concepts"></a>Conceitos de design

Normalmente, o som é obtido por uma ou todas as seguintes finalidades:

-   **Notification.** O som pode ser associado a eventos específicos. Por exemplo, um som de "novo email" informa os usuários quando o email chega sem interromper a tarefa atual.
-   **Receber.** O som pode fornecer comentários para ações específicas do usuário. Por exemplo, um som sutil que é reproduzido quando você libera o controle deslizante no controle de volume fornece comentários sobre o nível da configuração atual.
-   **Identidade visual.** O som pode ser associado a um conteúdo específico para marcar seu produto, aplicativo ou serviço. O Windows usa som dessa maneira para a inicialização do sistema operacional.
-   **Entretenimento.** O som é normalmente usado para aprimorar produtos de entretenimento e para tornar qualquer produto mais atraente. Por exemplo, a maioria dos jogos, aplicativos de treinamento e produtos de consumo usam som para usuários de entretenimento e aprimoram sua experiência.

Alguns sons podem atender a várias dessas finalidades de uma só vez. O som de inicialização do Windows, por exemplo, indica que o processo de inicialização foi concluído e que a área de trabalho está pronta para uso. Ele também fornece uma forma poderosa de identidade visual do produto e, até mesmo, envolve momentaneamente os usuários.

Os sons que atenderem a nenhuma dessas finalidades provavelmente serão eliminados.

### <a name="inappropriate-use-of-sound"></a>Uso inadequado de som

**Apesar dos benefícios do som, o uso apropriado de som requer um retentor significativo para que o contrário possa tornar um programa desagradável e distrair.** Os usuários desligarão seu som completamente se eles se tornarem imprecisados por sons frequentes, repetitivos, dissonantes, de interrupção e mal projetados; em parte, isso ocorre porque, por sua natureza, o som exige atenção e é difícil de ignorar. Para obter dicas sobre como encontrar um saldo razoável, consulte as [diretrizes de design de som](#sound-design).

Como as desvantagens do uso de som podem superar facilmente os benefícios, use o som somente quando houver uma vantagem clara. **Em caso de dúvida, não use som.**

### <a name="make-sound-supplemental"></a>Tornar o som suplementar

Mesmo que o som seja usado adequadamente, há muitas situações em que o som pode não ser eficaz para todos os usuários:

-   Alguns usuários podem trabalhar em um ambiente barulhento em que os sons não possam ser ouvidos.
-   Alguns usuários podem trabalhar em um ambiente silencioso que exige que o som seja desativado ou definido em um volume baixo.
-   Alguns usuários podem ter deficiências ou perdas.
-   O computador pode não ter alto-falantes.

Por esses motivos, **o som usado para notificações e comentários nunca deve ser o único método de comunicação,** mas, em vez disso, deve complementar visuais ou indicações de texto.

### <a name="desirable-characteristics-of-sound"></a>Características desejáveis do som

Em geral, os sons devem ser:

-   de média a alta frequência (600 Hertz \[ Hz \] a 2 kilohertz \[ kHz \] ).
-   curto (menos de um segundo).
-   flexível ou moderada no volume.
-   significativo.
-   agradável, sem alarme ou dissonante.
-   não verbal.
-   Não repetitivo.

Com som, menos é mais. **O efeito de som ideal é aquele que os usuários raramente percebem, mas eles perdem se estavam ausentes.**

**Um equívoco comum é que sons de eventos críticos precisam ser altos e dissonantedos para obter a atenção do usuário.** Isso não é verdade, porque o som é, na verdade, destinado a ser um meio suplementar de comunicação. No caso de uma mensagem de erro crítica, sua apresentação (talvez em uma caixa de diálogo modal), seu ícone (um ícone de erro) e seu texto e Tom são combinados para comunicar a natureza do erro. Um som de erro efetivo pode ser um pouco mais alto do que o som típico do Windows, mas não precisa ser significativamente mais alto.

### <a name="characteristics-of-windows-sounds"></a>Características dos sons do Windows

Além desta chamada geral para o mínimo, a estética do som do Windows usa luz, tons puros e sons de vidro e nada, com um esmaecimento suave e fade-out ("bordas" suaves) para evitar efeitos abruptas, dissonante e percussive. Elas foram projetadas para se sentir sutis, AdaBoost e consoante. Os sons do Windows usam eco, reverberação e equalização para alcançar uma sensação natural e ambiental.

O esquema de som padrão para o Windows geralmente não usa sons diários ou reconhecíveis que são muito específicos ou musicais. Exemplos de sons que ele evita são instrumentos musicais, como piano ou instrumentos de percussão, sons de animais, ruídos ambientais, fala, vozes, efeitos de som semelhantes a filmes ou outros sons de humanos. Além disso, os sons do Windows não devem ser percebidos como música (ou seja, desde Melodies de várias anotações). Isso torna os sons do Windows funcionalmente distintos de outros tipos de sons.

Como os sons do Windows foram projetados profissionalmente para ter as características desejáveis e apelo a um público amplo, **Considere o uso desses sons internos do Windows sempre que for apropriado.**

### <a name="designing-your-own-sounds"></a>Criando seus próprios sons

Se você precisar criar seus próprios sons, crie-os para ter as características descritas anteriormente. Busque que eles complementem suas tarefas ou eventos associados.

Entenda que a criação de sons originais é difícil de fazer muito bem, especialmente para os sons destinados a um público amplo. O som pode ser um elemento de design Polarizing. Para cada usuário que adora um som, haverá muitos que não gostariam dele.

**Crie os sons do seu programa como um grupo para se sentirem como variações relacionadas a um tema.** A experiência de auditoria do programa deve ser coordenada com sua experiência visual. Além disso, o "Tom" dos sons deve ser coordenado com o [Tom do texto](text-style-tone.md). Considere como o texto com um tom natural e agradável pode ser subminado quando acompanhado por sons inadequados, alarmes.

**Se você fizer apenas quatro coisas...**

1.  Use o som com o retentor Verifique se há um benefício geral de usuário claro. Em caso de dúvida, não use som.
2.  Use os sons internos do Windows sempre que apropriado.
3.  Se você criar seus próprios sons, certifique-se de que eles tenham as características de som desejáveis e como uma aparência completa, como variações de um tema.
4.  Não presuma que os sons precisam ser altos e dissonantes para obter a atenção do usuário.

## <a name="usage-patterns"></a>Padrões de uso

Os sons têm vários padrões de uso:



|                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                        |
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

## <a name="text"></a>Texto

-   Não use a frase adaptador de som. Em vez disso, use a placa de som.
-   Use o dispositivo para se referir genericamente a palestrantes, fones de ouvido e microfones.
-   Use o controlador para se referir ao hardware de áudio que controla os dispositivos, como placas de som e chipsets.
-   Use a frase esquema de som para descrever uma coleção de sons para eventos de programas comuns, como logon ou recebimento de novos emails. Use a frase tema da área de trabalho para descrever uma coleção de elementos visuais e sons para a área de trabalho do computador.
-   Use o termo áudio para fazer referência ampla a fala, música e sons. Use o termo som para se referir mais estreitamente aos sons do programa e do Windows descritos neste artigo.

 

