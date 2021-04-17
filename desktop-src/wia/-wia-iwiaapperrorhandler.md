---
description: A interface IWiaAppErrorHandler permite que os aplicativos exibam janelas de erro (durante transferências de dados) da qual o usuário pode escolher se deseja continuar, cancelar ou anular a transferência.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interface IWiaAppErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105795469"
---
# <a name="iwiaapperrorhandler-interface"></a><span data-ttu-id="5ece5-103">Interface IWiaAppErrorHandler</span><span class="sxs-lookup"><span data-stu-id="5ece5-103">IWiaAppErrorHandler interface</span></span>

<span data-ttu-id="5ece5-104">A interface **IWiaAppErrorHandler** permite que os aplicativos exibam janelas de erro (durante transferências de dados) da qual o usuário pode escolher se deseja continuar, cancelar ou anular a transferência.</span><span class="sxs-lookup"><span data-stu-id="5ece5-104">The **IWiaAppErrorHandler** interface enables applications to display error windows (during data transfers) from which the user can choose whether to continue, cancel, or abort the transfer.</span></span>

## <a name="members"></a><span data-ttu-id="5ece5-105">Membros</span><span class="sxs-lookup"><span data-stu-id="5ece5-105">Members</span></span>

<span data-ttu-id="5ece5-106">A interface **IWiaAppErrorHandler** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5ece5-106">The **IWiaAppErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5ece5-107">**IWiaAppErrorHandler** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5ece5-107">**IWiaAppErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="5ece5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ece5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5ece5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ece5-109">Methods</span></span>

<span data-ttu-id="5ece5-110">A interface **IWiaAppErrorHandler** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5ece5-110">The **IWiaAppErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="5ece5-111">Método</span><span class="sxs-lookup"><span data-stu-id="5ece5-111">Method</span></span>                                                        | <span data-ttu-id="5ece5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ece5-112">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ece5-113">**GetWindow**</span><span class="sxs-lookup"><span data-stu-id="5ece5-113">**GetWindow**</span></span>](-wia-iwiaapperrorhandler-getwindow.md)       | <span data-ttu-id="5ece5-114">Obtém um identificador para a caixa de diálogo que exibe mensagens de erro e fornece um ou mais botões para continuar, cancelar ou anular o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ece5-114">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span><br/> |
| [<span data-ttu-id="5ece5-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="5ece5-115">**ReportStatus**</span></span>](-wia-iwiaapperrorhandler-reportstatus.md) | <span data-ttu-id="5ece5-116">Lida com o status do dispositivo e mensagens de erro durante transferências de dados de imagem e exibe as mensagens para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5ece5-116">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="5ece5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ece5-117">Remarks</span></span>

<span data-ttu-id="5ece5-118">O objeto de tratamento de erros, ou retorno de chamada, que implementa essa interface é passado para [**IWiaTransfer::D aixar**](-wia-iwiatransfer-download.md) e [**IWiaTransfer:: upload**](-wia-iwiatransfer-upload.md).</span><span class="sxs-lookup"><span data-stu-id="5ece5-118">The error handling, or callback, object that implements this interface is passed into [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) and [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).</span></span>

<span data-ttu-id="5ece5-119">Esta interface não foi projetada para lidar com erros encontrados fora das transferências de dados de imagem, por exemplo, erros ao obter ou definir propriedades de dispositivo ou retornos de chamada não retornados em um driver.</span><span class="sxs-lookup"><span data-stu-id="5ece5-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

<span data-ttu-id="5ece5-120">Um manipulador de erro de driver deve implementar [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), em vez de **IWiaAppErrorHandler**.</span><span class="sxs-lookup"><span data-stu-id="5ece5-120">A driver error handler should implement [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), instead of **IWiaAppErrorHandler**.</span></span>

<span data-ttu-id="5ece5-121">O objeto que implementa essa interface também deve implementar [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span><span class="sxs-lookup"><span data-stu-id="5ece5-121">The object that implements this interface should also implement [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span></span>

<span data-ttu-id="5ece5-122">Se você quiser um manipulador de erro de driver e um manipulador de erro padrão para exibir as janelas de mensagens de erro, mas não quiser criar um manipulador de erro completo para o aplicativo, implemente essa interface e também implemente o método [**IWiaAppErrorHandler:: ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) para retornar o \_ status WIA \_ não \_ Tratado.</span><span class="sxs-lookup"><span data-stu-id="5ece5-122">If you want a driver error handler and default error handler to display error message windows, but you do not want to create a complete error handler for the application, implement this interface and also implement the [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) method to return WIA\_STATUS\_NOT\_HANDLED.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ece5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ece5-123">Requirements</span></span>



| <span data-ttu-id="5ece5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ece5-124">Requirement</span></span> | <span data-ttu-id="5ece5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5ece5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ece5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ece5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5ece5-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ece5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5ece5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ece5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5ece5-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ece5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5ece5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ece5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ece5-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ece5-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ece5-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="5ece5-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ece5-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ece5-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
