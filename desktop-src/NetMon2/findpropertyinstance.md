---
description: A função FindPropertyInstance localiza a primeira instância da propriedade especificada pelo parâmetro hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Função FindPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770367"
---
# <a name="findpropertyinstance-function"></a><span data-ttu-id="3df09-103">Função FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="3df09-103">FindPropertyInstance function</span></span>

<span data-ttu-id="3df09-104">A função **FindPropertyInstance** localiza a primeira instância da propriedade especificada pelo parâmetro *hProperty* .</span><span class="sxs-lookup"><span data-stu-id="3df09-104">The **FindPropertyInstance** function finds the first instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df09-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3df09-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="3df09-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3df09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df09-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3df09-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df09-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="3df09-108">Handle to the frame.</span></span> <span data-ttu-id="3df09-109">O identificador de quadro pode ser recuperado por uma chamada para a função [GetFrame](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="3df09-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3df09-110">*hProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3df09-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df09-111">Identificador para a propriedade que você deseja localizar.</span><span class="sxs-lookup"><span data-stu-id="3df09-111">Handle to the property you want to find.</span></span> <span data-ttu-id="3df09-112">O identificador de propriedade pode ser recuperado por uma chamada para a função [GetProperty](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="3df09-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df09-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3df09-113">Return value</span></span>

<span data-ttu-id="3df09-114">Se a função for bem-sucedida (ou seja, se a propriedade for encontrada), o valor de retorno será um ponteiro para a primeira instância da propriedade.</span><span class="sxs-lookup"><span data-stu-id="3df09-114">If the function is successful (that is, if the property is found), the return value is a pointer to the first instance of the property.</span></span>

<span data-ttu-id="3df09-115">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3df09-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3df09-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3df09-116">Remarks</span></span>

<span data-ttu-id="3df09-117">Para recuperar a próxima instância da propriedade, chame [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span><span class="sxs-lookup"><span data-stu-id="3df09-117">To retrieve the next instance of the property, call [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span></span>

<span data-ttu-id="3df09-118">Os [*especialistas*](e.md) e os [*analisadores*](p.md)podem chamar a função **FindPropertyInstance** .</span><span class="sxs-lookup"><span data-stu-id="3df09-118">[*Experts*](e.md) and [*parsers*](p.md)can call the **FindPropertyInstance** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3df09-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3df09-119">Requirements</span></span>



| <span data-ttu-id="3df09-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3df09-120">Requirement</span></span> | <span data-ttu-id="3df09-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3df09-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3df09-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3df09-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3df09-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3df09-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3df09-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3df09-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3df09-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3df09-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3df09-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3df09-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df09-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3df09-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3df09-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3df09-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="3df09-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3df09-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3df09-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3df09-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df09-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df09-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df09-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3df09-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df09-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="3df09-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




