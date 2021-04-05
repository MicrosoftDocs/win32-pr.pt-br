---
title: Função de retorno de chamada TranslateDispatch
description: Usado pelo cliente da função doreadermode para interceptar e controlar explicitamente todas as mensagens do Windows direcionadas para a área de rolagem da janela do modo de leitura. Essa é uma função de retorno de chamada definida pelo aplicativo.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Controles do Windows da função de retorno de chamada TranslateDispatch
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918338"
---
# <a name="translatedispatch-callback-function"></a><span data-ttu-id="1292a-105">Função de retorno de chamada TranslateDispatch</span><span class="sxs-lookup"><span data-stu-id="1292a-105">TranslateDispatch callback function</span></span>

<span data-ttu-id="1292a-106">\[O *TranslateDispatch* está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1292a-106">\[*TranslateDispatch* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1292a-107">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="1292a-107">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="1292a-108">Usado pelo cliente da função [**Doreadermode**](doreadermode.md) para interceptar e controlar explicitamente todas as mensagens do Windows direcionadas para a área de rolagem da janela do modo de leitura.</span><span class="sxs-lookup"><span data-stu-id="1292a-108">Used by the client of the [**DoReaderMode**](doreadermode.md) function to intercept and explicitly handle any windows messages targeted for the scrolling area of the reader mode window.</span></span> <span data-ttu-id="1292a-109">Essa é uma função de retorno de chamada definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1292a-109">This is an application-defined callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1292a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1292a-110">Syntax</span></span>


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a><span data-ttu-id="1292a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1292a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1292a-112">*lpMsg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1292a-112">*lpmsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1292a-113">Tipo: \**const [**msg**](/windows/win32/api/winuser/ns-winuser-msg) \** _</span><span class="sxs-lookup"><span data-stu-id="1292a-113">Type: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)\** _</span></span>

<span data-ttu-id="1292a-114">Um ponteiro para uma estrutura [_ *msg* \*](/windows/win32/api/winuser/ns-winuser-msg) que contém a mensagem interceptada.</span><span class="sxs-lookup"><span data-stu-id="1292a-114">A pointer to an [_ *MSG*\*](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the intercepted message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1292a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1292a-115">Return value</span></span>

<span data-ttu-id="1292a-116">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1292a-116">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1292a-117">**True** se a mensagem foi tratada por essa função; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1292a-117">**TRUE** if the message was handled by this function; otherwise, **FALSE**.</span></span> <span data-ttu-id="1292a-118">Se **for false**, a mensagem será tratada pela implementação do modo de leitor padrão.</span><span class="sxs-lookup"><span data-stu-id="1292a-118">If **FALSE**, the message is handled by the default reader mode implementation.</span></span> <span data-ttu-id="1292a-119">Essa implementação manipula movimentos e botões do mouse, bem como pressionamentos de tecla.</span><span class="sxs-lookup"><span data-stu-id="1292a-119">That implementation handles mouse movement and buttons as well as key presses.</span></span>

## <a name="examples"></a><span data-ttu-id="1292a-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1292a-120">Examples</span></span>

<span data-ttu-id="1292a-121">O exemplo a seguir descreve uma implementação dessa função.</span><span class="sxs-lookup"><span data-stu-id="1292a-121">The following example outlines an implementation of this function.</span></span>


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a><span data-ttu-id="1292a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1292a-122">Requirements</span></span>



| <span data-ttu-id="1292a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1292a-123">Requirement</span></span> | <span data-ttu-id="1292a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1292a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1292a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1292a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1292a-126">Windows Vista, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1292a-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1292a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1292a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1292a-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1292a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

