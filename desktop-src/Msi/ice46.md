---
description: O ICE46 verifica as propriedades personalizadas em condições, texto formatado e outros locais que diferem de uma propriedade definida pelo sistema somente pelo caso de um ou mais caracteres.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662063"
---
# <a name="ice46"></a><span data-ttu-id="406c6-103">ICE46</span><span class="sxs-lookup"><span data-stu-id="406c6-103">ICE46</span></span>

<span data-ttu-id="406c6-104">O ICE46 verifica as propriedades personalizadas em condições, texto formatado e outros locais que diferem de uma propriedade definida pelo sistema somente pelo caso de um ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="406c6-104">ICE46 checks for custom properties in conditions, formatted text, and other locations that differ from a system defined property only by the case of one or more characters.</span></span>

## <a name="result"></a><span data-ttu-id="406c6-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="406c6-105">Result</span></span>

<span data-ttu-id="406c6-106">O ICE46 posta uma mensagem informativa se houver uma propriedade personalizada em uma condição, um texto formatado e outro local que seja diferente de propriedades definidas pelo sistema somente no caso de um ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="406c6-106">ICE46 posts an informational message if there is a custom property in a condition, formatted text, and other location that differs from a system defined properties only in the case of one or more characters.</span></span>

## <a name="example"></a><span data-ttu-id="406c6-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="406c6-107">Example</span></span>

<span data-ttu-id="406c6-108">ICE46 relata os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="406c6-108">ICE46 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="406c6-109">Erro de ICE46</span><span class="sxs-lookup"><span data-stu-id="406c6-109">ICE46 error</span></span>                                                                                                                                            | <span data-ttu-id="406c6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="406c6-110">Description</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="406c6-111">A propriedade REINSTALLMODE definida na tabela de propriedades difere de outra propriedade definida somente por maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="406c6-111">Property ReinstallMode defined in property table differs from another defined property only by case.</span></span>                                                   | <span data-ttu-id="406c6-112">O nome da propriedade definida pelo sistema **REinstallmode** difere da propriedade personalizada somente por caso.</span><span class="sxs-lookup"><span data-stu-id="406c6-112">The system defined property name **REINSTALLMODE** differs from the custom property by case only.</span></span> <span data-ttu-id="406c6-113">As propriedades diferenciam maiúsculas de minúsculas, portanto, a propriedade personalizada não é a mesma que a propriedade do sistema.</span><span class="sxs-lookup"><span data-stu-id="406c6-113">Properties are case sensitive, so custom property is not the same as the system property.</span></span> <span data-ttu-id="406c6-114">Essa é uma causa comum de erros.</span><span class="sxs-lookup"><span data-stu-id="406c6-114">This is a common cause of errors.</span></span> |
| <span data-ttu-id="406c6-115">Propriedade ' MyProperty ' referenciada na coluna ' InstallExecuteSequence '. ' A condição ' da linha ' InstallFinalize ' difere de uma propriedade definida somente por caso.</span><span class="sxs-lookup"><span data-stu-id="406c6-115">Property 'Myproperty' referenced in column 'InstallExecuteSequence'.'Condition' of row 'InstallFinalize' differs from a defined property by case only.</span></span> | <span data-ttu-id="406c6-116">A tabela de propriedades define a tabela MyProperty, mas a propriedade referenciada é MyProperty.</span><span class="sxs-lookup"><span data-stu-id="406c6-116">The property table defines the table MyProperty, but the referenced property is Myproperty.</span></span> <span data-ttu-id="406c6-117">As propriedades diferenciam maiúsculas de minúsculas, portanto, as duas propriedades não são as mesmas.</span><span class="sxs-lookup"><span data-stu-id="406c6-117">Properties are case sensitive, so the two properties are NOT the same.</span></span> <span data-ttu-id="406c6-118">Essa é uma causa comum de erros.</span><span class="sxs-lookup"><span data-stu-id="406c6-118">This is a common cause of errors.</span></span>                          |



 

[<span data-ttu-id="406c6-119">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="406c6-119">Property Table</span></span>](property-table.md)



| <span data-ttu-id="406c6-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="406c6-120">Property</span></span>      | <span data-ttu-id="406c6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="406c6-121">Value</span></span>   |
|---------------|---------|
| <span data-ttu-id="406c6-122">ReinstallMode</span><span class="sxs-lookup"><span data-stu-id="406c6-122">ReinstallMode</span></span> | <span data-ttu-id="406c6-123">omus</span><span class="sxs-lookup"><span data-stu-id="406c6-123">omus</span></span>    |
| <span data-ttu-id="406c6-124">MyProperty</span><span class="sxs-lookup"><span data-stu-id="406c6-124">MyProperty</span></span>    | <span data-ttu-id="406c6-125">um valor</span><span class="sxs-lookup"><span data-stu-id="406c6-125">a value</span></span> |



 

<span data-ttu-id="406c6-126">[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="406c6-126">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="406c6-127">Ação</span><span class="sxs-lookup"><span data-stu-id="406c6-127">Action</span></span>          | <span data-ttu-id="406c6-128">Condição</span><span class="sxs-lookup"><span data-stu-id="406c6-128">Condition</span></span>  |
|-----------------|------------|
| <span data-ttu-id="406c6-129">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="406c6-129">InstallFinalize</span></span> | <span data-ttu-id="406c6-130">Myproperty</span><span class="sxs-lookup"><span data-stu-id="406c6-130">Myproperty</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="406c6-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="406c6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="406c6-132">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="406c6-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



