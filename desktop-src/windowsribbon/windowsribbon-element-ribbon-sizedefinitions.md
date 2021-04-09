---
title: Propriedade Ribbon. SizeDefinitions
description: Representa um contêiner para modelos de layout personalizados de controles da faixa de opção.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- Faixa de SizeDefinitions da propriedade Windows da faixa de propriedades
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008950"
---
# <a name="ribbonsizedefinitions-property"></a><span data-ttu-id="09e94-104">Propriedade Ribbon. SizeDefinitions</span><span class="sxs-lookup"><span data-stu-id="09e94-104">Ribbon.SizeDefinitions property</span></span>

<span data-ttu-id="09e94-105">Representa um contêiner para modelos de layout personalizados de controles da faixa de opção.</span><span class="sxs-lookup"><span data-stu-id="09e94-105">Represents a container for custom layout templates of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="09e94-106">Uso</span><span class="sxs-lookup"><span data-stu-id="09e94-106">Usage</span></span>

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="09e94-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="09e94-107">Attributes</span></span>

<span data-ttu-id="09e94-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="09e94-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="09e94-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="09e94-109">Child elements</span></span>



| <span data-ttu-id="09e94-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="09e94-110">Element</span></span>                                                                   | <span data-ttu-id="09e94-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="09e94-111">Description</span></span>                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="09e94-112">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="09e94-112">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> | <span data-ttu-id="09e94-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="09e94-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="09e94-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="09e94-114">Parent elements</span></span>



| <span data-ttu-id="09e94-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="09e94-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="09e94-116">**Faixa de opções**</span><span class="sxs-lookup"><span data-stu-id="09e94-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="09e94-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="09e94-117">Remarks</span></span>

<span data-ttu-id="09e94-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09e94-118">Optional.</span></span>

<span data-ttu-id="09e94-119">Pode ocorrer no máximo uma vez para cada [**faixa de faixas**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="09e94-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="09e94-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09e94-120">Examples</span></span>

<span data-ttu-id="09e94-121">O exemplo de código a seguir ilustra um modelo personalizado básico.</span><span class="sxs-lookup"><span data-stu-id="09e94-121">The following code example illustrates a basic custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a><span data-ttu-id="09e94-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e94-122">Requirements</span></span>



| <span data-ttu-id="09e94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e94-123">Requirement</span></span> | <span data-ttu-id="09e94-124">Valor</span><span class="sxs-lookup"><span data-stu-id="09e94-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="09e94-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e94-125">Minimum supported client</span></span><br/> | <span data-ttu-id="09e94-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="09e94-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="09e94-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09e94-127">Minimum supported server</span></span><br/> | <span data-ttu-id="09e94-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="09e94-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09e94-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="09e94-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e94-130">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="09e94-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





