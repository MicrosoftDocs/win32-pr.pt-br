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
ms.openlocfilehash: d0ba51fd041f36915eaafe20201876653f597e04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105754294"
---
# <a name="vector-markup-language-vml"></a><span data-ttu-id="a7677-113">Linguagem VML (VML)</span><span class="sxs-lookup"><span data-stu-id="a7677-113">Vector Markup Language (VML)</span></span>

<span data-ttu-id="a7677-114">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a7677-114">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a7677-115">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a7677-115">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!NOTE]
> <span data-ttu-id="a7677-116">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a7677-116">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a7677-117">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a7677-117">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a7677-118">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a7677-118">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a7677-119">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a7677-119">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

<span data-ttu-id="a7677-120">Linguagem VML (VML) é um formato de troca, edição e entrega baseado em XML para gráficos de vetor de alta qualidade na Web que atende às necessidades de usuários de produtividade e profissionais de design gráfico.</span><span class="sxs-lookup"><span data-stu-id="a7677-120">Vector Markup Language (VML) is an XML-based exchange, editing, and delivery format for high-quality vector graphics on the Web that meets the needs of both productivity users and graphic design professionals.</span></span> <span data-ttu-id="a7677-121">O XML é uma linguagem emergente simples, flexível e aberta baseada em texto que complementa o HTML.</span><span class="sxs-lookup"><span data-stu-id="a7677-121">XML is an emerging simple, flexible, and open text-based language that complements HTML.</span></span> <span data-ttu-id="a7677-122">(Consulte a [seção XML](/documentation/?frame=true) da biblioteca MSDN para obter informações detalhadas sobre XML.)</span><span class="sxs-lookup"><span data-stu-id="a7677-122">(See the [XML section](/documentation/?frame=true) of the MSDN Library for detailed information on XML.)</span></span>

<span data-ttu-id="a7677-123">Atualmente, a VML é suportada pelo Microsoft Internet Explorer versão 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a7677-123">VML is currently supported by Microsoft Internet Explorer version 5.0 or later.</span></span>

