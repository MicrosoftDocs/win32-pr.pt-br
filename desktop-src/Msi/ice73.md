---
description: ICE73 verifica se o pacote não reutiliza códigos de pacote, códigos de atualização ou códigos de produto dos exemplos do SDK Windows Installer. Os pacotes nunca devem reutilizar o pacote, a atualização ou os códigos de produto de outro produto.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770375"
---
# <a name="ice73"></a><span data-ttu-id="ed960-104">ICE73</span><span class="sxs-lookup"><span data-stu-id="ed960-104">ICE73</span></span>

<span data-ttu-id="ed960-105">ICE73 verifica se o pacote não reutiliza códigos de pacote, códigos de atualização ou códigos de produto dos exemplos do SDK Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ed960-105">ICE73 verifies that your package does not reuse package codes, upgrade codes, or product codes of the Windows Installer SDK samples.</span></span> <span data-ttu-id="ed960-106">Os pacotes nunca devem reutilizar o pacote, a atualização ou os códigos de produto de outro produto.</span><span class="sxs-lookup"><span data-stu-id="ed960-106">Packages should never reuse the package, upgrade, or product codes of another product.</span></span>

## <a name="result"></a><span data-ttu-id="ed960-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="ed960-107">Result</span></span>

<span data-ttu-id="ed960-108">O ICE73 gera um aviso se o pacote do seu produto reutiliza um código de pacote ou produto de um exemplo de SDK Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ed960-108">ICE73 outputs a warning if your product's package reuses a package or product code of a Windows Installer SDK sample.</span></span>

## <a name="example"></a><span data-ttu-id="ed960-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed960-109">Example</span></span>

<span data-ttu-id="ed960-110">ICE73 relata os seguintes erros para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="ed960-110">ICE73 reports the following errors for the example shown:</span></span>

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> <span data-ttu-id="ed960-111">Os asteriscos ( \* \* \* \* ) no GUID representam o intervalo de GUIDs reservados para pacotes SDK de Windows Installer subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ed960-111">The asterisks (\*\*\*\*) in the GUID represent the range of GUIDs reserved for subsequent Windows Installer SDK packages.</span></span>

 

<span data-ttu-id="ed960-112">Para corrigir os erros, gere um novo GUID exclusivo para os códigos do pacote e do produto do pacote.</span><span class="sxs-lookup"><span data-stu-id="ed960-112">To fix the errors, generate a new unique GUID for your package's product and package codes.</span></span> <span data-ttu-id="ed960-113">Você também precisará de um novo GUID exclusivo para o código de atualização do pacote.</span><span class="sxs-lookup"><span data-stu-id="ed960-113">You will also need a new unique GUID for your package's upgrade code.</span></span>

<span data-ttu-id="ed960-114">[Fluxo de informações de resumo](summary-information-stream.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="ed960-114">[Summary Information Stream](summary-information-stream.md) (partial)</span></span>



| <span data-ttu-id="ed960-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ed960-115">Property</span></span>       | <span data-ttu-id="ed960-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ed960-116">Value</span></span>                                  |
|----------------|----------------------------------------|
| <span data-ttu-id="ed960-117">DTI \_ REVNUMBER</span><span class="sxs-lookup"><span data-stu-id="ed960-117">PID\_REVNUMBER</span></span> | <span data-ttu-id="ed960-118">{000C1101-0000-0000-C000-000000000047}</span><span class="sxs-lookup"><span data-stu-id="ed960-118">{000C1101-0000-0000-C000-000000000047}</span></span> |



 

<span data-ttu-id="ed960-119">[Tabela de propriedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="ed960-119">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="ed960-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ed960-120">Property</span></span>                           | <span data-ttu-id="ed960-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ed960-121">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| [<span data-ttu-id="ed960-122">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="ed960-122">**ProductCode**</span></span>](productcode.md) | <span data-ttu-id="ed960-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span><span class="sxs-lookup"><span data-stu-id="ed960-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span></span> |
| [<span data-ttu-id="ed960-124">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="ed960-124">**UpgradeCode**</span></span>](upgradecode.md) | <span data-ttu-id="ed960-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span><span class="sxs-lookup"><span data-stu-id="ed960-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ed960-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed960-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed960-127">Códigos de pacote</span><span class="sxs-lookup"><span data-stu-id="ed960-127">Package Codes</span></span>](package-codes.md)
</dt> <dt>

[<span data-ttu-id="ed960-128">Códigos de produto</span><span class="sxs-lookup"><span data-stu-id="ed960-128">Product Codes</span></span>](product-codes.md)
</dt> <dt>

[<span data-ttu-id="ed960-129">**Propriedade de resumo do número de revisão**</span><span class="sxs-lookup"><span data-stu-id="ed960-129">**Revision Number Summary Property**</span></span>](revision-number-summary.md)
</dt> <dt>

[<span data-ttu-id="ed960-130">**Propriedade UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="ed960-130">**UpgradeCode Property**</span></span>](upgradecode.md)
</dt> <dt>

[<span data-ttu-id="ed960-131">**Propriedade ProductCode**</span><span class="sxs-lookup"><span data-stu-id="ed960-131">**ProductCode Property**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="ed960-132">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="ed960-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



