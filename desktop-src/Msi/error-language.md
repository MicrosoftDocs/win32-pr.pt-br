---
description: A propriedade de linguagem somente leitura do objeto de erro retorna o LANGid do erro atual.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Propriedade Error. Language (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747980"
---
# <a name="errorlanguage-property"></a><span data-ttu-id="b445d-103">Propriedade Error. Language</span><span class="sxs-lookup"><span data-stu-id="b445d-103">Error.Language property</span></span>

<span data-ttu-id="b445d-104">A propriedade de **linguagem** somente leitura do objeto de [**erro**](error-object.md) retorna o **LangID** do erro atual.</span><span class="sxs-lookup"><span data-stu-id="b445d-104">The read-only **Language** property of the [**Error**](error-object.md) object returns the **LANGID** of the current error.</span></span>

<span data-ttu-id="b445d-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b445d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b445d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b445d-106">Syntax</span></span>


```JScript
propVal = Error.Language
```



## <a name="property-value"></a><span data-ttu-id="b445d-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b445d-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="b445d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b445d-108">Remarks</span></span>

<span data-ttu-id="b445d-109">O valor da propriedade **Language** é-1, a menos que o erro seja do tipo MsmErrorLanguageUnsupported ou msmErrorLanguageFailed.</span><span class="sxs-lookup"><span data-stu-id="b445d-109">The value of the **Language** property is -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed.</span></span> <span data-ttu-id="b445d-110">Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b445d-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="b445d-111">C++</span><span class="sxs-lookup"><span data-stu-id="b445d-111">C++</span></span>

<span data-ttu-id="b445d-112">Consulte [**a \_ função obter linguagem (objeto de erro)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span><span class="sxs-lookup"><span data-stu-id="b445d-112">See [**get\_Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span></span>

## <a name="requirements"></a><span data-ttu-id="b445d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b445d-113">Requirements</span></span>



| <span data-ttu-id="b445d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b445d-114">Requirement</span></span> | <span data-ttu-id="b445d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b445d-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b445d-116">Versão</span><span class="sxs-lookup"><span data-stu-id="b445d-116">Version</span></span><br/> | <span data-ttu-id="b445d-117">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b445d-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b445d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b445d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b445d-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="b445d-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b445d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b445d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="b445d-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b445d-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

