---
description: Recupera uma matriz que contém os identificadores de propriedade de pacote para o traço especificado.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'Método IContextNode:: GetStrokePacketDescriptionById (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760987"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a><span data-ttu-id="4c67f-103">Método IContextNode:: GetStrokePacketDescriptionById</span><span class="sxs-lookup"><span data-stu-id="4c67f-103">IContextNode::GetStrokePacketDescriptionById method</span></span>

<span data-ttu-id="4c67f-104">Recupera uma matriz que contém os identificadores de propriedade de pacote para o traço especificado.</span><span class="sxs-lookup"><span data-stu-id="4c67f-104">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c67f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c67f-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a><span data-ttu-id="4c67f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c67f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c67f-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4c67f-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c67f-108">O identificador para o traço.</span><span class="sxs-lookup"><span data-stu-id="4c67f-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="4c67f-109">*pulStrokePacketDescriptionCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4c67f-109">*pulStrokePacketDescriptionCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c67f-110">O número de propriedades do pacote em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="4c67f-110">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="4c67f-111">*ppStrokePacketDescriptionGuids* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4c67f-111">*ppStrokePacketDescriptionGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c67f-112">Uma matriz que contém os identificadores de Propriedade do pacote.</span><span class="sxs-lookup"><span data-stu-id="4c67f-112">An array containing the packet property identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c67f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c67f-113">Return value</span></span>

<span data-ttu-id="4c67f-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4c67f-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c67f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c67f-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4c67f-116">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppStrokePacketDescriptionGuids* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="4c67f-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppStrokePacketDescriptionGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="4c67f-117">\**ppStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto no traço.</span><span class="sxs-lookup"><span data-stu-id="4c67f-117">\**ppStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="4c67f-118">Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4c67f-118">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c67f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c67f-119">Requirements</span></span>



| <span data-ttu-id="4c67f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c67f-120">Requirement</span></span> | <span data-ttu-id="4c67f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4c67f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c67f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c67f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c67f-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4c67f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4c67f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c67f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c67f-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c67f-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4c67f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c67f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c67f-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4c67f-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4c67f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4c67f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c67f-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c67f-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4c67f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c67f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c67f-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="4c67f-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4c67f-132">**IContextNode::GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="4c67f-132">**IContextNode::GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[<span data-ttu-id="4c67f-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="4c67f-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

