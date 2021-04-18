---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Adicionando instâncias de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e3df1b6c271c37c080968cc775ac11eba2e3ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104370828"
---
# <a name="adding-property-instances"></a><span data-ttu-id="8b74f-104">Adicionando instâncias de propriedade</span><span class="sxs-lookup"><span data-stu-id="8b74f-104">Adding Property Instances</span></span>

<span data-ttu-id="8b74f-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="8b74f-105">This topic is not current.</span></span> <span data-ttu-id="8b74f-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8b74f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8b74f-107">O esquema de impressão permite que as instâncias de propriedade estejam presentes em uma instância de opção.</span><span class="sxs-lookup"><span data-stu-id="8b74f-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="8b74f-108">As instâncias de propriedade definidas no documento PrintCapabilities não são propagadas para as instâncias de opção salvas no PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="8b74f-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="8b74f-109">Os elementos de propriedade não afetam o resultado do processo de Pontuação quando duas instâncias de opção são comparadas, mas as instâncias ScoredProperty afetam esse processo.</span><span class="sxs-lookup"><span data-stu-id="8b74f-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="8b74f-110">Todos os drivers de dispositivo que implementam um algoritmo de Pontuação devem observar essa convenção.</span><span class="sxs-lookup"><span data-stu-id="8b74f-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="8b74f-111">Os provedores de PrintCapabilities têm permissão para adicionar instâncias de propriedade a uma opção se essas instâncias forem específicas para essa opção específica e nenhuma outra, ou se o provedor pretender que o valor dessa propriedade apareça para cada opção no recurso.</span><span class="sxs-lookup"><span data-stu-id="8b74f-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="8b74f-112">Por exemplo, suponha que a propriedade de taxa de fotonotação seja dependente da opção selecionada para o recurso PageResolution.</span><span class="sxs-lookup"><span data-stu-id="8b74f-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="8b74f-113">Se a propriedade de impressão for colocada no nível raiz do documento PrintCapabilities, ela seria de valor único e refletiria apenas a taxa de impressão para a resolução selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="8b74f-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="8b74f-114">No entanto, se a propriedade de taxa de impressão tiver sido colocada dentro de cada opção PageResolution, cada instância da propriedade Print Rate poderá refletir a taxa impressa para a opção PageResolution que a continha.</span><span class="sxs-lookup"><span data-stu-id="8b74f-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="8b74f-115">O documento PrintCapabilities contém várias definições para a taxa de fotonota, uma correspondente a cada opção PageResolution.</span><span class="sxs-lookup"><span data-stu-id="8b74f-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="8b74f-116">Usando uma representação abreviada, as PrintCapabilities contêm:</span><span class="sxs-lookup"><span data-stu-id="8b74f-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

<span data-ttu-id="8b74f-117">Em algumas situações, colocar uma propriedade de taxa de impressão dentro de cada opção de resolução é mais conveniente para o cliente, pois o cliente pode determinar rapidamente o efeito que cada opção de resolução tem na taxa de impressão, sem a necessidade de obter um novo documento de PrintCapabilities para cada configuração de resolução.</span><span class="sxs-lookup"><span data-stu-id="8b74f-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="8b74f-118">Observe também que as instâncias de propriedade também podem ser adicionadas como elementos filho dos elementos de recurso.</span><span class="sxs-lookup"><span data-stu-id="8b74f-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="8b74f-119">Isso será útil se houver instâncias de propriedade ou valores de instâncias de propriedade que são específicos de cada recurso.</span><span class="sxs-lookup"><span data-stu-id="8b74f-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="8b74f-120">Por exemplo, pode haver uma propriedade que especifica se apenas uma opção pode ser selecionada ao mesmo tempo para um recurso ou se várias opções podem ser selecionadas.</span><span class="sxs-lookup"><span data-stu-id="8b74f-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="8b74f-121">Esse é o escolha \_ um, escolha \_ muitas propriedades usadas nos arquivos PPD e GPD.</span><span class="sxs-lookup"><span data-stu-id="8b74f-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="8b74f-122">Como algumas instâncias de recurso podem ser identificadas como escolha \_ uma, enquanto outras podem ser identificadas como escolher \_ muitos, essa propriedade deve ser definida para cada recurso.</span><span class="sxs-lookup"><span data-stu-id="8b74f-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="8b74f-123">A localização da propriedade como um elemento filho do recurso produz a associação entre a propriedade e o recurso.</span><span class="sxs-lookup"><span data-stu-id="8b74f-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b74f-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b74f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b74f-125">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="8b74f-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



