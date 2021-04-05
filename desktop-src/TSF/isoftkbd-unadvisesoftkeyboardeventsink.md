---
title: Método ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc. h)
description: O método ISoftKbd UnadviseSoftKeyboardEventSink remove um coletor de eventos de teclado flexível.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Estrutura de serviços de texto do método UnadviseSoftKeyboardEventSink
- Método UnadviseSoftKeyboardEventSink de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método UnadviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644971"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="88f23-106">Método ISoftKbd:: UnadviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="88f23-106">ISoftKbd::UnadviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="88f23-107">O método **ISoftKbd:: UnadviseSoftKeyboardEventSink** remove um coletor de eventos de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="88f23-107">The **ISoftKbd::UnadviseSoftKeyboardEventSink** method removes a soft keyboard event sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f23-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88f23-108">Syntax</span></span>


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a><span data-ttu-id="88f23-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88f23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88f23-110">*tid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88f23-110">*tid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88f23-111">Identificador do cliente que possui o coletor de eventos de teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="88f23-111">Identifier of the client that owns the soft keyboard event sink.</span></span> <span data-ttu-id="88f23-112">Esse valor foi passado quando o coletor de eventos foi instalado usando [ISoftKbd:: AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span><span class="sxs-lookup"><span data-stu-id="88f23-112">This value was passed when the event sink was installed using [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88f23-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88f23-113">Return value</span></span>

<span data-ttu-id="88f23-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="88f23-114">This method can return one of these values.</span></span>



| <span data-ttu-id="88f23-115">Valor</span><span class="sxs-lookup"><span data-stu-id="88f23-115">Value</span></span>                                                                                                   | <span data-ttu-id="88f23-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="88f23-116">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="88f23-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88f23-117"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="88f23-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="88f23-118">The method was successful.</span></span><br/>                         |
| <dl> <span data-ttu-id="88f23-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="88f23-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="88f23-120">O parâmetro *tid* é inválido.</span><span class="sxs-lookup"><span data-stu-id="88f23-120">The *tid* parameter is invalid.</span></span><br/>                    |
| <dl> <span data-ttu-id="88f23-121"><dt>**CONECTAR \_ E \_ noconnection**</dt></span><span class="sxs-lookup"><span data-stu-id="88f23-121"><dt>**CONNECT\_E\_NOCONNECTION**</dt></span></span> </dl> | <span data-ttu-id="88f23-122">O coletor de aviso identificado pelo *tid* não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="88f23-122">The advise sink identified by *tid* was not found.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="88f23-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88f23-123">Requirements</span></span>



| <span data-ttu-id="88f23-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="88f23-124">Requirement</span></span> | <span data-ttu-id="88f23-125">Valor</span><span class="sxs-lookup"><span data-stu-id="88f23-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88f23-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88f23-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88f23-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88f23-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="88f23-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88f23-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88f23-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88f23-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="88f23-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="88f23-130">Redistributable</span></span><br/>          | <span data-ttu-id="88f23-131">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="88f23-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="88f23-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88f23-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="88f23-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="88f23-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="88f23-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="88f23-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88f23-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88f23-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="88f23-136">DLL</span><span class="sxs-lookup"><span data-stu-id="88f23-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88f23-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88f23-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f23-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="88f23-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f23-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="88f23-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="88f23-140">ISoftKbd::AdviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="88f23-140">ISoftKbd::AdviseSoftKeyboardEventSink</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





