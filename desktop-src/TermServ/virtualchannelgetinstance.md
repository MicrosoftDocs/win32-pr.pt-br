---
title: Ponto de entrada VirtualChannelGetInstance
description: Chamado para que o plug-in crie uma instância da interface IWTSPlugin para todos os plug-ins implementados pela DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de ponto de entrada VirtualChannelGetInstance
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369422"
---
# <a name="virtualchannelgetinstance-entry-point"></a><span data-ttu-id="3a91a-104">Ponto de entrada VirtualChannelGetInstance</span><span class="sxs-lookup"><span data-stu-id="3a91a-104">VirtualChannelGetInstance entry point</span></span>

<span data-ttu-id="3a91a-105">Chamado para que o plug-in crie uma instância da interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos os plug-ins implementados pela dll.</span><span class="sxs-lookup"><span data-stu-id="3a91a-105">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

> [!Note]
>
> <span data-ttu-id="3a91a-106">Essa função é implementada pelo plug-in e deve ser exportada por nome, de modo que um aplicativo possa usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a função.</span><span class="sxs-lookup"><span data-stu-id="3a91a-106">This function is implemented by the plug-in and must be exported by name such that an application can use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to the function.</span></span>
>
> <span data-ttu-id="3a91a-107">O protótipo para essa função não está contido em nenhum arquivo de cabeçalho público, portanto, você deve declará-lo exatamente como mostrado.</span><span class="sxs-lookup"><span data-stu-id="3a91a-107">The prototype for this function is not contained in any public header file, so you must declare it exactly as shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3a91a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a91a-108">Syntax</span></span>


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a><span data-ttu-id="3a91a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a91a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a91a-110">*REFIID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a91a-110">*refiid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a91a-111">Especifica o tipo de interface a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="3a91a-111">Specifies the type of interface to return.</span></span> <span data-ttu-id="3a91a-112">Deve ser **IID \_ IWTSPlugin**.</span><span class="sxs-lookup"><span data-stu-id="3a91a-112">This must be **IID\_IWTSPlugin**.</span></span>

</dd> <dt>

<span data-ttu-id="3a91a-113">*pNumObjs* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3a91a-113">*pNumObjs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a91a-114">O endereço de uma variável **ULONG** que recebe o número de interfaces recuperadas.</span><span class="sxs-lookup"><span data-stu-id="3a91a-114">The address of a **ULONG** variable that receives the number of interfaces retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="3a91a-115">*ppObjArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3a91a-115">*ppObjArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a91a-116">O endereço de uma matriz de ponteiros que recebe os ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="3a91a-116">The address of an array of pointers that receives the interface pointers.</span></span> <span data-ttu-id="3a91a-117">Se esse parâmetro for **nulo**, a implementação deverá colocar o número de plug-ins implementados pela dll no parâmetro *pNumObjs* .</span><span class="sxs-lookup"><span data-stu-id="3a91a-117">If this parameter is **NULL**, the implementation must put the number of plug-ins implemented by the DLL in the *pNumObjs* parameter.</span></span> <span data-ttu-id="3a91a-118">Isso permite que o chamador aloque a matriz de tamanho apropriada para *ppObjArray*.</span><span class="sxs-lookup"><span data-stu-id="3a91a-118">This allows the caller to allocate the proper size array for *ppObjArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a91a-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a91a-119">Return value</span></span>

<span data-ttu-id="3a91a-120">Se esse ponto de entrada for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3a91a-120">If this entry point succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a91a-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a91a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a91a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a91a-122">Requirements</span></span>



| <span data-ttu-id="3a91a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a91a-123">Requirement</span></span> | <span data-ttu-id="3a91a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3a91a-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3a91a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a91a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a91a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a91a-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3a91a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a91a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a91a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a91a-128">Windows Server 2008</span></span><br/> |



 

