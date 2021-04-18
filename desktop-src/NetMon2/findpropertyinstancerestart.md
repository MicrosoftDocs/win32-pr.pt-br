---
description: Localiza a próxima instância da propriedade especificada pelo parâmetro hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Função FindPropertyInstanceRestart (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778708"
---
# <a name="findpropertyinstancerestart-function"></a><span data-ttu-id="a46e3-103">Função FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="a46e3-103">FindPropertyInstanceRestart function</span></span>

<span data-ttu-id="a46e3-104">A função **FindPropertyInstanceRestart** localiza a próxima instância da propriedade especificada pelo parâmetro *hProperty* .</span><span class="sxs-lookup"><span data-stu-id="a46e3-104">The **FindPropertyInstanceRestart** function finds the next instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a46e3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a46e3-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a><span data-ttu-id="a46e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a46e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a46e3-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a46e3-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a46e3-108">Um identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="a46e3-108">A handle to the frame.</span></span> <span data-ttu-id="a46e3-109">O identificador de quadro pode ser recuperado por uma chamada para a função [GetFrame](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="a46e3-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a46e3-110">*hProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a46e3-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a46e3-111">Um identificador para a propriedade a ser localizada.</span><span class="sxs-lookup"><span data-stu-id="a46e3-111">A handle to the property to find.</span></span> <span data-ttu-id="a46e3-112">O identificador de propriedade pode ser recuperado por uma chamada para a função [GetProperty](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a46e3-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a46e3-113">*lpRestartKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a46e3-113">*lpRestartKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a46e3-114">Um ponteiro para a instância de propriedade usado como o ponto de partida da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a46e3-114">A pointer to the property instance used as the starting point of the search.</span></span> <span data-ttu-id="a46e3-115">Se o parâmetro *lpRestartKey* for definido como **NULL**, a pesquisa começará no início do quadro ou no final do quadro, dependendo do valor do parâmetro *DirForward* .</span><span class="sxs-lookup"><span data-stu-id="a46e3-115">If the *lpRestartKey* parameter is set to **NULL**, the search begins at beginning of the frame, or the end of the frame, depending on the value of the *DirForward* parameter.</span></span>

<span data-ttu-id="a46e3-116">Se *lpRestartKey* apontar para **NULL**, a pesquisa começará no início do quadro se *DirForward* for **true** ou no final do quadro se o parâmetro for **false**.</span><span class="sxs-lookup"><span data-stu-id="a46e3-116">If *lpRestartKey* points to **NULL**, the search begins at the beginning of the frame if *DirForward* is **TRUE** or the at end of the frame if the parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a46e3-117">*DirForward* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a46e3-117">*DirForward* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a46e3-118">Um indicador da direção da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a46e3-118">An indicator of the search direction.</span></span> <span data-ttu-id="a46e3-119">Se o valor for **true**, a pesquisa será movida do local atual para o fim do quadro.</span><span class="sxs-lookup"><span data-stu-id="a46e3-119">If the value is **TRUE**, the search moves from the current location to the end of the frame.</span></span> <span data-ttu-id="a46e3-120">Se o valor for **false**, a pesquisa se moverá do local atual para o início do quadro.</span><span class="sxs-lookup"><span data-stu-id="a46e3-120">If the value is **FALSE**, the search moves from the current location to the beginning of the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a46e3-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a46e3-121">Return value</span></span>

<span data-ttu-id="a46e3-122">Se a função for bem-sucedida, o valor de retorno será o próximo **LPPROPERTYINST** válido.</span><span class="sxs-lookup"><span data-stu-id="a46e3-122">If the function is successful, the return value is the next valid **LPPROPERTYINST**.</span></span>

<span data-ttu-id="a46e3-123">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a46e3-123">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a46e3-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a46e3-124">Remarks</span></span>

<span data-ttu-id="a46e3-125">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **FindPropertyInstanceRestart** .</span><span class="sxs-lookup"><span data-stu-id="a46e3-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **FindPropertyInstanceRestart** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a46e3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a46e3-126">Requirements</span></span>



| <span data-ttu-id="a46e3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a46e3-127">Requirement</span></span> | <span data-ttu-id="a46e3-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a46e3-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a46e3-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a46e3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a46e3-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a46e3-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a46e3-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a46e3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a46e3-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a46e3-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a46e3-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a46e3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a46e3-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a46e3-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a46e3-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a46e3-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a46e3-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a46e3-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a46e3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a46e3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a46e3-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a46e3-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a46e3-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a46e3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a46e3-140">GetFrame</span><span class="sxs-lookup"><span data-stu-id="a46e3-140">GetFrame</span></span>](getframe.md)
</dt> <dt>

[<span data-ttu-id="a46e3-141">GetProperty</span><span class="sxs-lookup"><span data-stu-id="a46e3-141">GetProperty</span></span>](getproperty.md)
</dt> </dl>

 

 




