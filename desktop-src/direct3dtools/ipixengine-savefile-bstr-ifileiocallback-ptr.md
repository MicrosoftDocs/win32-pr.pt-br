---
description: Salva o log de gráficos no local especificado.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine:: SaveFile'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f7e1bed8765ca64123ccf13cbc3ee5f0d989b115
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500718"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span data-ttu-id="c3c5e-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>Método IPixEngine:: SaveFile</span><span class="sxs-lookup"><span data-stu-id="c3c5e-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine::SaveFile method</span></span>

<span data-ttu-id="c3c5e-104">Salva o log de gráficos no local especificado.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-104">Saves the graphics log to the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c5e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3c5e-105">Syntax</span></span>


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a><span data-ttu-id="c3c5e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3c5e-106">Parameters</span></span>

<span data-ttu-id="c3c5e-107">*Nome do arquivo* </span><span class="sxs-lookup"><span data-stu-id="c3c5e-107">*FileName* </span></span>  
<span data-ttu-id="c3c5e-108">Uma cadeia de caracteres COM que contém o nome do caminho do log de gráficos salvo.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-108">A COM string containing the pathname of the saved graphics log.</span></span>

<span data-ttu-id="c3c5e-109">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="c3c5e-109">*pFileIOCallback* </span></span>  
<span data-ttu-id="c3c5e-110">O endereço de um Functon usado para notificar o host de erros de e/s de arquivo durante o salvamento.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-110">The address of a functon used to notify the host of file IO errors during save.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3c5e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3c5e-111">Return value</span></span>

<span data-ttu-id="c3c5e-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c3c5e-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3c5e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c5e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3c5e-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c3c5e-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3c5e-115">Header</span></span></p></td><td><span data-ttu-id="c3c5e-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c3c5e-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c3c5e-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="c3c5e-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c3c5e-118">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="c3c5e-118">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
