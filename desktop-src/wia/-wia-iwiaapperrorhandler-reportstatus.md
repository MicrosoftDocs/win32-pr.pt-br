---
description: Lida com o status do dispositivo e mensagens de erro durante transferências de dados de imagem e exibe as mensagens para o usuário.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'Método IWiaAppErrorHandler:: ReportStatus (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811658"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a><span data-ttu-id="04336-103">Método IWiaAppErrorHandler:: ReportStatus</span><span class="sxs-lookup"><span data-stu-id="04336-103">IWiaAppErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="04336-104">Lida com o status do dispositivo e mensagens de erro durante transferências de dados de imagem e exibe as mensagens para o usuário.</span><span class="sxs-lookup"><span data-stu-id="04336-104">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="04336-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04336-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a><span data-ttu-id="04336-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04336-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04336-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04336-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04336-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="04336-108">Type: **LONG**</span></span>

<span data-ttu-id="04336-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="04336-109">Not used.</span></span> <span data-ttu-id="04336-110">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="04336-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="04336-111">*pWiaItem2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04336-111">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04336-112">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="04336-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="04336-113">Ponteiro para o item que está sendo transferido.</span><span class="sxs-lookup"><span data-stu-id="04336-113">Pointer to the item being transferred.</span></span>

</dd> <dt>

<span data-ttu-id="04336-114">_hrStatus \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04336-114">_hrStatus\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04336-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="04336-115">Type: **HRESULT**</span></span>

<span data-ttu-id="04336-116">Código de status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04336-116">Device status code.</span></span>

</dd> <dt>

<span data-ttu-id="04336-117">*lPercentComplete* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04336-117">*lPercentComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04336-118">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="04336-118">Type: **LONG**</span></span>

<span data-ttu-id="04336-119">Porcentagem concluída da operação atual.</span><span class="sxs-lookup"><span data-stu-id="04336-119">Percentage completed of current operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04336-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04336-120">Return value</span></span>

<span data-ttu-id="04336-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="04336-121">Type: **HRESULT**</span></span>

<span data-ttu-id="04336-122">Retorna *hrStatus* se a recuperação do erro não for possível.</span><span class="sxs-lookup"><span data-stu-id="04336-122">Returns *hrStatus* if recovery from the error is not possible.</span></span> <span data-ttu-id="04336-123">Caso contrário, ele retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="04336-123">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="04336-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="04336-124">Return code</span></span>                                                                                              | <span data-ttu-id="04336-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="04336-125">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04336-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04336-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="04336-127">Se *hrStatus* for um erro, a ação apropriada foi executada para corrigir o erro e a transferência poderá continuar.</span><span class="sxs-lookup"><span data-stu-id="04336-127">If *hrStatus* is an error, the appropriate action was taken to correct the error, and the transfer can continue.</span></span> <span data-ttu-id="04336-128">Se *hrStatus* for informativo, o usuário foi informado com uma caixa de diálogo sem janela restrita e optou por não cancelar a transferência.</span><span class="sxs-lookup"><span data-stu-id="04336-128">If *hrStatus* is informational, the user was informed with a modeless dialog box and chose not to cancel the transfer.</span></span><br/> |
| <dl> <span data-ttu-id="04336-129"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="04336-129"><dt>**S\_FALSE**</dt></span></span> </dl>                  | <span data-ttu-id="04336-130">O usuário cancelou a transferência da caixa de diálogo sem janela restrita de manipulador de erros.</span><span class="sxs-lookup"><span data-stu-id="04336-130">The user cancelled the transfer from the error handler modeless dialog box.</span></span> <span data-ttu-id="04336-131">Esse valor pode ser retornado em qualquer ponto, independentemente do que *hrStatus* é.</span><span class="sxs-lookup"><span data-stu-id="04336-131">This value can be returned at any point no matter what *hrStatus* is.</span></span> <br/>                                                                                      |
| <dl> <span data-ttu-id="04336-132"><dt>**\_status WIA \_ não \_ Tratado**</dt></span><span class="sxs-lookup"><span data-stu-id="04336-132"><dt>**WIA\_STATUS\_NOT\_HANDLED**</dt></span></span> </dl> | <span data-ttu-id="04336-133">Nenhuma ação foi executada; ou seja, nenhuma caixa de diálogo foi apresentada ao usuário.</span><span class="sxs-lookup"><span data-stu-id="04336-133">No action was taken; that is, no dialog box was presented to the user.</span></span> <span data-ttu-id="04336-134">O próximo manipulador de erro será invocado.</span><span class="sxs-lookup"><span data-stu-id="04336-134">The next error handler will be invoked.</span></span> <span data-ttu-id="04336-135">A ordem dos manipuladores de erro é: aplicativo, Driver e padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="04336-135">The order of error handlers is: application, driver, and system default.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="04336-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="04336-136">Remarks</span></span>

<span data-ttu-id="04336-137">O parâmetro *lPercentComplete* habilita uma janela de manipulador de erros para mostrar o progresso.</span><span class="sxs-lookup"><span data-stu-id="04336-137">The *lPercentComplete* parameter enables an error handler window to show progress.</span></span> <span data-ttu-id="04336-138">Por exemplo, um driver pode fornecer uma estimativa de quanto tempo o "aquecimento" leva.</span><span class="sxs-lookup"><span data-stu-id="04336-138">For example, a driver might provide an estimate of how long "warming up" takes.</span></span> <span data-ttu-id="04336-139">O parâmetro *lPercentComplete* passado para **IWiaAppErrorHandler:: ReportStatus** é o mesmo valor que o **lPercentComplete** que o driver define na estrutura [**WiaTransferParams**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="04336-139">The *lPercentComplete* parameter passed into **IWiaAppErrorHandler::ReportStatus** is the same value as the **lPercentComplete** that the driver sets into the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

<span data-ttu-id="04336-140">Um manipulador de erro pode usar as macros com êxito e com falha para descobrir se *hrStatus* tem erro de severidade \_ ou êxito na severidade \_ .</span><span class="sxs-lookup"><span data-stu-id="04336-140">An error handler can use the SUCCEEDED and FAILED macros to find out if *hrStatus* has SEVERITY\_ERROR or SEVERITY\_SUCCESS.</span></span>

<span data-ttu-id="04336-141">Se *hrStatus* for \_ êxito na gravidade, o usuário deverá ter permissão para cancelar a transferência.</span><span class="sxs-lookup"><span data-stu-id="04336-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

<span data-ttu-id="04336-142">Se *hrStatus* for um \_ erro de gravidade, o manipulador de erro deverá exibir uma caixa de diálogo modal pertencente à janela pai do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04336-142">If *hrStatus* is SEVERITY\_ERROR, the error handler should display a modal dialog box owned by the application parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="04336-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04336-143">Requirements</span></span>



| <span data-ttu-id="04336-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="04336-144">Requirement</span></span> | <span data-ttu-id="04336-145">Valor</span><span class="sxs-lookup"><span data-stu-id="04336-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04336-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04336-146">Minimum supported client</span></span><br/> | <span data-ttu-id="04336-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04336-147">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="04336-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04336-148">Minimum supported server</span></span><br/> | <span data-ttu-id="04336-149">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04336-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="04336-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04336-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="04336-151"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="04336-151"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="04336-152">INSERI</span><span class="sxs-lookup"><span data-stu-id="04336-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04336-153"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04336-153"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="04336-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04336-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="04336-155"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04336-155"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




