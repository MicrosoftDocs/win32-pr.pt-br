---
description: Recupera uma matriz que contém os dados de Propriedade do pacote para o traço especificado.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'Método IContextNode:: GetStrokePacketDataById (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794620"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a><span data-ttu-id="268f0-103">Método IContextNode:: GetStrokePacketDataById</span><span class="sxs-lookup"><span data-stu-id="268f0-103">IContextNode::GetStrokePacketDataById method</span></span>

<span data-ttu-id="268f0-104">Recupera uma matriz que contém os dados de Propriedade do pacote para o traço especificado.</span><span class="sxs-lookup"><span data-stu-id="268f0-104">Retrieves an array containing the packet property data for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="268f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="268f0-105">Syntax</span></span>


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="268f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="268f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="268f0-107">*strokeid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="268f0-107">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268f0-108">O identificador para o traço.</span><span class="sxs-lookup"><span data-stu-id="268f0-108">The identifier for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="268f0-109">*pStrokePacketDataCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="268f0-109">*pStrokePacketDataCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="268f0-110">O comprimento da matriz de dados do pacote.</span><span class="sxs-lookup"><span data-stu-id="268f0-110">The length of the packet data array.</span></span>

</dd> <dt>

<span data-ttu-id="268f0-111">*pplStrokePacketData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="268f0-111">*pplStrokePacketData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="268f0-112">Um ponteiro para os dados do pacote para o traço.</span><span class="sxs-lookup"><span data-stu-id="268f0-112">A pointer to the packet data for the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="268f0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="268f0-113">Return value</span></span>

<span data-ttu-id="268f0-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="268f0-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="268f0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="268f0-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="268f0-116">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *pplStrokePacketData* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="268f0-116">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokePacketData* when you no longer need the information.</span></span>

 

<span data-ttu-id="268f0-117">*plStrokePacketData* contém dados de pacote para todos os pontos no traço.</span><span class="sxs-lookup"><span data-stu-id="268f0-117">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="268f0-118">Para obter os tipos de dados de pacote incluídos para cada ponto no traço, use [**IContextNode:: GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span><span class="sxs-lookup"><span data-stu-id="268f0-118">To get the types of packet data included for each point in the stroke, use [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="268f0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="268f0-119">Requirements</span></span>



| <span data-ttu-id="268f0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="268f0-120">Requirement</span></span> | <span data-ttu-id="268f0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="268f0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="268f0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="268f0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="268f0-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="268f0-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="268f0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="268f0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="268f0-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="268f0-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="268f0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="268f0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="268f0-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="268f0-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="268f0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="268f0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="268f0-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="268f0-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="268f0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="268f0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268f0-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="268f0-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="268f0-132">**IContextNode::GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="268f0-132">**IContextNode::GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[<span data-ttu-id="268f0-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="268f0-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

