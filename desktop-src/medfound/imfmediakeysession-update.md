---
description: Passa um valor de chave com todos os dados associados exigidos pelo módulo de descriptografia de conteúdo para o sistema de chaves fornecido.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'Método IMFMediaKeySession:: Update'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105787556"
---
# <a name="imfmediakeysessionupdate-method"></a><span data-ttu-id="e9708-103">Método IMFMediaKeySession:: Update</span><span class="sxs-lookup"><span data-stu-id="e9708-103">IMFMediaKeySession::Update method</span></span>

<span data-ttu-id="e9708-104">Passa um valor de chave com todos os dados associados exigidos pelo módulo de descriptografia de conteúdo para o sistema de chaves fornecido.</span><span class="sxs-lookup"><span data-stu-id="e9708-104">Passes in a key value with any associated data required by the Content Decryption Module for the given key system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9708-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9708-105">Syntax</span></span>


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a><span data-ttu-id="e9708-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9708-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9708-107">*chave*</span><span class="sxs-lookup"><span data-stu-id="e9708-107">*key*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="e9708-108">*CB*</span><span class="sxs-lookup"><span data-stu-id="e9708-108">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="e9708-109">A contagem em bytes de *chave*.</span><span class="sxs-lookup"><span data-stu-id="e9708-109">The count in bytes of *key*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9708-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9708-110">Return value</span></span>

<span data-ttu-id="e9708-111">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e9708-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9708-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9708-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9708-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9708-113">Requirements</span></span>



| <span data-ttu-id="e9708-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9708-114">Requirement</span></span> | <span data-ttu-id="e9708-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e9708-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9708-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9708-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e9708-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9708-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9708-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9708-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e9708-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="e9708-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e9708-120">INSERI</span><span class="sxs-lookup"><span data-stu-id="e9708-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9708-121"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9708-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9708-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9708-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9708-123">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="e9708-123">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




