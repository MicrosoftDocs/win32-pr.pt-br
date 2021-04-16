---
title: Propriedade do servidor DevicePair (Asptlb. h)
description: Obtém o servidor para o par de dispositivo básico ativo.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- API de streaming de mídia de propriedade de servidor
- API de streaming de mídia de propriedade de servidor, interface DevicePair
- API de streaming de mídia da interface DevicePair, Propriedade do servidor
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768261"
---
# <a name="devicepairserver-property"></a><span data-ttu-id="080c8-106">Propriedade DevicePair:: Server</span><span class="sxs-lookup"><span data-stu-id="080c8-106">DevicePair::Server property</span></span>

<span data-ttu-id="080c8-107">Obtém o servidor para o par de dispositivo básico ativo.</span><span class="sxs-lookup"><span data-stu-id="080c8-107">Gets the server for the active basic device pair.</span></span>

<span data-ttu-id="080c8-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="080c8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="080c8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="080c8-109">Syntax</span></span>


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a><span data-ttu-id="080c8-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="080c8-110">Property value</span></span>

<span data-ttu-id="080c8-111">Recebe um objeto [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que representa o dispositivo de servidor.</span><span class="sxs-lookup"><span data-stu-id="080c8-111">Receives a [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) object that represents the server device.</span></span>

## <a name="requirements"></a><span data-ttu-id="080c8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="080c8-112">Requirements</span></span>



| <span data-ttu-id="080c8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="080c8-113">Requirement</span></span> | <span data-ttu-id="080c8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="080c8-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="080c8-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="080c8-115">Header</span></span><br/> | <dl> <span data-ttu-id="080c8-116"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="080c8-116"><dt>Asptlb.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="080c8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="080c8-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="080c8-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="080c8-118">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span></span>
</dt> </dl>

 

