---
description: Obtém um identificador para a caixa de diálogo que exibe mensagens de erro e fornece um ou mais botões para continuar, cancelar ou anular o aplicativo.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'Método IWiaAppErrorHandler:: GetWindow (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772509"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a><span data-ttu-id="33208-103">Método IWiaAppErrorHandler:: GetWindow</span><span class="sxs-lookup"><span data-stu-id="33208-103">IWiaAppErrorHandler::GetWindow method</span></span>

<span data-ttu-id="33208-104">Obtém um identificador para a caixa de diálogo que exibe mensagens de erro e fornece um ou mais botões para continuar, cancelar ou anular o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="33208-104">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="33208-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33208-105">Syntax</span></span>


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a><span data-ttu-id="33208-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33208-107">*phwnd* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="33208-107">*phwnd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33208-108">Tipo: \**HWND \** _</span><span class="sxs-lookup"><span data-stu-id="33208-108">Type: \**HWND\** _</span></span>

<span data-ttu-id="33208-109">HWND usado pelo manipulador de erro do aplicativo, o manipulador de erro do driver e o manipulador de erro padrão para caixas de diálogo de mensagem do dispositivo (erro e informativo).</span><span class="sxs-lookup"><span data-stu-id="33208-109">HWND used by the application error handler, the driver error handler, and the default error handler for device message dialog boxes (both error and informational).</span></span> <span data-ttu-id="33208-110">O valor de saída pode ser _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="33208-110">The output value may be _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33208-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33208-111">Return value</span></span>

<span data-ttu-id="33208-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="33208-112">Type: **HRESULT**</span></span>

<span data-ttu-id="33208-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33208-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33208-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33208-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="33208-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="33208-115">Remarks</span></span>

<span data-ttu-id="33208-116">*phwnd* aponta para a janela passada para o [**REPORTSTATUS**](-wia-iwiaerrorhandler-reportstatus.md) pelo proxy WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="33208-116">*phwnd* points to the window passed into [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) by the Windows Image Acquisition (WIA) 2.0 Proxy.</span></span> <span data-ttu-id="33208-117">Essa janela deve permanecer válida durante a transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="33208-117">This window must remain valid for the duration of the data transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="33208-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33208-118">Requirements</span></span>



| <span data-ttu-id="33208-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33208-119">Requirement</span></span> | <span data-ttu-id="33208-120">Valor</span><span class="sxs-lookup"><span data-stu-id="33208-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33208-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33208-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33208-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33208-122">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="33208-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33208-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33208-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33208-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="33208-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33208-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="33208-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="33208-126"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="33208-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="33208-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33208-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33208-128"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="33208-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33208-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="33208-130"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33208-130"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




