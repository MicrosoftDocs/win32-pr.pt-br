---
title: Sobre controles SysLink
description: Um controle SysLink é uma janela que renderiza o texto marcado para cima e notifica o aplicativo quando os usuários clicam em seus hiperlinks inseridos. Esse controle fornece uma alternativa conveniente ao uso do botão link de comando. Para obter mais informações, consulte tipos de botão.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008429"
---
# <a name="about-syslink-controls"></a>Sobre controles SysLink

Um controle SysLink é uma janela que renderiza o texto marcado para cima e notifica o aplicativo quando os usuários clicam em seus hiperlinks inseridos. Esse controle fornece uma alternativa conveniente ao uso do [**botão link de comando**](button-styles.md). Para obter mais informações, consulte [tipos de botão](button-types-and-styles.md).

Cada controle SysLink pode dar suporte a vários hiperlinks e você pode acessar cada hiperlink por meio de um índice baseado em zero. O controle SysLink é definido no ComCtl32.dll versão 6 e requer um manifesto ou diretiva que especifica que a versão 6 da DLL deve ser usada se estiver disponível. Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).

Este artigo inclui as seções a seguir.

-   [Marcação SysLink](#syslink-markup)
-   [Atributos de link](#link-attributes)
-   [Estados de link](#link-states)
-   [Limitações na exibição de texto bidirecional](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>Marcação SysLink

O controle SysLink dá suporte à marca de âncora ( &lt; a &gt; ) junto com os atributos **href** e **ID**. Um **href** pode ser qualquer protocolo, como http, FTP e mailto. Uma **ID** é um nome opcional, exclusivo dentro de um controle Syslink e está associado a um link individual. Os links também são atribuídos a um índice de base zero de acordo com sua posição dentro da cadeia de caracteres. Esse índice é usado para acessar um link.

## <a name="link-attributes"></a>Atributos de link

Os atributos de cada link podem ser definidos dentro da marca de âncora para cada link ou enviando a [**mensagem \_ SETITEM do LM**](lm-setitem.md) . Definir um atributo especificando-o dentro da cadeia de inicialização simplesmente inicializa o valor. Você pode alterar o valor de um atributo por meio do uso subsequente da mensagem **\_ SETITEM do LM** .

## <a name="link-states"></a>Estados de link

Os itens de link podem estar em qualquer um dos três Estados, representados pelos sinalizadores na tabela a seguir.



| Sinalizador de estado   | Aparência e significado                                            |
|--------------|-------------------------------------------------------------------|
| LIS \_ focado | O link tem o foco do teclado e pressionar Enter o ativa. |
| LIS \_ habilitado | O link está habilitado.                                              |
| LIS \_ visitado | O usuário já visitou a URL representada pelo link.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Limitações na exibição de texto bidirecional

Algumas linguagens, como árabe ou Hebraico, são escritas da direita para a esquerda (RTL); O inglês é escrito da esquerda para a direita (EPD). A combinação de DPE com EPD é chamada de texto bidirecional. Misturar construções de marcação direcional e Unicode EPD e RTL em cadeias de caracteres de recurso, como marcadores de fluxo bidirecionais para controlar o fluxo de cadeias de caracteres, pode não produzir o resultado esperado ao usar um controle SysLink. Por exemplo, uma sentença marcada como EPD pode não ser exibida corretamente no contexto RTL.

> [!Note]  
> Os controles SysLink não dão suporte à exibição bidirecional em todos os cenários. Use um controle SysLink somente se você souber que um layout simples EPD ou RTL é adequado. Caso contrário, considere o uso de uma tecnologia mais avançada, como [mshtml](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).

 

 

 