---
description: Cria um manipulador de fluxo de bytes para a origem de mídia MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: Função MFCreateMP3ByteStreamPlugin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754421"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a><span data-ttu-id="acedf-103">Função MFCreateMP3ByteStreamPlugin</span><span class="sxs-lookup"><span data-stu-id="acedf-103">MFCreateMP3ByteStreamPlugin function</span></span>

<span data-ttu-id="acedf-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="acedf-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="acedf-105">Em vez disso, os aplicativos devem usar o [resolvedor de origem](source-resolver.md) para criar a origem de mídia mp3.\]</span><span class="sxs-lookup"><span data-stu-id="acedf-105">Instead, applications should use the [Source Resolver](source-resolver.md) to create the MP3 media source.\]</span></span>

<span data-ttu-id="acedf-106">Cria um manipulador de fluxo de bytes para a origem de mídia MP3.</span><span class="sxs-lookup"><span data-stu-id="acedf-106">Creates a byte-stream handler for the MP3 media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="acedf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acedf-107">Syntax</span></span>


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a><span data-ttu-id="acedf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acedf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acedf-109">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="acedf-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acedf-110">O IID (identificador de interface) da interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="acedf-110">The interface identifier (IID) of the requested interface.</span></span> <span data-ttu-id="acedf-111">Defina esse parâmetro como **IID \_ IMFByteStreamHandler** para receber um ponteiro para a interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="acedf-111">Set this parameter to **IID\_IMFByteStreamHandler** to receive a pointer to the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span>

</dd> <dt>

<span data-ttu-id="acedf-112">*ppvHandler* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="acedf-112">*ppvHandler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acedf-113">Recebe um ponteiro para a interface.</span><span class="sxs-lookup"><span data-stu-id="acedf-113">Receives a pointer to the interface.</span></span> <span data-ttu-id="acedf-114">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="acedf-114">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acedf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="acedf-115">Return value</span></span>

<span data-ttu-id="acedf-116">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="acedf-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="acedf-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="acedf-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="acedf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="acedf-118">Remarks</span></span>

<span data-ttu-id="acedf-119">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="acedf-119">This function has no associated import library.</span></span> <span data-ttu-id="acedf-120">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a mf.dll.</span><span class="sxs-lookup"><span data-stu-id="acedf-120">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to mf.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="acedf-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acedf-121">Requirements</span></span>



| <span data-ttu-id="acedf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="acedf-122">Requirement</span></span> | <span data-ttu-id="acedf-123">Valor</span><span class="sxs-lookup"><span data-stu-id="acedf-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="acedf-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acedf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="acedf-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="acedf-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="acedf-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acedf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="acedf-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="acedf-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="acedf-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="acedf-128">End of client support</span></span><br/>    | <span data-ttu-id="acedf-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acedf-129">Windows Vista</span></span><br/>                             |
| <span data-ttu-id="acedf-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="acedf-130">End of server support</span></span><br/>    | <span data-ttu-id="acedf-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acedf-131">Windows Server 2008</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="acedf-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="acedf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acedf-133">Funções de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="acedf-133">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> <dt>

[<span data-ttu-id="acedf-134">Manipuladores de esquema e manipuladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="acedf-134">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="acedf-135">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="acedf-135">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
