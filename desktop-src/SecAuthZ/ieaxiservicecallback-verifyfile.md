---
description: Executa verificações de segurança no objeto ActiveX especificado e retorna o local onde o arquivo. cab correspondente foi baixado.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'Método IeAxiServiceCallback:: VERIFYFILE'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506136"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a><span data-ttu-id="5cfea-103">Método IeAxiServiceCallback:: VERIFYFILE</span><span class="sxs-lookup"><span data-stu-id="5cfea-103">IeAxiServiceCallback::VerifyFile method</span></span>

<span data-ttu-id="5cfea-104">O método **VERIFYFILE** executa verificações de segurança no objeto ActiveX especificado e retorna o local onde o arquivo. cab correspondente foi baixado.</span><span class="sxs-lookup"><span data-stu-id="5cfea-104">The **VerifyFile** method performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cfea-105">Syntax</span></span>


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a><span data-ttu-id="5cfea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cfea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cfea-107">*bstrFileUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5cfea-107">*bstrFileUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cfea-108">A URL do objeto ActiveX a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="5cfea-108">The URL of the ActiveX object to check.</span></span>

</dd> <dt>

<span data-ttu-id="5cfea-109">*bstrApprovedFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5cfea-109">*bstrApprovedFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cfea-110">O nome do arquivo em que o arquivo. cab associado ao objeto ActiveX foi baixado.</span><span class="sxs-lookup"><span data-stu-id="5cfea-110">The name of the file where the .cab file associated with the ActiveX object was downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cfea-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5cfea-111">Return value</span></span>

<span data-ttu-id="5cfea-112">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5cfea-112">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="5cfea-113">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="5cfea-113">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="5cfea-114">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="5cfea-114">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cfea-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cfea-115">Requirements</span></span>



| <span data-ttu-id="5cfea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cfea-116">Requirement</span></span> | <span data-ttu-id="5cfea-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5cfea-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfea-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cfea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5cfea-119">Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="5cfea-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5cfea-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cfea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5cfea-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5cfea-121">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="5cfea-122">IID</span><span class="sxs-lookup"><span data-stu-id="5cfea-122">IID</span></span><br/>                      | <span data-ttu-id="5cfea-123">IID \_ IeAxiServiceCallback é definido como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="5cfea-123">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="5cfea-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cfea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfea-125">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="5cfea-125">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

