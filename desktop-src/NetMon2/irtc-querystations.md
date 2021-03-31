---
description: Fornece uma lista de todos os computadores que atualmente usam Monitor de Rede para capturar dados de rede.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'Método IRTC:: QueryStations (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921366"
---
# <a name="irtcquerystations-method"></a><span data-ttu-id="55300-103">Método IRTC:: QueryStations</span><span class="sxs-lookup"><span data-stu-id="55300-103">IRTC::QueryStations method</span></span>

<span data-ttu-id="55300-104">O método **QueryStations** fornece uma lista de todos os computadores que atualmente usam Monitor de rede para capturar dados de rede.</span><span class="sxs-lookup"><span data-stu-id="55300-104">The **QueryStations** method provides a list of all computers currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="55300-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55300-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="55300-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55300-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55300-107">*lpQueryTable* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="55300-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55300-108">Um ponteiro para uma estrutura de [**QUERYTABLE**](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="55300-108">A pointer to a [**QUERYTABLE**](querytable.md) structure.</span></span> <span data-ttu-id="55300-109">Na entrada, essa estrutura deve conter o número máximo de computadores que você deseja Monitor de Rede para retornar e uma matriz de estruturas [**STATIONQUERY**](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="55300-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [**STATIONQUERY**](stationquery.md) structures.</span></span>

<span data-ttu-id="55300-110">Na saída, essa estrutura retorna o número de computadores capturando dados e uma estrutura [**STATIONQUERY**](stationquery.md) para cada computador encontrado.</span><span class="sxs-lookup"><span data-stu-id="55300-110">On output, this structure returns the number of computers capturing data and a [**STATIONQUERY**](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="55300-111">Lembre-se de que isso pode incluir computadores que usam versões do Monitor de Rede que são anteriores à versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="55300-111">Be aware that this may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55300-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55300-112">Return value</span></span>

<span data-ttu-id="55300-113">Se o método for bem-sucedido, o valor de retorno será **NMERR com \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="55300-113">If the method is successful, the return value is **NMERR\_SUCCESS**.</span></span>

<span data-ttu-id="55300-114">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="55300-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="55300-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="55300-115">Return code</span></span>                                                                                           | <span data-ttu-id="55300-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="55300-116">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="55300-117"><dt>**NMERR \_ \_ de \_ memória insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="55300-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="55300-118">A memória necessária para processar esta consulta não está disponível.</span><span class="sxs-lookup"><span data-stu-id="55300-118">The memory required to process this query is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55300-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="55300-119">Remarks</span></span>

<span data-ttu-id="55300-120">Esse método pode ser chamado a qualquer momento depois que o método [**CreateNPPInterface**](createnppinterface.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="55300-120">This method can be called at any time after the [**CreateNPPInterface**](createnppinterface.md) method is called.</span></span> <span data-ttu-id="55300-121">Uma chamada para esse método é uma chamada síncrona, que pode levar vários segundos para ser concluída enquanto Monitor de Rede aguarda que os computadores remotos respondam à consulta.</span><span class="sxs-lookup"><span data-stu-id="55300-121">A call to this method is a synchronous call, which may take several seconds to complete while Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="55300-122">Somente os computadores na sub-rede local podem ser consultados.</span><span class="sxs-lookup"><span data-stu-id="55300-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="55300-123">O usuário deve alocar a memória para a estrutura de tabela de [**consulta**](querytable.md) e liberar essa memória depois que a tabela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="55300-123">The user must allocate the memory for the [**QUERYTABLE**](querytable.md) structure and free that memory after the table is no longer required.</span></span> <span data-ttu-id="55300-124">Esse requisito inclui a memória necessária para a matriz [**STATIONQUERY**](stationquery.md) usada em **QUERYTABLE**.</span><span class="sxs-lookup"><span data-stu-id="55300-124">This requirement includes memory needed for the [**STATIONQUERY**](stationquery.md) array used in **QUERYTABLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="55300-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55300-125">Requirements</span></span>



| <span data-ttu-id="55300-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="55300-126">Requirement</span></span> | <span data-ttu-id="55300-127">Valor</span><span class="sxs-lookup"><span data-stu-id="55300-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55300-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55300-128">Minimum supported client</span></span><br/> | <span data-ttu-id="55300-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55300-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="55300-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55300-130">Minimum supported server</span></span><br/> | <span data-ttu-id="55300-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55300-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="55300-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="55300-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="55300-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="55300-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="55300-134">DLL</span><span class="sxs-lookup"><span data-stu-id="55300-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55300-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55300-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55300-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="55300-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55300-137">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="55300-137">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="55300-138">**CONSULTA**</span><span class="sxs-lookup"><span data-stu-id="55300-138">**QUERYTABLE**</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="55300-139">**STATIONQUERY**</span><span class="sxs-lookup"><span data-stu-id="55300-139">**STATIONQUERY**</span></span>](stationquery.md)
</dt> </dl>

 

 




