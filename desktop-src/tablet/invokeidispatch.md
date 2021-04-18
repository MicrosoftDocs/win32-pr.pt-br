---
description: Invoca a funcionalidade auxiliar para a interface IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: Função InvokeIDispatch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762326"
---
# <a name="invokeidispatch-function"></a><span data-ttu-id="ea54f-103">Função InvokeIDispatch</span><span class="sxs-lookup"><span data-stu-id="ea54f-103">InvokeIDispatch function</span></span>

<span data-ttu-id="ea54f-104">Invoca a funcionalidade auxiliar para a interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="ea54f-104">Invokes helper functionality for the IDispatch interface.</span></span>

<span data-ttu-id="ea54f-105">Esta função não se destina a ser usada pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea54f-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea54f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea54f-106">Syntax</span></span>


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a><span data-ttu-id="ea54f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea54f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea54f-108">*pDispatch*</span><span class="sxs-lookup"><span data-stu-id="ea54f-108">*pDispatch*</span></span> 
</dt> <dd>

<span data-ttu-id="ea54f-109">A instância da interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="ea54f-109">The instance of the IDispatch interface.</span></span>

</dd> <dt>

<span data-ttu-id="ea54f-110">*DISPID*</span><span class="sxs-lookup"><span data-stu-id="ea54f-110">*dispid*</span></span> 
</dt> <dd>

<span data-ttu-id="ea54f-111">O método, a propriedade ou o argumento a ser passado.</span><span class="sxs-lookup"><span data-stu-id="ea54f-111">The method, property, or argument to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="ea54f-112">*pDisp*</span><span class="sxs-lookup"><span data-stu-id="ea54f-112">*pDisp*</span></span> 
</dt> <dd>

<span data-ttu-id="ea54f-113">Os parâmetros a serem transmitidos.</span><span class="sxs-lookup"><span data-stu-id="ea54f-113">The parameters to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="ea54f-114">*pVarResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ea54f-114">*pVarResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea54f-115">Uma estrutura que recebe os valores recuperados.</span><span class="sxs-lookup"><span data-stu-id="ea54f-115">A structure that receives the retrieved values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea54f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea54f-116">Return value</span></span>

<span data-ttu-id="ea54f-117">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea54f-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ea54f-118">Se falhar, os códigos de retorno possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea54f-118">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="ea54f-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ea54f-119">Return code</span></span>                                                                                  | <span data-ttu-id="ea54f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea54f-120">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ea54f-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ea54f-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ea54f-122">O valor de *pDispatch* é inválido.</span><span class="sxs-lookup"><span data-stu-id="ea54f-122">The value for *pDispatch* is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ea54f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea54f-123">Requirements</span></span>



| <span data-ttu-id="ea54f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea54f-124">Requirement</span></span> | <span data-ttu-id="ea54f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ea54f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea54f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea54f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea54f-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ea54f-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ea54f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea54f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea54f-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ea54f-129">None supported</span></span><br/>                                                             |
| <span data-ttu-id="ea54f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea54f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea54f-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea54f-131"><dt>InkObj.dll</dt></span></span> </dl> |



 

 




