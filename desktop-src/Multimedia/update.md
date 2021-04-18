---
title: Atualizar comando
description: O comando Update redesenha o quadro atual no contexto de dispositivo especificado (DC). Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- atualizar o comando multimídia do Windows
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499769"
---
# <a name="update-command"></a><span data-ttu-id="73c4d-105">Atualizar comando</span><span class="sxs-lookup"><span data-stu-id="73c4d-105">update command</span></span>

<span data-ttu-id="73c4d-106">O comando Update redesenha o quadro atual no contexto de dispositivo especificado (DC).</span><span class="sxs-lookup"><span data-stu-id="73c4d-106">The update command repaints the current frame into the specified device context (DC).</span></span> <span data-ttu-id="73c4d-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="73c4d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="73c4d-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="73c4d-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="73c4d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73c4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c4d-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="73c4d-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="73c4d-111">Identificador de um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="73c4d-111">Identifier of an MCI device.</span></span> <span data-ttu-id="73c4d-112">Esse identificador ou alias é atribuído quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="73c4d-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="73c4d-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span><span class="sxs-lookup"><span data-stu-id="73c4d-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span></span>
</dt> <dd>

<span data-ttu-id="73c4d-114">Identificador de um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="73c4d-114">Handle of a DC.</span></span> <span data-ttu-id="73c4d-115">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **atualização** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="73c4d-115">The following table lists device types that recognize the **update** command and the flags used by each type.</span></span>



| <span data-ttu-id="73c4d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="73c4d-116">Value</span></span>        | <span data-ttu-id="73c4d-117">Significado</span><span class="sxs-lookup"><span data-stu-id="73c4d-117">Meaning</span></span>                       | <span data-ttu-id="73c4d-118">Significado</span><span class="sxs-lookup"><span data-stu-id="73c4d-118">Meaning</span></span>         |
|--------------|-------------------------------|-----------------|
| <span data-ttu-id="73c4d-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="73c4d-119">digitalvideo</span></span> | <span data-ttu-id="73c4d-120">HDC *HDC* HDC *HDC* em *Rect*</span><span class="sxs-lookup"><span data-stu-id="73c4d-120">hdc *hdc* hdc *hdc* at *rect*</span></span> | <span data-ttu-id="73c4d-121">pintar HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="73c4d-121">paint hdc *hdc*</span></span> |



 

<span data-ttu-id="73c4d-122">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszHDC** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="73c4d-122">The following table lists the flags that can be specified in the **lpszHDC** parameter and their meanings.</span></span>



| <span data-ttu-id="73c4d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="73c4d-123">Value</span></span>               | <span data-ttu-id="73c4d-124">Significado</span><span class="sxs-lookup"><span data-stu-id="73c4d-124">Meaning</span></span>                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c4d-125">HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="73c4d-125">hdc *hdc*</span></span>           | <span data-ttu-id="73c4d-126">Especifica o identificador do DC a ser pintado.</span><span class="sxs-lookup"><span data-stu-id="73c4d-126">Specifies the handle of the DC to paint.</span></span>                                                               |
| <span data-ttu-id="73c4d-127">HDC *HDC* at *Rect*</span><span class="sxs-lookup"><span data-stu-id="73c4d-127">hdc *hdc* at *rect*</span></span> | <span data-ttu-id="73c4d-128">Especifica o retângulo de recorte relativo ao retângulo do cliente.</span><span class="sxs-lookup"><span data-stu-id="73c4d-128">Specifies the clipping rectangle relative to the client rectangle.</span></span>                                     |
| <span data-ttu-id="73c4d-129">pintar HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="73c4d-129">paint hdc *hdc*</span></span>     | <span data-ttu-id="73c4d-130">Pinta o controlador de domínio quando o aplicativo recebe uma mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) destinada a um DC.</span><span class="sxs-lookup"><span data-stu-id="73c4d-130">Paints the DC when the application receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message intended for a DC.</span></span> |



 

<span data-ttu-id="73c4d-131">Para especificar o identificador do controlador de domínio, use a cadeia de caracteres "hdc" seguida de uma representação ASCII do identificador.</span><span class="sxs-lookup"><span data-stu-id="73c4d-131">To specify the handle of the DC, use the string "hdc" followed by an ASCII representation of the handle.</span></span> <span data-ttu-id="73c4d-132">O retângulo é especificado como **X1 Y1 x2 y2**.</span><span class="sxs-lookup"><span data-stu-id="73c4d-132">The rectangle is specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="73c4d-133">As coordenadas **X1 Y1** especificam o canto superior esquerdo do retângulo, e as coordenadas **x2 y2** especificam a largura e a altura.</span><span class="sxs-lookup"><span data-stu-id="73c4d-133">The coordinates **X1 Y1** specify the upper left corner of the rectangle, and the coordinates **X2 Y2** specify the width and height.</span></span>

</dd> <dt>

<span data-ttu-id="73c4d-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="73c4d-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="73c4d-135">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="73c4d-135">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="73c4d-136">Para dispositivos de vídeo digital, "teste" também pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="73c4d-136">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="73c4d-137">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="73c4d-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c4d-138">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="73c4d-138">Return Value</span></span>

<span data-ttu-id="73c4d-139">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="73c4d-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="73c4d-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73c4d-140">Examples</span></span>

<span data-ttu-id="73c4d-141">O comando a seguir atualiza toda a janela de exibição usada pelo dispositivo "filme".</span><span class="sxs-lookup"><span data-stu-id="73c4d-141">The following command updates the entire display window used by the "movie" device.</span></span> <span data-ttu-id="73c4d-142">O número 203 é um identificador para um controlador de domínio obtido da função [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .</span><span class="sxs-lookup"><span data-stu-id="73c4d-142">The number 203 is a handle to a DC obtained from the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span>

``` syntax
update movie hdc 203
```

## <a name="requirements"></a><span data-ttu-id="73c4d-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73c4d-143">Requirements</span></span>



| <span data-ttu-id="73c4d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="73c4d-144">Requirement</span></span> | <span data-ttu-id="73c4d-145">Valor</span><span class="sxs-lookup"><span data-stu-id="73c4d-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="73c4d-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73c4d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="73c4d-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="73c4d-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="73c4d-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73c4d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="73c4d-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="73c4d-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="73c4d-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="73c4d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c4d-151">MCI</span><span class="sxs-lookup"><span data-stu-id="73c4d-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="73c4d-152">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="73c4d-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

