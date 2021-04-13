---
description: Use esta anotação para associar um parâmetro de efeito a um controle de interface do usuário no ambiente de host. Isso permitirá que um usuário controle interativamente um parâmetro de efeito por meio do aplicativo host.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Anotação da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e873c83a01c5c2214cb49a93e75167e58a3389
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456864"
---
# <a name="ui-annotation"></a><span data-ttu-id="4feb2-104">Anotação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="4feb2-104">UI Annotation</span></span>

<span data-ttu-id="4feb2-105">Use esta anotação para associar um parâmetro de efeito a um controle de interface do usuário no ambiente de host.</span><span class="sxs-lookup"><span data-stu-id="4feb2-105">Use this annotation to associate an effect parameter with a UI control in the host environment.</span></span> <span data-ttu-id="4feb2-106">Isso permitirá que um usuário controle interativamente um parâmetro de efeito por meio do aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="4feb2-106">This will allow a user to interactively control an effect parameter through the host application.</span></span>

<span data-ttu-id="4feb2-107">DXSAS define um conjunto de controles padrão em termos do modelo de dados e do comportamento básico que os autores de efeito podem esperar de aplicativos de host.</span><span class="sxs-lookup"><span data-stu-id="4feb2-107">DXSAS defines a set of standard controls in terms of the data model and basic behavior that effect authors can expect from host applications.</span></span> <span data-ttu-id="4feb2-108">A anotação de controle é usada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4feb2-108">The control annotation is used like this:</span></span>


```
string SasUiControl = "ControlType";
```



<span data-ttu-id="4feb2-109">onde</span><span class="sxs-lookup"><span data-stu-id="4feb2-109">where</span></span>


```
ControlType
```



