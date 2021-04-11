---
description: 'Função de proxy do Windows Imaging Component (WIC) para IEnumString:: Next.'
ms.assetid: a3f6a32b-3043-4bea-a70b-0b4507b4e3a1
title: Função IEnumString_Next_WIC_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Next_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ae3e25b355268fe63025692bf116b60b45122e76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010461"
---
# <a name="ienumstring_next_wic_proxy-function"></a><span data-ttu-id="a8abd-103">IEnumString \_ próxima \_ função de proxy do WIC \_</span><span class="sxs-lookup"><span data-stu-id="a8abd-103">IEnumString\_Next\_WIC\_Proxy function</span></span>

<span data-ttu-id="a8abd-104">Função de proxy do Windows Imaging Component (WIC) para IEnumString:: Next.</span><span class="sxs-lookup"><span data-stu-id="a8abd-104">Windows Imaging Component (WIC) proxy function for IEnumString::Next.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8abd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8abd-105">Syntax</span></span>


```C++
HRESULT IEnumString_Next_WIC_Proxy(
  _In_ IEnumString *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="a8abd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8abd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8abd-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="a8abd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8abd-108">Tipo: \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="a8abd-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="a8abd-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="a8abd-109">PARAMDESC</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8abd-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8abd-110">Return value</span></span>

<span data-ttu-id="a8abd-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a8abd-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a8abd-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a8abd-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8abd-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8abd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8abd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8abd-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a8abd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8abd-115">Requirements</span></span>



| <span data-ttu-id="a8abd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8abd-116">Requirement</span></span> | <span data-ttu-id="a8abd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a8abd-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8abd-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8abd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8abd-119">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8abd-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a8abd-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8abd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8abd-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8abd-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a8abd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a8abd-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8abd-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8abd-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




