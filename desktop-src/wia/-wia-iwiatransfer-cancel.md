---
description: Cancela a operação de transferência atual.
ms.assetid: 42c6b2c3-7b6a-45d2-a7ce-844e95fe277b
title: 'Método IWiaTransfer:: Cancel (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Cancel
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 4764e922498a3c33278555cae37d09c1822959dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501791"
---
# <a name="iwiatransfercancel-method"></a><span data-ttu-id="9cd8f-103">Método IWiaTransfer:: Cancel</span><span class="sxs-lookup"><span data-stu-id="9cd8f-103">IWiaTransfer::Cancel method</span></span>

<span data-ttu-id="9cd8f-104">Cancela a operação de transferência atual.</span><span class="sxs-lookup"><span data-stu-id="9cd8f-104">Cancels the current transfer operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cd8f-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="9cd8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cd8f-106">Parameters</span></span>

<span data-ttu-id="9cd8f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9cd8f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9cd8f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cd8f-108">Return value</span></span>

<span data-ttu-id="9cd8f-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9cd8f-109">Type: **HRESULT**</span></span>

<span data-ttu-id="9cd8f-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9cd8f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9cd8f-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9cd8f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd8f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cd8f-112">Requirements</span></span>



| <span data-ttu-id="9cd8f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd8f-113">Requirement</span></span> | <span data-ttu-id="9cd8f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9cd8f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd8f-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cd8f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd8f-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cd8f-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9cd8f-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cd8f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd8f-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9cd8f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9cd8f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cd8f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cd8f-120"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cd8f-120"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="9cd8f-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="9cd8f-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9cd8f-122"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9cd8f-122"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="9cd8f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cd8f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9cd8f-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cd8f-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




