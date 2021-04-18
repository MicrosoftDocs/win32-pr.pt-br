---
description: Função de proxy para o método GetSpecVersion.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: Função IWICComponentInfo_GetSpecVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765020"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a><span data-ttu-id="9fadd-103">\_Função de \_ proxy IWICComponentInfo GetSpecVersion</span><span class="sxs-lookup"><span data-stu-id="9fadd-103">IWICComponentInfo\_GetSpecVersion\_Proxy function</span></span>

<span data-ttu-id="9fadd-104">Função de proxy para o método [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) .</span><span class="sxs-lookup"><span data-stu-id="9fadd-104">Proxy function for the [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fadd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fadd-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="9fadd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fadd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fadd-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="9fadd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fadd-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9fadd-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="9fadd-109">Ponteiro para este objeto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="9fadd-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="9fadd-110">*cchSpecVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fadd-110">*cchSpecVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fadd-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9fadd-111">Type: **UINT**</span></span>

<span data-ttu-id="9fadd-112">O tamanho do buffer *wzSpecVersion* .</span><span class="sxs-lookup"><span data-stu-id="9fadd-112">The size of the *wzSpecVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9fadd-113">*wzSpecVersion* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9fadd-113">*wzSpecVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fadd-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9fadd-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="9fadd-115">Quando esse método retorna, contém uma cadeia de caracteres invarient de cultura da versão de especificação do componente.</span><span class="sxs-lookup"><span data-stu-id="9fadd-115">When this method returns, contain a culture invarient string of the component's specification version.</span></span> <span data-ttu-id="9fadd-116">O formulário de versão é NN. NN. NN. NN.</span><span class="sxs-lookup"><span data-stu-id="9fadd-116">The version form is NN.NN.NN.NN.</span></span>

</dd> <dt>

<span data-ttu-id="9fadd-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9fadd-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fadd-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="9fadd-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="9fadd-119">Um ponteiro que recebe o comprimento real da versão de especificação do componente.</span><span class="sxs-lookup"><span data-stu-id="9fadd-119">A pointer that receives the actual length of the component's specification version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fadd-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9fadd-120">Return value</span></span>

<span data-ttu-id="9fadd-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9fadd-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9fadd-122">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9fadd-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9fadd-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9fadd-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fadd-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fadd-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9fadd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fadd-125">Requirements</span></span>



| <span data-ttu-id="9fadd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fadd-126">Requirement</span></span> | <span data-ttu-id="9fadd-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9fadd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fadd-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fadd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9fadd-129">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fadd-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9fadd-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fadd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9fadd-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fadd-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9fadd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9fadd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fadd-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fadd-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




