---
title: Método ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc. h)
description: O método ISoftKbd AdviseSoftKeyboardEventSink instala um coletor de eventos de teclado flexível para lidar com notificações OnKeySelection do teclado soft.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Estrutura de serviços de texto do método AdviseSoftKeyboardEventSink
- Método AdviseSoftKeyboardEventSink de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método AdviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369811"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="12d81-106">Método ISoftKbd:: AdviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="12d81-106">ISoftKbd::AdviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="12d81-107">O método **ISoftKbd:: AdviseSoftKeyboardEventSink** instala um coletor de eventos de teclado flexível para lidar com notificações OnKeySelection do teclado soft.</span><span class="sxs-lookup"><span data-stu-id="12d81-107">The **ISoftKbd::AdviseSoftKeyboardEventSink** method installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d81-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12d81-108">Syntax</span></span>


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a><span data-ttu-id="12d81-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12d81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d81-110">*dwKeyboardId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12d81-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d81-111">Identificador do teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="12d81-111">Identifier of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="12d81-112">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12d81-112">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d81-113">Identificador de interface para a interface do coletor.</span><span class="sxs-lookup"><span data-stu-id="12d81-113">Interface identifier for the sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="12d81-114">*punk* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12d81-114">*punk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d81-115">Ponteiro para [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a interface do coletor especificada por *riid*.</span><span class="sxs-lookup"><span data-stu-id="12d81-115">Pointer to [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) for the sink interface specified by *riid*.</span></span> <span data-ttu-id="12d81-116">Este parâmetro não pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="12d81-116">This parameter cannot be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="12d81-117">*pdwCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="12d81-117">*pdwCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12d81-118">Ponteiro para o buffer no qual esse método recupera o "cookie" do teclado virtual usado para conexão com o cliente.</span><span class="sxs-lookup"><span data-stu-id="12d81-118">Pointer to the buffer in which this method retrieves the soft keyboard "cookie" used for connection to the client.</span></span> <span data-ttu-id="12d81-119">O cookie deve ser exclusivo para cada conexão.</span><span class="sxs-lookup"><span data-stu-id="12d81-119">The cookie must be unique for each connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d81-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12d81-120">Return value</span></span>

<span data-ttu-id="12d81-121">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="12d81-121">This method can return one of these values.</span></span>



| <span data-ttu-id="12d81-122">Valor</span><span class="sxs-lookup"><span data-stu-id="12d81-122">Value</span></span>                                                                                        | <span data-ttu-id="12d81-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="12d81-123">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="12d81-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12d81-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="12d81-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="12d81-125">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="12d81-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="12d81-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="12d81-127">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="12d81-127">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="12d81-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12d81-128">Requirements</span></span>



| <span data-ttu-id="12d81-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d81-129">Requirement</span></span> | <span data-ttu-id="12d81-130">Valor</span><span class="sxs-lookup"><span data-stu-id="12d81-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12d81-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12d81-131">Minimum supported client</span></span><br/> | <span data-ttu-id="12d81-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="12d81-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="12d81-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12d81-133">Minimum supported server</span></span><br/> | <span data-ttu-id="12d81-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="12d81-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="12d81-135">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="12d81-135">Redistributable</span></span><br/>          | <span data-ttu-id="12d81-136">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="12d81-136">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="12d81-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12d81-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d81-138"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="12d81-138"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="12d81-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="12d81-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12d81-140"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12d81-140"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="12d81-141">DLL</span><span class="sxs-lookup"><span data-stu-id="12d81-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d81-142"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12d81-142"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d81-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="12d81-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d81-144">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="12d81-144">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="12d81-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="12d81-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

