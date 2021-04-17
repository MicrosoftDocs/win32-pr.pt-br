---
title: Suporte à entrada de fala
description: Suporte à entrada de fala
ms.assetid: 4702b941-fcc9-4d00-aba2-eca624b6d417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ecb6f2ddfbbe10f8b892ce922cd466eca96890
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105748304"
---
# <a name="speech-input-support"></a>Suporte à entrada de fala

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Além de dar suporte à interação entre mouse e teclado, o Microsoft Agent inclui suporte direto para entrada de fala. Como o suporte do Microsoft Agent para entrada de fala é baseado no Microsoft SAPI (fala, interface de programação de aplicativo), você pode usar o Microsoft Agent com mecanismos de controle e comando de reconhecimento de fala que incluem o suporte a SAPI-required. Para obter mais informações sobre os requisitos do mecanismo de fala, consulte [requisitos de suporte do mecanismo de fala](requirements-for-speech-recognition-engines.md).

A Microsoft fornece um mecanismo de reconhecimento de fala de comando e controle que você pode usar com o Microsoft Agent. Para obter mais informações, consulte [seleção do mecanismo de fala](speech-engine-selection.md).

O usuário pode iniciar a entrada de fala pressionando e segurando a tecla de atalho de escuta Push a Talk. Nesse modo de escuta, se o mecanismo de fala receber o início da entrada falada, ele manterá o canal de áudio aberto até detectar o final do expressão. No entanto, quando não estiver recebendo entrada, ela não bloqueará a saída de áudio. Isso permite que o usuário emita vários comandos de voz enquanto mantém pressionada a tecla e o caractere pode responder quando o usuário não está falando.

O modo de escuta atinge o tempo limite quando o usuário libera a chave de escuta. O usuário pode ajustar o tempo limite para esse modo usando as opções de caractere avançadas. Você não pode definir esse tempo limite do código do aplicativo cliente.

Se um caractere tentar falar enquanto o usuário estiver falando, a saída audível do caractere falhará, embora o texto ainda possa ser exibido em seu balão de palavras. Se o caractere tiver o canal de áudio enquanto a tecla de escuta for pressionada, o servidor transferirá automaticamente o controle de volta para o usuário depois de processar o texto no método [**Speak**](speak-method.md) . Um tom MIDI opcional é tocado para marcar o usuário para começar a falar. Isso permite que o usuário forneça entrada mesmo se o aplicativo que está direcionando o caractere não fornecer pausas lógicas em sua saída.

Você também pode usar o método [**Listen**](listen-method.md) para iniciar a entrada de fala. Chamar esse método ativa o reconhecimento de fala por um período de tempo predefinido. Se não houver nenhuma entrada durante esse intervalo, o Microsoft Agent desligará automaticamente o mecanismo de reconhecimento de fala e liberará o canal de áudio. Isso evita o bloqueio de entrada ou saída do dispositivo de áudio e minimiza a sobrecarga do processador que o reconhecimento de fala usa quando está ligado. Você também pode usar o método **Listen** para desativar a entrada de fala. No entanto, lembre-se de que, como o mecanismo de reconhecimento de fala Opera de forma assíncrona, o efeito pode não ser imediato. Como resultado, é possível receber um evento de [**comando**](command-event.md) mesmo após o código chamado **escutar** para desativar a entrada de fala.

Para dar suporte à entrada de fala, você define uma *gramática*, um conjunto de palavras que você deseja que o mecanismo de reconhecimento de fala escute e corresponda como a configuração de **voz** para um [**comando**](/windows/desktop/lwef/the-command-object) em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Você pode incluir palavras opcionais e alternativas e sequências repetidas na sua gramática. Observe que o Agent não habilita a tecla de atalho de escuta até que um de seus clientes tenha carregado com êxito um mecanismo de fala ou tenha criado uma **voz** para um de seus objetos de **comando** .

Se o usuário pressionar a tecla de atalho de escuta ou o aplicativo cliente chamar o método [**Listen**](listen-method.md) para iniciar a entrada de fala, o mecanismo de reconhecimento de fala tentará corresponder a uma entrada de expressão para a gramática dos comandos que foram definidos e passará as informações de volta ao servidor. Em seguida, o servidor notifica o aplicativo cliente usando o evento de [**comando**](command-event.md) ([**IAgentNotifySink:: Command**](iagentnotifysink--command.md)); repassando o objeto [**userinput**](/windows/desktop/lwef/iagentuserinput) que inclui a ID de comando da melhor correspondência e as duas próximas correspondências alternativas (se houver), uma pontuação de confiança e o texto correspondente para cada correspondência.

O servidor também notifica seu aplicativo cliente quando ele corresponde à entrada de fala para um de seus comandos fornecidos. Enquanto a ID de comando é **nula**, você ainda Obtém a pontuação de confiança e o texto correspondente. Quando estiver no modo de escuta, o servidor reproduzirá automaticamente a animação atribuída ao estado de **escuta** do caractere. Em seguida, quando um expressão é realmente detectado, o servidor reproduz a animação de estado **audição** do caractere. O servidor manterá o caractere em um estado cuidadosa até que o expressão seja encerrado. Isso fornece os comentários sociais apropriados para marcar o usuário para entrada.

Se o usuário desabilitar a entrada de fala em opções avançadas de caracteres, a tecla de escuta também será desabilitada. Da mesma forma, a tentativa de chamar o método [**Listen**](listen-method.md) quando a entrada de fala está desabilitada causará falha no método.

 

 