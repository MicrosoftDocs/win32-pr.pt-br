---
description: O procedimento a seguir descreve um cenário para gerar uma transformação que oculta permanentemente um recurso.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Gerando uma transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011301"
---
# <a name="generating-a-transform"></a><span data-ttu-id="0b8e6-103">Gerando uma transformação</span><span class="sxs-lookup"><span data-stu-id="0b8e6-103">Generating a Transform</span></span>

<span data-ttu-id="0b8e6-104">O procedimento a seguir descreve um cenário para gerar uma transformação que oculta permanentemente um recurso.</span><span class="sxs-lookup"><span data-stu-id="0b8e6-104">The following procedure describes a scenario to generate a transform that permanently hides a feature.</span></span>

<span data-ttu-id="0b8e6-105">**Para ocultar permanentemente um recurso de produto**</span><span class="sxs-lookup"><span data-stu-id="0b8e6-105">**To permanently hide a product feature**</span></span>

1.  <span data-ttu-id="0b8e6-106">Copie o pacote de instalação original.</span><span class="sxs-lookup"><span data-stu-id="0b8e6-106">Copy the original installation package.</span></span>
2.  <span data-ttu-id="0b8e6-107">Altere a cópia definindo o valor da coluna de exibição na tabela de [recursos](feature-table.md) para zero.</span><span class="sxs-lookup"><span data-stu-id="0b8e6-107">Alter the copy by setting the value of the Display column in the [Feature table](feature-table.md) to zero.</span></span> <span data-ttu-id="0b8e6-108">Isso especifica a ocultação do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b8e6-108">This specifies hiding the feature.</span></span>
3.  <span data-ttu-id="0b8e6-109">Crie uma transformação do pacote de instalação original para os novos pacotes de instalação chamando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span><span class="sxs-lookup"><span data-stu-id="0b8e6-109">Create a transform from the original installation package to the new installation packages by calling [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span></span>
4.  <span data-ttu-id="0b8e6-110">Crie as informações de resumo na transformação chamando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="0b8e6-110">Create the summary information in the transform by calling [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

<span data-ttu-id="0b8e6-111">A transformação está pronta para ser aplicada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="0b8e6-111">The transform is then ready to be applied during installation.</span></span> <span data-ttu-id="0b8e6-112">Para obter mais informações, consulte [aplicando transformações](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="0b8e6-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



