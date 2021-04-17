---
description: Recupera o número de versão do sistema de eventos.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'Método IEventSystem2:: GetVersion'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457162"
---
# <a name="ieventsystem2getversion-method"></a><span data-ttu-id="4af97-103">Método IEventSystem2:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="4af97-103">IEventSystem2::GetVersion method</span></span>

<span data-ttu-id="4af97-104">Recupera o número de versão do sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="4af97-104">Retrieves the version number of the event system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4af97-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4af97-105">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a><span data-ttu-id="4af97-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4af97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4af97-107">*pnVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4af97-107">*pnVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4af97-108">O número de versão do sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="4af97-108">The version number of the event system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4af97-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4af97-109">Return value</span></span>

<span data-ttu-id="4af97-110">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4af97-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="4af97-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4af97-111">Requirements</span></span>



| <span data-ttu-id="4af97-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4af97-112">Requirement</span></span> | <span data-ttu-id="4af97-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4af97-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4af97-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4af97-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4af97-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4af97-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4af97-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4af97-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4af97-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4af97-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4af97-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4af97-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af97-119">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="4af97-119">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




