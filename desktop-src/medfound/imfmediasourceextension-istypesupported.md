---
description: Obtém um valor que indica se o tipo MIME especificado tem suporte da origem de mídia.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'Método IMFMediaSourceExtension:: IsTypeSupported'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105785042"
---
# <a name="imfmediasourceextensionistypesupported-method"></a><span data-ttu-id="62070-103">Método IMFMediaSourceExtension:: IsTypeSupported</span><span class="sxs-lookup"><span data-stu-id="62070-103">IMFMediaSourceExtension::IsTypeSupported method</span></span>

<span data-ttu-id="62070-104">Obtém um valor que indica se o tipo MIME especificado tem suporte da origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="62070-104">Gets a value that indicates if the specified MIME type is supported by the media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="62070-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62070-105">Syntax</span></span>


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a><span data-ttu-id="62070-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62070-107">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="62070-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62070-108">O tipo de mídia para o qual verificar o suporte.</span><span class="sxs-lookup"><span data-stu-id="62070-108">The media type to check support for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62070-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62070-109">Return value</span></span>

<span data-ttu-id="62070-110">**true** se o tipo de mídia tiver suporte; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="62070-110">**true** if the media type is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62070-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62070-111">Requirements</span></span>



| <span data-ttu-id="62070-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="62070-112">Requirement</span></span> | <span data-ttu-id="62070-113">Valor</span><span class="sxs-lookup"><span data-stu-id="62070-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62070-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62070-114">Minimum supported client</span></span><br/> | <span data-ttu-id="62070-115">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="62070-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="62070-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62070-116">Minimum supported server</span></span><br/> | <span data-ttu-id="62070-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="62070-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="62070-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="62070-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62070-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62070-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62070-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="62070-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62070-121">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="62070-121">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




