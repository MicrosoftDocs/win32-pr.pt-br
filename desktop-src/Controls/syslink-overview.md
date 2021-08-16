---
title: Sobre controles SysLink
description: Um controle SysLink é uma janela que renderiza o texto marcado e notifica o aplicativo quando os usuários clicam em seus hiperlinks inseridos. Esse controle fornece uma alternativa conveniente ao uso do botão de link Comando. Para obter mais informações, consulte Tipos de botão.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4a5d64af48fc0b48b15f22fff55e5cb563339ac8d90446981c74e07f5d4713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168556"
---
# <a name="about-syslink-controls"></a>Sobre controles SysLink

Um controle SysLink é uma janela que renderiza o texto marcado e notifica o aplicativo quando os usuários clicam em seus hiperlinks inseridos. Esse controle fornece uma alternativa conveniente ao uso do [**botão de link Comando**](button-styles.md). Para obter mais informações, consulte [Tipos de botão](button-types-and-styles.md).

Cada controle SysLink pode dar suporte a vários hiperlinks e você pode acessar cada hiperlink por meio de um índice baseado em zero. O controle SysLink é definido no ComCtl32.dll versão 6 e requer um manifesto ou diretiva que especifica que a versão 6 da DLL deve ser usada se estiver disponível. Para obter mais informações, consulte [Habilitando estilos visuais.](cookbook-overview.md)

Este artigo inclui as seções a seguir.

-   [Marcação SysLink](#syslink-markup)
-   [Atributos de link](#link-attributes)
-   [Estados de link](#link-states)
-   [Limitações na exibição de texto bidirecional](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>Marcação SysLink

O controle SysLink dá suporte à marca de âncora( a ) juntamente com &lt; os atributos &gt; **HREF** e **ID**. Um **HREF** pode ser qualquer protocolo, como http, ftp e mailto. Uma **ID** é um nome opcional, exclusivo em um controle SysLink e está associada a um link individual. Os links também são atribuídos a um índice baseado em zero de acordo com sua posição dentro da cadeia de caracteres. Esse índice é usado para acessar um link.

## <a name="link-attributes"></a>Atributos de link

Os atributos de cada link podem ser definidos dentro da marca de âncora para cada link ou enviando a [**mensagem LM \_ SETITEM.**](lm-setitem.md) Definir um atributo especificando-o dentro da cadeia de caracteres de inicialização simplesmente inicializa o valor. Você pode alterar o valor de um atributo por meio do uso subsequente da **mensagem \_ LM SETITEM.**

## <a name="link-states"></a>Estados de link

Os itens de link podem estar em qualquer um dos três estados, representados pelos sinalizadores na tabela a seguir.



| Sinalizador de estado   | Aparência e significado                                            |
|--------------|-------------------------------------------------------------------|
| LIS \_ FOCALIZADO | O link tem o foco do teclado e pressionar Enter o ativa. |
| LIS \_ HABILITADO | O link está habilitado.                                              |
| LIS \_ VISITADO | O usuário já visitou a URL representada pelo link.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Limitações na exibição de texto bidirecional

Alguns idiomas, como árabe ou hebraico, são escritos da direita para a esquerda (RTL); O inglês é escrito da esquerda para a direita (LTR). A combinação de RTL com LTR é chamada de texto bidirecional. A combinação de constructos de marcação direcional UNICODE e RTL Unicode ou HTML em cadeias de caracteres de recurso, como marcadores de fluxo bidirecional para controlar o fluxo de cadeias de caracteres, pode não produzir o resultado esperado ao usar um controle SysLink. Por exemplo, uma frase marcada por LTR pode não ser exibida corretamente no contexto de RTL.

> [!Note]  
> Os controles SysLink não são suportados para exibição bidirecional em todos os cenários. Use um controle SysLink somente se você sabe que um layout LTR ou RTL simples é adequado. Caso contrário, considere usar uma tecnologia mais avançada, como [MSHTML.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85))

 

 

 