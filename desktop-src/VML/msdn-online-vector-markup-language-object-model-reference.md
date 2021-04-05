---
title: Referência de modelo de objeto VML
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008071"
---
# <a name="vml-object-model-reference"></a>Referência de modelo de objeto VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Neste tópico:

-   [Introdução](#introduction)
-   [Exemplo](#example)
-   [Configurando a VML](#setting-up-vml)
-   [Referência de OM de VML](#vml-om-reference)
    -   [Elemento Shape](#shape-element)
-   [Subelementos do elemento Shape](#subelements-of-the-shape-element)
    -   [Elemento background](#background-element)
    -   [Elemento de extrusão](#extrusion-element)
    -   [Elemento Fill](#fill-element)
    -   [Elemento Group](#group-element)
    -   [Elemento ImageData](#imagedata-element)
    -   [Elemento Path](#path-element)
    -   [Elemento Shadow](#shadow-element)
    -   [Elemento skew](#skew-element)
    -   [Elemento Stroke](#stroke-element)
    -   [Elemento TextPath](#textpath-element)
-   [Tipos de dados usados no modelo de objeto VML](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>Introdução

[Linguagem VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) é uma linguagem baseada em texto que usa [XML](https://www.w3.org/TR/REC-xml.mdl) para estender o HTML com a finalidade de exibir informações gráficas vetoriais. O Modelo de Objeto do Documento do VML (DOM) define uma interface programática para a manipulação dos elementos do documento. Isso permite que o usuário crie e modifique dinamicamente gráficos vetoriais por meio de uma interface neutra de plataforma e linguagem. O DOM do VML está em conformidade com a especificação de [modelo de objeto do documento](https://www.w3.org/TR/REC-DOM-Level-1/) .

A VML usa o elemento [Shape](#shape-element) como o bloco de construção básico para imagens gráficas vetoriais. Depois que uma forma é criada, você pode modificar a forma por meio de atributos ou de subelementos anexados. Por exemplo, para alterar a cor de uma forma, atribua um valor de cor ao atributo **FillColor** .


```HTML
myshape.fillcolor = "red"
```



Vários dos atributos de uma forma também são [subelementos](/windows) e têm seus próprios atributos, incluindo o seguinte:

-   [Tela de fundo](#background-element)
-   [Extrusão](#extrusion-element)
-   [Preencher](#fill-element)
-   [Grupo](#group-element)
-   [Imagedata](#imagedata-element)
-   [Caminho](#path-element)
-   [Shadow](#shadow-element)
-   [Inclinar](#skew-element)
-   [Pincel](#stroke-element)
-   [TextPath](#textpath-element)

O OM de VML usa vários [tipos de dados](/windows) para definir parâmetros. Os tipos de texto prefixados com "VG" são enumerações e aqueles prefixados com "IVg" são objetos. Clique aqui para obter uma lista. Os tipos de texto secundários são listados com parâmetros específicos.

## <a name="example"></a>Exemplo

O código VBScript a seguir mostra como criar uma forma simples:


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



No exemplo acima, uma forma é criada usando o método Modelo de Objeto do Documento **CreateElement**. A forma é uma forma Rect predefinida de VML. Embora o objeto exista, ele não pode fazer parte do documento até que seja anexado ao documento. Usando o método **AppendChild** , o Rect torna-se um filho de um elemento **div** chamado MyDiv. Alguns atributos de estilo mínimos (**posição**, **largura**, **altura**, **superior**, **esquerda**) são definidos para dar um tamanho específico à forma. Por fim, uma cor é atribuída com o atributo **FillColor** . Observe que qualquer linguagem de script ou qualquer linguagem que possa trabalhar com interfaces Modelo de Objeto do Documento pode ser usada.

## <a name="setting-up-vml"></a>Configurando a VML

Uma implementação de VML é por meio do Microsoft Internet Explorer 5,0 ou superior. Para configurar o objeto de renderização corretamente em uma página da Web, as seguintes adições devem ser feitas:

1.  O esquema deve ser configurado na inicial <HTML> Marque da seguinte maneira:
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  O comportamento de renderização deve fazer parte do estilo do documento:
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

Veja a seguir um exemplo de página da Web HTML configurada corretamente para VML mostrando a criação dinâmica de uma forma.


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



Observe que, em versões beta, uma marca de objeto ActiveX e um estilo de comportamento diferente eram necessários.

## <a name="vml-om-reference"></a>Referência de OM de VML

Essa referência define o elemento [Shape](#shape-element) , os [subelementos](/windows)e os [tipos de dados](/windows) que são usados pelo modelo de objeto de VML.

### <a name="shape-element"></a>Elemento Shape

As formas são os blocos de construção de imagens gráficas definidas por linguagem VML (VML). A forma é o elemento de nível superior e vários subelementos ajudam a definir a natureza de cada forma.

A VML fornece formas predefinidas:

**Atributos de forma**

-   **Arc**
-   **Curva**
-   **Linha**
-   **Múltipla**
-   **Rect**
-   **RoundRect**



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ajuste          | [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md). Uma lista delimitada por vírgulas de números que são os parâmetros para as fórmulas de guia que definem o caminho da forma. Os valores podem ser omitidos para permitir o uso de padrões. Pode haver até 8 valores de ajuste.                                                                                                   |
| Alt          | Cadeia de caracteres. Texto alternativo associado à forma. Usado para navegação não gráfica.                                                                                                                                                                                                                                                                                                 |
| Botão       | [VgTriState](msdn-online-vml-vgtristate.md). Exibe o comportamento do botão ao clicar.                                                                                                                                                                                                                                                                                                 |
| BWMode       | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina como a forma será renderizada no modo de exibição preto-e-branco em aplicativos ou quando impressa em impressoras pretas e brancas. Os valores incluem: **cor**, **automático**, **escala de cinza**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **preto**, **branco**, não **desenhado**. Padrão: **automático**. |
| BWNormal     | VgBlackWhiteMode. Quando BWMode é automático, essa propriedade é consultada sobre como renderizar a forma em preto e branco normal. Os valores incluem: **cor**, **automático**, **escala de cinza**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **preto**, **branco**, não **desenhado**. Padrão: **automático**.                                                |
| BWPure       | VgBlackWhiteMode. Quando BWMode é automático, essa propriedade é consultada sobre como renderizar a forma em B/W puro. Os valores incluem: **cor**, **automático**, **escala de cinza**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **preto**, **branco**, não **desenhado**. Padrão: **automático**.                                                              |
| ChildShapes  | IVgGroupShapes. Uma coleção de outras formas neste grupo. Esta coleção dá suporte aos métodos de comprimento e item padrão.                                                                                                                                                                                                                                                       |
| Chromakey    | [IVgColor](msdn-online-vml-ivgcolor.md). Um valor de cor que será transparente e mostrará qualquer coisa por trás da forma.                                                                                                                                                                                                                                                             |
| Control1     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Ponto de controle para curva.                                                                                                                                                                                                                                                                                                  |
| Control2     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Ponto de controle para curva.                                                                                                                                                                                                                                                                                                  |
| CoordOrigin  | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md) As coordenadas no canto superior esquerdo do retângulo do contêiner. Intervalo de 0 a infinito.                                                                                                                                                                                                                               |
| CoordSize    | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). A largura e a altura do espaço de coordenadas dentro do retângulo de referência dessa forma. Se não for especificado, será o mesmo que a largura e a altura do retângulo. Intervalo de 0 a infinito. Padrão: "1000, 1000".                                                                                               |
| Ângulo de fim     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Ângulo de extremidade da forma.                                                                                                                                                                                                                                                                                          |
| Extrusão    | IVgExtrusion. Especifica o valor do objeto de extrusão para esta forma. Consulte o elemento de [extrusão](msdn-online-vml-extrusion-element.md) para obter detalhes.                                                                                                                                                                                                                               |
| Preencher         | VgFillFormat. Especifica o valor de preenchimento para esta forma. Consulte o elemento [Fill](msdn-online-vml-fill-element.md) para obter mais detalhes.                                                                                                                                                                                                                                                |
| EstiloDePreenchimento    | [IVgColor](msdn-online-vml-ivgcolor.md). A cor primária do pincel a ser usada para preencher o caminho desta forma.                                                                                                                                                                                                                                                                  |
| Preencher       | [VgTriState](msdn-online-vml-vgtristate.md). Se for true, o caminho que define a forma será preenchido. Por padrão, ele será preenchido usando uma cor sólida, a menos que haja um subelemento Fill que especifique propriedades de preenchimento mais complexas. Se for false, o preenchimento será transparente.                                                                                                           |
| Inverter         | VgFlipOrientation. Os valores são: X Y XY YX                                                                                                                                                                                                                                                                                                                                         |
| ForceDash    | [VgTriState](msdn-online-vml-vgtristate.md). Indica que um contorno tracejado deve ser renderizado quando não há nenhuma linha e nenhum preenchimento para uma forma. Esse comportamento é geralmente útil para tornar as formas invisíveis visíveis na edição de aplicativos para que possam ser selecionadas e operadas, como em um mapa de imagem.                                                                 |
| Fórmulas     | IVgFormulas. Uma matriz de fórmulas que define uma forma.                                                                                                                                                                                                                                                                                                                          |
| De         | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Ponto de partida da linha.                                                                                                                                                                                                                                                                                                   |
| HRef         | [Cadeia de caracteres](#data-types-used-in-the-vml-object-model). A URL para saltar se essa forma for clicada.                                                                                                                                                                                                                                                                                 |
| ImageData    | IVgImageData. Informações da imagem se a forma for uma imagem. Consulte o elemento ImageData para obter mais informações.                                                                                                                                                                                                                                                                       |
| OnEd         | [VgTriState](msdn-online-vml-vgtristate.md). Oculta todos os identificadores, exceto a parte superior esquerda e inferior direita, como nos identificadores de um segmento de linha reta.                                                                                                                                                                                                                             |
| Opacidade      | [VgFraction](msdn-online-vml-vgfraction-data-type.md). A opacidade de toda a forma. Um número entre 0,0 e 1,0.                                                                                                                                                                                                                                                           |
| Caminho         | IVgPath. Uma cadeia de caracteres que contém os comandos que definem o caminho.                                                                                                                                                                                                                                                                                                                  |
| Pontos       | [IVgPoints](msdn-online-vml-ivgpoints-data-type.md). Uma coleção de pontos que define uma forma.                                                                                                                                                                                                                                                                                   |
| Imprimir        | [VgTriState](msdn-online-vml-vgtristate.md). Se for true, essa forma deve ser impressa.                                                                                                                                                                                                                                                                                        |
| Rotação     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Define a rotação da forma. O valor é propagado para o estilo de forma.                                                                                                                                                                                                                                              |
| Escala        | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Escala de forma.                                                                                                                                                                                                                                                                                                           |
| Shadow       | IVgShadow. Especifica a sombra desta forma. Consulte o elemento [Shadow](msdn-online-vml-shadow-element.md) para obter detalhes.                                                                                                                                                                                                                                                        |
| Spt          | Reservado.                                                                                                                                                                                                                                                                                                                                                                        |
| StartAngle   | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Ângulo inicial da forma.                                                                                                                                                                                                                                                                                        |
| Traço       | VgStrokeFormat. Consulte elemento de traço para obter detalhes.                                                                                                                                                                                                                                                                                                                                  |
| StrokeColor  | [IVgColor](msdn-online-vml-ivgcolor.md). A cor primária do pincel a ser usada para traçar o caminho desta forma.                                                                                                                                                                                                                                                                |
| Traçados      | [VgTriState](msdn-online-vml-vgtristate.md). Se for true, o caminho que define a forma será traçado.                                                                                                                                                                                                                                                                              |
| StrokeWeight | [VGLength](msdn-online-vml-vglength.md). A largura do pincel a ser usada para traçar o caminho. Intervalos entre 0 e 1584.                                                                                                                                                                                                                                                           |
| TextPath     | IVgTextPath. Especifica o objeto TextPath da forma. Consulte o elemento [TextPath](msdn-online-vml-textpath-element.md) para obter mais informações.                                                                                                                                                                                                                                  |
| Para           | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Ponto de extremidade da linha.                                                                                                                                                                                                                                                                                                        |
| Tipo         | Cadeia de caracteres. Tipo de forma.                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Subelementos do elemento Shape

Os subelementos a seguir fazem parte do modelo de objeto VML.

-   [Tela de fundo](#background-element)
-   [Extrusão](#extrusion-element)
-   [Preencher](#fill-element)
-   [Grupo](#group-element)
-   [Imagedata](#imagedata-element)
-   [Caminho](#path-element)
-   [Shadow](#shadow-element)
-   [Inclinar](#skew-element)
-   [Pincel](#stroke-element)
-   [TextPath](#textpath-element)

### <a name="background-element"></a>Elemento background

Descreve o preenchimento do plano de fundo de uma página usando preenchimentos de VML.

**Atributos**



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BWMode    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina como a forma será renderizada no modo de exibição preto e branco em aplicativos ou quando impressa.                                     |
| BWNormal  | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Quando BWMode é automático, essa propriedade é consultada sobre como renderizar a forma em preto e branco normal.                        |
| BWPure    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Quando BWMode é automático, essa propriedade é consultada sobre como renderizar a forma em preto e branco puro.                          |
| Preencher      | VgFillFormat. Especifica o preenchimento desta forma. Confira elemento [Fill](msdn-online-vml-fill-element.md) para obter mais informações.                                                             |
| EstiloDePreenchimento | [IVgColor](msdn-online-vml-ivgcolor.md). A cor primária do pincel a ser usada para preencher o caminho desta forma. Duplicata do valor de cor no elemento Fill. O padrão é branco. |



 

### <a name="extrusion-element"></a>Elemento de extrusão

Descreve uma extrusão 3D da forma.

**Atributos**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AutoRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Se for true, o centro de rotação do grupo de objetos 3D (na verdade, há apenas um objeto no grupo) será determinado automaticamente para ser o centro do grupo; caso contrário, ele é determinado pelos parâmetros RotationCenter, que são uma fração da forma com 0, 0, sendo o centro.</td>
</tr>
<tr class="even">
<td>Profundidade de fundo</td>
<td><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>. Quantidade de extrusão regressiva. Varia de 0 a 32767.</td>
</tr>
<tr class="odd">
<td>Brightness</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Brilho geral da cena. O padrão é &quot; 20.000 &quot; .</td>
</tr>
<tr class="even">
<td>Cor</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. A cor da extrusão. Usado somente se ColorMode for personalizado. Caso contrário, o define automaticamente a cor do efeito de extrusão como o mesmo que FillColor.</td>
</tr>
<tr class="odd">
<td>ColorMode</td>
<td>Vg3DColorMode. Os valores são:
<ul>
<li>Auto (padrão)</li>
<li>Personalizado</li>
</ul></td>
</tr>
<tr class="even">
<td>Difusão</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. A taxa de incidente para a luz refletida difusamente. Valores menores que 1,0 são normais, mas valores maiores que um podem gerar efeitos interessantes.</td>
</tr>
<tr class="odd">
<td>Edge</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Define o tamanho de uma borda chanfrada arredondada simulada. Varia de 0 a 32767 em ponto flutuante pts. O padrão é &quot; 1pt &quot; .</td>
</tr>
<tr class="even">
<td>Faceta</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Define a faceta da cena. O padrão é &quot; 30.000 &quot; .</td>
</tr>
<tr class="odd">
<td>ForeDepth</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Quantidade de extrusão posterior. Varia de 0 a 32767.</td>
</tr>
<tr class="even">
<td>LightFace</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Determimes se a face frontal do objeto responderá às alterações na iluminação 3D, por exemplo, quando um objeto for girado.</td>
</tr>
<tr class="odd">
<td>LightHarsh</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Iluminação de inverso para a fonte de luz primária. O padrão é Falso.</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Iluminação de durabilidade para a fonte de luz secundária. O padrão é Falso.</td>
</tr>
<tr class="odd">
<td>LightLevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensidade da fonte de luz primária. O padrão é &quot; 38000 &quot; .</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensidade da fonte de luz secundária. O padrão é &quot; 38000 &quot; .</td>
</tr>
<tr class="odd">
<td>LightPosition</td>
<td>Vector3D. Posição da fonte de luz primária. O padrão é &quot; 50000, 0, 10000 &quot; .</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3D. Posição da fonte de luz secundária. O padrão é &quot; -50000, 0, 10000 &quot; .</td>
</tr>
<tr class="odd">
<td>LockRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. &quot;Lockrotationcenter &quot; significa que a rotação do grupo é definida para ser por ângulo de rotação [1] graus sobre o eixo y na página seguido por ângulo de rotação [0] graus sobre o eixo x. Quando LockRotationCenter é false, a rotação é definida de acordo com os graus de ângulo de orientação sobre o vetor definido por orientação. Portanto, por exemplo, lockrotationcenter = false orientationangle = 45 Orientation = (0, 1, 0) é equivalente a lockrotationcenter = true RotationAngle = (0, 45).</td>
</tr>
<tr class="even">
<td>Metal</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Faz com que a luz refletida de forma especulada seja a cor do material em vez da cor da fonte de luz, tornando o objeto aparentemente mais metálico.</td>
</tr>
<tr class="odd">
<td>Ativado</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Ativa e desativa a exibição do efeito de extrusão.</td>
</tr>
<tr class="even">
<td>Orientation</td>
<td>Vector3D. Orientação da câmera.</td>
</tr>
<tr class="odd">
<td>OrientationAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Ângulo entre a orientação da câmera e o plano XY.</td>
</tr>
<tr class="even">
<td>Aérea</td>
<td>Vg3DExtrudePlane. Permite a extrusão dos planos ortogonal ao plano de tela. Requer que ForeDepth e a profundidade de fundo sejam especificadas em unidades de desenho em vez de emus. Os valores são:
<ul>
<li>XY</li>
<li>ZX</li>
<li>YZ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Renderizar</td>
<td>Vg3DRenderMode. Os valores são:
<ul>
<li>Solid (padrão)</li>
<li>WireFrame</li>
<li>BoundingCube</li>
</ul></td>
</tr>
<tr class="even">
<td>RotationAngle</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. AngleX, incline ou AngleZ é controlado pelo atributo ShapeRotation.</td>
</tr>
<tr class="odd">
<td>RotationCenter</td>
<td>Vector3D. Centro de rotação.</td>
</tr>
<tr class="even">
<td>Luminosidade</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Determina o quão concentrado ou distribuído a reflexão especular é. Um valor alto seria de 8 a 10 e aproximaria um espelho, e um valor baixo seria de 2 a 3 e seria um roupas sequined aproximado. São recomendados valores de 3 a 7. Valores altos refletirão as fontes de luz do Pinpoint.</td>
</tr>
<tr class="odd">
<td>SkewAmt</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>. Se Type for Parallel, o atributo determinará a quantidade de distorção. Varia de 0 a 100.</td>
</tr>
<tr class="even">
<td>SkewAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Se Type for Parallel, o atributo determinará o grau de distorção. O padrão é &quot; -45 &quot; .</td>
</tr>
<tr class="odd">
<td>Refletir</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. A taxa de incidentes para a luz refletida especulada. Valores menores que 1,0 são normais, mas valores maiores que um podem gerar efeitos interessantes.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgExtrusionType. Os valores são:
<ul>
<li>Paralelo (padrão)</li>
<li>Perspectiva</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ponto</td>
<td>Vector3D. O ponto em que a cena está sendo visualizada.</td>
</tr>
<tr class="even">
<td>ViewpointOrigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Pode ter valores de 0,5 a 0,5 para posicionar a origem do ponto de vista dentro da caixa delimitadora de forma.</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Elemento Fill

Descreve como um caminho deve ser preenchido para preenchimentos mais complexos do que uma cor sólida.

**Atributos**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Alinhe a imagem com a forma. Se for false, alinhar a imagem com a janela.</td>
</tr>
<tr class="even">
<td>Ângulo</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. O ângulo ao longo do qual o gradiente vai. 0 graus é ao longo do eixo horizontal da esquerda para a direita.</td>
</tr>
<tr class="odd">
<td>Aspecto</td>
<td><strong>VgAspectType</strong>. O atributo ImageSize será ajustado para preservar o aspecto da imagem. Os valores são:
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorar</td>
<td>Ignorar problemas de aspecto.</td>
</tr>
<tr class="even">
<td>Mínimo</td>
<td>A imagem é pelo menos tão grande quanto o tamanho da imagem.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>A imagem não é maior que o tamanho da imagem.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Cor</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> A cor de preenchimento principal. Mesmo que o atributo FillColor na forma.</td>
</tr>
<tr class="odd">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. A cor secundária de um preenchimento quando o tipo de imagem é padrão ou um preenchimento gradiente.</td>
</tr>
<tr class="even">
<td>Cores</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>. Cores intermediárias no gradiente e suas posições relativas ao longo do gradiente, por exemplo, &quot; 30% vermelho, 70% azul, 90% verde &quot; . A cor primária (atributo de cor em forma) é 0% e a cor secundária (atributo Color2) é de 100%.</td>
</tr>
<tr class="odd">
<td>Foco</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>. Ponto focal para preenchimento de gradiente linear. Os valores vão de-100 a + 100.</td>
</tr>
<tr class="even">
<td>FocusPosition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Posição do retângulo mais interno para gradientes radiais. O vetor é uma fração (0,0-1,0) da largura e da altura da forma.</td>
</tr>
<tr class="odd">
<td>FocusSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Tamanho do retângulo mais interno para gradientes radiais. O vetor é uma fração (0,0 a 1,0) da largura e da altura da forma.</td>
</tr>
<tr class="even">
<td>Método</td>
<td>VgSigmaType. Os valores são:
<ul>
<li>Nenhum</li>
<li>Linear</li>
<li>Sigma</li>
<li>Qualquer</li>
</ul>
<p>O padrão é Sigma.</p></td>
</tr>
<tr class="odd">
<td>Ativado</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Ativa a exibição de preenchimento. O mesmo que o atributo Fill na forma.</td>
</tr>
<tr class="even">
<td>Opacidade</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacidade do preenchimento.</td>
</tr>
<tr class="odd">
<td>Opacity2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. A opacidade secundária para gradientes.</td>
</tr>
<tr class="even">
<td>Origem</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Ponto relativo ao canto superior esquerdo da imagem que é tratada como a origem da imagem. O padrão é o centro da imagem. O vetor é uma fração (de 0,0 a 1,0) da largura e da altura da imagem.</td>
</tr>
<tr class="odd">
<td>Posição</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Ponto no retângulo de referência da forma para posicionar a origem da imagem. O padrão é o centro do retângulo do contêiner. O vetor é uma fração (0,0-1,0) da largura e da altura da imagem.</td>
</tr>
<tr class="even">
<td>Tamanho</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. O tamanho da imagem. O padrão é o tamanho do pixel da imagem. Pode ser especificado em coordenadas absolutas ou em porcentagem.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>. URL para uma imagem a ser carregada para preenchimentos de imagem e padrão. Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgFillType. Pode ser um dos seguintes tipos:
<ul>
<li>Tela de fundo</li>
<li>Quadro</li>
<li>Gradient</li>
<li>GradientCenter</li>
<li>GradientRadial</li>
<li>GradientTitle</li>
<li>GradientUnscaled</li>
<li>Padrão</li>
<li>Sólido</li>
<li>Tile</li>
</ul>
O bloco, o padrão e o quadro exigem que os atributos da imagem sejam fornecidos. Gradiente e GradientRadial exigem que os atributos de gradiente sejam fornecidos.</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>Elemento Group

Um grupo é uma coleção de formas individuais que podem ser posicionadas e transformadas como uma unidade.



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| Item   | [IVgShape](#data-types-used-in-the-vml-object-model). Item especificado na matriz de formas. |
| Comprimento | [Integer](#data-types-used-in-the-vml-object-model). Número de formas neste grupo.         |



 

### <a name="imagedata-element"></a>Elemento ImageData

Descreve uma imagem a ser renderizada na parte superior de uma forma.



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binível     | [VgTriState](msdn-online-vml-vgtristate.md). Exibir imagem em apenas duas cores (geralmente preto e branco).                                                                                                                                                                                                                                                     |
| BlackLevel  | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Permite ajuste para definir o nível de forma que os pretos apareçam como verdadeiros pretos e todas as outras cores fiquem visíveis como sombras acima do preto.                                                                                                                                                                        |
| Chromakey   | [IVgColor](msdn-online-vml-ivgcolor.md). Cor transparente da imagem.                                                                                                                                                                                                                                                                                         |
| CropBottom  | [VgNumber](#data-types-used-in-the-vml-object-model). Cortar distância da parte inferior da imagem expressa como uma porcentagem do tamanho da imagem.                                                                                                                                                                                                                           |
| CropLeft    | [VgNumber](#data-types-used-in-the-vml-object-model). Corte de distância da borda esquerda da imagem expressa como uma fração do tamanho da imagem (de 0,0 a 1,0). No entanto, o "corte de saída" tem suporte e, portanto, os valores inferiores a 0 e maiores que 1 têm suporte; por exemplo,-5, 20 descortaremos os limites 25X o tamanho da imagem com 4/5 em um lado da imagem. |
| CropRight   | [VgNumber](#data-types-used-in-the-vml-object-model). Cortar distância da direita da imagem expressa como uma porcentagem do tamanho da imagem.                                                                                                                                                                                                                            |
| CropTop     | [VgNumber](#data-types-used-in-the-vml-object-model). Cortar distância da parte superior da imagem expressa como uma porcentagem do tamanho da imagem.                                                                                                                                                                                                                              |
| EmbossColor | [IVgColor](msdn-online-vml-ivgcolor.md). Isso é definido como uma porcentagem da cor da sombra para criar um efeito de imagem em alto-relevo.                                                                                                                                                                                                                                 |
| Conheça        | [VgPositiveNumber](#data-types-used-in-the-vml-object-model). Ajusta a intensidade de todas as cores. Basicamente define como o branco brilhante será. Varia de 0 a 32767.                                                                                                                                                                                           |
| Gama       | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Correção gama. Aumentá-lo dá mais contraste a uma imagem.                                                                                                                                                                                                                                           |
| GrayScale   | [VgTriState](msdn-online-vml-vgtristate.md). Exibir imagem em cores de escala de cinza.                                                                                                                                                                                                                                                                              |
| Src         | [Cadeia de caracteres](#data-types-used-in-the-vml-object-model). URL para uma imagem a ser carregada para preenchimentos de imagem e padrão. Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.                                                                                                                                                           |



 

### <a name="path-element"></a>Elemento Path

Define o caminho que compõe a forma, usando uma cadeia de caracteres que contém um conjunto avançado de comandos de "movimento de caneta".



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Limo</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>. Define o ponto em que a forma é alongada; por exemplo, para uma forma Giraffe, o ponto de limo estaria no pescoço, portanto, quando a forma for redimensionada, o pescoço será alongado e o restante da forma manterá suas dimensões.</td>
</tr>
<tr class="even">
<td>TextBoxRect</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>. Matriz que contém os retângulos que definem onde o texto deve ir.</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>. Faz a correspondência do atributo v na marca de caminho. Observe que o caminho pode corresponder ao atributo ou elemento de caminho.</td>
</tr>
<tr class="even">
<td>Valor</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>. Uma representação de texto dos comandos que definem o caminho. Os valores de coordenadas X ou y podem ser uma referência a uma fórmula no formulário em &quot; @# &quot; que # é o número ordinal da fórmula, por exemplo, &quot; @2 &quot; . Essa cadeia de caracteres de atributo é composta por um conjunto avançado de comandos, incluindo o seguinte: <br/> 
<table>
<thead>
<tr class="header">
<th>Comando</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AE (angleellipseto)</td>
<td><strong>Centro</strong>(x, y) <strong>tamanho</strong>(w, h) <strong>início-ângulo</strong>, <strong>ângulo de extremidade</strong><br/> Desenhe um segmento de uma elipse. Uma linha reta é desenhada a partir do ponto atual até o ponto inicial do segmento.<br/></td>
</tr>
<tr class="even">
<td>Al (angleelipse)</td>
<td>O mesmo que a AE, exceto que há um m implícito para o ponto inicial do segmento.</td>
</tr>
<tr class="odd">
<td>ar (arco)</td>
<td>O mesmo que em. No entanto, um novo subcaminho é iniciado por um m implícito até o ponto inicial do arco.</td>
</tr>
<tr class="even">
<td>at (ArcTo)</td>
<td><strong>esquerda</strong>, <strong>superior</strong>, <strong>direita</strong>, <strong>inferior</strong>, <strong>início</strong>(x, y) <strong>fim</strong>(x, y) <br/> Os quatro primeiros valores definem a caixa delimitadora de uma elipse. Os últimos quatro definem dois vetores radiais. Um segmento da elipse é desenhado que começa no ângulo definido pelo vetor RADIUS inicial e termina no ângulo definido pelo vetor de término. Uma linha reta é desenhada a partir do ponto atual até o início do arco. O arco é sempre desenhado em uma direção no sentido anti-horário. <br/></td>
</tr>
<tr class="odd">
<td>c (curvato)</td>
<td><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>para</strong>(x, y) <br/> Desenhe uma curva de Bézier cúbica do ponto atual até a coordenada fornecida pelos dois parâmetros finais, os pontos de controle fornecidos pelos quatro primeiros parâmetros. O ponto atual torna-se o ponto de extremidade do Bezier.<br/></td>
</tr>
<tr class="even">
<td>e (final)</td>
<td>Finalizar o conjunto atual de subcaminhos. Um determinado conjunto de subcaminhos (como delimitados por fim) é preenchido usando eofill. Os conjuntos subsequentes de subcaminhos são preenchidos de forma independente e sobrepostas em itens existentes.</td>
</tr>
<tr class="odd">
<td>l (LineTo)</td>
<td>x, y<br/> Desenha uma linha do ponto atual para a coordenada x, y, que se torna o novo ponto atual. Pares de coordenadas adicionais podem ser especificados para formar uma polilinha, por exemplo, &quot; l 10, 13, 45, 27, 89,-12 &quot; .<br/></td>
</tr>
<tr class="even">
<td>m (MoveTo)</td>
<td>x, y<br/> Inicie um novo subcaminho na coordenada x, y.<br/></td>
</tr>
<tr class="odd">
<td>NF (Nofill)</td>
<td>O conjunto de subcaminhos atual (delimitado por fim) não será preenchido.</td>
</tr>
<tr class="even">
<td>NS (nostroke)</td>
<td>O conjunto de subcaminhos atual (delimitado por fim) não será traçado.</td>
</tr>
<tr class="odd">
<td>QB (quadraticbezier)</td>
<td>(<strong>ControlPoint</strong>(x, y)) *,<strong>fim</strong>(x, y) <br/> Define uma ou mais curvas de Bézier quadráticas por meio de pontos de controle e um ponto de extremidade. Pontos intermediários (em curva) são obtidos pela interpolação entre pontos de controle sucessivos semelhantes a fontes TrueType. O subcaminho não precisa ser um início; nesse caso, o subcaminho é fechado e o último ponto define o ponto de partida.<br/></td>
</tr>
<tr class="even">
<td>qx (ellipticalquadrantx)</td>
<td><strong>fim</strong>(x, y) <br/> Uma elipse de trimestre é desenhada do ponto atual para o ponto de extremidade fornecido. Inicialmente, o segmento elíptico é tangential a uma linha paralela ao eixo x; ou seja, o segmento começa horizontalmente.<br/></td>
</tr>
<tr class="odd">
<td>qy (ellipticalquadranty)</td>
<td><strong>fim</strong>(x, y) <br/> O mesmo que QX, exceto que o segmento elíptico é inicialmente tangential para uma linha paralela ao eixo y; ou seja, o segmento começa verticalmente.<br/></td>
</tr>
<tr class="even">
<td>r (rlineto)</td>
<td>x, y <br/> Desenhe uma linha do ponto atual para a coordenada relativa (cpx + x, CPY + y). Se pares de coordenadas adicionais forem fornecidos, cada novo ponto será calculado em relação ao último.<br/></td>
</tr>
<tr class="odd">
<td>t (rmoveto)</td>
<td>x, y<br/> Inicie um novo subcaminho nas coordenadas relativas (cpx + x, CPY + y) em que cpx, CPY é a posição atual. <br/></td>
</tr>
<tr class="even">
<td>v (curvato)</td>
<td><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>para</strong> (x, y) <br/> Curva de Bézier cúbica usando as coordenadas fornecidas em relação ao ponto atual. Todos os pontos são computados em relação ao mesmo ponto de partida.<br/></td>
</tr>
<tr class="odd">
<td>WA (clockwisearcto)</td>
<td>O mesmo que em, mas o arco é desenhado em uma direção horária.</td>
</tr>
<tr class="even">
<td>WR (clockwisearc)</td>
<td>O mesmo que ar, mas é desenhado em direção horária.</td>
</tr>
<tr class="odd">
<td>x (fechar)</td>
<td>Feche o subcaminho atual, desenhando uma linha reta do ponto atual para o ponto de mover original.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a>Elemento Shadow

Descreve um efeito de sombra em uma forma.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Cor</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Cor da sombra primária. O padrão é RGB (128128128)</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Cor da segunda sombra ou realce em uma sombra em relevo ou em baixo-relevo. O padrão é RGB (203203203).</td>
</tr>
<tr class="odd">
<td>Matriz</td>
<td><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>. Uma matriz de transformação de perspectiva no formato, &quot; Sxx, SXY, syx, syy, px, py &quot; [s = Scale, p = Perspective]. Os s itens especificam como a sombra deve ser dimensionada em relação à forma, e os itens p especificam como a sombra deve ser distorcida em relação à forma. Por exemplo, a matriz a seguir redimensiona a forma por um fator de 2 e a inclina por um fator de 4 em todas as direções: <br/> &quot;2, 2, 2, 2, 4, 4&quot;<br/> Essa matriz só será usada se o tipo da sombra for definido como perspectiva.<br/></td>
</tr>
<tr class="even">
<td>Obscurecida</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. A sombra pode ser vista por meio de se não houver preenchimento da forma. O padrão é Falso.</td>
</tr>
<tr class="odd">
<td>Deslocamento</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>. Valor do deslocamento x, y do local da forma. O padrão é &quot; 2PT, 2PT &quot; .</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Valor do deslocamento x, y segundo do local da forma? s. Os valores são uma medida absoluta ou um valor fracionário de Shape (-0,5 a + 0,5).</td>
</tr>
<tr class="odd">
<td>Ativado</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Ativa e desativa a exibição da sombra.</td>
</tr>
<tr class="even">
<td>Opacidade</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacidade do efeito de sombra.</td>
</tr>
<tr class="odd">
<td>Origem</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Um par de valores fracionários de forma de-0,5 a + 0,5.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>. Os valores são:
<ul>
<li>Único (padrão)</li>
<li>Double</li>
<li>Perspectiva</li>
<li>ShapeRelative</li>
<li>DrawingRelative</li>
<li>Emboss</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a>Elemento skew

Descreve um efeito de inclinação de perspectiva em uma forma. A distorção é aplicada aos dados gráficos vetoriais, não aos dados da imagem.



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Matriz | [IVgSkewMatrix](#data-types-used-in-the-vml-object-model). Uma matriz de transformação de perspectiva no formato "Sxx, SXY, syx, syy, px, py" \[ s = Scale, p = Perspective \] . Se o deslocamento estiver em unidades absolutas, então px, py estão nas unidades da UME ^-1; caso contrário, eles são uma fração inversa do tamanho da forma. |
| Deslocamento | [IvgSkewOffset](#data-types-used-in-the-vml-object-model). Valor do deslocamento x, y do local da forma. O padrão é "2PT, 2PT".                                                                                                                                                   |
| Ativado     | [VgTriState](msdn-online-vml-vgtristate.md). Ativa ou desativa a exibição da distorção.                                                                                                                                                                                             |
| Origem | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Um par de valores fracionários de forma de-0,5 a + 0,5.                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Elemento Stroke

Descreve como desenhar o caminho se algo além de uma linha sólida com uma cor sólida for desejada.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Cor</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. A cor da linha. O mesmo que o atributo StrokeColor na forma, mas o substitui.</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Cor secundária. Usado quando FillType é padrão.</td>
</tr>
<tr class="odd">
<td>DashStyle</td>
<td><strong>VgLineDashStyle</strong>. Formato de estilo de tracejado. Pode ser um valor específico ou uma sequência de números com um padrão de Dash definido pelo usuário. Os valores são:
<ul>
<li>Solid (padrão)</li>
<li>ShortDash</li>
<li>ShortDot</li>
<li>ShortDashDot</li>
<li>ShortDashDotDot</li>
<li>Ponto</li>
<li>Traço</li>
<li>DashDot</li>
<li>LongDash</li>
<li>LongDashDot</li>
<li>LongDashDotDot</li>
</ul></td>
</tr>
<tr class="even">
<td>Seta de fim</td>
<td><strong>VgArrowheadStyle</strong>. Ponta de seta para o final da linha. Os valores são:
<ul>
<li>Nenhum (padrão)</li>
<li>Bloquear</li>
<li>Clássico</li>
<li>Diamond</li>
<li>Oval</li>
<li>Aberto</li>
<li>Divisa</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndArrowLength</td>
<td><strong>VgArrowHeadLength</strong>. Comprimento da ponta de seta para o fim da linha. Os valores são:
<ul>
<li>Short</li>
<li>Médio (padrão)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrowWidth</td>
<td><strong>VgArrowheadWidth</strong>. Largura da ponta de seta para o fim da linha. Os valores são:
<ul>
<li>Encontrar</li>
<li>Médio (padrão)</li>
<li>Ampla</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndCap</td>
<td><strong>VgLineEndCapStyle</strong>. Os valores são:
<ul>
<li>Plano</li>
<li>Square</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>FillType</td>
<td><strong>VgLineFillType</strong>. Os valores são:
<ul>
<li>Solid (padrão)</li>
<li>Tile</li>
<li>Padrão</li>
<li>Quadro</li>
</ul></td>
</tr>
<tr class="odd">
<td>ImageAlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Alinhe a imagem com a forma. Se for false, alinhar a imagem com a janela.</td>
</tr>
<tr class="even">
<td>ImageAspect</td>
<td><strong>VgAspectType</strong>. O atributo ImageSize será ajustado para preservar o aspecto da imagem. Os valores são:
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorar</td>
<td>Ignorar problemas de aspecto.</td>
</tr>
<tr class="even">
<td>Mínimo</td>
<td>A imagem é pelo menos tão grande quanto o tamanho da imagem.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>A imagem não é maior que o tamanho da imagem.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>ImageSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Tamanho da imagem com a qual formar o pincel. O padrão é o tamanho da imagem.</td>
</tr>
<tr class="even">
<td>Joinstyle</td>
<td><strong>VgLineJoinStyle</strong>. Os valores são:
<ul>
<li>Round (junção arredondada)</li>
<li>Bisel (junta chanfrada)</li>
<li>Mitre (junta de Mitre)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Estilo de Linha</td>
<td><strong>VgLineStyle</strong>. Os valores são:
<ul>
<li>Único</li>
<li>ThinThin (1:1:1)</li>
<li>ThinThick (1:1:2)</li>
<li>ThickThin (2:1:1)</li>
<li>ThickBetweenThin (1:1:2:1:1)</li>
</ul></td>
</tr>
<tr class="even">
<td>MiterLimit</td>
<td><a href="msdn-online-vml-vglength.md">Comprimento</a>. A distância máxima entre o ponto interno e o ponto externo de uma junção. Esse número é um múltiplo da espessura da linha. Varia de 0 a 32.767.</td>
</tr>
<tr class="odd">
<td>Ativado</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Ativa e desativa a exibição da linha. O mesmo que o atributo Stroke na forma, mas o substitui.</td>
</tr>
<tr class="even">
<td>Opacidade</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacidade do traço.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td>Cadeia de caracteres. URL para uma imagem a ser carregada para preenchimentos de imagem e padrão. Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.</td>
</tr>
<tr class="even">
<td>StartArrow</td>
<td><strong>VgArrowheadStyle</strong>. Ponta de seta para o início da linha. Os valores são:
<ul>
<li>Nenhum (padrão)</li>
<li>Bloquear</li>
<li>Clássico</li>
<li>Diamond</li>
<li>Oval</li>
<li>Aberto</li>
<li>Divisa</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>StartArrowLength</td>
<td>VgArrowHeadLength. Comprimento da ponta de seta para o início da linha. Os valores são:
<ul>
<li>Short</li>
<li>Médio (padrão)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>StartArrowWidth</td>
<td>VgArrowheadWidth. Largura da ponta de seta para o início da linha. Os valores são:
<ul>
<li>Estreito médio (padrão) largo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Peso</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Largura da linha. Varia de 0 a 1584.
<div class="alert">
<blockquote>
[!Note]<br />
O atributo DashStyle permite que o usuário especifique um padrão de traço definido por personalizado. Isso é feito usando uma série de números. Os estilos de traço são definidos em termos do comprimento do traço (a parte desenhada do traço) e o comprimento do espaço entre os traços. Os comprimentos são relativos à largura da linha; um comprimento de &quot; 1 &quot; é igual à largura da linha. O estilo EndCap é aplicado a cada traço; os estilos de seta não são. A cadeia de caracteres define primeiro o comprimento do traço em seguida, o comprimento do espaço. Isso pode ser repetido para formar estilos de traço complexos. A cadeia de caracteres sempre deve conter um par de números; Se ele contiver um número ímpar de números, o último pode ser desconsiderado. A tabela a seguir lista alguns valores típicos e uma descrição do efeito pretendido. &quot;0 &quot; implica um ponto que deve ser consta simétrico (com Endcaps arredondado deve ser um círculo). Se a linha EndCap for simples, um visualizador deverá escolher um sistema operacional interno onde for possível (ou seja, algo que seja rápido de desenhar). O exemplo a seguir mostra alguns exemplos.
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>traços curtos (cada traço e o espaço entre é duas vezes a largura da linha)</td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>ponto (cada traço é a largura da linha enquanto cada espaço é duas vezes a largura da linha)</td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>Dash (cada traço é quatro vezes a largura da linha enquanto cada espaço é duas vezes a largura da linha)</td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>tracejado longo</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>traço ponto</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>ponto de tracejado longo</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>ponto ponto traço longo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>Elemento TextPath

Descreve um caminho de vetor baseado nos dados de texto, na fonte e nos estilos fornecidos. O caminho de texto é distorcido para estar em conformidade com um elemento **path** , se fornecido.



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| FitPath  | [VgTriState](msdn-online-vml-vgtristate.md). Dimensiona o texto para preencher o caminho em que ele se encontra.                                 |
| FitShape | [VgTriState](msdn-online-vml-vgtristate.md). Alonga o caminho do texto para as bordas da caixa de forma.                      |
| Ativado       | [VgTriState](msdn-online-vml-vgtristate.md). Determina se os caminhos de caracteres são exibidos ou não.                    |
| String   | Cadeia de caracteres. O texto a ser renderizado como um caminho de texto.                                                                                    |
| Trim     | [VgTriState](msdn-online-vml-vgtristate.md). Remove qualquer espaço adicional reservado para ascendentes e descendentes, se não for usado. |
| XScale   | [VgTriState](msdn-online-vml-vgtristate.md). Use a medida x reta em vez de medir ao longo do caminho.                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>Tipos de dados usados no modelo de objeto VML

Os tipos de dados a seguir são usados pelo modelo de objeto VML.

-   [Double](/windows)
-   [Fixo](/windows)
-   [Inteiro](/windows)
-   [IVgAdjustments](/windows)
-   [IVgColor](/windows)
-   [IVgEquation](/windows)
-   [IVgFixedRectangle](/windows)
-   [IVgFixedRectangleArray](/windows)
-   [IVgFormula](/windows)
-   [IVgFormulas](/windows)
-   [IVgGradientColorArray](/windows)
-   [IVgPoints](/windows)
-   [IVgSkewMatrix](/windows)
-   [IVgSkewOffset](/windows)
-   [IVgVector2D](/windows)
-   [IVgVector3D](/windows)
-   [Comprimento](/windows)
-   [Medida](/windows)
-   [Cadeia de caracteres](/windows)
-   [VgBlackWhiteMode](/windows)
-   [VgFraction](/windows)
-   [VgTriState](/windows)

**Tipo de dados Double**

Um inteiro de precisão dupla com intervalo de-infinito para infinito.

**Tipo de dados fixo**

Número de ponto flutuante com intervalo de-32766,0 a 32766,0.

**Tipo de dados Integer**

Um número inteiro com um intervalo de-infinito para infinito.

**Tipo de dados IVgAdjustments**

Coleção de ajustes em uma forma que pode ser usada para alterar as dimensões de uma forma. Os ajustes podem ser usados como espaços reservados temporários ou por qualquer motivo que você usaria variáveis. Há apenas oito ajustes na coleção.



| Atributos | Descrição                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [IVgTriState](msdn-online-vml-vgtristate.md). Determina se existe um ajuste especificado. Observe que um índice deve ser usado; ou seja, Exists (item) deve ser usado para recuperar a existência de um item.                                                                                                                                                                   |
| Item       | [Longo](#data-types-used-in-the-vml-object-model). Matriz de ajustes indexados de 0 a 7. Observe que os ajustes podem ser do SPARC especificado; ou seja, os valores intermediários da matriz nem sempre podem ser preenchidos. Por exemplo, item 1, 3 e 5 podem ter valores para um comprimento de 3, com item (0), Item (2) e item (4) especificado. Para ver se existe um item, use o atributo Exists. |
| Comprimento     | [Integer](#data-types-used-in-the-vml-object-model). Número de ajustes. Não pode ser maior que 8.                                                                                                                                                                                                                                                                          |
| Valor      | [Cadeia de caracteres](#data-types-used-in-the-vml-object-model). Representação de texto de valores numéricos, com vírgulas entre cada número.                                                                                                                                                                                                                                                    |



 

**IVgColor**

Especifica uma cor.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RGB</td>
<td><strong>VgRGBType</strong>. Valor RGB (Long) da cor. Somente válido se o tipo for RGB.</td>
</tr>
<tr class="even">
<td>R</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente vermelho da cor. Pode variar entre 0 e 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente verde da cor. Pode variar entre 0 e 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente azul da cor. Pode variar entre 0 e 255.</td>
</tr>
<tr class="odd">
<td>String</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>. Representação de texto da cor. Há suporte para os seguintes tipos de cor nomeados:
<ul>
<li>Preto (#000000)</li>
<li>Prata (#C0C0C0)</li>
<li>Cinza (#808080)</li>
<li>Branco (#FFFFFF)</li>
<li>Bordô (#800000)</li>
<li>Vermelho (#FF0000)</li>
<li>Roxo (#800080)</li>
<li>Fuchsia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Verde-limão (#00FF00)</li>
<li>Verde-oliva (#808000)</li>
<li>Amarelo (#FFFF00)</li>
<li>Azul (#000080)</li>
<li>Azul (#0000FF)</li>
<li>Azul-petróleo (#008080)</li>
<li>Azul-piscina (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgColorType</strong>. Tipo de cor. Um dos seguintes tipos:
<ul>
<li>Mixed</li>
<li>nomeado</li>
<li>RGB</li>
<li>Esquema</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgEquation**

Equações usadas para fórmulas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Operação</td>
<td><strong>VgEquationOperationType</strong> Nome da operação a ser executada nos parâmetros. As seguintes operações podem ser usadas em uma equação:
<table>
<thead>
<tr class="header">
<th>Operação</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abs</td>
<td>Valor absoluto. <br/> <strong>ABS</strong>(v) <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>Aritmética polar--resulta em unidades FD (graus multiplicado por 65536).<br/> <strong>ATAN2</strong>(P1, v) <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>Cosseno, argumento em unidades FD (graus multiplicado por 65536).<br/> v * <strong>cos</strong>(P1) <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>Preserva a precisão total no cálculo intermediário.<br/> v * <strong>cos (ATAN2 (</strong> P2, P1 <strong>))</strong><br/></td>
</tr>
<tr class="odd">
<td>Ellipse</td>
<td>Ellipse</td>
</tr>
<tr class="even">
<td>If</td>
<td>Se o teste de condição. v > 0 <strong>?</strong> P1: P2</td>
</tr>
<tr class="odd">
<td>Máx</td>
<td>O maior de dois valores. <br/> <strong>Max</strong>(v, P1) <br/></td>
</tr>
<tr class="even">
<td>Mid</td>
<td>Média (v + P1)/2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>O menor de dois valores. <strong>mín</strong>. (v, P1)</td>
</tr>
<tr class="even">
<td>Mod</td>
<td>Módulo.</td>
</tr>
<tr class="odd">
<td>Produto</td>
<td>Usado para multiplicação e divisão. v * P1/P2</td>
</tr>
<tr class="even">
<td>Sin</td>
<td>Seno, argumento em unidades FD (graus multiplicado por 65536). <br/> v * <strong>sin</strong>(P1) <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>Preserva a precisão total no cálculo intermediário. v * <strong>sin</strong>(<strong>ATAN2</strong>(P2, P1))</td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>O resultado é positivo e arredonda para baixo. <br/> <strong>sqrt</strong>(v) <br/></td>
</tr>
<tr class="odd">
<td>Somar</td>
<td>Usado para adição e subtração.<br/> v + P1 P2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>Ângulo existente (dimensionado por 65536), onde P1 e P2 estão em graus.<br/> v + P1 * 65536 + P2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>Tangente, o argumento está em unidades FD (graus multiplicado por 65536). <br/> v * tan (P1)<br/></td>
</tr>
<tr class="even">
<td>Val</td>
<td>Define um valor de guia de algum outro valor.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param1</td>
<td><strong>Integer</strong>. O primeiro parâmetro.</td>
</tr>
<tr class="odd">
<td>Paramtype1</td>
<td><strong>VgFormulaParamType</strong>. O tipo do primeiro parâmetro. Os seguintes valores têm suporte:
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor</td>
<td>O parâmetro é um valor simples.</td>
</tr>
<tr class="even">
<td>AdjustmentReference</td>
<td>O parâmetro é uma referência a um ajuste. Por exemplo, se o primeiro parâmetro for 1, o valor do primeiro ajuste será usado.</td>
</tr>
<tr class="odd">
<td>FormulaReference</td>
<td>O parâmetro é o resultado de uma referência ao resultado de uma fórmula anterior. Por exemplo, se o primeiro parâmetro for 2, o resultado da fórmula 2 será usado.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param2</td>
<td><strong>Integer</strong>. O segundo parâmetro.</td>
</tr>
<tr class="odd">
<td>Paramtype2</td>
<td><strong>VgFormulaParamType</strong> O tipo de parâmetro 2.</td>
</tr>
<tr class="even">
<td>Val</td>
<td><strong>Integer</strong>. O resultado.</td>
</tr>
<tr class="odd">
<td>Valtype2</td>
<td><strong>VgFormulaParamType</strong>. O tipo do resultado.</td>
</tr>
</tbody>
</table>



 

**IVgFixedRectangle**

Especifica um retângulo fixo.



| Atributos | Descrição                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valor      | [Cadeia de caracteres](#data-types-used-in-the-vml-object-model). Valor de texto que especifica o caminho.         |
| Esquerda       | [Double](#data-types-used-in-the-vml-object-model). Coordenada da extrema esquerda do retângulo.   |
| Parte superior        | [Double](#data-types-used-in-the-vml-object-model). Coordenada superior do retângulo.    |
| Direita      | [Double](#data-types-used-in-the-vml-object-model). Coordenada da extrema direita do retângulo.  |
| Inferior     | [Double](#data-types-used-in-the-vml-object-model). Coordenada inferior do retângulo. |



 

**IVgFixedRectangleArray**

Matriz de retângulos fixos.



| Atributos | Descrição                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| Valor      | [Cadeia de caracteres](#data-types-used-in-the-vml-object-model). Representação de texto da matriz.                           |
| Comprimento     | [Integer](#data-types-used-in-the-vml-object-model). Número de retângulos nesta matriz.                    |
| Item       | [IVgFixedRectangle](#data-types-used-in-the-vml-object-model). O objeto Rectangle no índice especificado. |



 

Tipo de dados **IVgFormula**

Definições para fórmulas que podem variar o caminho de uma forma ou ser usadas para outras finalidades de cálculo. As fórmulas podem se basear no atributo **adj** de uma forma, que pode ser alterada. As fórmulas também podem fazer referência a outras fórmulas.



| Atributos | Description                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eqn        | [IVgEquation](#data-types-used-in-the-vml-object-model). Cada fórmula define um único valor como o resultado da avaliação da expressão. A expressão é definida por esse atributo e tem a forma geral de uma operação seguida por até três argumentos, que podem ser valores de ajuste (por exemplo, \# 2), os resultados de fórmulas anteriores (por exemplo, @2 ), números fixos ou valores predefinidos. |



 

**Tipo de dados IVgFormulas**

Uma coleção de objetos de fórmula.



| Atributos | Description                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Comprimento     | [Integer](#data-types-used-in-the-vml-object-model). Número de objetos de fórmula na coleção.                                                |
| Item       | [IVgFormula](#data-types-used-in-the-vml-object-model). Uma fórmula específica. Observe que a matriz de fórmulas pode ser herdada do tipo de forma. |



 

**IVgGradientColorArray**

Uma matriz de cores que define um gradiente (intervalo combinado de cores).



| Atributos | Descrição                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| Valor      | [Cadeia de caracteres](#data-types-used-in-the-vml-object-model). Especifica a matriz de cores; por exemplo, "vermelho. 2; verde. 4; Black. 7 " |
| Comprimento     | [Integer](#data-types-used-in-the-vml-object-model). Número de cores na matriz.                                          |



 



| Métodos     | Descrição                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Addcolor    | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Adiciona uma nova cor no ponto de extremidade especificado por fração. A nova cor é branca por padrão e é o valor de retorno. A cor pode ser alterada por referência. |
| RemoveColor | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Remove uma cor no ponto de extremidade especificado por fração. Observação: se 0,0 ou 1,0 não existir, ele será implícito e a cor branca será usada nesse ponto.          |



 

**Tipo de dados IVgPoints**

Matriz de pontos que define uma forma.



| Atributos | Descrição                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valor      | [Cadeia de caracteres](#data-types-used-in-the-vml-object-model). Representação de texto da matriz.           |
| Comprimento     | [Integer](#data-types-used-in-the-vml-object-model). Número de pontos nesta matriz.        |
| Item       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md). O ponto no índice especificado. |



 

**Tipo de dados IVgSkewMatrix**

Uma matriz usada para inclinar formas, uma matriz de transformação de perspectiva no formato "*Sxx, SXY, syx, syy, px, py* " \[ *s* = Scale, *p* = Perspective \] . Se o deslocamento estiver em unidades absolutas, *px, py* estão nas unidades da UME ^-1; caso contrário, eles são uma fração inversa do tamanho da forma.



| Atributos   | Description                                         |
|--------------|-----------------------------------------------------|
| XtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| XtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveX | [Double](#data-types-used-in-the-vml-object-model). |
| Perspectiva | [Double](#data-types-used-in-the-vml-object-model). |



 

**IVgSkewOffset**

Especifica o deslocamento da distorção.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor</td>
<td><a href="#data-types-used-in-the-vml-object-model">Cadeia de caracteres</a>. Representação de texto do deslocamento.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X. Porcentagem ou medida. Se não houver unidades, o tipo ShapeRelative será implícito; caso contrário, o tipo absoluto será implícito.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgSkewTransformType</strong>. Especifica o tipo de transformação. Os valores válidos são pontos inteiros que variam entre-infinito e infinito. 
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShapeRelative</td>
<td>Os valores do deslocamento são porcentagens (proporção) do tamanho da forma original; por exemplo, um valor de 0,5 significa um deslocamento metade do tamanho da forma.</td>
</tr>
<tr class="even">
<td>Absoluto</td>
<td>Os valores são unidades absolutas.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

**Tipo de dados IVgVector2D**

Especifica um vetor bidimensional que consiste em dois números **duplos** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor</td>
<td><strong>Cadeia de caracteres</strong>. Representação de texto de ambos os números de vetor separados por um espaço.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X deste vetor.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y deste vetor.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgVectorType</strong>. Unidades esperadas para este vetor. Os valores são:
<ul>
<li>Medida</li>
<li>Comprimento</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Número inteiro de porcentagem de números</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Tipo de dados IVgVector3D**

Especifica um vetor tridimensional que consiste em três números **duplos** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Valor</td>
<td><strong>Cadeia de caracteres</strong>. Representação de texto de três números de vetor separados por um espaço.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X deste vetor.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y deste vetor.</td>
</tr>
<tr class="even">
<td>Z</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Z deste vetor.</td>
</tr>
<tr class="odd">
<td>Tipo</td>
<td><strong>VgVectorType</strong>. Unidades esperadas para este vetor. Os valores são:
<ul>
<li>Medida</li>
<li>Comprimento</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Número</li>
<li>Percentual</li>
<li>Integer</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Tipo de dados length**

Um número de ponto flutuante com um intervalo de 0 a infinito.

**Tipo de dados Measure**

Um número de ponto flutuante de-infinito para infinito.

**Tipo de dados String**

Dados de caractere de qualquer comprimento.

**VgBlackWhiteMode**

Modo de renderização para preto e branco. Os valores possíveis são:

-   **Cor**
-   **Automático**
-   **Escala**
-   **LightGrayScale**
-   **InverseGray**
-   **GrayOutline**
-   **BlackTextAndLines**
-   **HighContrast**
-   **Preto**
-   **Branca**
-   **Não desenhado**

**Tipo de dados VgFraction**

Número de ponto flutuante com intervalo de 0,0 a 1,0. As frações também podem ser especificadas como uma porcentagem; por exemplo, "50%".

**Tipo de dados VgTriState**

Enumeração usada para valores que podem ser um dos três Estados:

-   **TRUE**
-   **FALSE**
-   **MIXED**