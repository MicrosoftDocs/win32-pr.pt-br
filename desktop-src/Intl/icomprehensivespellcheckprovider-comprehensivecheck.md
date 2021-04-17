---
description: 'Verifique a ortografia do texto do provedor de maneira mais completa do que ISpellCheckProvider:: check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'Método IComprehensiveSpellCheckProvider:: ComprehensiveCheck'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782926"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a><span data-ttu-id="8243d-103">Método IComprehensiveSpellCheckProvider:: ComprehensiveCheck</span><span class="sxs-lookup"><span data-stu-id="8243d-103">IComprehensiveSpellCheckProvider::ComprehensiveCheck method</span></span>

<span data-ttu-id="8243d-104">Verifique a ortografia do texto do provedor de maneira mais completa do que [**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="8243d-104">Spell-check the provider text in a more thorough manner than [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="syntax"></a><span data-ttu-id="8243d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8243d-105">Syntax</span></span>


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a><span data-ttu-id="8243d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8243d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8243d-107">*texto* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="8243d-107">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8243d-108">O texto a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="8243d-108">The text to check.</span></span>

</dd> <dt>

<span data-ttu-id="8243d-109">*resultado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8243d-109">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8243d-110">O resultado da verificação desse texto, como uma enumeração de erros de ortografia ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), se houver.</span><span class="sxs-lookup"><span data-stu-id="8243d-110">The result of checking this text, as an enumeration of spelling errors ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8243d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8243d-111">Return value</span></span>

<span data-ttu-id="8243d-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8243d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8243d-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8243d-113">Return value</span></span>                                                                             | <span data-ttu-id="8243d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8243d-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8243d-115"><dt>S \_ OK</dt></span><span class="sxs-lookup"><span data-stu-id="8243d-115"><dt>S\_OK</dt></span></span> </dl>         | <span data-ttu-id="8243d-116">Bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8243d-116">Successful.</span></span><br/>                |
| <dl> <span data-ttu-id="8243d-117"><dt>E \_ INVALIDARG</dt></span><span class="sxs-lookup"><span data-stu-id="8243d-117"><dt>E\_INVALIDARG</dt></span></span> </dl> | <span data-ttu-id="8243d-118">o *texto* é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="8243d-118">*text* is an empty string.</span></span><br/> |
| <dl> <span data-ttu-id="8243d-119"><dt>\_ponteiro E</dt></span><span class="sxs-lookup"><span data-stu-id="8243d-119"><dt>E\_POINTER</dt></span></span> </dl>    | <span data-ttu-id="8243d-120">o *texto* é um ponteiro nulo.</span><span class="sxs-lookup"><span data-stu-id="8243d-120">*text* is a null pointer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="8243d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="8243d-121">Remarks</span></span>

<span data-ttu-id="8243d-122">Essa interface não precisa ser implementada por um provedor de verificação ortográfica.</span><span class="sxs-lookup"><span data-stu-id="8243d-122">This interface isn't required to be implemented by a spell check provider.</span></span> <span data-ttu-id="8243d-123">Mas se o provedor oferecer suporte a dois "modos" de verificação ortográfica (uma mais rápida e mais lenta, mas mais completa), ele deverá implementar essa interface no mesmo objeto que implementa o [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) para dar suporte ao modo de verificação mais completo.</span><span class="sxs-lookup"><span data-stu-id="8243d-123">But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) to support the more thorough checking mode.</span></span> <span data-ttu-id="8243d-124">Quando um cliente chama [**ISpellChecker:: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), a funcionalidade de verificação ortográfica fará a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do provedor para [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)e chamará **IComprehensiveSpellCheckProvider. ComprehensiveCheck** se a interface tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="8243d-124">When a client calls [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), the spell checking functionality will [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) the provider for [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider), and call **IComprehensiveSpellCheckProvider.ComprehensiveCheck** if the interface is supported.</span></span> <span data-ttu-id="8243d-125">Se a interface não tiver suporte, ela será revertida silenciosamente para [**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="8243d-125">If the interface isn't supported, it will silently fall back to [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="see-also"></a><span data-ttu-id="8243d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8243d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8243d-127">**IComprehensiveSpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="8243d-127">**IComprehensiveSpellCheckProvider**</span></span>](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[<span data-ttu-id="8243d-128">**IEnumSpellingError**</span><span class="sxs-lookup"><span data-stu-id="8243d-128">**IEnumSpellingError**</span></span>](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[<span data-ttu-id="8243d-129">**ISpellChecker::ComprehensiveCheck**</span><span class="sxs-lookup"><span data-stu-id="8243d-129">**ISpellChecker::ComprehensiveCheck**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[<span data-ttu-id="8243d-130">**ISpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="8243d-130">**ISpellCheckProvider**</span></span>](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[<span data-ttu-id="8243d-131">**ISpellCheckProvider:: verificar**</span><span class="sxs-lookup"><span data-stu-id="8243d-131">**ISpellCheckProvider::Check**</span></span>](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
