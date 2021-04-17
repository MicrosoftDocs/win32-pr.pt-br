---
title: Função de retorno de chamada GetTSAudioEndpointEnumeratorForSession
description: Retorna uma referência a um enumerador de ponto de extremidade de áudio para a ID de sessão especificada.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Função de retorno de chamada GetTSAudioEndpointEnumeratorForSession Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782881"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a><span data-ttu-id="88448-104">Função de retorno de chamada GetTSAudioEndpointEnumeratorForSession</span><span class="sxs-lookup"><span data-stu-id="88448-104">GetTSAudioEndpointEnumeratorForSession callback function</span></span>

<span data-ttu-id="88448-105">Retorna uma referência a um enumerador de ponto de extremidade de áudio para a ID de sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="88448-105">Returns a reference to an audio endpoint enumerator for the specified session ID.</span></span> <span data-ttu-id="88448-106">Os consumidores deste enumerador de ponto de extremidade de áudio, como MMDevAPI.dll, chamam essa função para recuperar um enumerador de ponto de extremidade de áudio em uma sessão Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="88448-106">Consumers of this audio endpoint enumerator, such as MMDevAPI.dll, call this function to retrieve an audio endpoint enumerator in a Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="88448-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88448-107">Syntax</span></span>


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="88448-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88448-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88448-109">*SessionID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88448-109">*SessionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88448-110">O identificador da sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="88448-110">The identifier of the Remote Desktop Services session.</span></span>

</dd> <dt>

<span data-ttu-id="88448-111">*ppEndpointEnumerator* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="88448-111">*ppEndpointEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88448-112">O endereço de um ponteiro para uma interface [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="88448-112">The address of a pointer to an [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88448-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88448-113">Return value</span></span>

<span data-ttu-id="88448-114">Se o método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="88448-114">If the method succeeds, it returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="88448-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="88448-115">Remarks</span></span>

<span data-ttu-id="88448-116">Essa função não está definida em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="88448-116">This function is not defined in a header file.</span></span> <span data-ttu-id="88448-117">Você deve implementar e exportar essa função em seu enumerador de ponto de extremidade personalizado e usar a assinatura mostrada no bloco de sintaxe anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="88448-117">You should implement and export this function in your custom endpoint enumerator and use the signature shown in the syntax block earlier in this topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="88448-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88448-118">Requirements</span></span>



| <span data-ttu-id="88448-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="88448-119">Requirement</span></span> | <span data-ttu-id="88448-120">Valor</span><span class="sxs-lookup"><span data-stu-id="88448-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="88448-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88448-121">Minimum supported client</span></span><br/> | <span data-ttu-id="88448-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="88448-122">None supported</span></span><br/>         |
| <span data-ttu-id="88448-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88448-123">Minimum supported server</span></span><br/> | <span data-ttu-id="88448-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88448-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88448-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="88448-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88448-126">Implementando um enumerador de ponto de extremidade de áudio personalizado</span><span class="sxs-lookup"><span data-stu-id="88448-126">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[<span data-ttu-id="88448-127">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="88448-127">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

