---
title: Mensagem de EM_INSERTTABLE (RichEdit. h)
description: Insere uma ou mais linhas de tabela idênticas com células vazias.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- Controles de EM_INSERTTABLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454759"
---
# <a name="em_inserttable-message"></a><span data-ttu-id="aa59d-104">\_Mensagem em InsertTable</span><span class="sxs-lookup"><span data-stu-id="aa59d-104">EM\_INSERTTABLE message</span></span>

<span data-ttu-id="aa59d-105">Insere uma ou mais linhas de tabela idênticas com células vazias.</span><span class="sxs-lookup"><span data-stu-id="aa59d-105">Inserts one or more identical table rows with empty cells.</span></span>


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a><span data-ttu-id="aa59d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa59d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa59d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa59d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa59d-108">Um ponteiro para uma estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="aa59d-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa59d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa59d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa59d-110">Um ponteiro para uma estrutura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="aa59d-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa59d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa59d-111">Return value</span></span>

<span data-ttu-id="aa59d-112">Retornará S \_ OK se a tabela for inserida ou um código de erro, se não for.</span><span class="sxs-lookup"><span data-stu-id="aa59d-112">Returns S\_OK if the table is inserted, or an error code if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa59d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa59d-113">Remarks</span></span>

<span data-ttu-id="aa59d-114">Se o membro **cpStartRow** do [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) for 1, essa mensagem excluirá o texto selecionado (se houver) e, em seguida, inserirá linhas de tabela vazia com os parâmetros de linha e célula fornecidos por *wParam* e *lParam*.</span><span class="sxs-lookup"><span data-stu-id="aa59d-114">If the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) is  1, this message deletes the selected text (if any), and then inserts empty table rows with the row and cell parameters given by *wParam* and *lParam*.</span></span> <span data-ttu-id="aa59d-115">Ele deixa a seleção apontando para o início da primeira célula na primeira linha.</span><span class="sxs-lookup"><span data-stu-id="aa59d-115">It leaves the selection pointing to the start of the first cell in the first row.</span></span> <span data-ttu-id="aa59d-116">Em seguida, o cliente pode preencher as células da tabela apontando a seleção (ou um [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) para as várias marcas de extremidade da célula e inserindo e Formatando o texto desejado.</span><span class="sxs-lookup"><span data-stu-id="aa59d-116">The client can then populate the table cells by pointing the selection (or an [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) to the various cell end marks and inserting and formatting the desired text.</span></span> <span data-ttu-id="aa59d-117">Esse texto pode incluir linhas de tabela aninhadas.</span><span class="sxs-lookup"><span data-stu-id="aa59d-117">Such text can include nested table rows.</span></span> <span data-ttu-id="aa59d-118">Como alternativa, se o membro **cpStartRow** do **TABLEROWPARMS** for 0 ou maior, as linhas da tabela serão inseridas na posição do caractere fornecido pelo **cpStartRow**.</span><span class="sxs-lookup"><span data-stu-id="aa59d-118">Alternatively, if the **cpStartRow** member of the **TABLEROWPARMS** is 0 or greater, table rows are inserted at the character position given by **cpStartRow**.</span></span> <span data-ttu-id="aa59d-119">Isso só alterará a seleção atual se a tabela for inserida dentro do texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="aa59d-119">This only changes the current selection if the table is inserted inside the selected text.</span></span>

<span data-ttu-id="aa59d-120">Uma tabela de edição rica da Microsoft consiste em uma sequência de linhas de tabela que, por sua vez, consiste em sequências de parágrafos.</span><span class="sxs-lookup"><span data-stu-id="aa59d-120">A Microsoft Rich Edit table consists of a sequence of table rows which, in turn, consist of sequences of paragraphs.</span></span> <span data-ttu-id="aa59d-121">Uma linha de tabela começa com o delimitador de dois caracteres especial do parágrafo U + FFF9 U + 000D e termina com o caractere delimitador de dois caracteres no parágrafo U + FFFB U + 000D.</span><span class="sxs-lookup"><span data-stu-id="aa59d-121">A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D.</span></span> <span data-ttu-id="aa59d-122">Cada célula é encerrada pela marca de célula U + 0007, que é tratada como uma marca de fim de parágrafo difícil, assim como U + 000D (CR).</span><span class="sxs-lookup"><span data-stu-id="aa59d-122">Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is.</span></span> <span data-ttu-id="aa59d-123">Os parâmetros de linha e célula da tabela são tratados como formatação de parágrafo especial dos delimitadores de linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="aa59d-123">The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters.</span></span> <span data-ttu-id="aa59d-124">A formatação contém as informações na estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="aa59d-124">The formatting contains the information in the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span> <span data-ttu-id="aa59d-125">Os parâmetros de célula fornecidos pela estrutura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) são armazenados em uma versão expandida da matriz Tabs.</span><span class="sxs-lookup"><span data-stu-id="aa59d-125">The cell parameters given by the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure are stored in an expanded version of the tabs array.</span></span> <span data-ttu-id="aa59d-126">Esse formato permite que as tabelas sejam aninhadas em outras tabelas, até quinze níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="aa59d-126">This format allows tables to be nested within other tables, up to fifteen levels deep.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa59d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa59d-127">Requirements</span></span>



| <span data-ttu-id="aa59d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa59d-128">Requirement</span></span> | <span data-ttu-id="aa59d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="aa59d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa59d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa59d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aa59d-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="aa59d-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="aa59d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa59d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aa59d-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="aa59d-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa59d-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa59d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa59d-135"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa59d-135"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa59d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa59d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa59d-137">**em \_ INSERTIMAGE**</span><span class="sxs-lookup"><span data-stu-id="aa59d-137">**EM\_INSERTIMAGE**</span></span>](em-insertimage.md)
</dt> </dl>

 

 





