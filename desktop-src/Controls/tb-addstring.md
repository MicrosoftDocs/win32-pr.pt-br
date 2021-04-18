---
title: Mensagem de TB_ADDSTRING (commctrl. h)
description: Adiciona uma nova cadeia de caracteres ao pool de cadeias da barra de ferramentas.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- Controles de TB_ADDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755828"
---
# <a name="tb_addstring-message"></a><span data-ttu-id="74f88-104">\_Mensagem de caracteres ADDSTRING TB</span><span class="sxs-lookup"><span data-stu-id="74f88-104">TB\_ADDSTRING message</span></span>

<span data-ttu-id="74f88-105">Adiciona uma nova cadeia de caracteres ao pool de cadeias da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="74f88-105">Adds a new string to the toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="74f88-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74f88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74f88-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74f88-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74f88-108">Manipule a instância de módulo com um arquivo executável que contém o recurso de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="74f88-108">Handle to the module instance with an executable file that contains the string resource.</span></span> <span data-ttu-id="74f88-109">Se *lParam* apontar para uma matriz de caractere com uma ou mais cadeias de caracteres, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="74f88-109">If *lParam* instead points to a character array with one or more strings, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74f88-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74f88-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74f88-111">Identificador de recurso para o recurso de cadeia de caracteres ou um ponteiro para uma matriz TCHAR.</span><span class="sxs-lookup"><span data-stu-id="74f88-111">Resource identifier for the string resource, or a pointer to a TCHAR array.</span></span> <span data-ttu-id="74f88-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="74f88-112">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74f88-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74f88-113">Return value</span></span>

<span data-ttu-id="74f88-114">Retorna o índice da primeira nova cadeia de caracteres se for bem-sucedida ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="74f88-114">Returns the index of the first new string if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="74f88-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="74f88-115">Remarks</span></span>

<span data-ttu-id="74f88-116">Se *wParam* for **NULL**, *lParam* apontará para uma matriz de caracteres com uma ou mais cadeias terminadas com nulo.</span><span class="sxs-lookup"><span data-stu-id="74f88-116">If *wParam* is **NULL**, *lParam* points to a character array with one or more null-terminated strings.</span></span> <span data-ttu-id="74f88-117">A última cadeia de caracteres na matriz deve ser terminada com dois caracteres nulos.</span><span class="sxs-lookup"><span data-stu-id="74f88-117">The last string in the array must be terminated with two null characters.</span></span>

<span data-ttu-id="74f88-118">Se *wParam* for o HINSTANCE do aplicativo ou de outro módulo que contém um recurso de cadeia de caracteres, *lParam* será o identificador de recurso da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="74f88-118">If *wParam* is the HINSTANCE of the application or of another module containing a string resource, *lParam* is the resource identifier of the string.</span></span> <span data-ttu-id="74f88-119">Cada item na cadeia de caracteres deve começar com um caractere separador arbitrário e a cadeia de caracteres deve terminar com dois caracteres.</span><span class="sxs-lookup"><span data-stu-id="74f88-119">Each item in the string must begin with an arbitrary separator character, and the string must end with two such characters.</span></span> <span data-ttu-id="74f88-120">Por exemplo, o texto para três botões pode aparecer na tabela de cadeia de caracteres como "/New/Open/Save//".</span><span class="sxs-lookup"><span data-stu-id="74f88-120">For example, the text for three buttons might appear in the string table as "/New/Open/Save//".</span></span> <span data-ttu-id="74f88-121">A mensagem retorna o índice de "New" no pool de cadeias de caracteres da barra de ferramentas e os outros itens estão em posições consecutivas.</span><span class="sxs-lookup"><span data-stu-id="74f88-121">The message returns the index of "New" in the toolbar's string pool, and the other items are in consecutive positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="74f88-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74f88-122">Requirements</span></span>



| <span data-ttu-id="74f88-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="74f88-123">Requirement</span></span> | <span data-ttu-id="74f88-124">Valor</span><span class="sxs-lookup"><span data-stu-id="74f88-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74f88-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74f88-125">Minimum supported client</span></span><br/> | <span data-ttu-id="74f88-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74f88-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74f88-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74f88-127">Minimum supported server</span></span><br/> | <span data-ttu-id="74f88-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74f88-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74f88-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74f88-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f88-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74f88-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="74f88-131">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="74f88-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74f88-132">**TB \_ ADDSTRINGW** (Unicode) e **TB \_ addstringa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74f88-132">**TB\_ADDSTRINGW** (Unicode) and **TB\_ADDSTRINGA** (ANSI)</span></span><br/>                 |



 

 





