---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar uma contagem dos arquivos selecionados na janela do Gerenciador de arquivos ativa (a janela de diretório ou a janela de resultados da pesquisa).
title: Mensagem de FM_GETSELCOUNT (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: 727e098a98ecfe4a4349ebcf9c6f931a8579b70d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842367"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="69221-103">\_Mensagem GETSELCOUNT de FM</span><span class="sxs-lookup"><span data-stu-id="69221-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="69221-104">Enviado por uma extensão do Gerenciador de arquivos para recuperar uma contagem dos arquivos selecionados na janela do Gerenciador de arquivos ativa (a janela de diretório ou a janela de resultados da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="69221-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="69221-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69221-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69221-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69221-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="69221-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="69221-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="69221-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69221-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="69221-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="69221-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69221-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69221-110">Return value</span></span>

<span data-ttu-id="69221-111">Retorna o número de arquivos selecionados.</span><span class="sxs-lookup"><span data-stu-id="69221-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="69221-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69221-112">Requirements</span></span>



| <span data-ttu-id="69221-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="69221-113">Requirement</span></span> | <span data-ttu-id="69221-114">Valor</span><span class="sxs-lookup"><span data-stu-id="69221-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69221-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69221-115">Minimum supported client</span></span><br/> | <span data-ttu-id="69221-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69221-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="69221-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69221-117">Minimum supported server</span></span><br/> | <span data-ttu-id="69221-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69221-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="69221-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="69221-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="69221-120"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="69221-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69221-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="69221-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69221-122">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="69221-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="69221-123">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="69221-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="69221-124">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="69221-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




