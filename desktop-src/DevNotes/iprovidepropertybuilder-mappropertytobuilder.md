---
description: Verifica se um construtor deve ser associado a uma determinada propriedade.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'Método IProvidePropertyBuilder:: MapPropertyToBuilder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753062"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a><span data-ttu-id="d0ce3-103">Método IProvidePropertyBuilder:: MapPropertyToBuilder</span><span class="sxs-lookup"><span data-stu-id="d0ce3-103">IProvidePropertyBuilder::MapPropertyToBuilder method</span></span>

<span data-ttu-id="d0ce3-104">Verifica se um construtor deve ser associado a uma determinada propriedade.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-104">Checks whether a builder should be associated with a particular property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ce3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0ce3-105">Syntax</span></span>


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="d0ce3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0ce3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ce3-107">*DISPID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0ce3-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ce3-108">O DISPID da propriedade em questão.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-108">The DISPID of the property in question.</span></span>

</dd> <dt>

<span data-ttu-id="d0ce3-109">*pdwCtlBldType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d0ce3-109">*pdwCtlBldType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ce3-110">O Construtor a ser mapeado.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-110">The builder to be mapped.</span></span> <span data-ttu-id="d0ce3-111">Esse parâmetro pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="d0ce3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d0ce3-112">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="d0ce3-113">Significado</span><span class="sxs-lookup"><span data-stu-id="d0ce3-113">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <span data-ttu-id="d0ce3-114"><dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d0ce3-114"><dt>**CTLBLDTYPE\_FSTDPROPBUILDER**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="d0ce3-115">Invocar um Standard Builder do sistema (sem suporte no Visual Studio).</span><span class="sxs-lookup"><span data-stu-id="d0ce3-115">Invoke a standard system builder (not supported in Visual Studio).</span></span><br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <span data-ttu-id="d0ce3-116"><dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d0ce3-116"><dt>**CTLBLDTYPE\_FINTERNALBUILDER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="d0ce3-117">Invocar um construtor personalizado.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-117">Invoke a custom builder.</span></span><br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <span data-ttu-id="d0ce3-118"><dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d0ce3-118"><dt>**CTLBLDTYPE\_EDITSOBJDIRECTLY**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="d0ce3-119">O Construtor modifica o objeto.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-119">Builder modifies the object.</span></span> <span data-ttu-id="d0ce3-120">Esse comportamento é comum.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-120">This is common behavior.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="d0ce3-121">*pbstrGuidBldr* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d0ce3-121">*pbstrGuidBldr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ce3-122">O GUID que identifica o construtor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-122">The GUID that identifies the builder for this property.</span></span>

</dd> <dt>

<span data-ttu-id="d0ce3-123">*builderAvailable* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d0ce3-123">*builderAvailable* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ce3-124">Esse parâmetro será **true** se essa propriedade atualmente der suporte a um construtor.</span><span class="sxs-lookup"><span data-stu-id="d0ce3-124">This parameter is **TRUE** if this property currently supports a builder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ce3-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0ce3-125">Return value</span></span>

<span data-ttu-id="d0ce3-126">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0ce3-126">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ce3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0ce3-127">Requirements</span></span>



| <span data-ttu-id="d0ce3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ce3-128">Requirement</span></span> | <span data-ttu-id="d0ce3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d0ce3-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ce3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d0ce3-130">DLL</span></span><br/> | <dl> <span data-ttu-id="d0ce3-131"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0ce3-131"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ce3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0ce3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ce3-133">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="d0ce3-133">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




