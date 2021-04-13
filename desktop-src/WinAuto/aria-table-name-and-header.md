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
# <a name="aria-data-table-error"></a>Erro de tabela de dados do ARIA

## <a name="text"></a>Texto

A tabela contém dados, mas não tem marcação acessível definida por meio de elementos do **Aria-Label**, **Aria-labelledby**, **título**, **legenda** ou **th** .

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a tabelas HTML com mais de uma célula. Esse erro não se aplica a tabelas com `role="presentation"` porque elas são consideradas como tabelas de layout.

Esse erro indica que uma tabela de dados não tem um nome acessível ou informações de cabeçalho.

Para corrigir esse erro, defina um nome acessível usando a marca de [**legenda**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) ou os atributos [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) . Se a tabela não tiver informações de cabeçalho, use as marcas do [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) para marcar células de cabeçalho.

## <a name="example"></a>Exemplo


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



 

 




