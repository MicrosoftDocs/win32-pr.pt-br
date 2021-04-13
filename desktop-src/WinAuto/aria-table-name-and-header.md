---
title: Erro de tabela de dados do ARIA
description: Erro de tabela de dados do ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366833"
---
# <a name="aria-data-table-error"></a><span data-ttu-id="db286-104">Erro de tabela de dados do ARIA</span><span class="sxs-lookup"><span data-stu-id="db286-104">ARIA Data Table Error</span></span>

## <a name="text"></a><span data-ttu-id="db286-105">Texto</span><span class="sxs-lookup"><span data-stu-id="db286-105">Text</span></span>

<span data-ttu-id="db286-106">A tabela contém dados, mas não tem marcação acessível definida por meio de elementos do **Aria-Label**, **Aria-labelledby**, **título**, **legenda** ou **th** .</span><span class="sxs-lookup"><span data-stu-id="db286-106">Table contains data but doesn't have accessible markup defined though **aria-label**, **aria-labelledby**, **title**, **caption** or **th** elements.</span></span>

## <a name="type"></a><span data-ttu-id="db286-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="db286-107">Type</span></span>

<span data-ttu-id="db286-108">Erro</span><span class="sxs-lookup"><span data-stu-id="db286-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="db286-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="db286-109">Description</span></span>

<span data-ttu-id="db286-110">Esse erro se aplica a tabelas HTML com mais de uma célula.</span><span class="sxs-lookup"><span data-stu-id="db286-110">This error applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="db286-111">Esse erro não se aplica a tabelas com `role="presentation"` porque elas são consideradas como tabelas de layout.</span><span class="sxs-lookup"><span data-stu-id="db286-111">This error does not apply to tables with `role="presentation"` because these are considered to be layout tables.</span></span>

<span data-ttu-id="db286-112">Esse erro indica que uma tabela de dados não tem um nome acessível ou informações de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="db286-112">This error indicates that a data table doesn’t have an accessible name or header information.</span></span>

<span data-ttu-id="db286-113">Para corrigir esse erro, defina um nome acessível usando a marca de [**legenda**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) ou os atributos [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .</span><span class="sxs-lookup"><span data-stu-id="db286-113">To fix this error, define an accessible name by using the [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) tag, or the [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span> <span data-ttu-id="db286-114">Se a tabela não tiver informações de cabeçalho, use as marcas do [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) para marcar células de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="db286-114">If the table is missing header information, use [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags to mark header cells.</span></span>

## <a name="example"></a><span data-ttu-id="db286-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="db286-115">Example</span></span>


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




