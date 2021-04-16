---
description: O método FormatText do objeto Record formata os campos de acordo com o modelo no campo 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Método record. FormatText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749988"
---
# <a name="recordformattext-method"></a><span data-ttu-id="e1c53-103">Método record. FormatText</span><span class="sxs-lookup"><span data-stu-id="e1c53-103">Record.FormatText method</span></span>

<span data-ttu-id="e1c53-104">O método **FormatText** do objeto [**Record**](record-object.md) formata os campos de acordo com o modelo no campo 0.</span><span class="sxs-lookup"><span data-stu-id="e1c53-104">The **FormatText** method of the [**Record**](record-object.md) object formats fields according to the template in field 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1c53-105">Syntax</span></span>


```JScript
Record.FormatText()
```



## <a name="parameters"></a><span data-ttu-id="e1c53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1c53-106">Parameters</span></span>

<span data-ttu-id="e1c53-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e1c53-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1c53-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1c53-108">Return value</span></span>

<span data-ttu-id="e1c53-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e1c53-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1c53-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1c53-110">Remarks</span></span>

<span data-ttu-id="e1c53-111">O método **FormatText** segue a funcionalidade da função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) se **MsiFormatRecord** recebeu um identificador de instalador nulo como seu primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1c53-111">The **FormatText** method follows the functionality of the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function if **MsiFormatRecord** was passed a null installer handle as its first parameter.</span></span> <span data-ttu-id="e1c53-112">Como resultado, somente os parâmetros de campo de registro são processados e as propriedades não estão disponíveis para substituição.</span><span class="sxs-lookup"><span data-stu-id="e1c53-112">As a result, only the record field parameters are processed and properties are not available for substitution.</span></span>

<span data-ttu-id="e1c53-113">Por exemplo, uma cadeia de caracteres como "Formatar este campo: \[ 1 \] , formatar esta propriedade: \[ propriedade \] " é resolvida como "Formatar este campo: valor do campo 1, formatar esta propriedade: \[ propriedade \] ".</span><span class="sxs-lookup"><span data-stu-id="e1c53-113">For example, a string such as "format this field: \[1\], format this property: \[property\]" is resolved to "format this field: value from field 1, format this property: \[property\]."</span></span>

<span data-ttu-id="e1c53-114">Os parâmetros que devem ser [formatados](formatted.md) são colocados entre colchetes \[ ... \] .</span><span class="sxs-lookup"><span data-stu-id="e1c53-114">Parameters that are to be [formatted](formatted.md) are enclosed in square brackets \[...\].</span></span> <span data-ttu-id="e1c53-115">Os colchetes podem ser iterados porque as substituições são resolvidas de dentro para fora.</span><span class="sxs-lookup"><span data-stu-id="e1c53-115">The square brackets can be iterated because the substitutions are resolved from the inside out.</span></span>

<span data-ttu-id="e1c53-116">Se uma parte da cadeia de caracteres estiver entre chaves {} e não contiver colchetes, ela permanecerá inalterada, incluindo as chaves.</span><span class="sxs-lookup"><span data-stu-id="e1c53-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, it is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="e1c53-117">Observação no caso de [ações personalizadas de execução adiada](deferred-execution-custom-actions.md), o **FormatText** dá suporte apenas a um conjunto limitado de propriedades: as propriedades CustomActionData e ProductCode.</span><span class="sxs-lookup"><span data-stu-id="e1c53-117">Note in the case of [deferred execution custom actions](deferred-execution-custom-actions.md), **FormatText** only supports a limited set of properties: the CustomActionData and ProductCode properties.</span></span> <span data-ttu-id="e1c53-118">Para obter mais informações, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e1c53-118">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1c53-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1c53-119">Requirements</span></span>



| <span data-ttu-id="e1c53-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1c53-120">Requirement</span></span> | <span data-ttu-id="e1c53-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e1c53-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c53-122">Versão</span><span class="sxs-lookup"><span data-stu-id="e1c53-122">Version</span></span><br/> | <span data-ttu-id="e1c53-123">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1c53-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e1c53-124">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1c53-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e1c53-125">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1c53-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e1c53-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e1c53-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1c53-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1c53-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e1c53-128">IID</span><span class="sxs-lookup"><span data-stu-id="e1c53-128">IID</span></span><br/>     | <span data-ttu-id="e1c53-129">IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e1c53-129">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="e1c53-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1c53-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1c53-131">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="e1c53-131">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[<span data-ttu-id="e1c53-132">Binário</span><span class="sxs-lookup"><span data-stu-id="e1c53-132">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="e1c53-133">Tipos de dados de coluna</span><span class="sxs-lookup"><span data-stu-id="e1c53-133">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




