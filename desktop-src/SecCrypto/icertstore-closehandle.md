---
description: Fecha um identificador HCERTSTORE adquirido por meio da Propriedade StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'Método ICertStore:: CloseHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754599"
---
# <a name="icertstoreclosehandle-method"></a><span data-ttu-id="aeafa-103">Método ICertStore:: CloseHandle</span><span class="sxs-lookup"><span data-stu-id="aeafa-103">ICertStore::CloseHandle method</span></span>

<span data-ttu-id="aeafa-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="aeafa-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="aeafa-105">O método **CloseHandle** fecha um identificador HCERTSTORE adquirido por meio da propriedade [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="aeafa-105">The **CloseHandle** method closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeafa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aeafa-106">Syntax</span></span>


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a><span data-ttu-id="aeafa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aeafa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeafa-108">*HCERTSTORE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aeafa-108">*hCertStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeafa-109">O identificador HCERTSTORE a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="aeafa-109">The HCERTSTORE handle to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeafa-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aeafa-110">Return value</span></span>

<span data-ttu-id="aeafa-111">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aeafa-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="aeafa-112">Um valor de **S \_ OK** indica êxito.</span><span class="sxs-lookup"><span data-stu-id="aeafa-112">A value of **S\_OK** indicates success.</span></span> <span data-ttu-id="aeafa-113">Qualquer outro valor indica que a operação falhou.</span><span class="sxs-lookup"><span data-stu-id="aeafa-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeafa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aeafa-114">Remarks</span></span>

<span data-ttu-id="aeafa-115">Esse método não libera o identificador HCERTSTORE contido em um objeto [**Store**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="aeafa-115">This method does not release the HCERTSTORE handle contained within a [**Store**](store.md) object.</span></span> <span data-ttu-id="aeafa-116">Ele deve ser usado apenas para liberar um identificador HCERTSTORE adquirido por meio da propriedade [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="aeafa-116">It should be used only to release a HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeafa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeafa-117">Requirements</span></span>



| <span data-ttu-id="aeafa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeafa-118">Requirement</span></span> | <span data-ttu-id="aeafa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="aeafa-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeafa-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="aeafa-120">Redistributable</span></span><br/> | <span data-ttu-id="aeafa-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="aeafa-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aeafa-122">DLL</span><span class="sxs-lookup"><span data-stu-id="aeafa-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="aeafa-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeafa-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeafa-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="aeafa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeafa-125">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="aeafa-125">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




