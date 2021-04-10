---
description: Abre um log de gráficos.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine:: OpenFile'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087545"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span data-ttu-id="6a923-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Método IPixEngine:: OpenFile</span><span class="sxs-lookup"><span data-stu-id="6a923-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine::OpenFile method</span></span>

<span data-ttu-id="6a923-104">Abre um log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="6a923-104">Opens a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a923-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a923-105">Syntax</span></span>


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a><span data-ttu-id="6a923-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a923-106">Parameters</span></span>

<span data-ttu-id="6a923-107">*Nome do arquivo* </span><span class="sxs-lookup"><span data-stu-id="6a923-107">*FileName* </span></span>  
<span data-ttu-id="6a923-108">Uma cadeia de caracteres COM que contém o nome do log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="6a923-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="6a923-109">*registryBoot* </span><span class="sxs-lookup"><span data-stu-id="6a923-109">*registryBoot* </span></span>  
<span data-ttu-id="6a923-110">Uma cadeia de caracteres COM que contém a raiz do registro.</span><span class="sxs-lookup"><span data-stu-id="6a923-110">A COM string containing the registry root.</span></span> <span data-ttu-id="6a923-111">O mecanismo é exibido aqui para o DIA e outras chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="6a923-111">The engine looks here for DIA and other registry keys.</span></span>

<span data-ttu-id="6a923-112">*retornos* </span><span class="sxs-lookup"><span data-stu-id="6a923-112">*callbacks* </span></span>  
<span data-ttu-id="6a923-113">O endereço de uma função usada para notificar o host que novos quadros foram analisados.</span><span class="sxs-lookup"><span data-stu-id="6a923-113">The address of a function used to notify the host that new frames have been parsed.</span></span>

<span data-ttu-id="6a923-114">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="6a923-114">*pFileIOCallback* </span></span>  
<span data-ttu-id="6a923-115">O endereço de uma função usada para notificar o host de erros de e/s de arquivo durante a análise.</span><span class="sxs-lookup"><span data-stu-id="6a923-115">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="6a923-116">*uiLocale* </span><span class="sxs-lookup"><span data-stu-id="6a923-116">*uiLocale* </span></span>  
<span data-ttu-id="6a923-117">A ID de localidade usada para apresentar mensagens de erro de acordo com as configurações de localidade.</span><span class="sxs-lookup"><span data-stu-id="6a923-117">The locale ID used to present error messages according to locale settings.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a923-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a923-118">Return value</span></span>

<span data-ttu-id="6a923-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6a923-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a923-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a923-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a923-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a923-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6a923-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a923-122">Header</span></span></p></td><td><span data-ttu-id="6a923-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6a923-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6a923-124"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="6a923-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6a923-125">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="6a923-125">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
