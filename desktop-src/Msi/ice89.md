---
description: ICE89 valida que o valor na \_ coluna pai ProgID na tabela ProgID é uma chave estrangeira válida para a coluna ProgID na tabela ProgID. Cada pai do ProgId deve ter um registro na tabela ProgId.
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d14ec5b17a20b9046625feb464865bd0c08419e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922462"
---
# <a name="ice89"></a><span data-ttu-id="6273d-104">ICE89</span><span class="sxs-lookup"><span data-stu-id="6273d-104">ICE89</span></span>

<span data-ttu-id="6273d-105">ICE89 valida que o valor na \_ coluna pai ProgID na [tabela ProgID](progid-table.md) é uma chave estrangeira válida para a coluna ProgId na tabela ProgID.</span><span class="sxs-lookup"><span data-stu-id="6273d-105">ICE89 validates that the value in the Progid\_Parent column in [ProgId table](progid-table.md) is a valid foreign key into the ProgId column in ProgId table.</span></span> <span data-ttu-id="6273d-106">Cada pai do ProgId deve ter um registro na tabela ProgId.</span><span class="sxs-lookup"><span data-stu-id="6273d-106">Every ProgId parent should have a record in the ProgId table.</span></span>

## <a name="result"></a><span data-ttu-id="6273d-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="6273d-107">Result</span></span>

<span data-ttu-id="6273d-108">ICE89 posta os erros a seguir.</span><span class="sxs-lookup"><span data-stu-id="6273d-108">ICE89 posts the following errors.</span></span>



| <span data-ttu-id="6273d-109">Erro de ICE89</span><span class="sxs-lookup"><span data-stu-id="6273d-109">ICE89 error</span></span>                                                           | <span data-ttu-id="6273d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6273d-110">Description</span></span>                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="6273d-111">O pai do ProgId \_ ' \[ 1 \] ' na tabela ProgId não é um ProgID válido.</span><span class="sxs-lookup"><span data-stu-id="6273d-111">The ProgId\_Parent '\[1\]' in the ProgId table is not a valid ProgId.</span></span> | <span data-ttu-id="6273d-112">Há um pai ProgId especificado que não está listado na tabela ProgId.</span><span class="sxs-lookup"><span data-stu-id="6273d-112">There is a ProgId parent specified that is not listed in the ProgId table.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6273d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6273d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6273d-114">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="6273d-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



