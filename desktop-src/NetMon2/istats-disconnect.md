---
description: Desconecta o NPP da rede.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: 'IStats: método:D isconnect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747732"
---
# <a name="istatsdisconnect-method"></a><span data-ttu-id="dec3e-103">Método IStats::D isconnect</span><span class="sxs-lookup"><span data-stu-id="dec3e-103">IStats::Disconnect method</span></span>

<span data-ttu-id="dec3e-104">O método **Disconnect desconecta** o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="dec3e-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec3e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dec3e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="dec3e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dec3e-106">Parameters</span></span>

<span data-ttu-id="dec3e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dec3e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dec3e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dec3e-108">Return value</span></span>

<span data-ttu-id="dec3e-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="dec3e-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dec3e-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="dec3e-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dec3e-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dec3e-111">Return code</span></span>                                                                                            | <span data-ttu-id="dec3e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="dec3e-112">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dec3e-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="dec3e-114">O NPP está capturando dados no momento.</span><span class="sxs-lookup"><span data-stu-id="dec3e-114">The NPP is currently capturing data.</span></span> <span data-ttu-id="dec3e-115">Não é possível desconectar da rede enquanto uma captura de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="dec3e-115">You cannot disconnect from the network while a data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="dec3e-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="dec3e-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="dec3e-117">The NPP is not connected to the network.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="dec3e-118"><dt>**NMERR \_ \_ somente não estatísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-118"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="dec3e-119">O NPP está conectado à rede, mas não com o método [**IStats:: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="dec3e-119">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="dec3e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="dec3e-120">Remarks</span></span>

<span data-ttu-id="dec3e-121">Este método não pode ser chamado quando o NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="dec3e-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="dec3e-122">Chame o método **IStats::D isconnect** primeiro e, em seguida, chame [**IStats:: Stop**](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="dec3e-122">Call the **IStats::Disconnect** method first and then call [**IStats::Stop**](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dec3e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec3e-123">Requirements</span></span>



| <span data-ttu-id="dec3e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec3e-124">Requirement</span></span> | <span data-ttu-id="dec3e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="dec3e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec3e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dec3e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dec3e-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dec3e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dec3e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dec3e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dec3e-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dec3e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dec3e-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dec3e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec3e-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dec3e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dec3e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec3e-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec3e-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec3e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="dec3e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec3e-135">**IStats**</span><span class="sxs-lookup"><span data-stu-id="dec3e-135">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="dec3e-136">**IStats:: conectar**</span><span class="sxs-lookup"><span data-stu-id="dec3e-136">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="dec3e-137">**IStats:: Stop**</span><span class="sxs-lookup"><span data-stu-id="dec3e-137">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 




