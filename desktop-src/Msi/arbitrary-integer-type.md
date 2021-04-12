---
description: O tipo de inteiro arbitrário do tipo semântico é um dos tipos de formato inteiro.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Tipo de inteiro arbitrário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091543"
---
# <a name="arbitrary-integer-type"></a><span data-ttu-id="468b0-103">Tipo de inteiro arbitrário</span><span class="sxs-lookup"><span data-stu-id="468b0-103">Arbitrary Integer Type</span></span>

<span data-ttu-id="468b0-104">O tipo de inteiro arbitrário do [tipo semântico](semantic-types.md) é um dos [tipos de formato inteiro](integer-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="468b0-104">The Arbitrary Integer Type of [semantic type](semantic-types.md) is one of the [Integer Format Types](integer-format-types.md).</span></span> <span data-ttu-id="468b0-105">Esse tipo de item configurável é um inteiro fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="468b0-105">This type of configurable item is an integer provided by the user.</span></span> <span data-ttu-id="468b0-106">A ferramenta de mesclagem substitui esse inteiro nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="468b0-106">The merge tool substitutes this integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="468b0-107">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "2" na coluna formato e deixar em branco as colunas Type e ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="468b0-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "2" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="468b0-108">As colunas Type e ContextData são reservadas e devem ser nulas.</span><span class="sxs-lookup"><span data-stu-id="468b0-108">The Type and ContextData columns are reserved and must be null.</span></span>

 

 



