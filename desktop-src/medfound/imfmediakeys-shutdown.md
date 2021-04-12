---
description: 'Saiba mais sobre o método: IMFMediaKeys:: Shutdown'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: 'Método IMFMediaKeys:: Shutdown'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9fcee861b53aaf0c9fda2c6265f50fcee60f674c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297962"
---
# <a name="imfmediakeysshutdown-method"></a><span data-ttu-id="cec17-103">Método IMFMediaKeys:: Shutdown</span><span class="sxs-lookup"><span data-stu-id="cec17-103">IMFMediaKeys::Shutdown method</span></span>

## <a name="syntax"></a><span data-ttu-id="cec17-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cec17-104">Syntax</span></span>


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="cec17-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cec17-105">Parameters</span></span>

<span data-ttu-id="cec17-106">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cec17-106">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cec17-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cec17-107">Return value</span></span>

<span data-ttu-id="cec17-108">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cec17-108">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cec17-109">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cec17-109">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cec17-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cec17-110">Remarks</span></span>

<span data-ttu-id="cec17-111">O **desligamento** deve ser chamado pelo aplicativo antes da versão final.</span><span class="sxs-lookup"><span data-stu-id="cec17-111">**Shutdown** should be called by the application before final release.</span></span> <span data-ttu-id="cec17-112">A referência do módulo de descriptografia de conteúdo (CDM) e todos os outros recursos são liberados neste ponto.</span><span class="sxs-lookup"><span data-stu-id="cec17-112">The Content Decryption Module (CDM) reference and any other resources is released at this point.</span></span> <span data-ttu-id="cec17-113">No entanto, as sessões relacionadas não são liberadas ou fechadas.</span><span class="sxs-lookup"><span data-stu-id="cec17-113">However, related sessions are not freed or closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec17-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cec17-114">Requirements</span></span>



| <span data-ttu-id="cec17-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cec17-115">Requirement</span></span> | <span data-ttu-id="cec17-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cec17-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec17-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cec17-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cec17-118">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cec17-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cec17-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cec17-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cec17-120">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="cec17-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cec17-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="cec17-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cec17-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cec17-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec17-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="cec17-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec17-124">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="cec17-124">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




