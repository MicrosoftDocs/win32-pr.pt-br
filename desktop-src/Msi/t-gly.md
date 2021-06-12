---
description: Saiba mais Windows Installer conceitos que começam com a letra T, como processamento e transformação de transações.
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9489455f880ba558e5a9f8584be19718823035
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011259"
---
# <a name="t-windows-installer"></a><span data-ttu-id="d272c-103">T (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="d272c-103">T (Windows Installer)</span></span>

<span data-ttu-id="d272c-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="d272c-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d272c-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**processamento de transação**</span><span class="sxs-lookup"><span data-stu-id="d272c-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="d272c-106">Uma ou mais operações processadas juntas como um único inteiro indivisível chamado de transação.</span><span class="sxs-lookup"><span data-stu-id="d272c-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="d272c-107">Todas as operações constituintes devem ser bem-sucedidas para que a transação seja bem-sucedida, caso contrário, todas as operações serão re roll back para o estado original.</span><span class="sxs-lookup"><span data-stu-id="d272c-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="d272c-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Transformar**</span><span class="sxs-lookup"><span data-stu-id="d272c-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="d272c-109">Modelo das diferenças entre dois bancos [*de dados do instalador*](i-gly.md) que podem ser aplicados para produzir alterações semelhantes em outros bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="d272c-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="d272c-110">Por exemplo, uma transformação de localização pode ser usada para alterar o idioma de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d272c-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="d272c-111">Para obter mais informações, consulte [Merges and Transforms](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="d272c-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="d272c-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transformar sinalizadores de condição de erro**</span><span class="sxs-lookup"><span data-stu-id="d272c-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="d272c-113">Conjunto de propriedades usadas para sinalizar as condições de erro de uma [*transformação*](/windows).</span><span class="sxs-lookup"><span data-stu-id="d272c-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="d272c-114">Para obter mais informações, [**consulte MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="d272c-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="d272c-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transformar sinalizadores de validação**</span><span class="sxs-lookup"><span data-stu-id="d272c-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="d272c-116">Conjunto de propriedades usadas para verificar se [*a transformação*](/windows) pode ser aplicada ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d272c-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="d272c-117">Para ver uma lista dessas propriedades, consulte [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="d272c-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
