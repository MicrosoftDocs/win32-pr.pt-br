---
description: Obtém informações sobre o computador de reprodução atual.
MS-HAID: vspixengine.IPixEngine2\_GetPlaybackMachine\_BSTR\_BOOL\_ptr\_BSTR\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine2:: GetPlaybackMachine'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D6C3C391-F039-4A5A-AA88-87A3624ECAD2
api_name:
- IPixEngine2.GetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c572d1a87fb537fd53a7f3e8f8048d1046980b20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812223"
---
# <a name="span-idvspixengineipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptrspanipixengine2getplaybackmachine-method"></a><span data-ttu-id="42890-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>Método IPixEngine2:: GetPlaybackMachine</span><span class="sxs-lookup"><span data-stu-id="42890-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>IPixEngine2::GetPlaybackMachine method</span></span>

<span data-ttu-id="42890-104">Obtém informações sobre o computador de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="42890-104">Gets information about the current playback machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="42890-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42890-105">Syntax</span></span>


```C++
HRESULT GetPlaybackMachine(
   BSTR   logFile,
   BOOL * pUseAuthentication,
   BSTR * pMachine
);
```

## <a name="parameters"></a><span data-ttu-id="42890-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42890-106">Parameters</span></span>

<span data-ttu-id="42890-107">*Restaura* </span><span class="sxs-lookup"><span data-stu-id="42890-107">*logFile* </span></span>  
<span data-ttu-id="42890-108">Uma cadeia de caracteres COM que contém o nome do log de gráficos associado.</span><span class="sxs-lookup"><span data-stu-id="42890-108">A COM string containing the name of the associated graphics log.</span></span>

<span data-ttu-id="42890-109">*pUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="42890-109">*pUseAuthentication* </span></span>  
<span data-ttu-id="42890-110">Em retorno, true se a conexão usar autenticação; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="42890-110">On return, true if the connection uses authentication; otherwise, false.</span></span>

<span data-ttu-id="42890-111">*pMachine* </span><span class="sxs-lookup"><span data-stu-id="42890-111">*pMachine* </span></span>  
<span data-ttu-id="42890-112">No retorno, uma cadeia de caracteres COM que contém o nome da máquina de reprodução.</span><span class="sxs-lookup"><span data-stu-id="42890-112">On return, a COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="42890-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42890-113">Return value</span></span>

<span data-ttu-id="42890-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="42890-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42890-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42890-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="42890-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42890-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="42890-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42890-117">Header</span></span></p></td><td><span data-ttu-id="42890-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="42890-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="42890-119"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="42890-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="42890-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="42890-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
