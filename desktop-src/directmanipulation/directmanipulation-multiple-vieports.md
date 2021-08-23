---
description: Ao usar vários viewports, clique em testingdetermines quais visores são afetados pela entrada do usuário, tirando o local da tela de um contato e determinando qual retângulo do visor o contato visita.
ms.assetid: 960EF92D-F439-4A84-AAF9-1469E2830573
title: Usando vários viewports no DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: e422d99d8a71fbf24af5fc60641da7ac808b54215c56e5d81b8c222226ef8452
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787508"
---
# <a name="using-multiple-viewports-in-directmanipulation"></a>Usando vários viewports no DirectManipulation

Ao usar vários viewports, o *teste de clique* determina quais visores são afetados pela entrada do usuário, tirando o local da tela de um contato e determinando qual retângulo do visor o contato acessa.

Um cenário comum na [manipulação direta](direct-manipulation-portal.md) é posicionar um visor dentro de outro, também conhecido como *visores de aninhamento*. Se o contato atingir mais de um visor, a ordem das chamadas  [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) pelo [*WndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) da janela determinará a relação pai-filho das visores aninhados.

Regra: o elemento filho deve chamar [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)antes de chamar o pai.

![diagrama mostrando hierachy de teste de clique](images/dm-art-8.png)

Um contato fica inativo em um visor. [**Setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) deve ser chamado primeiro no visor laranja (filho) e, em seguida, o visor verde (pai) para estabelecer a hierarquia correta.

## <a name="targeting-the-correct-viewport"></a>Direcionando o visor correto

Um contato pode ser associado a qualquer número de visores e cada contato pode ser atribuído a um conjunto diferente de visores.

Cada visor pode ser configurado para dar suporte a interações específicas, conforme necessário.

Com base nessas configurações, a [manipulação direta](direct-manipulation-portal.md) identifica qual visor manipula a entrada. O visor mais filho na hierarquia de teste de clique tem a primeira chance de lidar com a entrada. No entanto, o encadeamento e a promoção pai podem alterar qual visor manipula a entrada.

## <a name="chaining"></a>Encadeamento

Quando o final do conteúdo é atingido durante uma manipulação, a [manipulação direta](direct-manipulation-portal.md) aplica um efeito de limite para indicar que o conteúdo pode não ficar mais. No entanto, se um visor filho for *encadeado* a um visor pai, esse efeito será suprimido. Em vez disso, o visor ancestral mais próximo na hierarquia de teste de clique que dá suporte à manipulação, lida com a entrada. Se a direção da manipulação for invertida de modo que o ancestral retorne ao ponto em que o encadeamento foi disparado, a manipulação de "descadeias" e o controle será transferido de volta para o visor filho.

![diagrama mostrando a manipulação encadeada](images/dm-art-9.png)

Quando o usuário passa o visor filho até a borda do conteúdo, a manipulação "encadeia" para o visor pai e o usuário começa a panorâmica do conteúdo pai em vez disso.

> [!Note]  
> A cadeia dos eixos X e Y independentemente uma da outra, portanto, se uma panorâmica diagonal atingir o limite x antes do limite y, a manipulação moverá o pai na direção x enquanto continua a mover o filho na direção y. Para habilitar ou desabilitar o encadeamento, chame a API [**Setchaining**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining) no visor filho.

### <a name="rails"></a>Rails

A especificação de Rails na configuração de um visor afeta a maneira como a entrada é encadeada do visor. Especificamente, a entrada não pode encadear de um visor filho Rails para seu pai no modo de panorâmica "não encadeado" de trilhos. Para entrada de encadeamento quando Rails são definidos, o usuário deve ter o movimento panorâmico vertical ou horizontalmente e estar bloqueado para os trilhos.

### <a name="zooming"></a>Zoom

Se um visor filho estiver aninhado dentro de um pai e ambos estiverem configurados para zoom, uma manipulação de zoom poderá encadear de filho para pai. No entanto, se a manipulação continuar, ela só funcionará no pai e não poderá "desencadear" para o filho. Se o usuário encadear um zoom do filho para o pai, a [manipulação direta](direct-manipulation-portal.md) suspenderá o filho até que todos os contatos associados à manipulação sejam removidos da tela. Neste ponto, o filho é liberado da suspensão e o usuário pode deslocar o visor filho.

## <a name="gesture-targeting-parent-promotion"></a>Direcionamento de gesto: promoção pai

O *direcionamento de gestos* é o processo pelo qual a [manipulação direta](direct-manipulation-portal.md) agrupa contatos e determina qual visor processa a entrada. *Promoção pai* refere-se aos casos em que a entrada é transferida do filho para o pai. Por exemplo, quando um usuário coloca dois contatos e pinça em um visor filho configurado apenas para rolagem, a entrada é promovida para o pai para que ocorra um zoom. A promoção pai ocorre independentemente se o encadeamento está habilitado no visor filho.

Ao contrário do encadeamento, a promoção pai não é revertida. O visor pai continua processando a entrada de interação até que todos os contatos sejam levantados (os visores filho param de processar a entrada).
