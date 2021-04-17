---
description: Obtém um valor que indica se o sistema de chave especificado dá suporte ao tipo de mídia especificado.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'Método IMFMediaEngineClassFactoryEx:: IsTypeSupported'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105813304"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a><span data-ttu-id="4d6d7-103">Método IMFMediaEngineClassFactoryEx:: IsTypeSupported</span><span class="sxs-lookup"><span data-stu-id="4d6d7-103">IMFMediaEngineClassFactoryEx::IsTypeSupported method</span></span>

<span data-ttu-id="4d6d7-104">Obtém um valor que indica se o sistema de chave especificado dá suporte ao tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="4d6d7-104">Gets a value that indicates if the specified key system supports the specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d6d7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d6d7-105">Syntax</span></span>


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a><span data-ttu-id="4d6d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d6d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d6d7-107">*tipo*</span><span class="sxs-lookup"><span data-stu-id="4d6d7-107">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6d7-108">O tipo de MIME para o qual verificar o suporte.</span><span class="sxs-lookup"><span data-stu-id="4d6d7-108">The MIME type to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="4d6d7-109">*sistema de*</span><span class="sxs-lookup"><span data-stu-id="4d6d7-109">*keySystem*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6d7-110">O sistema principal para o qual verificar o suporte.</span><span class="sxs-lookup"><span data-stu-id="4d6d7-110">The key system to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="4d6d7-111">*isSupported*</span><span class="sxs-lookup"><span data-stu-id="4d6d7-111">*isSupported*</span></span> 
</dt> <dd>

<span data-ttu-id="4d6d7-112">**true** se o tipo for compatível com o *keysystem*; caso contrário, **false.**</span><span class="sxs-lookup"><span data-stu-id="4d6d7-112">**true** if type is supported by *keySystem*; otherwise, **false.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d6d7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d6d7-113">Return value</span></span>

<span data-ttu-id="4d6d7-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4d6d7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d6d7-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d6d7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d6d7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d6d7-116">Requirements</span></span>



| <span data-ttu-id="4d6d7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d6d7-117">Requirement</span></span> | <span data-ttu-id="4d6d7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4d6d7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d6d7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d6d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d6d7-120">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d6d7-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d6d7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d6d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d6d7-122">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="4d6d7-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4d6d7-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="4d6d7-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4d6d7-124"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4d6d7-124"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d6d7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d6d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d6d7-126">**IMFMediaEngineClassFactoryEx**</span><span class="sxs-lookup"><span data-stu-id="4d6d7-126">**IMFMediaEngineClassFactoryEx**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




