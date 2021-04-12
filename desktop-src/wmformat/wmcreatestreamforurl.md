---
title: Função WMCreateStreamForURL
description: A função WMCreateStreamForURL é implementada pelo aplicativo para criar um objeto de IStream COM para uma determinada URL.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Formato de mídia do Windows da função WMCreateStreamForURL
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364901"
---
# <a name="wmcreatestreamforurl-function"></a><span data-ttu-id="295e6-104">Função WMCreateStreamForURL</span><span class="sxs-lookup"><span data-stu-id="295e6-104">WMCreateStreamForURL function</span></span>

<span data-ttu-id="295e6-105">A função **WMCreateStreamForURL** é implementada pelo aplicativo para criar um objeto de **IStream** com para uma determinada URL.</span><span class="sxs-lookup"><span data-stu-id="295e6-105">The **WMCreateStreamForURL** function is implemented by the application to create a COM **IStream** object for a given URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="295e6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="295e6-106">Syntax</span></span>


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a><span data-ttu-id="295e6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="295e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="295e6-108">*pwszURL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="295e6-108">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="295e6-109">Ponteiro para uma cadeia de caracteres largos que contém a URL.</span><span class="sxs-lookup"><span data-stu-id="295e6-109">Pointer to a wide-character string containing the URL.</span></span>

</dd> <dt>

<span data-ttu-id="295e6-110">*pfCorrectSource* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="295e6-110">*pfCorrectSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="295e6-111">Ponteiro para um sinalizador, true impedirá que o SDK tente outros plug-ins de origem para esta URL.</span><span class="sxs-lookup"><span data-stu-id="295e6-111">Pointer to a flag, true will prevent the SDK from trying other source plug-ins for this URL.</span></span>

</dd> <dt>

<span data-ttu-id="295e6-112">*PPStream* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="295e6-112">*ppStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="295e6-113">Ponteiro para um ponteiro para o objeto **IStream** criado pelo método.</span><span class="sxs-lookup"><span data-stu-id="295e6-113">Pointer to a pointer to the **IStream** object created by the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="295e6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="295e6-114">Return value</span></span>

<span data-ttu-id="295e6-115">Se a função for bem sucedido, ela deverá retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="295e6-115">If the function succeeds, it must return S\_OK.</span></span> <span data-ttu-id="295e6-116">Se falhar, ele deve retornar um código de erro **HRESULT** apropriado e \* *PPStream* deve ser definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="295e6-116">If it fails, it must return an appropriate **HRESULT** error code, and \**ppStream* should be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="295e6-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="295e6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="295e6-118">**Plug-ins de origem**</span><span class="sxs-lookup"><span data-stu-id="295e6-118">**Source Plug-ins**</span></span>](source-plug-ins.md)
</dt> </dl>

 

 




