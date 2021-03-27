---
description: Enviado para a função CPlApplet de um aplicativo do painel de controle quando o usuário clica duas vezes no ícone de uma caixa de diálogo com suporte no aplicativo.
title: Mensagem de CPL_DBLCLK (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988744"
---
# <a name="cpl_dblclk-message"></a><span data-ttu-id="ede38-103">CPL \_ mensagem DBLCLK</span><span class="sxs-lookup"><span data-stu-id="ede38-103">CPL\_DBLCLK message</span></span>

<span data-ttu-id="ede38-104">Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo do painel de controle quando o usuário clica duas vezes no ícone de uma caixa de diálogo com suporte no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ede38-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the user double-clicks the icon of a dialog box supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="ede38-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ede38-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede38-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="ede38-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="ede38-107">O número da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ede38-107">The dialog box number.</span></span> <span data-ttu-id="ede38-108">Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**CPL \_ GetCount**](cpl-getcount.md) (CPL \_ GetCount – 1).</span><span class="sxs-lookup"><span data-stu-id="ede38-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="ede38-109">*lData*</span><span class="sxs-lookup"><span data-stu-id="ede38-109">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="ede38-110">O valor que o aplicativo do painel de controle carregou no membro **lpData** da estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ede38-110">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="ede38-111">O aplicativo carrega o membro **lpData** em resposta à mensagem [**CPL de \_ consulta**](cpl-inquire.md) ou [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) .</span><span class="sxs-lookup"><span data-stu-id="ede38-111">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede38-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ede38-112">Return value</span></span>

<span data-ttu-id="ede38-113">Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, o valor de retorno será zero; caso contrário, ele será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ede38-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, the return value is zero; otherwise, it is nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede38-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ede38-114">Remarks</span></span>

<span data-ttu-id="ede38-115">Em resposta a essa mensagem, um aplicativo do painel de controle deve exibir a caixa de diálogo correspondente.</span><span class="sxs-lookup"><span data-stu-id="ede38-115">In response to this message, a Control Panel application must display the corresponding dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ede38-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ede38-116">Requirements</span></span>



| <span data-ttu-id="ede38-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ede38-117">Requirement</span></span> | <span data-ttu-id="ede38-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ede38-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ede38-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ede38-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ede38-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ede38-120">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ede38-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ede38-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ede38-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ede38-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ede38-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ede38-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ede38-124"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ede38-124"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ede38-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ede38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede38-126">**CPL de \_ seleção**</span><span class="sxs-lookup"><span data-stu-id="ede38-126">**CPL\_SELECT**</span></span>](cpl-select.md)
</dt> </dl>

 

 
