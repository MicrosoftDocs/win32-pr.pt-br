---
description: Uma função de retorno de chamada usada para notificar o host de informações sobre os arquivos de origem associados à pilha de chamadas.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ISourceFileInfoCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a60122615cf15e9ed39ae7809e574c4d3d0c1146
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088785"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span data-ttu-id="0a758-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>Método ISourceFileInfoCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="0a758-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback::ResultCallback method</span></span>

<span data-ttu-id="0a758-104">Uma função de retorno de chamada usada para notificar o host de informações sobre os arquivos de origem associados à pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="0a758-104">A callback function used to notify the host of information about source files associated with the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a758-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a758-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="0a758-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a758-106">Parameters</span></span>

<span data-ttu-id="0a758-107">*contar* </span><span class="sxs-lookup"><span data-stu-id="0a758-107">*count* </span></span>  
<span data-ttu-id="0a758-108">O número de arquivos de origem retornados.</span><span class="sxs-lookup"><span data-stu-id="0a758-108">The number of source files returned.</span></span>

<span data-ttu-id="0a758-109">*count0 \_ sourceFileInfoBuffer* </span><span class="sxs-lookup"><span data-stu-id="0a758-109">*count0\_sourceFileInfoBuffer* </span></span>  
<span data-ttu-id="0a758-110">Os arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="0a758-110">The source files.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a758-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a758-111">Return value</span></span>

<span data-ttu-id="0a758-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0a758-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a758-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a758-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a758-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a758-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0a758-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a758-115">Header</span></span></p></td><td><span data-ttu-id="0a758-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0a758-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0a758-117"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="0a758-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0a758-118">**ISourceFileInfoCallback**</span><span class="sxs-lookup"><span data-stu-id="0a758-118">**ISourceFileInfoCallback**</span></span>](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
