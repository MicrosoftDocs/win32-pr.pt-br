---
title: Estrutura READERMODEINFO
description: Contém as informações necessárias para inicializar a função doreadermode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Controles do Windows da estrutura READERMODEINFO
- Controles do Windows de ponteiro de estrutura PREADERMODEINFO
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455525"
---
# <a name="readermodeinfo-structure"></a><span data-ttu-id="16d81-105">Estrutura READERMODEINFO</span><span class="sxs-lookup"><span data-stu-id="16d81-105">READERMODEINFO structure</span></span>

<span data-ttu-id="16d81-106">\[O **READERMODEINFO** é compatível com o Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="16d81-106">\[**READERMODEINFO** is supported through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="16d81-107">Ele pode não ter suporte em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="16d81-107">It might be unsupported in subsequent versions.\]</span></span>

<span data-ttu-id="16d81-108">Contém as informações necessárias para inicializar a função [**Doreadermode**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="16d81-108">Contains information required to initialize the [**DoReaderMode**](doreadermode.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="16d81-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16d81-109">Syntax</span></span>


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a><span data-ttu-id="16d81-110">Membros</span><span class="sxs-lookup"><span data-stu-id="16d81-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="16d81-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="16d81-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="16d81-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="16d81-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="16d81-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="16d81-113">Required.</span></span> <span data-ttu-id="16d81-114">O tamanho da estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="16d81-114">The size of the structure, in bytes.</span></span> <span data-ttu-id="16d81-115">Defina esse parâmetro como **sizeof (readermode) antes de** chamar [**doreadermode**](doreadermode.md).</span><span class="sxs-lookup"><span data-stu-id="16d81-115">Set this parameter to **sizeof(READERMODE)** before you call [**DoReaderMode**](doreadermode.md).</span></span>

</dd> <dt>

<span data-ttu-id="16d81-116">**HWND**</span><span class="sxs-lookup"><span data-stu-id="16d81-116">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="16d81-117">Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="16d81-117">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="16d81-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="16d81-118">Required.</span></span> <span data-ttu-id="16d81-119">O identificador da janela a ser usada para o modo de leitura.</span><span class="sxs-lookup"><span data-stu-id="16d81-119">The handle of the window to be used for reader mode.</span></span>

</dd> <dt>

<span data-ttu-id="16d81-120">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="16d81-120">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="16d81-121">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="16d81-121">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="16d81-122">Sinalizadores que personalizam a funcionalidade da janela do modo de leitura.</span><span class="sxs-lookup"><span data-stu-id="16d81-122">Flags customizing the functionality of the reader mode window.</span></span> <span data-ttu-id="16d81-123">Esse parâmetro pode ser 0; caso contrário, um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="16d81-123">This parameter can be 0; otherwise, one or more of the following values.</span></span>



| <span data-ttu-id="16d81-124">Valor</span><span class="sxs-lookup"><span data-stu-id="16d81-124">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="16d81-125">Significado</span><span class="sxs-lookup"><span data-stu-id="16d81-125">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <span data-ttu-id="16d81-126"><dt>**RMF \_ ZEROCURSOR**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="16d81-126"><dt>**RMF\_ZEROCURSOR**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="16d81-127">Define o cursor no centro da área especificada na **prc**.</span><span class="sxs-lookup"><span data-stu-id="16d81-127">Sets the cursor in the center of the area specified in **prc**.</span></span> <span data-ttu-id="16d81-128">Se esse sinalizador não for especificado, a posição do cursor permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="16d81-128">If this flag is not specified, the cursor position remains unchanged.</span></span><br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <span data-ttu-id="16d81-129"><dt>**RMF \_ VERTICALONLY**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="16d81-129"><dt>**RMF\_VERTICALONLY**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="16d81-130">Permite apenas a rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="16d81-130">Allows only vertical scrolling.</span></span><br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <span data-ttu-id="16d81-131"><dt>**RMF \_ HORIZONTALONLY**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="16d81-131"><dt>**RMF\_HORIZONTALONLY**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="16d81-132">Permite apenas a rolagem horizontal.</span><span class="sxs-lookup"><span data-stu-id="16d81-132">Allows only horizontal scrolling.</span></span><br/>                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="16d81-133">**popular**</span><span class="sxs-lookup"><span data-stu-id="16d81-133">**prc**</span></span>
</dt> <dd>

<span data-ttu-id="16d81-134">Tipo: **lpRect**</span><span class="sxs-lookup"><span data-stu-id="16d81-134">Type: **LPRECT**</span></span>

</dd> <dd>

<span data-ttu-id="16d81-135">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica a área de rolagem na janela modo de leitor.</span><span class="sxs-lookup"><span data-stu-id="16d81-135">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the scrolling area in the reader mode window.</span></span> <span data-ttu-id="16d81-136">Se esse membro for **nulo**, a janela inteira será usada como a área de rolagem.</span><span class="sxs-lookup"><span data-stu-id="16d81-136">If this member is **NULL**, then the entire window is used as the scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="16d81-137">**pfnScroll**</span><span class="sxs-lookup"><span data-stu-id="16d81-137">**pfnScroll**</span></span>
</dt> <dd>

<span data-ttu-id="16d81-138">Tipo: **PFNREADERSCROLL**</span><span class="sxs-lookup"><span data-stu-id="16d81-138">Type: **PFNREADERSCROLL**</span></span>

</dd> <dd>

<span data-ttu-id="16d81-139">Um ponteiro para uma função de retorno de chamada [*ReaderScroll*](readerscroll.md) definida pelo aplicativo usado para notificar o aplicativo que a janela precisa ser rolada em uma direção específica.</span><span class="sxs-lookup"><span data-stu-id="16d81-139">A pointer to an application-defined [*ReaderScroll*](readerscroll.md) callback function used to notify the application that the window needs to be scrolled in a particular direction.</span></span>

</dd> <dt>

<span data-ttu-id="16d81-140">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="16d81-140">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="16d81-141">Tipo: **PFNREADERTRANSLATEDISPATCH**</span><span class="sxs-lookup"><span data-stu-id="16d81-141">Type: **PFNREADERTRANSLATEDISPATCH**</span></span>

</dd> <dd>

<span data-ttu-id="16d81-142">Um ponteiro para uma função de retorno de chamada [*TranslateDispatch*](translatedispatch.md) definida pelo aplicativo usada para obter a primeira notificação de todas as mensagens enviadas para a janela do modo de leitura.</span><span class="sxs-lookup"><span data-stu-id="16d81-142">A pointer to an application-defined [*TranslateDispatch*](translatedispatch.md) callback function used to get first notification of any messages sent to the reader mode window.</span></span>

</dd> <dt>

<span data-ttu-id="16d81-143">**lParam**</span><span class="sxs-lookup"><span data-stu-id="16d81-143">**lParam**</span></span>
</dt> <dd>

<span data-ttu-id="16d81-144">Tipo: **[ **lParam**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="16d81-144">Type: **[**LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="16d81-145">Informações adicionais conforme necessário pelo aplicativo, lidas pelo chamador na função de retorno de chamada [*ReaderScroll*](readerscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="16d81-145">Additional information as needed by the application, read by the caller in the [*ReaderScroll*](readerscroll.md) callback function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16d81-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="16d81-146">Remarks</span></span>

<span data-ttu-id="16d81-147">Essa estrutura não é declarada em nenhum cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="16d81-147">This structure is not declared in any public header.</span></span> <span data-ttu-id="16d81-148">Para usá-lo, você deve incluir a declaração mostrada acima em seu próprio cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="16d81-148">To use it, you must include the declaration shown above in your own header.</span></span>

## <a name="requirements"></a><span data-ttu-id="16d81-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16d81-149">Requirements</span></span>



| <span data-ttu-id="16d81-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="16d81-150">Requirement</span></span> | <span data-ttu-id="16d81-151">Valor</span><span class="sxs-lookup"><span data-stu-id="16d81-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="16d81-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16d81-152">Minimum supported client</span></span><br/> | <span data-ttu-id="16d81-153">Windows Vista, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16d81-153">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="16d81-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16d81-154">Minimum supported server</span></span><br/> | <span data-ttu-id="16d81-155">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="16d81-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

