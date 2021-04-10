---
description: Verifica se a região de mídia na unidade de DVD corresponde à região da unidade de DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: Função DvdLauncher
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089442"
---
# <a name="dvdlauncher-function"></a><span data-ttu-id="4679f-103">Função DvdLauncher</span><span class="sxs-lookup"><span data-stu-id="4679f-103">DvdLauncher function</span></span>

<span data-ttu-id="4679f-104">Verifica se a região de mídia na unidade de DVD corresponde à região da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="4679f-104">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>

## <a name="syntax"></a><span data-ttu-id="4679f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4679f-105">Syntax</span></span>


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="4679f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4679f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4679f-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4679f-107">*HWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4679f-108">Um identificador para a janela de nível superior a ser usado para qualquer interface do usuário necessária.</span><span class="sxs-lookup"><span data-stu-id="4679f-108">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="4679f-109">*Letra_da_unidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4679f-109">*DriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4679f-110">A letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="4679f-110">The drive letter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4679f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4679f-111">Return value</span></span>

<span data-ttu-id="4679f-112">Se a função for bem sucedido e as regiões corresponderem, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="4679f-112">If the function succeeds and the regions match, the return value is nonzero.</span></span> <span data-ttu-id="4679f-113">Caso contrário, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="4679f-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4679f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4679f-114">Remarks</span></span>

<span data-ttu-id="4679f-115">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="4679f-115">This function has no associated import library.</span></span> <span data-ttu-id="4679f-116">Você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a StorProp.dll.</span><span class="sxs-lookup"><span data-stu-id="4679f-116">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to StorProp.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="4679f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4679f-117">Requirements</span></span>



| <span data-ttu-id="4679f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4679f-118">Requirement</span></span> | <span data-ttu-id="4679f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4679f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4679f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4679f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4679f-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4679f-121">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4679f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4679f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4679f-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4679f-123">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4679f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4679f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4679f-125"><dt>StorProp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4679f-125"><dt>StorProp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4679f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4679f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4679f-127">Funções de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4679f-127">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

