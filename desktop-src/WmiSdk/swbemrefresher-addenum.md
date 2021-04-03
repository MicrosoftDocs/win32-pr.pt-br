---
description: Adiciona um novo enumerador ao objeto SWbemRefresher. Esse enumerador é para todas as instâncias da classe que é especificada no parâmetro strClass.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Método SWbemRefresher. AddEnum (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663789"
---
# <a name="swbemrefresheraddenum-method"></a><span data-ttu-id="1640f-104">Método SWbemRefresher. AddEnum</span><span class="sxs-lookup"><span data-stu-id="1640f-104">SWbemRefresher.AddEnum method</span></span>

<span data-ttu-id="1640f-105">O método **SWbemRefresher. AddEnum** adiciona um novo enumerador ao objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="1640f-105">The **SWbemRefresher.AddEnum** method adds a new enumerator to the [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="1640f-106">Esse enumerador é para todas as instâncias da classe que é especificada no parâmetro *strClass* .</span><span class="sxs-lookup"><span data-stu-id="1640f-106">This enumerator is for all the instances of the class that is specified in the *strClass* parameter.</span></span>

<span data-ttu-id="1640f-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1640f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1640f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1640f-108">Syntax</span></span>


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1640f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1640f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1640f-110">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="1640f-110">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="1640f-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1640f-111">Required.</span></span> <span data-ttu-id="1640f-112">Um objeto [**SWbemServices**](swbemservices.md) que representa uma conexão com o namespace no qual o objeto que está sendo adicionado ao atualizador reside.</span><span class="sxs-lookup"><span data-stu-id="1640f-112">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="1640f-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="1640f-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="1640f-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1640f-114">Required.</span></span> <span data-ttu-id="1640f-115">Cadeia de caracteres que contém a classe que está sendo adicionada ao atualizador.</span><span class="sxs-lookup"><span data-stu-id="1640f-115">String that contains the class that is being added to the refresher.</span></span> <span data-ttu-id="1640f-116">Essa classe é usada como um enumerador das instâncias da classe.</span><span class="sxs-lookup"><span data-stu-id="1640f-116">This class is used as an enumerator of the instances of the class.</span></span> <span data-ttu-id="1640f-117">A propriedade [**index**](swbemrefreshableitem-index.md) do [**SWbemRefreshableItem**](swbemrefreshableitem.md) retornado representa o índice do enumerador na coleção de atualizadores.</span><span class="sxs-lookup"><span data-stu-id="1640f-117">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the enumerator in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="1640f-118">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="1640f-118">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1640f-119">Cadeia de caracteres que contém o caminho do objeto do objeto para o qual o método é executado.</span><span class="sxs-lookup"><span data-stu-id="1640f-119">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="1640f-120">*objWbemNamedvalueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="1640f-120">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1640f-121">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="1640f-121">Typically, this is undefined.</span></span> <span data-ttu-id="1640f-122">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1640f-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="1640f-123">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="1640f-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1640f-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1640f-124">Return value</span></span>

<span data-ttu-id="1640f-125">Se a chamada for bem-sucedida, um objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) que contém um enumerador para todas as instâncias da classe especificada será retornado.</span><span class="sxs-lookup"><span data-stu-id="1640f-125">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains an enumerator for all the instances for the specified class is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="1640f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1640f-126">Requirements</span></span>



| <span data-ttu-id="1640f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1640f-127">Requirement</span></span> | <span data-ttu-id="1640f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1640f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1640f-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1640f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1640f-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1640f-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1640f-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1640f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1640f-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1640f-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1640f-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1640f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1640f-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1640f-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1640f-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1640f-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="1640f-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1640f-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1640f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1640f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1640f-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1640f-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1640f-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="1640f-139">CLSID</span></span><br/>                    | <span data-ttu-id="1640f-140">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="1640f-140">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="1640f-141">IID</span><span class="sxs-lookup"><span data-stu-id="1640f-141">IID</span></span><br/>                      | <span data-ttu-id="1640f-142">ISWbemRefresher de IID \_</span><span class="sxs-lookup"><span data-stu-id="1640f-142">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="1640f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="1640f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1640f-144">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="1640f-144">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




