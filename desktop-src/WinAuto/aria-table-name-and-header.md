---
title: Erro de tabela de dados do ARIA
description: Erro de tabela de dados do ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 025443ab452ff0103c8808c27dce834a03cb8c96e0d9106a7abb4409b64a0697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133969"
---
# <a name="aria-data-table-error"></a>Erro de tabela de dados do ARIA

## <a name="text"></a>Texto

A tabela contém dados, mas não tem marcação acessível definida embora **aria-label**, **aria-labelledby**, **title**, **caption** **ou th** elements.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a tabelas HTML com mais de uma célula. Esse erro não se aplica a tabelas com `role="presentation"` porque elas são consideradas tabelas de layout.

Esse erro indica que uma tabela de dados não tem um nome acessível ou informações de header.

Para corrigir esse erro, defina um nome acessível usando a marca [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) ou os atributos [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)ou [**title.**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) Se a tabela não tiver informações de título, use [**marcas THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) para marcar células de título.

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



 

 




