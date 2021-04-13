---
description: O método Disconnect desconecta o NPP da rede.
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
ms.openlocfilehash: df58d6ac0e61ecc370510474c3bc067726d9824b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165349"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="57b77-103">Método IRTC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="57b77-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="57b77-104">O método **Disconnect desconecta** o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="57b77-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b77-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57b77-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="57b77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57b77-106">Parameters</span></span>

<span data-ttu-id="57b77-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="57b77-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="57b77-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57b77-108">Return value</span></span>

<span data-ttu-id="57b77-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="57b77-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="57b77-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="57b77-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="57b77-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="57b77-111">Return code</span></span>                                                                                          | <span data-ttu-id="57b77-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="57b77-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57b77-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="57b77-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="57b77-114">O NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="57b77-114">The NPP is capturing data.</span></span> <span data-ttu-id="57b77-115">Não é possível desconectar da rede enquanto a captura de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="57b77-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="57b77-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="57b77-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="57b77-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="57b77-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="57b77-118"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="57b77-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="57b77-119">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="57b77-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="57b77-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="57b77-120">Remarks</span></span>

<span data-ttu-id="57b77-121">Este método não pode ser chamado quando o NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="57b77-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="57b77-122">Você deve chamar o método [IRTC:: Stop](irtc-stop.md) antes de chamar IRTC::D isconnect.</span><span class="sxs-lookup"><span data-stu-id="57b77-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b77-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57b77-123">Requirements</span></span>



| <span data-ttu-id="57b77-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="57b77-124">Requirement</span></span> | <span data-ttu-id="57b77-125">Valor</span><span class="sxs-lookup"><span data-stu-id="57b77-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b77-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57b77-126">Minimum supported client</span></span><br/> | <span data-ttu-id="57b77-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="57b77-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="57b77-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57b77-128">Minimum supported server</span></span><br/> | <span data-ttu-id="57b77-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="57b77-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="57b77-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="57b77-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b77-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="57b77-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="57b77-132">DLL</span><span class="sxs-lookup"><span data-stu-id="57b77-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57b77-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57b77-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b77-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="57b77-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b77-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="57b77-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="57b77-136">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="57b77-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="57b77-137">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="57b77-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




