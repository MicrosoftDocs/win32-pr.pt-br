---
description: ICE61 valida a tabela de atualização de um banco de dados Windows Installer.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752257"
---
# <a name="ice61"></a><span data-ttu-id="53ef4-103">ICE61</span><span class="sxs-lookup"><span data-stu-id="53ef4-103">ICE61</span></span>

<span data-ttu-id="53ef4-104">ICE61 verifica a tabela de atualização para garantir que as seguintes condições sejam verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="53ef4-104">ICE61 checks the upgrade table to ensure that the following conditions are true:</span></span>

-   <span data-ttu-id="53ef4-105">Todas as propriedades Actionproperty não são previamente autorizadas na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="53ef4-105">All ActionProperty properties are not pre-authored in the Property table.</span></span>
-   <span data-ttu-id="53ef4-106">Todas as propriedades Actionproperty são propriedades públicas.</span><span class="sxs-lookup"><span data-stu-id="53ef4-106">All ActionProperty properties are Public Properties.</span></span>
-   <span data-ttu-id="53ef4-107">Todas as propriedades Actionproperty são incluídas na propriedade [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="53ef4-107">All ActionProperty properties are included in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>
-   <span data-ttu-id="53ef4-108">Todas as propriedades Actionproperty são exclusivas para cada registro na tabela de atualização.</span><span class="sxs-lookup"><span data-stu-id="53ef4-108">All ActionProperty properties are unique to each record in the Upgrade table.</span></span>
-   <span data-ttu-id="53ef4-109">Todos os valores de VersionMax não são menores que os valores de VersionMin correspondentes.</span><span class="sxs-lookup"><span data-stu-id="53ef4-109">All VersionMax values are not less than the corresponding VersionMin values.</span></span>
-   <span data-ttu-id="53ef4-110">Os valores VersionMin e VersionMax são versões válidas do produto.</span><span class="sxs-lookup"><span data-stu-id="53ef4-110">VersionMin and VersionMax values are valid product versions.</span></span> <span data-ttu-id="53ef4-111">Consulte a propriedade [**ProductVersion**](productversion.md) para obter o formato de versão de produto válido.</span><span class="sxs-lookup"><span data-stu-id="53ef4-111">See the [**ProductVersion**](productversion.md) property for the valid product version format.</span></span>
-   <span data-ttu-id="53ef4-112">Nenhuma tentativa é feita para remover uma versão mais recente ou igual do produto atual.</span><span class="sxs-lookup"><span data-stu-id="53ef4-112">No attempt is made to remove a newer or equal version of the current product.</span></span>

<span data-ttu-id="53ef4-113">Falha ao corrigir um aviso ou erro relatado por ICE61 geralmente leva a problemas na atualização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53ef4-113">Failure to fix a warning or error reported by ICE61 generally leads to problems in upgrading your application.</span></span> <span data-ttu-id="53ef4-114">Dependendo do erro exato, isso pode ser qualquer coisa desde deixar arquivos da versão mais antiga por trás, excluir arquivos da versão mais antiga, mesmo que sejam necessários para o novo aplicativo ou concluir a falha da atualização.</span><span class="sxs-lookup"><span data-stu-id="53ef4-114">Depending on the exact error, this could be anything from leaving files from the older version behind, deleting files from the older version even though they are needed by the new application, or complete failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="53ef4-115">Resultado</span><span class="sxs-lookup"><span data-stu-id="53ef4-115">Result</span></span>

<span data-ttu-id="53ef4-116">ICE61 posta um aviso ou erro se qualquer uma das condições acima não for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="53ef4-116">ICE61 posts a warning or error if any of the above conditions are not true.</span></span>

## <a name="example"></a><span data-ttu-id="53ef4-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="53ef4-117">Example</span></span>

<span data-ttu-id="53ef4-118">ICE61 relata os erros e avisos a seguir para os exemplos mostrados.</span><span class="sxs-lookup"><span data-stu-id="53ef4-118">ICE61 reports the following errors and warning for the examples shown.</span></span>

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

<span data-ttu-id="53ef4-119">Nesse caso, a primeira linha tentaria remover um produto da mesma versão.</span><span class="sxs-lookup"><span data-stu-id="53ef4-119">In this case, the first row would try to remove a product of the same version.</span></span> <span data-ttu-id="53ef4-120">(A coluna VersionMax é igual à versão do produto na tabela de propriedades).</span><span class="sxs-lookup"><span data-stu-id="53ef4-120">(VersionMax column is equal to the product version in the Property table).</span></span>

<span data-ttu-id="53ef4-121">Para corrigir esse erro, use uma versão na coluna VersionMax inferior à versão atual especificada na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="53ef4-121">To fix this error, use a version in the VersionMax column lower than the current version specified in the Property table.</span></span> <span data-ttu-id="53ef4-122">Remova o bit **msidbUpgradeAttributesVersionMaxInclusive** da coluna atributos se o VersionMax for igual à versão atual.</span><span class="sxs-lookup"><span data-stu-id="53ef4-122">Remove the **msidbUpgradeAttributesVersionMaxInclusive** bit from the Attributes column if the VersionMax is equal to the current version.</span></span> <span data-ttu-id="53ef4-123">Se a intenção for apenas detectar o produto e não removê-lo, adicionar o bit **msidbUpgradeAttributesOnlyDetect** à coluna atributos também corrigirá esse erro.</span><span class="sxs-lookup"><span data-stu-id="53ef4-123">If the intent is only to detect the product and not remove it, adding the **msidbUpgradeAttributesOnlyDetect** bit to the Attributes column will also fix this error.</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

<span data-ttu-id="53ef4-124">A menos que a propriedade esteja listada na propriedade [**SecureCustomProperties**](securecustomproperties.md) , a propriedade não será passada para o lado do servidor da instalação quando a propriedade for encontrada.</span><span class="sxs-lookup"><span data-stu-id="53ef4-124">Unless the property is listed in the [**SecureCustomProperties**](securecustomproperties.md) property, the property is not passed to the server side of the install when the property is found.</span></span>

<span data-ttu-id="53ef4-125">Para corrigir esse erro, adicione a propriedade a [**SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="53ef4-125">To fix this error, add the property to [**SecureCustomProperties**](securecustomproperties.md).</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

<span data-ttu-id="53ef4-126">As propriedades de atualização devem ser propriedades públicas para que o resultado seja passado para o lado do servidor da instalação.</span><span class="sxs-lookup"><span data-stu-id="53ef4-126">Upgrade properties must be public properties for the result to be passed to the server side of the installation.</span></span>

<span data-ttu-id="53ef4-127">Para corrigir esse erro, use todas as letras maiúsculas no nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="53ef4-127">To fix this error, use all uppercase letters in the property name.</span></span>

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

<span data-ttu-id="53ef4-128">Uma propriedade só pode ser usada em uma linha da tabela de atualização.</span><span class="sxs-lookup"><span data-stu-id="53ef4-128">A property can only be used in one row of the Upgrade table.</span></span>

<span data-ttu-id="53ef4-129">Para corrigir esse erro, use uma propriedade diferente para a segunda linha.</span><span class="sxs-lookup"><span data-stu-id="53ef4-129">To fix this error, use a different property for the second row.</span></span>

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

<span data-ttu-id="53ef4-130">A versão mínima deve ser menor que a versão máxima.</span><span class="sxs-lookup"><span data-stu-id="53ef4-130">The minimum version must be less than the maximum version.</span></span>

<span data-ttu-id="53ef4-131">Para corrigir esse erro, verifique se há erros de digitação nos números de versão.</span><span class="sxs-lookup"><span data-stu-id="53ef4-131">To fix this error, check your version numbers for typos.</span></span> <span data-ttu-id="53ef4-132">Se eles estiverem corretos e você quiser usar o intervalo entre as duas versões, alterne-as para que VersionMin seja menor que VersionMax.</span><span class="sxs-lookup"><span data-stu-id="53ef4-132">If they are correct and you want to use the range between the two versions, switch them so that VersionMin is less than VersionMax.</span></span>

[<span data-ttu-id="53ef4-133">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="53ef4-133">Property Table</span></span>](property-table.md)



| <span data-ttu-id="53ef4-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="53ef4-134">Property</span></span>                                                 | <span data-ttu-id="53ef4-135">Valor</span><span class="sxs-lookup"><span data-stu-id="53ef4-135">Value</span></span>                                  |
|----------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="53ef4-136">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="53ef4-136">**UpgradeCode**</span></span>](upgradecode.md)                       | <span data-ttu-id="53ef4-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="53ef4-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |
| [<span data-ttu-id="53ef4-138">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="53ef4-138">**ProductVersion**</span></span>](productversion.md)                 | <span data-ttu-id="53ef4-139">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="53ef4-139">2.01.0000</span></span>                              |
| [<span data-ttu-id="53ef4-140">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="53ef4-140">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="53ef4-141">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="53ef4-141">OLDAPPFOUND</span></span>                            |



 

[<span data-ttu-id="53ef4-142">Atualizar tabela</span><span class="sxs-lookup"><span data-stu-id="53ef4-142">Upgrade Table</span></span>](upgrade-table.md)



| <span data-ttu-id="53ef4-143">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="53ef4-143">UpgradeCode</span></span>                            | <span data-ttu-id="53ef4-144">VersionMin</span><span class="sxs-lookup"><span data-stu-id="53ef4-144">VersionMin</span></span> | <span data-ttu-id="53ef4-145">VersionMax</span><span class="sxs-lookup"><span data-stu-id="53ef4-145">VersionMax</span></span> | <span data-ttu-id="53ef4-146">Idioma</span><span class="sxs-lookup"><span data-stu-id="53ef4-146">Language</span></span> | <span data-ttu-id="53ef4-147">Atributos</span><span class="sxs-lookup"><span data-stu-id="53ef4-147">Attributes</span></span> | <span data-ttu-id="53ef4-148">Remover</span><span class="sxs-lookup"><span data-stu-id="53ef4-148">Remove</span></span>                | <span data-ttu-id="53ef4-149">Açãoproperty</span><span class="sxs-lookup"><span data-stu-id="53ef4-149">ActionProperty</span></span>  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| <span data-ttu-id="53ef4-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="53ef4-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |            | <span data-ttu-id="53ef4-151">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="53ef4-151">2.01.0000</span></span>  |          | <span data-ttu-id="53ef4-152">513</span><span class="sxs-lookup"><span data-stu-id="53ef4-152">513</span></span>        |                       | <span data-ttu-id="53ef4-153">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="53ef4-153">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="53ef4-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="53ef4-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> | <span data-ttu-id="53ef4-155">2.01.0001</span><span class="sxs-lookup"><span data-stu-id="53ef4-155">2.01.0001</span></span>  | <span data-ttu-id="53ef4-156">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="53ef4-156">2.01.0000</span></span>  |          |            |                       | <span data-ttu-id="53ef4-157">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="53ef4-157">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="53ef4-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span><span class="sxs-lookup"><span data-stu-id="53ef4-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span></span> | <span data-ttu-id="53ef4-159">1.00.0000</span><span class="sxs-lookup"><span data-stu-id="53ef4-159">1.00.0000</span></span>  | <span data-ttu-id="53ef4-160">2.00.0000</span><span class="sxs-lookup"><span data-stu-id="53ef4-160">2.00.0000</span></span>  | <span data-ttu-id="53ef4-161">1046</span><span class="sxs-lookup"><span data-stu-id="53ef4-161">1033</span></span>     |            | <span data-ttu-id="53ef4-162">\[AppFeatureEnglish\]</span><span class="sxs-lookup"><span data-stu-id="53ef4-162">\[AppFeatureEnglish\]</span></span> | <span data-ttu-id="53ef4-163">EnglishAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="53ef4-163">EnglishAPPFOUND</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="53ef4-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53ef4-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53ef4-165">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="53ef4-165">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



