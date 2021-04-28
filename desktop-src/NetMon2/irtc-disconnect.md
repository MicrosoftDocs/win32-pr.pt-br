---
description: 'IRTC: método isconnect:D-o método Disconnect desconecta o NPP da rede.'
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: 'IRTC: método:D isconnect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 43acb88e2c7b6108a162c4715de02375121021f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110714"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="9de4c-103">Método IRTC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="9de4c-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="9de4c-104">O método **Disconnect desconecta** o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="9de4c-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de4c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9de4c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="9de4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9de4c-106">Parameters</span></span>

<span data-ttu-id="9de4c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9de4c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9de4c-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9de4c-108">Return value</span></span>

<span data-ttu-id="9de4c-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="9de4c-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9de4c-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="9de4c-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9de4c-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9de4c-111">Return code</span></span>                                                                                          | <span data-ttu-id="9de4c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9de4c-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9de4c-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9de4c-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="9de4c-114">O NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="9de4c-114">The NPP is capturing data.</span></span> <span data-ttu-id="9de4c-115">Não é possível desconectar da rede enquanto a captura de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="9de4c-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="9de4c-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="9de4c-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9de4c-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="9de4c-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="9de4c-118"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="9de4c-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="9de4c-119">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="9de4c-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="9de4c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9de4c-120">Remarks</span></span>

<span data-ttu-id="9de4c-121">Este método não pode ser chamado quando o NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="9de4c-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="9de4c-122">Você deve chamar o método [IRTC:: Stop](irtc-stop.md) antes de chamar IRTC::D isconnect.</span><span class="sxs-lookup"><span data-stu-id="9de4c-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de4c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9de4c-123">Requirements</span></span>



| <span data-ttu-id="9de4c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9de4c-124">Requirement</span></span> | <span data-ttu-id="9de4c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9de4c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de4c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9de4c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9de4c-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9de4c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9de4c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9de4c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9de4c-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9de4c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9de4c-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9de4c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de4c-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de4c-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9de4c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9de4c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9de4c-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9de4c-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de4c-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9de4c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de4c-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="9de4c-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="9de4c-136">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="9de4c-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="9de4c-137">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="9de4c-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




