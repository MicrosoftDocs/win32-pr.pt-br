---
description: Parâmetros de agrupamento
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: Parâmetros de agrupamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfb674d4349f351ce36fe1e236d1ecd3b265d8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646370"
---
# <a name="grouping-parameters"></a>Parâmetros de agrupamento

Um parâmetro de agrupamento identifica uma coleção de [sessões de áudio](audio-sessions.md) que são controladas por um único controle de volume no programa de controle de volume do sistema, SNDVOL. O parâmetro GROUPING é um GUID que identifica exclusivamente a coleção dentro do escopo do computador.

A finalidade de um parâmetro de agrupamento é semelhante à do GUID de sessão de uma sessão de processo cruzado. Ou seja, o parâmetro GROUPING permite que o usuário controle uma coleção de fluxos de qualquer número de processos como uma única unidade. No entanto, o parâmetro de agrupamento atende a essa finalidade em circunstâncias em que as sessões entre processos não podem fornecer uma solução.

Se vários clientes atribuirem seus respectivos fluxos a sessões separadas, mas atribuirem o mesmo parâmetro de agrupamento a todas as sessões, o SNDVOL exibirá um único controle de volume para essas sessões. Para fornecer suporte para parâmetros de agrupamento, SNDVOL ou qualquer aplicativo de controle de volume semelhante deve fazer o seguinte:

-   Antes de exibir os controles de volume, verifique os parâmetros de agrupamento de todas as sessões ativas. Agrupe em um único controle de volume todas as sessões que têm o mesmo parâmetro de agrupamento.
-   Quando o usuário altera a configuração em um controle de volume para um determinado parâmetro de agrupamento, atualize os níveis de volume de todas as sessões que compartilham esse parâmetro de agrupamento.

Os parâmetros de agrupamento ajudam a reduzir o número de controles de volume exibidos pelo SNDVOL. Os usuários podem ficar confusos se o SNDVOL obstruir sua exibição com muitos controles. Sem suporte para parâmetros de agrupamento, o SNDVOL sempre exibiria um controle de volume separado para cada sessão, o que pode não ser apropriado em todas as circunstâncias. Além disso, os parâmetros de agrupamento fornecem uma maneira conveniente de garantir que as sessões que contêm tipos semelhantes de conteúdo de áudio possam ser facilmente definidas para o mesmo nível de volume.

Conforme explicado anteriormente, as APIs de áudio de nível superior normalmente atribuem seus fluxos à sessão padrão de processo específica (identificada pelo valor GUID de sessão GUID \_ NULL). Esse padrão permite que o SNDVOL exiba um controle de volume separado para cada processo de aplicativo cliente, que é frequentemente o comportamento desejado. Além disso, se várias instâncias do mesmo cliente forem executadas em processos separados, mas exigirem um único controle de volume compartilhado, os clientes poderão simplesmente atribuir seus fluxos à mesma sessão entre processos. Nenhum desses casos requer o uso de parâmetros de agrupamento. No entanto, um caso importante, como exemplificado pelo Microsoft Internet Explorer, requer o uso de parâmetros de agrupamento para atingir o comportamento desejado.

O Internet Explorer permite que os usuários abram várias janelas de navegador e essas janelas podem não ser executadas no mesmo processo. Os usuários poderão ficar confusos se SNDVOL exibir um controle de volume separado para cada instância do aplicativo, todos com o mesmo rótulo, "Internet Explorer". Uma sessão de processo cruzado não é uma solução viável nesse caso – se várias instâncias do Internet Explorer forem executadas em processos diferentes, elas poderão não ser capazes de atribuir todos os fluxos de áudio a uma única sessão entre processos. O motivo é que as janelas do Internet Explorer podem estar executando instâncias do Windows Media Player ou outro plug-in de multimídia que usa uma API de áudio de nível superior para reproduzir seus fluxos de áudio. Essas APIs normalmente atribuem os fluxos em um processo a uma sessão padrão, específica ao processo. O Internet Explorer não tem controle sobre a atribuição desses fluxos a sessões.

O WASAPI resolve esse problema habilitando cada instância do Internet Explorer a acessar os controles de sessão para sua sessão padrão, específica do processo e atribuir um parâmetro de agrupamento a essa sessão. Se todas as instâncias do Internet Explorer atribuirem o mesmo parâmetro de agrupamento a todas as suas sessões de áudio, o SNDVOL exibirá um único controle de volume para essas sessões.

Por padrão, uma sessão não pertence a nenhum agrupamento. Se um cliente não atribuir uma sessão explicitamente a um agrupamento, o SNDVOL exibirá um controle de volume dedicado para essa sessão. O valor do parâmetro de agrupamento GUID \_ NULL indica que uma sessão não pertence a nenhum agrupamento. Se nenhum cliente tiver atribuído explicitamente um parâmetro de agrupamento a uma sessão, o valor do parâmetro de agrupamento dessa sessão será o GUID \_ NULL por padrão.

Um cliente pode alterar dinamicamente o Agrupamento ao qual uma sessão é atribuída.

Um agrupamento pode incluir qualquer combinação de sessões de processo cruzado e sessões específicas do processo em um [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md).

A interface do usuário SNDVOL permite que o usuário exiba os controles de volume para apenas um dispositivo de ponto de extremidade de áudio por vez. Quando o usuário ajusta os controles de volume para um dispositivo específico, os níveis de volume de sessões que se conectam a outros dispositivos não são afetados. Em particular, um controle de volume para um determinado parâmetro de agrupamento afeta apenas as sessões que compartilham o parâmetro de agrupamento e que estão conectados ao dispositivo selecionado no momento. Uma sessão que tem um parâmetro de agrupamento idêntico, mas que está conectada a outro dispositivo, não é afetada.

Conforme descrito anteriormente, o SNDVOL rotula cada controle de volume exibido com um nome de exibição e ícone. No caso de um controle de volume para um agrupamento, SNDVOL arbitrariamente seleciona uma das sessões no agrupamento como a origem para o nome de exibição e o ícone que ele exibe com o controle de volume. Portanto, para garantir que SNDVOL sempre exiba o mesmo nome de exibição e ícone para um agrupamento, todas as instâncias de aplicativo que atribuem sessões a esse agrupamento devem garantir que suas respectivas sessões tenham o mesmo nome de exibição e ícone. Para obter mais informações sobre nomes de exibição e ícones, consulte [sessões de áudio](audio-sessions.md).

Um aplicativo como SNDVOL pode se registrar para receber notificações quando o parâmetro de agrupamento de uma sessão é alterado. Essas notificações podem ser úteis se o aplicativo armazenar em cache informações sobre a atribuição de sessões para agrupar parâmetros. Uma notificação informa ao aplicativo que as informações armazenadas em cache podem não ser mais válidas.

Para atribuir um parâmetro de agrupamento a uma sessão, chame o método [**IAudioSessionControl:: SetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) . Para obter o parâmetro de agrupamento atribuído a uma sessão, chame o método [**IAudioSessionControl:: GetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessões de áudio](audio-sessions.md)
</dt> </dl>

 

 



