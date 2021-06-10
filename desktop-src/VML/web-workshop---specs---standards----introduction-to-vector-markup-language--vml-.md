---
title: linguagem VML (VML)
description: linguagem VML (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- linguagem VML (VML),sobre
- VML (linguagem VML),sobre
- gráficos vetoriais, sobre
- vector graphics,linguagem VML (VML)
- linguagem VML (VML), World Wide Web Consortium (W3C)
- VML (linguagem VML),World Wide Web Consortium (W3C)
- vector graphics,World Wide Web Consortium (W3C)
- gráficos vetoriais, benefícios do VML
- linguagem VML (VML), benefícios
- VML (linguagem VML), benefícios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4637fff0550ce9c93e295c51fc529f62c370b8aa
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910255"
---
# <a name="vector-markup-language-vml"></a>linguagem VML (VML)

Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!NOTE]
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

linguagem VML (VML) é um formato de troca, edição e entrega baseado em XML para gráficos vetoriais de alta qualidade na Web que atende às necessidades de usuários de produtividade e profissionais de design gráfico. XML é uma linguagem baseada em texto simples, flexível e aberta que complementa HTML. (Consulte a [seção XML](/documentation/?frame=true) da Biblioteca MSDN para obter informações detalhadas sobre XML.)

Atualmente, o VML é suportado pela Microsoft Internet Explorer versão 5.0 ou posterior.

O VML foi proposto para o W3C como um padrão para gráficos vetoriais na Web [(consulte linguagem VML (VML)](https://www.w3.org/TR/NOTE-VML)). A Microsoft continua a ser responsável pelo desenvolvimento e implementação de tecnologias baseadas em XML, trabalhando com os principais parceiros do setor (AutoDesk, Hewlett-Packard, Macromedia, Visio) e o W3C para avançar os padrões baseados na Web. Esperamos trabalhar com o W3C para, em última análise, conduzir para um formato padrão para gráficos vetoriais na Web.

O VML também é suportado pelo Microsoft Office 2000 ou posterior. O Microsoft Word, o Microsoft Excel e o Microsoft PowerPoint podem ser usados para criar gráficos VML.

### <a name="using-vml"></a>Usando o VML

Para usar o VML em suas páginas da Web, use um elemento de estilo para importar o comportamento do VML, conforme mostrado no código a seguir.

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
> Para melhores resultados ao usar documentos de modo estrito, certifique-se de que sua marcação é válida e bem formada. Para obter mais informações, consulte o ! Página de referência DOCTYPE.


### <a name="benefits-of-vml"></a>Benefícios do VML

-   O VML facilita a geração para usuários e autores de produtividade. Ele facilita a troca (por meio de recortar e colar) e a edição subsequente de elementos gráficos vetoriais entre uma ampla variedade de aplicativos de design e produtividade.
-   O VML fornece downloads gráficos mais rápidos e uma melhor experiência do usuário. Ele permite a entrega de gráficos vetoriais de alta qualidade, totalmente integrados e escalonáveis para a Web, em um formato baseado em texto aberto. Em vez de referenciar gráficos como arquivos externos, os gráficos VML são entregues em linha com a página HTML, permitindo que eles interajam e dimensionem com a interação do usuário.
-   O VML é aberto e baseado em padrões. É um formato baseado em XML. O XML 1.0 é uma linguagem aberta, simples e baseada em texto para descrever dados estruturados na Web e complementa HTML para exibição. O VML também dá suporte a outros padrões W3C, como o folhas de estilos em cascata 2.0 (CSS), que especifica informações de estilo e posicionamento 2D, bem como o DOM (Modelo de Objeto do Documento), que permite que os desenvolvedores interajam consistentemente com elementos de página como objetos.

### <a name="for-additional-information"></a>Para obter informações adicionais

Confira os links abaixo:

-   Para obter respostas para perguntas frequentes sobre o VML, consulte as Perguntas [frequentes sobre o VML.](frequently-asked-questions-about-vml.yml)
-   Para ver um tutorial sobre como usar o VML em páginas da Web, consulte [How to Use VML on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), que complementa a especificação do [VML](https://www.w3.org/TR/NOTE-datetime.html) enviada ao W3C.
-   Para obter informações sobre tipos de dados VML, consulte o [documento Tipos básicos de VML.](basic-vml-types.md)
-   Para obter a referência completa sobre o VML, incluindo informações sobre como usar o VML com marcas, bem como scripts, consulte a [Referência de VML](msdn-online-vml-introduction.md).