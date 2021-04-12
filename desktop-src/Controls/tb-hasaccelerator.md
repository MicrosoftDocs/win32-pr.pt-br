---
title: Mensagem de TB_HASACCELERATOR (commctrl. h)
description: Recupera uma contagem de botões da barra de ferramentas que têm o caractere de acelerador especificado.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- Controles de TB_HASACCELERATOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455275"
---
# <a name="tb_hasaccelerator-message"></a><span data-ttu-id="fe198-104">TB de \_ mensagem HASACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="fe198-104">TB\_HASACCELERATOR message</span></span>

<span data-ttu-id="fe198-105">\[Destinado ao uso interno; Não recomendado para uso em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fe198-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="fe198-106">Essa mensagem pode não ter suporte em versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fe198-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="fe198-107">Recupera uma contagem de botões da barra de ferramentas que têm o caractere de acelerador especificado.</span><span class="sxs-lookup"><span data-stu-id="fe198-107">Retrieves a count of toolbar buttons that have the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe198-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe198-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe198-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe198-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe198-110">Um **WCHAR** que representa o caractere do acelerador de entrada a ser testado.</span><span class="sxs-lookup"><span data-stu-id="fe198-110">A **WCHAR** representing the input accelerator character to test.</span></span>

</dd> <dt>

<span data-ttu-id="fe198-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe198-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe198-112">Ponteiro para um **int** que recebe o número de botões que têm o caractere de acelerador.</span><span class="sxs-lookup"><span data-stu-id="fe198-112">Pointer to an **int** that receives the number of buttons that have the accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe198-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe198-113">Return value</span></span>

<span data-ttu-id="fe198-114">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="fe198-114">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="fe198-115">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="fe198-115">Security Considerations</span></span>

<span data-ttu-id="fe198-116">O uso dessa mensagem pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="fe198-116">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe198-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe198-117">Remarks</span></span>

<span data-ttu-id="fe198-118">Primeiro, o sistema consulta todos os botões da barra de ferramentas para os aceleradores correspondentes.</span><span class="sxs-lookup"><span data-stu-id="fe198-118">First, the system queries all toolbar buttons for matching accelerators.</span></span> <span data-ttu-id="fe198-119">Se nenhuma correspondência for encontrada, o sistema enviará a notificação [tbn \_ MAPACCELERATOR](tbn-mapaccelerator.md) para a janela pai, solicitando o índice do botão que tem o caractere de acelerador especificado.</span><span class="sxs-lookup"><span data-stu-id="fe198-119">If no matches are found, the system sends the [TBN\_MAPACCELERATOR](tbn-mapaccelerator.md) notification to the parent window, requesting the index of the button that has the specified accelerator character.</span></span> <span data-ttu-id="fe198-120">Se o pai fornecer um índice, a contagem será definida como 1.</span><span class="sxs-lookup"><span data-stu-id="fe198-120">If the parent provides an index, the count is set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe198-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe198-121">Requirements</span></span>



| <span data-ttu-id="fe198-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe198-122">Requirement</span></span> | <span data-ttu-id="fe198-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fe198-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe198-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe198-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fe198-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe198-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe198-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe198-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fe198-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe198-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe198-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe198-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe198-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe198-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





