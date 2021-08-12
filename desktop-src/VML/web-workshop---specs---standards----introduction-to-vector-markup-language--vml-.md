---
title: Linguagem VML (VML)
description: Linguagem VML (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Linguagem VML (VML), sobre
- VML (linguagem VML), sobre
- elementos gráficos vetoriais, sobre
- gráficos vetoriais, linguagem VML (VML)
- Linguagem VML (VML), World Wide Web Consortium (W3C)
- VML (linguagem VML), World Wide Web Consortium (W3C)
- gráficos vetoriais, World Wide Web Consortium (W3C)
- gráficos vetoriais, benefícios da VML
- Linguagem VML (VML), benefícios
- VML (linguagem VML), benefícios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6199b481c58bbc5cd769ba43e614f21ae0105b4ef703858b559cdd76ff5516bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596062"
---
# <a name="vector-markup-language-vml"></a>Linguagem VML (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!NOTE]
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

Linguagem VML (VML) é um formato de troca, edição e entrega baseado em XML para gráficos de vetor de alta qualidade na Web que atende às necessidades de usuários de produtividade e profissionais de design gráfico. O XML é uma linguagem emergente simples, flexível e aberta baseada em texto que complementa o HTML. (consulte a [seção xml](/documentation/?frame=true) do Biblioteca MSDN para obter informações detalhadas sobre XML.)

Atualmente, a VML é suportada pelo Microsoft Internet Explorer versão 5,0 ou posterior.

A VML foi proposta para o W3C como padrão para gráficos vetoriais na Web (consulte [linguagem VML (VML)](https://www.w3.org/TR/NOTE-VML)). a Microsoft continua a liderar a cobrança no desenvolvimento e na implementação de tecnologias baseadas em XML, trabalhando com parceiros líderes do setor (AutoDesk, Hewlett-Packard, Macromedia Visio) e o W3C para aprimorar os padrões baseados na Web. Esperamos trabalhar com o W3C para, por fim, conduzir para um formato padrão para gráficos vetoriais na Web.

a VML também tem suporte no Microsoft Office 2000 ou posterior. Microsoft Word, Microsoft Excel e Microsoft PowerPoint podem ser usados para criar elementos gráficos VML.

### <a name="using-vml"></a>Usando VML

Para usar a VML em suas páginas da Web, use um elemento Style para importar o comportamento da VML, conforme mostrado no código a seguir.

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

Em seguida, declare o namespace VML, conforme mostrado no exemplo de código a seguir.

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

Por fim, adicione elementos VML para definir efeitos visuais. Por exemplo, o código VML a seguir cria uma oval vermelha.

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> Para obter melhores resultados ao usar documentos de modo estrito, certifique-se de que sua marcação é válida e bem formada. Para obter mais informações, consulte o! Página de referência de DOCTYPE.


### <a name="benefits-of-vml"></a>Benefícios do VML

-   A VML torna a criação mais fácil para usuários e autores de produtividade. Ele facilita a troca (por meio de recortar e colar) e a edição subsequente de gráficos vetoriais entre uma ampla variedade de aplicativos de produtividade e design.
-   A VML fornece downloads gráficos mais rápidos e uma melhor experiência do usuário. Ele permite a entrega de gráficos vetoriais escalonáveis, totalmente integrados e de alta qualidade para a Web, em um formato aberto baseado em texto. Em vez de referenciar gráficos como arquivos externos, os elementos gráficos VML são entregues embutidos com a página HTML, permitindo que eles interajam e dimensionem com a interação do usuário.
-   A VML é aberta e baseada em padrões. É um formato baseado em XML. O XML 1,0 é uma linguagem aberta, simples e baseada em texto para descrever dados estruturados na Web e complementa o HTML para exibição. A VML também dá suporte a outros padrões W3C, como folhas de estilos em cascata 2,0 (CSS), que especifica as informações de estilo e o posicionamento de 2D, bem como o Modelo de Objeto do Documento (DOM), que permite aos desenvolvedores interagir consistentemente com elementos de página como objetos.

### <a name="for-additional-information"></a>Para obter informações adicionais

Consulte os links abaixo:

-   Para obter respostas para perguntas frequentes sobre a VML, consulte as [perguntas frequentes](frequently-asked-questions-about-vml.yml)sobre a VML.
-   Para obter um tutorial sobre como usar o VML em páginas da Web, consulte [como usar a VML em páginas da Web](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), que complementa a [especificação de VML](https://www.w3.org/TR/NOTE-datetime.html) enviada ao W3C.
-   Para obter informações sobre tipos de dados VML, consulte o documento [tipos básicos de VML](basic-vml-types.md) .
-   Para obter a referência completa sobre o VML, incluindo informações sobre como usar a VML com marcas, bem como scripts, consulte a [referência da VML](msdn-online-vml-introduction.md).