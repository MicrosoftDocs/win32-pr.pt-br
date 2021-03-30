---
title: Intervalos
description: Intervalos
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- TSF (estrutura de serviços de texto), intervalos
- TSF (estrutura de serviços de texto), intervalos
- serviços de texto, intervalos
- Aplicativos habilitados para TSF, intervalos
- ranges
- TSF (estrutura de serviços de texto), âncoras
- TSF (estrutura de serviços de texto), âncoras
- serviços de texto, âncoras
- Aplicativos habilitados para TSF, âncoras
- âncoras
- TSF (estrutura de serviços de texto), clones
- TSF (estrutura de serviços de texto), clones
- serviços de texto, clones
- Aplicativos habilitados para TSF, clones
- clones
- TSF (estrutura de serviços de texto), backups
- TSF (estrutura de serviços de texto), backups
- serviços de texto, backups
- Aplicativos habilitados para TSF, backups
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916612"
---
# <a name="ranges"></a>Intervalos

## <a name="anchors"></a>Âncoras

Um intervalo é delimitado por duas *âncoras*, uma âncora inicial e uma âncora final. Existe uma âncora em um slot imaginário entre dois caracteres. A âncora inicial está relacionada ao texto que segue a âncora e a âncora final está relacionada ao texto que precede a âncora. As âncoras de início e de término podem existir no mesmo local. Nesse caso, o intervalo tem comprimento zero.

Por exemplo, comece com o seguinte texto:


```C++
This is text.
```



Agora, aplique um intervalo a esse texto com as âncoras início e término na posição 0. Ele é visualmente representado como:


```C++
<anchor></anchor>This is text.
```



As âncoras não ocupam nenhum espaço no próprio texto. Este é um intervalo de comprimento zero e seu texto está vazio.

Agora, mude a âncora final + 3 posições. Ele é visualmente representado como:


```C++
<anchor>Thi</anchor>s is text.
```



A âncora inicial é posicionada logo antes do caractere na posição 0 e a âncora final é posicionada logo após o caractere na posição 3 porque a âncora final foi movida para os três locais certos. O intervalo de texto agora é "Thi".

Além disso, a âncora inicial não pode ser feita para seguir a âncora final e a âncora final não pode ser feita para preceder a âncora inicial.

## <a name="anchor-gravity"></a>Gravidade da âncora

Cada âncora tem uma configuração de *gravidade* que determina como a âncora responde quando o texto é inserido no fluxo de texto na posição da âncora. Quando uma inserção é feita na posição de uma âncora, um ajuste deve ser feito na posição da âncora. A gravidade determina como esse ajuste de posição de ancoragem é feito.

Por exemplo:


```C++
It is <anchor></anchor>cold today.
```



Se a palavra "muito" for inserida na posição do intervalo, a âncora de início poderá ser posicionada antes ou depois da palavra inserida:


```C++
It is <anchor>very </anchor>cold today.
```



\- Ou –


```C++
It is very <anchor></anchor>cold today.
```



A gravidade da âncora especifica como a âncora é reposicionada quando uma inserção é feita em sua posição. A gravidade pode ser *retroativa* ou *posterior*.

Se a âncora tiver gravidade regressiva, a âncora retrocederá, em relação ao ponto de inserção, na inserção para que o texto inserido siga a âncora:


```C++
It is <anchor>very </anchor>cold today.
```



Se a âncora tiver gravidade progressiva, a âncora avançará (em relação ao ponto de inserção) na inserção para que o texto inserido preceda a âncora:


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a>Clones e backups

Há duas maneiras de fazer uma "cópia" de um objeto Range. A primeira é fazer um *clone* do intervalo usando [ITfRange:: clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone). A segunda é fazer um *backup* do intervalo usando [ITfContext:: CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).

Um clone é uma cópia de um intervalo que não inclui dados estáticos. As âncoras do intervalo são copiadas, mas o clone ainda cobre um intervalo de texto dentro do contexto. Um clone é um objeto de intervalo em todos os aspectos. Isso significa que o texto e as propriedades de um intervalo clonado são dinâmicos e serão alterados se o texto e/ou as propriedades do intervalo cobertos pelo clone forem alterados.

Um backup armazena o texto e as propriedades de um intervalo no momento em que o backup é feito como dados estáticos. Um backup também clona o intervalo original para que as alterações no tamanho e na posição do intervalo original possam ser rastreadas. Isso significa que o texto e as propriedades de um intervalo de backup são estáticos e não são alterados se o texto e/ou as propriedades do intervalo cobertos pelo backup forem alterados.

Por exemplo, o seguinte intervalo (pRange) no contexto:


```C++
"This is some <pRange>text</pRange>."
```



Agora faça um clone e um backup desse intervalo:


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



Agora, os objetos contêm o seguinte:


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Agora, altere o texto de pRange:


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



Agora, os objetos contêm o seguinte:


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



Definir o texto fez com que o texto dentro do contexto fosse alterado. Ele também fez com que a âncora final de pRange e pClone fosse alterada. pClone agora contém "outras palavras" porque o texto foi alterado dentro do intervalo e essas alterações são controladas por todos os intervalos. Quando o texto coberto por pRange e pClone alterado, o texto de pClone também mudou.

O texto em pBackup não foi alterado do pRange original porque os dados (texto e propriedades) no backup não estão relacionados ao contexto e são armazenados separadamente. O clone contido no backup realmente muda, mas os dados são estáticos.

Ao restaurar um backup, o backup pode ser aplicado ao clone dentro do backup ou a um intervalo diferente inteiramente. Para aplicar o backup ao clone no backup, passe **NULL** para [ITfRangeBackup:: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , conforme mostrado no exemplo de código a seguir:


```C++
pBackup->Restore(ec, NULL);
```



Agora, os objetos contêm o seguinte:


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



Para restaurar o backup em um intervalo diferente, passe um ponteiro para o objeto Range ao chamar **ITfRangeBackup:: Restore**. O texto e as propriedades de backup serão aplicados ao novo intervalo. Por exemplo, usando o exemplo acima antes da chamada de **restauração** , pRange será modificado para demonstrar isso:


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



Agora, os objetos contêm o seguinte:


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



Quando a âncora final de pRange foi deslocada para os dois locais à esquerda, a âncora final de pClone não foi alterada.

Agora, restaure o backup usando pRange com o seguinte exemplo de código:


```C++
pBackup->Restore(ec, pRange);
```



Agora, os objetos contêm o seguinte:


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



O texto coberto por pRange foi substituído por "text", uma parte do texto coberta por pClone foi alterada e pBackup muda para corresponder a pRange.

 

 




