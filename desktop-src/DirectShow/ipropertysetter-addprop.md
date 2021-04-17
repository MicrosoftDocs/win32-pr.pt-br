---
description: O método addprop adiciona uma propriedade ao setter da propriedade, com uma matriz de pares time-Value que definem o valor da propriedade em um intervalo de tempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'Método IPropertySetter:: addprop (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759535"
---
# <a name="ipropertysetteraddprop-method"></a><span data-ttu-id="6c165-103">Método IPropertySetter:: addprop</span><span class="sxs-lookup"><span data-stu-id="6c165-103">IPropertySetter::AddProp method</span></span>

> [!Note]  
> <span data-ttu-id="6c165-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6c165-104">\[Deprecated.</span></span> <span data-ttu-id="6c165-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6c165-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6c165-106">O `AddProp` método adiciona uma propriedade ao setter da propriedade, com uma matriz de pares time-Value que definem o valor da propriedade em um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="6c165-106">The `AddProp` method adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c165-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c165-107">Syntax</span></span>


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="6c165-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c165-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c165-109">*Parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c165-109">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c165-110">[**Dexter \_**](dexter-param.md) A estrutura do parâmetro que especifica a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6c165-110">[**DEXTER\_PARAM**](dexter-param.md) structure that specifies the property.</span></span> <span data-ttu-id="6c165-111">O membro **nValores** da estrutura deve ser igual ao tamanho da matriz fornecida no parâmetro *paValue* .</span><span class="sxs-lookup"><span data-stu-id="6c165-111">The **nValues** member of the structure must equal the size of the array given in the *paValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6c165-112">*paValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c165-112">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c165-113">Ponteiro para uma matriz de estruturas de [**\_ valor Dexter**](dexter-value.md) que contêm pares de tempo-valor.</span><span class="sxs-lookup"><span data-stu-id="6c165-113">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures that contain time-value pairs.</span></span> <span data-ttu-id="6c165-114">A matriz deve estar em ordem de tempo crescente.</span><span class="sxs-lookup"><span data-stu-id="6c165-114">The array must be in ascending time order.</span></span> <span data-ttu-id="6c165-115">Os tempos são relativos à hora de início do efeito ou da transição.</span><span class="sxs-lookup"><span data-stu-id="6c165-115">The times are relative to the starting time of the effect or transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c165-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c165-116">Return value</span></span>

<span data-ttu-id="6c165-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6c165-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c165-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c165-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c165-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c165-119">Remarks</span></span>

<span data-ttu-id="6c165-120">A primeira estrutura de [**\_ valor de Dexter**](dexter-value.md) deve especificar um tempo de referência de zero e um sinalizador de interpolação (**DwInterp**) do **\_ salto DEXTERF** ou o método retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="6c165-120">The first [**DEXTER\_VALUE**](dexter-value.md) structure must specify a reference time of zero and an interpolation flag (**dwInterp**) of **DEXTERF\_JUMP**, or the method returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="6c165-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6c165-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6c165-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6c165-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6c165-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6c165-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c165-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c165-124">Requirements</span></span>



| <span data-ttu-id="6c165-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c165-125">Requirement</span></span> | <span data-ttu-id="6c165-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6c165-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c165-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c165-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6c165-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c165-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6c165-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c165-129">Library</span></span><br/> | <dl> <span data-ttu-id="6c165-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c165-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c165-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c165-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c165-132">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="6c165-132">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="6c165-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="6c165-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




