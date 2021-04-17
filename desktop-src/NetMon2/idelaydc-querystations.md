---
description: O método QueryStations fornece uma lista de todos os computadores que atualmente estão usando Monitor de Rede para capturar dados.
ms.assetid: 8e578f50-685e-4799-90ca-5da8810ec2a3
title: 'Método IDelaydC:: QueryStations (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5a45f5046dbd2e5714424baf42621e0c1d5539ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780200"
---
# <a name="idelaydcquerystations-method"></a><span data-ttu-id="83eed-103">Método IDelaydC:: QueryStations</span><span class="sxs-lookup"><span data-stu-id="83eed-103">IDelaydC::QueryStations method</span></span>

<span data-ttu-id="83eed-104">O método **QueryStations** fornece uma lista de todos os computadores que atualmente estão usando monitor de rede para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="83eed-104">The **QueryStations** method provides a list of all computers that are currently using Network Monitor to capture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="83eed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83eed-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="83eed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83eed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83eed-107">*lpQueryTable* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="83eed-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83eed-108">Ponteiro para uma estrutura de [QUERYTABLE](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="83eed-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="83eed-109">Na entrada, essa estrutura deve conter o número máximo de computadores que você deseja Monitor de Rede para retornar e uma matriz de estruturas [STATIONQUERY](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="83eed-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="83eed-110">Na saída, essa estrutura retorna o número de computadores que estão capturando dados e uma estrutura [STATIONQUERY](stationquery.md) para cada computador encontrado.</span><span class="sxs-lookup"><span data-stu-id="83eed-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="83eed-111">Observe que essa lista pode incluir computadores que usam versões do Monitor de Rede que são anteriores à versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="83eed-111">Note that this list might include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83eed-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83eed-112">Return value</span></span>

<span data-ttu-id="83eed-113">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="83eed-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="83eed-114">Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:</span><span class="sxs-lookup"><span data-stu-id="83eed-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="83eed-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="83eed-115">Return code</span></span>                                                                                           | <span data-ttu-id="83eed-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="83eed-116">Description</span></span>                                               |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="83eed-117"><dt>**NMERR \_ \_ de \_ memória insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="83eed-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="83eed-118">Não havia memória disponível para processar esta consulta.</span><span class="sxs-lookup"><span data-stu-id="83eed-118">No memory was available to process this query.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83eed-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="83eed-119">Remarks</span></span>

<span data-ttu-id="83eed-120">Esse método pode ser chamado a qualquer momento depois que [CreateNPPInterface](createnppinterface.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="83eed-120">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="83eed-121">Uma chamada para esse método é uma chamada síncrona, que pode levar vários segundos para ser concluída, pois Monitor de Rede aguarda que os computadores remotos respondam à consulta.</span><span class="sxs-lookup"><span data-stu-id="83eed-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="83eed-122">Somente os computadores na sub-rede local podem ser consultados.</span><span class="sxs-lookup"><span data-stu-id="83eed-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="83eed-123">É sua responsabilidade alocar a memória para a estrutura [QUERYTABLE](querytable.md) e liberar essa memória depois que a tabela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="83eed-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="83eed-124">Esse requisito inclui a memória necessária para a matriz [STATIONQUERY](stationquery.md) usada em QUERYTABLE.</span><span class="sxs-lookup"><span data-stu-id="83eed-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="83eed-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83eed-125">Requirements</span></span>



| <span data-ttu-id="83eed-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="83eed-126">Requirement</span></span> | <span data-ttu-id="83eed-127">Valor</span><span class="sxs-lookup"><span data-stu-id="83eed-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83eed-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83eed-128">Minimum supported client</span></span><br/> | <span data-ttu-id="83eed-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83eed-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="83eed-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83eed-130">Minimum supported server</span></span><br/> | <span data-ttu-id="83eed-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="83eed-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="83eed-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="83eed-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="83eed-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="83eed-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="83eed-134">DLL</span><span class="sxs-lookup"><span data-stu-id="83eed-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83eed-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83eed-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83eed-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="83eed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83eed-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="83eed-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="83eed-138">CONSULTA</span><span class="sxs-lookup"><span data-stu-id="83eed-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="83eed-139">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="83eed-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




