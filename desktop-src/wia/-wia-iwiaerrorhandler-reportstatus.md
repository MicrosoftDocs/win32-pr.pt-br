---
description: Manipula mensagens de status e de erro durante transferências de dados de imagem e as exibe para o usuário.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'Método IWiaErrorHandler:: ReportStatus (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756662"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a><span data-ttu-id="e7bbb-103">Método IWiaErrorHandler:: ReportStatus</span><span class="sxs-lookup"><span data-stu-id="e7bbb-103">IWiaErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="e7bbb-104">Manipula mensagens de status e de erro durante transferências de dados de imagem e as exibe para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-104">Handles status and error messages during image data transfers and displays them to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bbb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7bbb-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a><span data-ttu-id="e7bbb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7bbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7bbb-107">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbb-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbb-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="e7bbb-108">Type: **HWND**</span></span>

<span data-ttu-id="e7bbb-109">**HWND** que é a janela pai da janela de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-109">**HWND** that is the parent window for the message window.</span></span>

</dd> <dt>

<span data-ttu-id="e7bbb-110">*punkItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbb-110">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbb-111">Tipo: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="e7bbb-111">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="e7bbb-112">Ponteiro para a interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) do item que está sendo transferido.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-112">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the item being transferred.</span></span> <span data-ttu-id="e7bbb-113">Esse objeto implementa minimamente [_ *IWiaItem2* \*](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="e7bbb-113">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="e7bbb-114">*hrStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbb-114">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbb-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7bbb-115">Type: **HRESULT**</span></span>

<span data-ttu-id="e7bbb-116">**HRESULT** que é o código de status recebido por [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="e7bbb-116">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="e7bbb-117">*cbResLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbb-117">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbb-118">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="e7bbb-118">Type: **LONG**</span></span>

<span data-ttu-id="e7bbb-119">**Longo** que é o tamanho dos dados referenciados por *pbData*.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-119">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="e7bbb-120">*pbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bbb-120">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bbb-121">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="e7bbb-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="e7bbb-122">Ponteiro para o buffer de dados como recebido por [_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="e7bbb-122">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7bbb-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7bbb-123">Return value</span></span>

<span data-ttu-id="e7bbb-124">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7bbb-124">Type: **HRESULT**</span></span>

<span data-ttu-id="e7bbb-125">Retorna *hrStatus* se o erro não puder ser recuperado de.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-125">Returns *hrStatus* if the error cannot be recovered from.</span></span> <span data-ttu-id="e7bbb-126">Caso contrário, ele retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-126">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="e7bbb-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e7bbb-127">Return code</span></span>                                                                             | <span data-ttu-id="e7bbb-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7bbb-128">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7bbb-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbb-129"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e7bbb-130">A ação apropriada foi tomada para corrigir o erro e a transferência pode continuar.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-130">The appropriate action was taken to correct the error and the transfer can continue.</span></span> <br/> |
| <dl> <span data-ttu-id="e7bbb-131"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbb-131"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e7bbb-132">Nenhuma ação foi tomada para manipular o erro ou o status do relatório para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-132">No action was taken to handle the error or report status to the user.</span></span> <br/>                |
| <dl> <span data-ttu-id="e7bbb-133"><dt>**E \_ anular**</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbb-133"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="e7bbb-134">O usuário optou por anular a transferência em resposta à caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-134">The user chose to abort the transfer in response to the displayed dialog box.</span></span> <br/>        |



 

## <a name="remarks"></a><span data-ttu-id="e7bbb-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7bbb-135">Remarks</span></span>

<span data-ttu-id="e7bbb-136">O WIA (Windows Image Acquisition) 2,0 chama **IWiaErrorHandler:: ReportStatus** quando o driver envia uma mensagem de **\_ \_ \_ status do dispositivo msg de ti** para [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="e7bbb-136">Windows Image Acquisition (WIA) 2.0 calls **IWiaErrorHandler::ReportStatus** when the driver sends an **IT\_MSG\_DEVICE\_STATUS** message to [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span> <span data-ttu-id="e7bbb-137">Esse método manipula a mensagem e exibe informações para o usuário sobre o status ou o erro.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-137">This method handles the message and displays information to the user about the status or error.</span></span> <span data-ttu-id="e7bbb-138">Se a mensagem for sobre um erro, o método permitirá que o usuário escolha, se possível, se deseja tentar se recuperar do erro e continuar a transferência ou para anular.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-138">If the message is about an error, the method lets the user choose, if possible, whether to try to recover from the error and continue the transfer or to abort.</span></span>

<span data-ttu-id="e7bbb-139">*hrStatus* é definido como a \_ transferência de status \_ do WIA \_ comece a informar ao manipulador que uma transferência foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-139">*hrStatus* is set to WIA\_STATUS\_TRANSFER\_BEGIN to inform the handler a transfer has started.</span></span> <span data-ttu-id="e7bbb-140">Ele é definido como \_ \_ \_ término da transferência de status do WIA quando a transferência é concluída.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-140">It is set to WIA\_STATUS\_TRANSFER\_END when the transfer is complete.</span></span>

<span data-ttu-id="e7bbb-141">Se *hrStatus* for \_ êxito na gravidade, o usuário deverá ter permissão para cancelar a transferência.</span><span class="sxs-lookup"><span data-stu-id="e7bbb-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7bbb-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7bbb-142">Requirements</span></span>



| <span data-ttu-id="e7bbb-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7bbb-143">Requirement</span></span> | <span data-ttu-id="e7bbb-144">Valor</span><span class="sxs-lookup"><span data-stu-id="e7bbb-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bbb-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bbb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bbb-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7bbb-146">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e7bbb-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bbb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bbb-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7bbb-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e7bbb-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7bbb-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7bbb-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbb-150"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="e7bbb-151">INSERI</span><span class="sxs-lookup"><span data-stu-id="e7bbb-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7bbb-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbb-152"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="e7bbb-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7bbb-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7bbb-154"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7bbb-154"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