<span data-ttu-id="a7677-124">A VML foi proposta para o W3C como padrão para gráficos vetoriais na Web (consulte [linguagem VML (VML)](https://www.w3.org/TR/NOTE-VML)).</span><span class="sxs-lookup"><span data-stu-id="a7677-124">VML has been proposed to the W3C as a standard for vector graphics on the Web (see [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)).</span></span> <span data-ttu-id="a7677-125">A Microsoft continua a liderar a cobrança no desenvolvimento e na implementação de tecnologias baseadas em XML, trabalhando com parceiros líderes do setor (AutoDesk, Hewlett-Packard, Macromedia, Visio) e o W3C para aprimorar os padrões baseados na Web.</span><span class="sxs-lookup"><span data-stu-id="a7677-125">Microsoft is continuing to lead the charge in the development and implementation of XML-based technologies, working with leading industry partners (AutoDesk, Hewlett-Packard, Macromedia, Visio) and the W3C to advance Web-based standards.</span></span> <span data-ttu-id="a7677-126">Esperamos trabalhar com o W3C para, por fim, conduzir para um formato padrão para gráficos vetoriais na Web.</span><span class="sxs-lookup"><span data-stu-id="a7677-126">We expect to work with the W3C to ultimately drive to one standard format for vector graphics on the Web.</span></span>

<span data-ttu-id="a7677-127">A VML também tem suporte no Microsoft Office 2000 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a7677-127">VML is also supported by Microsoft Office 2000 or later.</span></span> <span data-ttu-id="a7677-128">O Microsoft Word, o Microsoft Excel e o Microsoft PowerPoint podem ser usados para criar gráficos VML.</span><span class="sxs-lookup"><span data-stu-id="a7677-128">Microsoft Word, Microsoft Excel, and Microsoft PowerPoint can be used to create VML graphics.</span></span>

### <a name="using-vml"></a><span data-ttu-id="a7677-129">Usando VML</span><span class="sxs-lookup"><span data-stu-id="a7677-129">Using VML</span></span>

<span data-ttu-id="a7677-130">Para usar a VML em suas páginas da Web, use um elemento Style para importar o comportamento da VML, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7677-130">To use VML in your web pages, use a style element to import the VML behavior, as shown in the following code.</span></span>

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

<span data-ttu-id="a7677-131">Em seguida, declare o namespace VML, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7677-131">Next, declare the VML namespace, as shown in the following code sample.</span></span>

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

<span data-ttu-id="a7677-132">Por fim, adicione elementos VML para definir efeitos visuais.</span><span class="sxs-lookup"><span data-stu-id="a7677-132">Finally, add VML elements to define visuals effects.</span></span> <span data-ttu-id="a7677-133">Por exemplo, o código VML a seguir cria uma oval vermelha.</span><span class="sxs-lookup"><span data-stu-id="a7677-133">For example, the following VML code creates a red oval.</span></span>

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> <span data-ttu-id="a7677-134">Para obter melhores resultados ao usar documentos de modo estrito, certifique-se de que sua marcação é válida e bem formada.</span><span class="sxs-lookup"><span data-stu-id="a7677-134">For best results when using strict mode documents, be sure that your markup is valid and well-formed.</span></span> <span data-ttu-id="a7677-135">Para obter mais informações, consulte o! Página de referência de DOCTYPE.</span><span class="sxs-lookup"><span data-stu-id="a7677-135">For more information, please see the !DOCTYPE reference page.</span></span>


### <a name="benefits-of-vml"></a><span data-ttu-id="a7677-136">Benefícios do VML</span><span class="sxs-lookup"><span data-stu-id="a7677-136">Benefits of VML</span></span>

-   <span data-ttu-id="a7677-137">A VML torna a criação mais fácil para usuários e autores de produtividade.</span><span class="sxs-lookup"><span data-stu-id="a7677-137">VML makes authoring easier for productivity users and authors.</span></span> <span data-ttu-id="a7677-138">Ele facilita a troca (por meio de recortar e colar) e a edição subsequente de gráficos vetoriais entre uma ampla variedade de aplicativos de produtividade e design.</span><span class="sxs-lookup"><span data-stu-id="a7677-138">It facilitates the exchange (via cut and paste) and subsequent editing of vector graphics between a wide variety of productivity and design applications.</span></span>
-   <span data-ttu-id="a7677-139">A VML fornece downloads gráficos mais rápidos e uma melhor experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7677-139">VML provides faster graphic downloads and a better user experience.</span></span> <span data-ttu-id="a7677-140">Ele permite a entrega de gráficos vetoriais escalonáveis, totalmente integrados e de alta qualidade para a Web, em um formato aberto baseado em texto.</span><span class="sxs-lookup"><span data-stu-id="a7677-140">It allows the delivery of high-quality, fully integrated, scalable vector graphics to the Web, in an open text-based format.</span></span> <span data-ttu-id="a7677-141">Em vez de referenciar gráficos como arquivos externos, os elementos gráficos VML são entregues embutidos com a página HTML, permitindo que eles interajam e dimensionem com a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a7677-141">Rather than referencing graphics as external files, VML graphics are delivered inline with the HTML page, allowing them to interact and scale with user interaction.</span></span>
-   <span data-ttu-id="a7677-142">A VML é aberta e baseada em padrões.</span><span class="sxs-lookup"><span data-stu-id="a7677-142">VML is open and standards-based.</span></span> <span data-ttu-id="a7677-143">É um formato baseado em XML.</span><span class="sxs-lookup"><span data-stu-id="a7677-143">It is an XML-based format.</span></span> <span data-ttu-id="a7677-144">O XML 1,0 é uma linguagem aberta, simples e baseada em texto para descrever dados estruturados na Web e complementa o HTML para exibição.</span><span class="sxs-lookup"><span data-stu-id="a7677-144">XML 1.0 is an open, simple, text-based language for describing structured data on the Web, and complements HTML for display.</span></span> <span data-ttu-id="a7677-145">A VML também dá suporte a outros padrões W3C, como folhas de estilos em cascata 2,0 (CSS), que especifica as informações de estilo e o posicionamento de 2D, bem como o Modelo de Objeto do Documento (DOM), que permite aos desenvolvedores interagir consistentemente com elementos de página como objetos.</span><span class="sxs-lookup"><span data-stu-id="a7677-145">VML also supports other W3C standards, such as Cascading Style Sheets 2.0 (CSS), which specifies style information and 2-D positioning, as well as the Document Object Model (DOM), which allows developers to interact consistently with page elements as objects.</span></span>

### <a name="for-additional-information"></a><span data-ttu-id="a7677-146">Para obter informações adicionais</span><span class="sxs-lookup"><span data-stu-id="a7677-146">For additional information</span></span>

<span data-ttu-id="a7677-147">Consulte os links abaixo:</span><span class="sxs-lookup"><span data-stu-id="a7677-147">See the links below:</span></span>

-   <span data-ttu-id="a7677-148">Para obter respostas para perguntas frequentes sobre a VML, consulte as [perguntas frequentes](frequently-asked-questions-about-vml.md)sobre a VML.</span><span class="sxs-lookup"><span data-stu-id="a7677-148">For answers to frequently asked questions about VML, see the [VML FAQ](frequently-asked-questions-about-vml.md).</span></span>
-   <span data-ttu-id="a7677-149">Para obter um tutorial sobre como usar o VML em páginas da Web, consulte [como usar a VML em páginas da Web](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), que complementa a [especificação de VML](https://www.w3.org/TR/NOTE-datetime.html) enviada ao W3C.</span><span class="sxs-lookup"><span data-stu-id="a7677-149">For a tutorial on using VML on Web pages, see [How to Use VML on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), which complements the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) submitted to the W3C.</span></span>
-   <span data-ttu-id="a7677-150">Para obter informações sobre tipos de dados VML, consulte o documento [tipos básicos de VML](basic-vml-types.md) .</span><span class="sxs-lookup"><span data-stu-id="a7677-150">For information on VML data types, see the [Basic VML Types](basic-vml-types.md) document.</span></span>
-   <span data-ttu-id="a7677-151">Para obter a referência completa sobre o VML, incluindo informações sobre como usar a VML com marcas, bem como scripts, consulte a [referência da VML](msdn-online-vml-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="a7677-151">For the complete reference on VML, including information on how to use VML with tags as well as scripting, see the [VML Reference](msdn-online-vml-introduction.md).</span></span>