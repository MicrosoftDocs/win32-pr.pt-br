---
description: Função de proxy para o método getauthor.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: Função IWICComponentInfo_GetAuthor_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f181a567ae4089870d324c7a7e0d67a34b965b5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773036"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a><span data-ttu-id="c3434-103">\_Função de proxy IWICComponentInfo Getauthor \_</span><span class="sxs-lookup"><span data-stu-id="c3434-103">IWICComponentInfo\_GetAuthor\_Proxy function</span></span>

<span data-ttu-id="c3434-104">Função de proxy para o método [**getauthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) .</span><span class="sxs-lookup"><span data-stu-id="c3434-104">Proxy function for the [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3434-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3434-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="c3434-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3434-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3434-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="c3434-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3434-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="c3434-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="c3434-109">Ponteiro para este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="c3434-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="c3434-110">*cchAuthor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3434-110">*cchAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3434-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c3434-111">Type: **UINT**</span></span>

<span data-ttu-id="c3434-112">O tamanho do buffer *wzAuthor* .</span><span class="sxs-lookup"><span data-stu-id="c3434-112">The size of the *wzAuthor* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c3434-113">*wzAuthor* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c3434-113">*wzAuthor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3434-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="c3434-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="c3434-115">Um ponteiro que recebe o nome do autor do componente.</span><span class="sxs-lookup"><span data-stu-id="c3434-115">A pointer that receives the name of the component's author.</span></span>

<span data-ttu-id="c3434-116">A cadeia de caracteres retornada é específica da localidade, 1033 por padrão.</span><span class="sxs-lookup"><span data-stu-id="c3434-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="c3434-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c3434-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3434-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="c3434-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="c3434-119">Um ponteiro que recebe o comprimento real do nome de autores do componente.</span><span class="sxs-lookup"><span data-stu-id="c3434-119">A pointer that receives the actual length of the component's authors name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3434-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3434-120">Return value</span></span>

<span data-ttu-id="c3434-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c3434-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c3434-122">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c3434-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c3434-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3434-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3434-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3434-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c3434-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3434-125">Requirements</span></span>



| <span data-ttu-id="c3434-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3434-126">Requirement</span></span> | <span data-ttu-id="c3434-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c3434-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3434-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3434-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c3434-129">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3434-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c3434-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3434-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c3434-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c3434-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c3434-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c3434-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3434-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3434-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




