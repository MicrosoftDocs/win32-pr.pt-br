---
description: Função de proxy para o método Commit.
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: Função IWICBitmapEncoder_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0cd3cfbe5e1c80d82cd90303d26f2da33cf467d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010459"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="6f3d5-103">Função de proxy de \_ confirmação IWICBitmapEncoder \_</span><span class="sxs-lookup"><span data-stu-id="6f3d5-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="6f3d5-104">Função de proxy para o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) .</span><span class="sxs-lookup"><span data-stu-id="6f3d5-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f3d5-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="6f3d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f3d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f3d5-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="6f3d5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3d5-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="6f3d5-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="6f3d5-109">Ponteiro para este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="6f3d5-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f3d5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f3d5-110">Return value</span></span>

<span data-ttu-id="6f3d5-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f3d5-111">Type: **HRESULT**</span></span>

<span data-ttu-id="6f3d5-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f3d5-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f3d5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f3d5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f3d5-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6f3d5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f3d5-115">Requirements</span></span>



| <span data-ttu-id="6f3d5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f3d5-116">Requirement</span></span> | <span data-ttu-id="6f3d5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6f3d5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3d5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f3d5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3d5-119">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f3d5-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6f3d5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f3d5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3d5-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f3d5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6f3d5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6f3d5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f3d5-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f3d5-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




