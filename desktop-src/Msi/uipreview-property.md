---
description: A Propriedade Property do objeto UIPreview é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador ou, se for prefixada com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Propriedade UIPreview. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759369"
---
# <a name="uipreviewproperty-property"></a><span data-ttu-id="33f43-103">Propriedade UIPreview. Property</span><span class="sxs-lookup"><span data-stu-id="33f43-103">UIPreview.Property property</span></span>

<span data-ttu-id="33f43-104">A propriedade **Property** do objeto [**UIPreview**](uipreview-object.md) é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador ou, se for prefixada com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="33f43-104">The **Property** property of the [**UIPreview**](uipreview-object.md) object is a read-write property that represents the string value of a named installer property, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="33f43-105">Isso é exposto para permitir a exibição adequada de caixas de diálogo que dependem de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="33f43-105">This is exposed to allow proper display of dialog boxes that are dependent upon property values.</span></span> <span data-ttu-id="33f43-106">Os valores de cadeia de caracteres ou inteiros podem ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="33f43-106">Either string or integer values may be supplied.</span></span> <span data-ttu-id="33f43-107">Uma propriedade ou variável de ambiente inexistente é equivalente ao valor que está sendo nulo.</span><span class="sxs-lookup"><span data-stu-id="33f43-107">A nonexistent property or environment variable is equivalent to its value being null.</span></span>

<span data-ttu-id="33f43-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="33f43-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f43-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="33f43-109">Syntax</span></span>


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="33f43-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="33f43-110">Property value</span></span>

<span data-ttu-id="33f43-111">O nome de uma propriedade que diferencia maiúsculas de minúsculas ou um nome que não diferencia maiúsculas de minúsculas de uma variável de ambiente prefixado por um sinal de porcentagem (%).</span><span class="sxs-lookup"><span data-stu-id="33f43-111">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="33f43-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33f43-112">Requirements</span></span>



| <span data-ttu-id="33f43-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="33f43-113">Requirement</span></span> | <span data-ttu-id="33f43-114">Valor</span><span class="sxs-lookup"><span data-stu-id="33f43-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f43-115">Versão</span><span class="sxs-lookup"><span data-stu-id="33f43-115">Version</span></span><br/> | <span data-ttu-id="33f43-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="33f43-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="33f43-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="33f43-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="33f43-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="33f43-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="33f43-119">DLL</span><span class="sxs-lookup"><span data-stu-id="33f43-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="33f43-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33f43-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="33f43-121">IID</span><span class="sxs-lookup"><span data-stu-id="33f43-121">IID</span></span><br/>     | <span data-ttu-id="33f43-122">IID \_ IUIPreview é definido como 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="33f43-122">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




