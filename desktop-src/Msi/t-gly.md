---
description: Saiba mais Windows conceitos do Instalador que começam com a letra T, como processamento e transformação de transações.
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7148ff7ca92a55698baa8f21e28ee6c4a54d69fd498adaea29c924bc23bc9fda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626706"
---
# <a name="t-windows-installer"></a>T (Windows Instalador)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**processamento de transação**
</dt> <dd>

Uma ou mais operações processadas juntas como um único inteiro indivisível chamado de transação. Todas as operações constituintes devem ser bem-sucedidas para que a transação seja bem-sucedida, caso contrário, todas as operações serão re roll back para o estado original.

</dd> <dt>

<span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Transformar**
</dt> <dd>

Modelo das diferenças entre dois bancos [*de dados do instalador*](i-gly.md) que podem ser aplicados para produzir alterações semelhantes em outros bancos de dados. Por exemplo, uma transformação de localização pode ser usada para alterar o idioma de um aplicativo. Para obter mais informações, consulte [Merges and Transforms](merges-and-transforms.md).

</dd> <dt>

<span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transformar sinalizadores de condição de erro**
</dt> <dd>

Conjunto de propriedades usadas para sinalizar as condições de erro de uma [*transformação*](/windows). Para obter mais informações, [**consulte MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

</dd> <dt>

<span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transformar sinalizadores de validação**
</dt> <dd>

Conjunto de propriedades usadas para verificar se a [*transformação*](/windows) pode ser aplicada ao banco de dados. Para ver uma lista dessas propriedades, consulte [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

</dd> </dl>

 

 
