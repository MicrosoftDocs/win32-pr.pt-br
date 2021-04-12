---
description: Define o computador de reprodução atual para o log de gráficos especificado.
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine2:: SetPlaybackMachine'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d7366da4aa999828309136900edfe725af4f622
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500716"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span data-ttu-id="804fc-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>Método IPixEngine2:: SetPlaybackMachine</span><span class="sxs-lookup"><span data-stu-id="804fc-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2::SetPlaybackMachine method</span></span>

<span data-ttu-id="804fc-104">Define o computador de reprodução atual para o log de gráficos especificado.</span><span class="sxs-lookup"><span data-stu-id="804fc-104">Sets the current playback machine for the specified graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="804fc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="804fc-105">Syntax</span></span>


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a><span data-ttu-id="804fc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="804fc-106">Parameters</span></span>

<span data-ttu-id="804fc-107">*Restaura* </span><span class="sxs-lookup"><span data-stu-id="804fc-107">*logFile* </span></span>  
<span data-ttu-id="804fc-108">Uma cadeia de caracteres COM contianing o nome do log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="804fc-108">A COM string contianing the name of the graphics log.</span></span>

<span data-ttu-id="804fc-109">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="804fc-109">*bUseAuthentication* </span></span>  
<span data-ttu-id="804fc-110">true para usar a autenticação; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="804fc-110">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="804fc-111">*Tradução* </span><span class="sxs-lookup"><span data-stu-id="804fc-111">*machine* </span></span>  
<span data-ttu-id="804fc-112">Uma cadeia de caracteres COM que contém o nome da máquina de reprodução.</span><span class="sxs-lookup"><span data-stu-id="804fc-112">A COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="804fc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="804fc-113">Return value</span></span>

<span data-ttu-id="804fc-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="804fc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="804fc-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="804fc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="804fc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="804fc-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="804fc-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="804fc-117">Header</span></span></p></td><td><span data-ttu-id="804fc-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="804fc-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="804fc-119"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="804fc-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="804fc-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="804fc-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
