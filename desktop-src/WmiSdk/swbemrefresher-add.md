---
description: O método SWbemRefresher. add adiciona um novo objeto SWbemRefreshableItem à coleção no objeto SWbemRefresher. Objeto SWbemRefreshableItem para a coleção no objeto SWbemRefresher.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Método SWbemRefresher. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782507"
---
# <a name="swbemrefresheradd-method"></a><span data-ttu-id="7149b-103">Método SWbemRefresher. Add</span><span class="sxs-lookup"><span data-stu-id="7149b-103">SWbemRefresher.Add method</span></span>

<span data-ttu-id="7149b-104">O método **SWbemRefresher. Add** adiciona um novo objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) à coleção no objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="7149b-104">The **SWbemRefresher.Add** method adds a new [**SWbemRefreshableItem**](swbemrefreshableitem.md) object to the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="7149b-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7149b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7149b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7149b-106">Syntax</span></span>


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7149b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7149b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7149b-108">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="7149b-108">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="7149b-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7149b-109">Required.</span></span> <span data-ttu-id="7149b-110">Um objeto [**SWbemServices**](swbemservices.md) que representa uma conexão com o namespace no qual o objeto que está sendo adicionado ao atualizador reside.</span><span class="sxs-lookup"><span data-stu-id="7149b-110">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="7149b-111">*strInstancePath*</span><span class="sxs-lookup"><span data-stu-id="7149b-111">*strInstancePath*</span></span> 
</dt> <dd>

<span data-ttu-id="7149b-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="7149b-112">Required.</span></span> <span data-ttu-id="7149b-113">Cadeia de caracteres que contém o caminho relativo do objeto no namespace.</span><span class="sxs-lookup"><span data-stu-id="7149b-113">String that contains the relative path of the object in the namespace.</span></span> <span data-ttu-id="7149b-114">O caminho deve conter uma instância.</span><span class="sxs-lookup"><span data-stu-id="7149b-114">The path must contain an instance.</span></span> <span data-ttu-id="7149b-115">A propriedade [**index**](swbemrefreshableitem-index.md) do [**SWbemRefreshableItem**](swbemrefreshableitem.md) retornado representa o índice do objeto na coleção de atualizadores.</span><span class="sxs-lookup"><span data-stu-id="7149b-115">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="7149b-116">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="7149b-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7149b-117">Cadeia de caracteres que contém o caminho do objeto do objeto para o qual o método é executado.</span><span class="sxs-lookup"><span data-stu-id="7149b-117">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="7149b-118">*objWbemNamedvalueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="7149b-118">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7149b-119">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="7149b-119">Typically, this is undefined.</span></span> <span data-ttu-id="7149b-120">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7149b-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="7149b-121">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="7149b-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7149b-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7149b-122">Return value</span></span>

<span data-ttu-id="7149b-123">Se a chamada for bem-sucedida, um objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) que contém um único objeto atualizável será retornado.</span><span class="sxs-lookup"><span data-stu-id="7149b-123">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains a single refreshable object is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7149b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7149b-124">Requirements</span></span>



| <span data-ttu-id="7149b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7149b-125">Requirement</span></span> | <span data-ttu-id="7149b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7149b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7149b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7149b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7149b-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7149b-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7149b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7149b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7149b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7149b-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7149b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7149b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7149b-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7149b-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7149b-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7149b-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="7149b-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7149b-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7149b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7149b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7149b-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7149b-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7149b-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="7149b-137">CLSID</span></span><br/>                    | <span data-ttu-id="7149b-138">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="7149b-138">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="7149b-139">IID</span><span class="sxs-lookup"><span data-stu-id="7149b-139">IID</span></span><br/>                      | <span data-ttu-id="7149b-140">ISWbemRefresher de IID \_</span><span class="sxs-lookup"><span data-stu-id="7149b-140">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="7149b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="7149b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7149b-142">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="7149b-142">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




