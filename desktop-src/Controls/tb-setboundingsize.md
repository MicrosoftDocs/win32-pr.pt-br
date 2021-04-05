---
title: Mensagem de TB_SETBOUNDINGSIZE (commctrl. h)
description: Define o tamanho delimitador para um controle de barra de ferramentas de várias colunas.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- Controles de TB_SETBOUNDINGSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824150"
---
# <a name="tb_setboundingsize-message"></a><span data-ttu-id="8f2c5-104">TB de \_ mensagem SETBOUNDINGSIZE</span><span class="sxs-lookup"><span data-stu-id="8f2c5-104">TB\_SETBOUNDINGSIZE message</span></span>

<span data-ttu-id="8f2c5-105">\[Destinado ao uso interno; Não recomendado para uso em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="8f2c5-106">Essa mensagem pode não ter suporte em versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8f2c5-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="8f2c5-107">Define o tamanho delimitador para um controle de barra de ferramentas de várias colunas.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-107">Sets the bounding size for a multi-column toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f2c5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f2c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f2c5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f2c5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f2c5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8f2c5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f2c5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f2c5-112">Ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) cujo membro **CY** contém a altura delimitadora.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-112">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure whose **cy** member contains the bounding height.</span></span> <span data-ttu-id="8f2c5-113">O membro **CX** (a largura) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-113">The **cx** member (the width) is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f2c5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f2c5-114">Return value</span></span>

<span data-ttu-id="8f2c5-115">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-115">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="8f2c5-116">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="8f2c5-116">Security Considerations</span></span>

<span data-ttu-id="8f2c5-117">O uso dessa mensagem pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-117">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f2c5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f2c5-118">Remarks</span></span>

<span data-ttu-id="8f2c5-119">O tamanho de limite controla como os botões são organizados em colunas.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-119">The bounding size controls how buttons are organized into columns.</span></span> <span data-ttu-id="8f2c5-120">Se o controle Toolbar não tiver o estilo [**de \_ \_ várias colunas TBSTYLE ex**](toolbar-extended-styles.md) , essa mensagem não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="8f2c5-120">If the toolbar control does not have the [**TBSTYLE\_EX\_MULTICOLUMN**](toolbar-extended-styles.md) style, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f2c5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f2c5-121">Requirements</span></span>



| <span data-ttu-id="8f2c5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f2c5-122">Requirement</span></span> | <span data-ttu-id="8f2c5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8f2c5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2c5-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f2c5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8f2c5-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f2c5-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f2c5-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f2c5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8f2c5-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f2c5-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f2c5-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f2c5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f2c5-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f2c5-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

