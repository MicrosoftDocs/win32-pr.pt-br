---
description: Carrega uma textura de um arquivo e notifica o host de forma assíncrona quando ele é concluído.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine5:: LoadTextureFromFileAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bef4e4e5117680f7c18f13cc99f801c8e8b8bdfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087892"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span data-ttu-id="78836-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>Método IPixEngine5:: LoadTextureFromFileAsync</span><span class="sxs-lookup"><span data-stu-id="78836-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureFromFileAsync method</span></span>

<span data-ttu-id="78836-104">Carrega uma textura de um arquivo e notifica o host de forma assíncrona quando ele é concluído.</span><span class="sxs-lookup"><span data-stu-id="78836-104">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="78836-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78836-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="78836-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78836-106">Parameters</span></span>

<span data-ttu-id="78836-107">*Nome do arquivo* </span><span class="sxs-lookup"><span data-stu-id="78836-107">*fileName* </span></span>  
<span data-ttu-id="78836-108">Uma cadeia de caracteres COM que contém o nome do arquivo de textura.</span><span class="sxs-lookup"><span data-stu-id="78836-108">A COM string containing the name of the texture file.</span></span>

<span data-ttu-id="78836-109">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="78836-109">*histogramDataFileName* </span></span>  
<span data-ttu-id="78836-110">Uma cadeia de caracteres COM que contém o nome do arquivo de dados de histograma associado à textura.</span><span class="sxs-lookup"><span data-stu-id="78836-110">A COM string containing the name of the histogram data file associated with the texture.</span></span>

<span data-ttu-id="78836-111">*retornos* </span><span class="sxs-lookup"><span data-stu-id="78836-111">*callbacks* </span></span>  
<span data-ttu-id="78836-112">O endereço de um objeto que fornece a interface de retornos de chamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="78836-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="78836-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="78836-113">*requestCookie* </span></span>  
<span data-ttu-id="78836-114">Um cookie que idenfies exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="78836-114">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="78836-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="78836-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="78836-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="78836-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="78836-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78836-117">Return value</span></span>

<span data-ttu-id="78836-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="78836-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78836-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="78836-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78836-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78836-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="78836-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78836-121">Header</span></span></p></td><td><span data-ttu-id="78836-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="78836-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="78836-123"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="78836-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="78836-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="78836-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
