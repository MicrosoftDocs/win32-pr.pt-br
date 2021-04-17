---
description: Geralmente, é desejável copiar um conjunto mais complicado de informações do que pode estar contido no formato serializado da tinta (ISF).
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: Armazenando tinta em HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372e6e77ea0284bc44fa70883964e53b3063bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757336"
---
# <a name="storing-ink-in-html"></a>Armazenando tinta em HTML

Geralmente, é desejável copiar um conjunto mais complicado de informações do que pode estar contido no formato serializado da tinta (ISF). O HTML é especialmente útil como um formato de interoperabilidade devido à sua forte aceitação como um padrão do setor e à sua capacidade de representar conteúdo heterogêneo.

O HTML é amplamente compreendido, bem documentado e familiar para muitos desenvolvedores. Há muitas ferramentas para produção em HTML. Além disso, o Microsoft Windows contém APIs (interfaces de programação de aplicativo) para renderização e manipulação de HTML. Por fim, as APIs da plataforma do Tablet PC fornecem o formato de persistência GIF reforçada, que é adequado para inserção em outros formatos, o que é o HTML mais importante. Esse formato consiste em um arquivo GIF com ISF (Ink serializado Format) incorporado em um bloco de extensão de aplicativo.

Esses arquivos GIF são representações de objetos de tinta que:

-   Renderizar em aplicativos que não são habilitados para tinta, como navegadores ou processadores de texto herdados.
-   Contêm todas as informações necessárias da tinta original que deseja manter para fins como edição ou reconhecimento.

Esses arquivos GIF podem ser produzidos usando os métodos de persistência das APIs da plataforma Tablet PC. Eles são GIFs e devem usar a extensão GIF e, para um aplicativo que não está habilitado para tinta, não há nada diferente sobre eles de um GIF normal. Para um aplicativo habilitado para tinta, no entanto, há um conjunto avançado de dados subjacentes à imagem.

Depois que ele é produzido pelas APIs da plataforma Tablet PC, um GIF reforçada é referenciado por uma marca IMG em HTML. Em seguida, o HTML é armazenado no slot de área de transferência HTML do CF padrão \_ . Isso permite que o HTML fique visível para outros aplicativos, sejam eles habilitados para tinta. A própria imagem pode ser armazenada no cache da Internet do Windows e definida para atingir a idade após um período de tempo apropriado.

Adorners específicos para a marca IMG são fornecidos ou necessários. Esses adornos identificam o HTML como contendo tinta. O exemplo a seguir refere-se a um GIF reforçada usando marcas HTML:

`<img href="34372423432.gif" />`

Se for necessário fazer referência à imagem por outros meios, como folhas de estilo em cascata ou linguagem VML (VML), ainda deverá haver uma marca IMG fazendo referência à imagem. Isso permite cortar e colar dentro e fora de qualquer aplicativo que aceite representações HTML de tinta.

Os aplicativos que dão suporte à tinta em HTML devem:

-   Gere \_ o CF HTML quando o usuário executar uma cópia. Ao gerar o \_ HTML do CF na cópia (ou salvar como HTML), use o método [Microsoft. Ink. Ink. Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) , especificando o valor [Microsoft. Ink. PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) no parâmetro *p* , para gerar uma imagem GIF reforçada. O texto alt deve ser definido para o resultado de reconhecimento mais preciso. Você pode definir o posicionamento como absoluto ou in-loco, conforme desejado.
-   Verifique todas as marcas IMG para determinar se as imagens que eles apontam contêm tinta, se o slot de HTML do CF \_ for escolhido para uma colagem. Nesse caso, trate as imagens como objetos de [tinta](/previous-versions/aa515768(v=msdn.10)) internamente. Embora somente arquivos GIF tenham suporte nesta versão, seu aplicativo deve verificar imagens não GIF também, caso haja suporte para formatos de imagem adicionais no futuro.
-   Suporte à cópia e colagem de ISF. Os aplicativos que oferecem suporte a HTML também devem oferecer suporte a ISF para aprimorar a interoperabilidade com aplicativos habilitados para tinta que não reconhecem HTML. Isso é semelhante à Convenção de que os aplicativos que colocam HTML na área de transferência também colocam texto.

Para obter mais informações sobre GIFs reforçada, consulte [blocos de construção](building-blocks.md).

 

 
