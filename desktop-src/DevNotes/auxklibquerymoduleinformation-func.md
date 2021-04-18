---
description: Recupera informações sobre o conjunto de módulos carregado atualmente para o sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Função AuxKlibQueryModuleInformation (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771687"
---
# <a name="auxklibquerymoduleinformation-function"></a><span data-ttu-id="de1a5-103">Função AuxKlibQueryModuleInformation</span><span class="sxs-lookup"><span data-stu-id="de1a5-103">AuxKlibQueryModuleInformation function</span></span>

<span data-ttu-id="de1a5-104">Recupera informações sobre o conjunto de módulos carregado atualmente para o sistema.</span><span class="sxs-lookup"><span data-stu-id="de1a5-104">Retrieves information about the currently loaded set of modules for the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="de1a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de1a5-105">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a><span data-ttu-id="de1a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de1a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de1a5-107">*BufferSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="de1a5-107">*BufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de1a5-108">Na entrada, o tamanho do buffer *QueryInfo* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="de1a5-108">On input, the size of the *QueryInfo* buffer, in bytes.</span></span> <span data-ttu-id="de1a5-109">Na saída, recebe o tamanho real necessário.</span><span class="sxs-lookup"><span data-stu-id="de1a5-109">On output, receives the actual required size.</span></span> <span data-ttu-id="de1a5-110">Como a lista de módulos do sistema pode ser alterada entre as chamadas, esse valor também pode ser alterado entre as chamadas.</span><span class="sxs-lookup"><span data-stu-id="de1a5-110">Because the system module list can change between calls, this value can also change between calls.</span></span>

</dd> <dt>

<span data-ttu-id="de1a5-111">*Elementos de* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="de1a5-111">*ElementSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de1a5-112">O tamanho, em bytes, de um elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="de1a5-112">The size, in bytes, of an array element.</span></span> <span data-ttu-id="de1a5-113">Esse tamanho determina o formato da saída.</span><span class="sxs-lookup"><span data-stu-id="de1a5-113">This size determines the format of the output.</span></span>

</dd> <dt>

<span data-ttu-id="de1a5-114">*QueryInfo* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="de1a5-114">*QueryInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="de1a5-115">Um ponteiro para um buffer que recebe as informações do módulo.</span><span class="sxs-lookup"><span data-stu-id="de1a5-115">A pointer to a buffer that receives the module information.</span></span> <span data-ttu-id="de1a5-116">Essas informações são retornadas em uma matriz cujos elementos são uma das seguintes estruturas: [**informações \_ \_ básicas do \_ módulo aux**](aux-module-basic-info-struct.md) ou [**\_ \_ \_ informações estendidas do módulo aux**](aux-module-extended-info-struct.md).</span><span class="sxs-lookup"><span data-stu-id="de1a5-116">This information is returned in an array whose elements are one of the following structures: [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) or [**AUX\_MODULE\_EXTENDED\_INFO**](aux-module-extended-info-struct.md).</span></span> <span data-ttu-id="de1a5-117">A estrutura específica usada depende do tamanho do elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="de1a5-117">The specific structure used depends on the specified element size.</span></span>

<span data-ttu-id="de1a5-118">Se esse parâmetro for **nulo**, a função retornará o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="de1a5-118">If this parameter is **NULL**, the function returns the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de1a5-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de1a5-119">Return value</span></span>

<span data-ttu-id="de1a5-120">Se a função for bem-sucedida, o valor de retorno será \_ êxito no status.</span><span class="sxs-lookup"><span data-stu-id="de1a5-120">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="de1a5-121">Se a função falhar, o valor de retorno poderá ser um dos códigos de status definidos em Ntstatus. h, que está disponível no WDK.</span><span class="sxs-lookup"><span data-stu-id="de1a5-121">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="de1a5-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="de1a5-122">Remarks</span></span>

<span data-ttu-id="de1a5-123">Você deve chamar a função [**AuxKlibInitialize**](auxklibinitialize-func.md) antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="de1a5-123">You must call the [**AuxKlibInitialize**](auxklibinitialize-func.md) function before calling this function.</span></span>

<span data-ttu-id="de1a5-124">A biblioteca de objetos que implementa essa API pode ser baixada [aqui](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="de1a5-124">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="de1a5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de1a5-125">Requirements</span></span>



| <span data-ttu-id="de1a5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de1a5-126">Requirement</span></span> | <span data-ttu-id="de1a5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="de1a5-127">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de1a5-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="de1a5-128">Redistributable</span></span><br/> | <span data-ttu-id="de1a5-129">Biblioteca de API auxiliar do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="de1a5-129">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="de1a5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de1a5-130">Header</span></span><br/>          | <dl> <span data-ttu-id="de1a5-131"><dt>\_Klib aux. h</dt></span><span class="sxs-lookup"><span data-stu-id="de1a5-131"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="de1a5-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de1a5-132">Library</span></span><br/>         | <dl> <span data-ttu-id="de1a5-133"><dt>\_Klib. lib do aux</dt></span><span class="sxs-lookup"><span data-stu-id="de1a5-133"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de1a5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="de1a5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1a5-135">**AuxKlibInitialize**</span><span class="sxs-lookup"><span data-stu-id="de1a5-135">**AuxKlibInitialize**</span></span>](auxklibinitialize-func.md)
</dt> <dt>

[<span data-ttu-id="de1a5-136">**\_ \_ informações básicas do módulo aux \_**</span><span class="sxs-lookup"><span data-stu-id="de1a5-136">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> <dt>

[<span data-ttu-id="de1a5-137">**\_ \_ informações estendidas do módulo aux \_**</span><span class="sxs-lookup"><span data-stu-id="de1a5-137">**AUX\_MODULE\_EXTENDED\_INFO**</span></span>](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