<span data-ttu-id="4feb2-110">é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4feb2-110">is one of the following:</span></span>



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4feb2-111">ControlType</span><span class="sxs-lookup"><span data-stu-id="4feb2-111">ControlType</span></span> | <span data-ttu-id="4feb2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4feb2-112">Description</span></span>                                                                                                                                                                     | <span data-ttu-id="4feb2-113">Tipo de dados interno</span><span class="sxs-lookup"><span data-stu-id="4feb2-113">Internal Data Type</span></span>                                                                                 | <span data-ttu-id="4feb2-114">Anotações de propriedade de controle</span><span class="sxs-lookup"><span data-stu-id="4feb2-114">Control Property Annotations</span></span>                                                                                 |
| <span data-ttu-id="4feb2-115">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4feb2-115">None</span></span>        | <span data-ttu-id="4feb2-116">Nenhum controle deve ser mostrado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-116">No control should be shown.</span></span> <span data-ttu-id="4feb2-117">Observe que um controle ficará visível se [SasUiVisible](#sasuivisible) for true e o tipo de controle for qualquer tipo diferente de None.</span><span class="sxs-lookup"><span data-stu-id="4feb2-117">Note that a control is visible if [SasUiVisible](#sasuivisible) is True and the control type is any type other than None.</span></span>                           | <span data-ttu-id="4feb2-118">N/D</span><span class="sxs-lookup"><span data-stu-id="4feb2-118">n/a</span></span>                                                                                                | <span data-ttu-id="4feb2-119">N/D</span><span class="sxs-lookup"><span data-stu-id="4feb2-119">n/a</span></span>                                                                                                          |
| <span data-ttu-id="4feb2-120">Qualquer</span><span class="sxs-lookup"><span data-stu-id="4feb2-120">Any</span></span>         | <span data-ttu-id="4feb2-121">Isso implica que nenhum controle especial é solicitado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-121">This implies that no special control is requested.</span></span> <span data-ttu-id="4feb2-122">O controle apresentado é o resultado do comportamento definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4feb2-122">The control presented is the result of application-defined behavior.</span></span>                                                         | <span data-ttu-id="4feb2-123">N/D</span><span class="sxs-lookup"><span data-stu-id="4feb2-123">n/a</span></span>                                                                                                | <span data-ttu-id="4feb2-124">N/D</span><span class="sxs-lookup"><span data-stu-id="4feb2-124">n/a</span></span>                                                                                                          |
| <span data-ttu-id="4feb2-125">ColorPicker</span><span class="sxs-lookup"><span data-stu-id="4feb2-125">ColorPicker</span></span> | <span data-ttu-id="4feb2-126">Representa um valor de cor como uma amostra de cor.</span><span class="sxs-lookup"><span data-stu-id="4feb2-126">Represent a color value as a color swatch.</span></span> <span data-ttu-id="4feb2-127">O valor é empacotado nos componentes XYZ do vetor associado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-127">The value is packed into the XYZ components of the associated vector.</span></span> <span data-ttu-id="4feb2-128">O componente W do vetor associado sempre é definido como um.</span><span class="sxs-lookup"><span data-stu-id="4feb2-128">The W component of the associated vector is always set to one.</span></span> | <span data-ttu-id="4feb2-129">float *n* , em que *n* é de 1 a 4, inclusive.</span><span class="sxs-lookup"><span data-stu-id="4feb2-129">float *N* where *N* is 1 to 4 inclusive.</span></span>                                                            | [<span data-ttu-id="4feb2-130">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="4feb2-130">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="4feb2-131">Direção</span><span class="sxs-lookup"><span data-stu-id="4feb2-131">Direction</span></span>   | <span data-ttu-id="4feb2-132">Um vetor de direção.</span><span class="sxs-lookup"><span data-stu-id="4feb2-132">A direction vector.</span></span>                                                                                                                                                             | <span data-ttu-id="4feb2-133">float *n* , em que *n* é de 2 a 4, inclusive.</span><span class="sxs-lookup"><span data-stu-id="4feb2-133">float *N* where *N* is 2 to 4 inclusive.</span></span>                                                            | <span data-ttu-id="4feb2-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4feb2-134">None</span></span>                                                                                                         |
| <span data-ttu-id="4feb2-135">FilePicker</span><span class="sxs-lookup"><span data-stu-id="4feb2-135">FilePicker</span></span>  | <span data-ttu-id="4feb2-136">Uma caixa de diálogo que permite ao usuário procurar e selecionar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4feb2-136">A dialog box that allows the user to browse and select a file.</span></span>                                                                                                                  | <span data-ttu-id="4feb2-137">string</span><span class="sxs-lookup"><span data-stu-id="4feb2-137">string</span></span>                                                                                             | <span data-ttu-id="4feb2-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4feb2-138">None</span></span>                                                                                                         |
| <span data-ttu-id="4feb2-139">ListPicker</span><span class="sxs-lookup"><span data-stu-id="4feb2-139">ListPicker</span></span>  | <span data-ttu-id="4feb2-140">Uma lista de valores de cadeia de caracteres da qual o usuário pode selecionar uma entrada.</span><span class="sxs-lookup"><span data-stu-id="4feb2-140">A list of string values from which the user can select one entry.</span></span> <span data-ttu-id="4feb2-141">Os valores são gerados a partir da anotação [SasUiEnum](#sasuienum) .</span><span class="sxs-lookup"><span data-stu-id="4feb2-141">The values are generated from the [SasUiEnum](#sasuienum) annotation.</span></span>                                         | <span data-ttu-id="4feb2-142">Uma matriz de cadeias de caracteres junto com um valor inteiro que contém o índice do valor da cadeia de caracteres selecionada.</span><span class="sxs-lookup"><span data-stu-id="4feb2-142">An array of strings along with an integer value containing the index of the selected string value.</span></span> | [<span data-ttu-id="4feb2-143">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="4feb2-143">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="4feb2-144">Numérico</span><span class="sxs-lookup"><span data-stu-id="4feb2-144">Numeric</span></span>     | <span data-ttu-id="4feb2-145">Um conjunto de controles de entrada numéricos (como caixas de texto).</span><span class="sxs-lookup"><span data-stu-id="4feb2-145">A set of numerical input controls (such as text boxes).</span></span>                                                                                                                         | <span data-ttu-id="4feb2-146">float *m* x *N* em que *m* e *N* são de 1 a 4, inclusive.</span><span class="sxs-lookup"><span data-stu-id="4feb2-146">float *M* x *N* where *M* and *N* are 1 to 4 inclusive.</span></span>                                               | <span data-ttu-id="4feb2-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span><span class="sxs-lookup"><span data-stu-id="4feb2-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span></span>                                    |
| <span data-ttu-id="4feb2-148">Controle deslizante</span><span class="sxs-lookup"><span data-stu-id="4feb2-148">Slider</span></span>      | <span data-ttu-id="4feb2-149">Um conjunto de controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="4feb2-149">A set of sliders.</span></span>                                                                                                                                                               | <span data-ttu-id="4feb2-150">float *m* x *N* em que *m* e *N* são de 1 a 4, inclusive</span><span class="sxs-lookup"><span data-stu-id="4feb2-150">float *M* x *N* where *M* and *N* are 1 to 4 inclusive</span></span>                                                | <span data-ttu-id="4feb2-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span><span class="sxs-lookup"><span data-stu-id="4feb2-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span></span> |
| <span data-ttu-id="4feb2-152">String</span><span class="sxs-lookup"><span data-stu-id="4feb2-152">String</span></span>      | <span data-ttu-id="4feb2-153">Uma caixa de texto para editar o conteúdo da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4feb2-153">An text box for editing string content.</span></span>                                                                                                                                         | <span data-ttu-id="4feb2-154">string</span><span class="sxs-lookup"><span data-stu-id="4feb2-154">string</span></span>                                                                                             | <span data-ttu-id="4feb2-155">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4feb2-155">None</span></span>                                                                                                         |



 

<span data-ttu-id="4feb2-156">Se o tipo de dados interno não for idêntico ao tipo do parâmetro associado, a conversão ocorrerá quando os dados forem transferidos do parâmetro aplicativo host para o parâmetro de efeito.</span><span class="sxs-lookup"><span data-stu-id="4feb2-156">If the internal data type is not identical to the associated parameter's type, casting will occur when data is transferred from the host application parameter to the effect parameter.</span></span>

<span data-ttu-id="4feb2-157">O padrão é a cadeia de caracteres "None".</span><span class="sxs-lookup"><span data-stu-id="4feb2-157">The default is the string "None".</span></span>

## <a name="ui-common-properties"></a><span data-ttu-id="4feb2-158">Propriedades comuns da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="4feb2-158">UI Common Properties</span></span>

### <a name="sasuidescription"></a><span data-ttu-id="4feb2-159">SasUiDescription</span><span class="sxs-lookup"><span data-stu-id="4feb2-159">SasUiDescription</span></span>

<span data-ttu-id="4feb2-160">Use esta anotação para especificar uma cadeia de caracteres para descrever uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="4feb2-160">Use this annotation to specify a string to describe a tool.</span></span> <span data-ttu-id="4feb2-161">Isso pode ser usado para elementos da interface do usuário, como dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="4feb2-161">This could be used for UI elements such as tool tips.</span></span>


```
string SasUiDescription = "descriptive string";
```



<span data-ttu-id="4feb2-162">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4feb2-162">For instance:</span></span>


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



<span data-ttu-id="4feb2-163">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="4feb2-163">The default is an empty string.</span></span>

### <a name="sasuilabel"></a><span data-ttu-id="4feb2-164">SasUiLabel</span><span class="sxs-lookup"><span data-stu-id="4feb2-164">SasUiLabel</span></span>

<span data-ttu-id="4feb2-165">Use esta anotação para especificar uma cadeia de caracteres para rotular qualquer controle de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4feb2-165">Use this annotation to specify a string to label any UI control.</span></span>


```
string SasUiLabel = "some label;
```



<span data-ttu-id="4feb2-166">Veja um exemplo:</span><span class="sxs-lookup"><span data-stu-id="4feb2-166">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



<span data-ttu-id="4feb2-167">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="4feb2-167">The default is an empty string.</span></span>

### <a name="sasuivisible"></a><span data-ttu-id="4feb2-168">SasUiVisible</span><span class="sxs-lookup"><span data-stu-id="4feb2-168">SasUiVisible</span></span>

<span data-ttu-id="4feb2-169">Use essa anotação para especificar se o parâmetro associado deve ser exibido ao usuário.</span><span class="sxs-lookup"><span data-stu-id="4feb2-169">Use this annotation to specify whether the associated parameter should be displayed to the user.</span></span>


```
bool SasUiVisible = false;
```



<span data-ttu-id="4feb2-170">Se definido como true, o aplicativo host deverá exibir um controle de interface do usuário para editar o parâmetro de efeito anotado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-170">If set to True, the host application should display a UI control for editing the annotated effect parameter.</span></span> <span data-ttu-id="4feb2-171">Se for false, nenhuma interface do usuário será exibida no aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="4feb2-171">If false, no UI is displayed in the host application.</span></span>

<span data-ttu-id="4feb2-172">Veja um exemplo:</span><span class="sxs-lookup"><span data-stu-id="4feb2-172">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



<span data-ttu-id="4feb2-173">O padrão é True.</span><span class="sxs-lookup"><span data-stu-id="4feb2-173">The default is True.</span></span>

## <a name="ui-control-properties"></a><span data-ttu-id="4feb2-174">Propriedades do controle da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="4feb2-174">UI Control Properties</span></span>

<span data-ttu-id="4feb2-175">As anotações de propriedade de controle são modificadores adicionais que ajudam a determinar como um controle específico Opera.</span><span class="sxs-lookup"><span data-stu-id="4feb2-175">Control property annotations are additional modifiers that help determine how a particular control operates.</span></span>

### <a name="sasuienum"></a><span data-ttu-id="4feb2-176">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="4feb2-176">SasUiEnum</span></span>

<span data-ttu-id="4feb2-177">Essa anotação permite restringir o intervalo de valores para um controle.</span><span class="sxs-lookup"><span data-stu-id="4feb2-177">This annotation allows you to restrict the range of values for a control.</span></span> <span data-ttu-id="4feb2-178">A anotação contém uma cadeia de caracteres de valores delimitada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4feb2-178">The annotation contains a string of values delimited by commas.</span></span>

<span data-ttu-id="4feb2-179">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="4feb2-179">The default is an empty string.</span></span>

### <a name="sasuimax"></a><span data-ttu-id="4feb2-180">SasUiMax</span><span class="sxs-lookup"><span data-stu-id="4feb2-180">SasUiMax</span></span>

<span data-ttu-id="4feb2-181">Esta Anotação especifica o valor máximo do parâmetro associado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-181">This annotation specifies the maximum value of the associated parameter.</span></span> <span data-ttu-id="4feb2-182">Ele só pode ser associado a um parâmetro de tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="4feb2-182">It can only be associated with a numerically-typed parameter.</span></span> <span data-ttu-id="4feb2-183">O valor máximo do parâmetro, na verdade, será calculado como:</span><span class="sxs-lookup"><span data-stu-id="4feb2-183">The maximum value of the parameter will actually be calculated as:</span></span>


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



<span data-ttu-id="4feb2-184">\_Tipo \_ de parâmetro Max é o valor máximo para o tipo usado pelo parâmetro associado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-184">PARAMETER\_TYPE\_MAX is the maximum value for the type used by the associated parameter.</span></span> <span data-ttu-id="4feb2-185">Isso significa que o valor do parâmetro, levando em conta a anotação [SasUiMax](#sasuimax) é calculada como:</span><span class="sxs-lookup"><span data-stu-id="4feb2-185">This means that the value of the parameter, taking into account the [SasUiMax](#sasuimax) annotation is calculated as:</span></span>


```
ParameterValue = min(NewParameterValue, MaxValue);
```



<span data-ttu-id="4feb2-186">O valor padrão é FLT \_ Max, conforme definido em Math. h.</span><span class="sxs-lookup"><span data-stu-id="4feb2-186">The default value is FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuimin"></a><span data-ttu-id="4feb2-187">SasUiMin</span><span class="sxs-lookup"><span data-stu-id="4feb2-187">SasUiMin</span></span>

<span data-ttu-id="4feb2-188">Esta Anotação especifica o valor mínimo do parâmetro associado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-188">This annotation specifies the minimum value of the associated parameter.</span></span> <span data-ttu-id="4feb2-189">Ele só pode ser associado a qualquer parâmetro de tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="4feb2-189">It can only be associated with any numerically-typed parameter.</span></span> <span data-ttu-id="4feb2-190">O valor mínimo do parâmetro será realmente calculado como:</span><span class="sxs-lookup"><span data-stu-id="4feb2-190">The minimum value of the parameter will actually be calculated as:</span></span>


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



<span data-ttu-id="4feb2-191">\_Tipo \_ de parâmetro min é o valor mínimo para o tipo usado pelo parâmetro associado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-191">PARAMETER\_TYPE\_MIN is the minimum value for the type used by the associated parameter.</span></span> <span data-ttu-id="4feb2-192">Isso significa que o valor do parâmetro, levando em conta a anotação [SasUiMin](#sasuimin) é calculada como:</span><span class="sxs-lookup"><span data-stu-id="4feb2-192">This means that the value of the parameter, taking into account the [SasUiMin](#sasuimin) annotation is calculated as:</span></span>


```
ParameterValue = max(NewParameterValue, MinValue);
```



<span data-ttu-id="4feb2-193">O valor padrão é-FLT \_ Max, conforme definido em Math. h.</span><span class="sxs-lookup"><span data-stu-id="4feb2-193">The default value is -FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuisteps"></a><span data-ttu-id="4feb2-194">SasUiSteps</span><span class="sxs-lookup"><span data-stu-id="4feb2-194">SasUiSteps</span></span>

<span data-ttu-id="4feb2-195">Esta Anotação especifica o número de etapas que podem ser usadas ao incrementar ou decrementar o valor do parâmetro associado.</span><span class="sxs-lookup"><span data-stu-id="4feb2-195">This annotation specifies the number of steps that can be used when incrementing or decrementing the associated parameter value.</span></span> <span data-ttu-id="4feb2-196">A anotação só é significativa em um parâmetro de tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="4feb2-196">The annotation is only meaningful on a numerically-typed parameter.</span></span> <span data-ttu-id="4feb2-197">Zero Especifica que o aplicativo host escolherá um número razoável de etapas.</span><span class="sxs-lookup"><span data-stu-id="4feb2-197">Zero specifies that the host application will choose a reasonable number of steps.</span></span>

<span data-ttu-id="4feb2-198">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="4feb2-198">The default value is 0.</span></span>

### <a name="sasuistepspower"></a><span data-ttu-id="4feb2-199">SasUiStepsPower</span><span class="sxs-lookup"><span data-stu-id="4feb2-199">SasUiStepsPower</span></span>

<span data-ttu-id="4feb2-200">Esta Anotação especifica o expoente na função Power, que tem o intervalo \[ 0,0 f, 1,0 f \] .</span><span class="sxs-lookup"><span data-stu-id="4feb2-200">This annotation specifies the exponent in the power function, which has the range \[0.0f, 1.0f\].</span></span> <span data-ttu-id="4feb2-201">Os aplicativos host devem implementar o seguinte método ao calcular os valores de parâmetro:</span><span class="sxs-lookup"><span data-stu-id="4feb2-201">Host applications must implement the following method when calculating parameter values:</span></span>


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



<span data-ttu-id="4feb2-202">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="4feb2-202">The default value is 1.0f.</span></span>

### <a name="sasuistride"></a><span data-ttu-id="4feb2-203">SasUiStride</span><span class="sxs-lookup"><span data-stu-id="4feb2-203">SasUiStride</span></span>

<span data-ttu-id="4feb2-204">Esta Anotação especifica o incremento que deve ser usado ao incrementar ou decrementar esse valor.</span><span class="sxs-lookup"><span data-stu-id="4feb2-204">This annotation specifies the increment that should be used when incrementing or decrementing this value.</span></span> <span data-ttu-id="4feb2-205">Ao contrário de [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) é útil com um controle Spinner, por exemplo, onde os dados são desvinculados e o usuário incrementa o valor do parâmetro por Stride em vez de um número predefinido de etapas.</span><span class="sxs-lookup"><span data-stu-id="4feb2-205">Unlike [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) is useful with a spinner control, for instance, where the data is unbounded and the user would rather increment the parameter value by stride rather than by a pre-defined number of steps.</span></span> <span data-ttu-id="4feb2-206">Os aplicativos host devem incrementar (ou decrementar dependendo do comportamento do controle) pelo valor de SasUiStride da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4feb2-206">Host applications should increment (or decrement depending on the control behavior) by the value of SasUiStride as follows:</span></span>


```
ParameterValue = ParameterValue +/- SasUiStride
```



<span data-ttu-id="4feb2-207">O valor padrão é 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="4feb2-207">The default value is 1.0f.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4feb2-208">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4feb2-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4feb2-209">Referência de semântica e anotações padrão do DirectX</span><span class="sxs-lookup"><span data-stu-id="4feb2-209">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



