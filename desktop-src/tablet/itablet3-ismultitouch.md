---
description: Determina se um dispositivo de entrada dá suporte a multitoque.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'Método ITablet3:: IsMultiTouch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171158"
---
# <a name="itablet3ismultitouch-method"></a><span data-ttu-id="d48d6-103">Método ITablet3:: IsMultiTouch</span><span class="sxs-lookup"><span data-stu-id="d48d6-103">ITablet3::IsMultiTouch method</span></span>

<span data-ttu-id="d48d6-104">Determina se um dispositivo de entrada dá suporte a multitoque.</span><span class="sxs-lookup"><span data-stu-id="d48d6-104">Determines whether an input device supports multitouch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d48d6-105">Syntax</span></span>


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a><span data-ttu-id="d48d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d48d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d48d6-107">*bIsMultiTouch* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d48d6-107">*bIsMultiTouch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d48d6-108">Indica se o dispositivo é multitoque.</span><span class="sxs-lookup"><span data-stu-id="d48d6-108">Indicates whether the device is multitouch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d48d6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d48d6-109">Return value</span></span>

<span data-ttu-id="d48d6-110">Retorna **S \_ OK** em caso de êxito; caso contrário, retorna um código de erro como **E \_ falha**.</span><span class="sxs-lookup"><span data-stu-id="d48d6-110">Returns **S\_OK** on success, otherwise returns an error code such as **E\_FAIL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d48d6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d48d6-111">Remarks</span></span>

<span data-ttu-id="d48d6-112">Depois de determinar por meio de [**IRealTimeStylus3:: MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) ou **ITablet3:: IsMultiTouch** que multitoque está disponível, um aplicativo pode optar por aceitar as mensagens de entrada de multitoque.</span><span class="sxs-lookup"><span data-stu-id="d48d6-112">After determining through [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) or **ITablet3::IsMultiTouch** that multitouch is available, an application may choose to opt in for multitouch input messages.</span></span> <span data-ttu-id="d48d6-113">Informações adicionais sobre como filtrar métodos multitoque estão disponíveis na seção da propriedade **IRealTimeStylus3:: MultiTouchEnabled** .</span><span class="sxs-lookup"><span data-stu-id="d48d6-113">Additional information on filtering multitouch methods is available in the **IRealTimeStylus3::MultiTouchEnabled** property section.</span></span>

## <a name="examples"></a><span data-ttu-id="d48d6-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d48d6-114">Examples</span></span>


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a><span data-ttu-id="d48d6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d48d6-115">Requirements</span></span>



| <span data-ttu-id="d48d6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d48d6-116">Requirement</span></span> | <span data-ttu-id="d48d6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d48d6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d48d6-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d48d6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d48d6-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d48d6-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d48d6-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d48d6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d48d6-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d48d6-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d48d6-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d48d6-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="d48d6-123"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d48d6-123"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48d6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d48d6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48d6-125">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="d48d6-125">**ITablet3**</span></span>](itablet3.md)
</dt> <dt>

[<span data-ttu-id="d48d6-126">**MultiTouchEnabled**</span><span class="sxs-lookup"><span data-stu-id="d48d6-126">**MultiTouchEnabled**</span></span>](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




