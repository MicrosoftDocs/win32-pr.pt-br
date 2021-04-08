---
description: Vários consumidores, como o consumidor de evento de script ativo ou o consumidor de evento de linha de comando, têm propriedades de cadeia de caracteres com o qualificador de modelo.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Usando modelos de cadeia de caracteres padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829263"
---
# <a name="using-standard-string-templates"></a><span data-ttu-id="01913-103">Usando modelos de cadeia de caracteres padrão</span><span class="sxs-lookup"><span data-stu-id="01913-103">Using Standard String Templates</span></span>

<span data-ttu-id="01913-104">Vários consumidores, como o consumidor de evento de script ativo ou o consumidor de evento de linha de comando, têm propriedades de cadeia de caracteres com o qualificador de **modelo** .</span><span class="sxs-lookup"><span data-stu-id="01913-104">Several consumers, such as the Active Script Event Consumer or the Command Line Event Consumer, have string properties with the **Template** qualifier.</span></span> <span data-ttu-id="01913-105">Essas propriedades usam modelos de cadeia de caracteres padrão para construir uma cadeia de caracteres configurada em parte pela instância do consumidor e em parte por um evento.</span><span class="sxs-lookup"><span data-stu-id="01913-105">These properties use standard string templates to construct a string that is configured in part by the consumer instance and in part by an event.</span></span> <span data-ttu-id="01913-106">A estrutura de um modelo de cadeia de caracteres padrão é semelhante à especificação de variável de ambiente do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="01913-106">The structure of a standard string template is similar to the Microsoft Windows environment variable specification.</span></span>

<span data-ttu-id="01913-107">A lista a seguir mostra alguns exemplos da linguagem do modelo:</span><span class="sxs-lookup"><span data-stu-id="01913-107">The following list shows some examples of the template language:</span></span>

-   <span data-ttu-id="01913-108">A cadeia de caracteres "texto aqui" sempre produz a cadeia de caracteres "texto aqui".</span><span class="sxs-lookup"><span data-stu-id="01913-108">The string "Some text here" always produces the string "Some text here".</span></span>
-   <span data-ttu-id="01913-109">"% CPUUtilization%" sempre produz o valor da propriedade **CPUUtilization** do evento que está sendo entregue.</span><span class="sxs-lookup"><span data-stu-id="01913-109">"%CPUUtilization%" always produces the value of the **CPUUtilization** property of the event being delivered.</span></span> <span data-ttu-id="01913-110">Se a propriedade não for uma cadeia de caracteres, ela será convertida em uma cadeia de caracteres; por exemplo, "90" ou "TRUE".</span><span class="sxs-lookup"><span data-stu-id="01913-110">If the property is not a string, it is converted to a string; for example, "90" or "TRUE".</span></span>
-   <span data-ttu-id="01913-111">"A utilização da CPU desse processador é% CPUUtilization% no momento" incorpora o valor da propriedade **CPUUtilization** do evento à cadeia de caracteres, produzindo algo como "a utilização da CPU desse processador é 90 no momento".</span><span class="sxs-lookup"><span data-stu-id="01913-111">"The CPU utilization of this processor is %CPUUtilization% at this time" embeds the value of the **CPUUtilization** property of the event into the string, producing something like, "The CPU utilization of this processor is 90 at this time".</span></span>
-   <span data-ttu-id="01913-112">"% TargetInstance. CPUUtilization%" recupera o valor da propriedade **CPUUtilization** na instância inserida da propriedade **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="01913-112">"%TargetInstance.CPUUtilization%" retrieves the value of the **CPUUtilization** property in the embedded instance of the **TargetInstance** property.</span></span>
-   <span data-ttu-id="01913-113">"%%" produz um único% Sign.</span><span class="sxs-lookup"><span data-stu-id="01913-113">"%%" produces a single % sign.</span></span>
-   <span data-ttu-id="01913-114">Se a propriedade que está sendo recuperada for uma matriz, toda a matriz será produzida no seguinte formato: "(1, 5, 10, 1024)".</span><span class="sxs-lookup"><span data-stu-id="01913-114">If the property being retrieved is an array, the entire array is produced in the following format: "(1,5,10,1024)".</span></span> <span data-ttu-id="01913-115">Se houver apenas um elemento na matriz, os parênteses serão omitidos.</span><span class="sxs-lookup"><span data-stu-id="01913-115">If there is only one element in the array, the parentheses are omitted.</span></span> <span data-ttu-id="01913-116">Se não houver nenhum elemento na matriz, "()" será produzido.</span><span class="sxs-lookup"><span data-stu-id="01913-116">If there are no elements in the array, "()" is produced.</span></span>
-   <span data-ttu-id="01913-117">Se uma propriedade for um objeto inserido, a representação MOF do objeto será produzida (semelhante ao método [**IWbemClassObject:: GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).</span><span class="sxs-lookup"><span data-stu-id="01913-117">If a property is an embedded object, the MOF representation of the object is produced (similar to the [**IWbemClassObject::GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) method).</span></span>
-   <span data-ttu-id="01913-118">Se uma propriedade de uma matriz inserida de objetos for solicitada, ela será tratada como uma propriedade com um valor de matriz.</span><span class="sxs-lookup"><span data-stu-id="01913-118">If a property of an embedded array of objects is requested, it is treated as a property with an array value.</span></span> <span data-ttu-id="01913-119">Por exemplo:% MyEvents. TargetInstance. DriverLetter% poderia produzir ' ("C:", "D:") ' se MyEvents for uma matriz de eventos de modificação de instância incorporada.</span><span class="sxs-lookup"><span data-stu-id="01913-119">For example: %MyEvents.TargetInstance.DriverLetter% could produce '("C:","D:")' if MyEvents is an array of embedded instance modification events.</span></span>

## <a name="string-literals"></a><span data-ttu-id="01913-120">Literais de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="01913-120">String Literals</span></span>

<span data-ttu-id="01913-121">Qualquer coisa dentro de um par de aspas é considerada uma literal de cadeia de caracteres e não será substituída.</span><span class="sxs-lookup"><span data-stu-id="01913-121">Anything inside a pair of quotes is considered a string literal and will not be replaced.</span></span>

<span data-ttu-id="01913-122">O exemplo a seguir mostra a cadeia de caracteres que o compilador vê para "a utilização da CPU é% CPUUtilization%".</span><span class="sxs-lookup"><span data-stu-id="01913-122">The following example shows the string that the compiler sees for "CPU utilization is %CPUUtilization%".</span></span>

``` syntax
CPU utilization is %CPUUtilization%
```

<span data-ttu-id="01913-123">Essa cadeia de caracteres produz a saída a seguir.</span><span class="sxs-lookup"><span data-stu-id="01913-123">This string produces the following output.</span></span>

``` syntax
CPU utilization is 90
```

<span data-ttu-id="01913-124">Por outro lado, a cadeia de caracteres "a utilização da CPU é \\ "% CPUUtilization% \\ "" é vista pelo compilador da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="01913-124">On the other hand, the string "CPU utilization is \\"%CPUUtilization%\\"" is seen by the compiler as follows.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

<span data-ttu-id="01913-125">Essa cadeia de caracteres produz a saída a seguir, sem substituição de variável.</span><span class="sxs-lookup"><span data-stu-id="01913-125">This string produces the following output, with no variable substitution.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a><span data-ttu-id="01913-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01913-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01913-127">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="01913-127">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



