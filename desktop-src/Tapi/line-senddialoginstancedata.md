---
description: A mensagem de SENDDIALOGINSTANCEDATA da linha TSPI \_ faz com que a TAPI chame a \_ função TUISPI PROVIDERGENERICDIALOGDATA na DLL da interface do usuário associada a htDlgInst, passando a ela o bloco de parâmetro apontado por lpParams, de comprimento dwSize.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Mensagem de LINE_SENDDIALOGINSTANCEDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792619"
---
# <a name="line_senddialoginstancedata-message"></a><span data-ttu-id="eb838-103">Mensagem de SENDDIALOGINSTANCEDATA de linha \_</span><span class="sxs-lookup"><span data-stu-id="eb838-103">LINE\_SENDDIALOGINSTANCEDATA message</span></span>

<span data-ttu-id="eb838-104">A mensagem **de \_ SENDDIALOGINSTANCEDATA da linha** TSPI faz com que a TAPI chame a função [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) na DLL da interface do usuário associada a *htDlgInst*, passando a ela o bloco de parâmetro apontado por *lpParams*, de comprimento *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="eb838-104">The TSPI **LINE\_SENDDIALOGINSTANCEDATA** message causes TAPI to call the [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function in the UI DLL associated with *htDlgInst*, passing it the parameter block pointed to by *lpParams*, of length *dwSize*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="eb838-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb838-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb838-106">*htDlgInst*</span><span class="sxs-lookup"><span data-stu-id="eb838-106">*htDlgInst*</span></span> 
</dt> <dd>

<span data-ttu-id="eb838-107">O HTAPIDIALOGINSTANCE que foi retornado ao provedor de serviços quando a instância da caixa de diálogo foi criada usando a [**linha \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span><span class="sxs-lookup"><span data-stu-id="eb838-107">The HTAPIDIALOGINSTANCE that was returned to the service provider when the dialog box instance was created using [**LINE\_CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb838-108">*lpParams*</span><span class="sxs-lookup"><span data-stu-id="eb838-108">*lpParams*</span></span> 
</dt> <dd>

<span data-ttu-id="eb838-109">Ponteiro para um bloco de parâmetro específico de provedor que é transmitido para a função de interface do usuário [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) , o tamanho especificado por *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="eb838-109">Pointer to a provider-specific parameter block that is conveyed to the UI DLL [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function, the size of which is specified by *dwSize*.</span></span> <span data-ttu-id="eb838-110">Se esse parâmetro for definido como **NULL**, essa será uma solicitação para fechar a caixa de diálogo imediatamente e limpar (a DLL da interface do usuário não deve invocar [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) durante essa limpeza).</span><span class="sxs-lookup"><span data-stu-id="eb838-110">If this parameter is set to **NULL**, this is a request to close the dialog box immediately and clean up (the UI DLL should not invoke [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) during this cleanup).</span></span>

</dd> <dt>

<span data-ttu-id="eb838-111">*dwSize*</span><span class="sxs-lookup"><span data-stu-id="eb838-111">*dwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="eb838-112">O tamanho em bytes do bloco de parâmetro a ser transmitido para a DLL da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="eb838-112">The size in bytes of the parameter block to be conveyed to the UI DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb838-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb838-113">Requirements</span></span>



| <span data-ttu-id="eb838-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb838-114">Requirement</span></span> | <span data-ttu-id="eb838-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eb838-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="eb838-116">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="eb838-116">TAPI version</span></span><br/> | <span data-ttu-id="eb838-117">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="eb838-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="eb838-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb838-118">Header</span></span><br/>       | <dl> <span data-ttu-id="eb838-119"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb838-119"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb838-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb838-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb838-121">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="eb838-121">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[<span data-ttu-id="eb838-122">**TUISPI \_ providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="eb838-122">**TUISPI\_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[<span data-ttu-id="eb838-123">**CREATEDIALOGINSTANCE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="eb838-123">**LINE\_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
</dt> </dl>

 

