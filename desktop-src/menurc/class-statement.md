---
title: Declaração de classe
description: Define a classe da caixa de diálogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menus de instruções de classe e outros recursos
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917237"
---
# <a name="class-statement"></a><span data-ttu-id="52b81-104">Declaração de classe</span><span class="sxs-lookup"><span data-stu-id="52b81-104">CLASS statement</span></span>

<span data-ttu-id="52b81-105">Define a classe da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="52b81-105">Defines the class of the dialog box.</span></span>

<span data-ttu-id="52b81-106">A instrução **Class** aparece na seção opcional antes de uma instrução de [**caixa de diálogo**](dialog-resource.md) Main.</span><span class="sxs-lookup"><span data-stu-id="52b81-106">The **CLASS** statement appears in the optional section before a [**DIALOG**](dialog-resource.md) statement's main.</span></span> <span data-ttu-id="52b81-107">Se nenhuma classe for fornecida, a classe de diálogo padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="52b81-107">If no class is given, the standard dialog class is used.</span></span>

``` syntax
CLASS class
```

<dl> <dt>

<span data-ttu-id="52b81-108"><span id="class"></span><span id="CLASS"></span>*classes*</span><span class="sxs-lookup"><span data-stu-id="52b81-108"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="52b81-109">Um inteiro não assinado de 16 bits ou uma cadeia de caracteres entre aspas duplas ("), que identifica a classe da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="52b81-109">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="52b81-110">Se o procedimento de janela da classe não processar uma mensagem enviada a ele, ele deverá chamar a função [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) para garantir que todas as mensagens sejam tratadas corretamente para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="52b81-110">If the window procedure for the class does not process a message sent to it, it must call the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function to ensure that all messages are handled properly for the dialog box.</span></span> <span data-ttu-id="52b81-111">Uma classe privada pode usar **DefDlgProc** como o procedimento de janela padrão.</span><span class="sxs-lookup"><span data-stu-id="52b81-111">A private class can use **DefDlgProc** as the default window procedure.</span></span> <span data-ttu-id="52b81-112">A classe deve ser registrada com o membro **cbWndExtra** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) definida como **DLGWINDOWEXTRA**.</span><span class="sxs-lookup"><span data-stu-id="52b81-112">The class must be registered with the **cbWndExtra** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure set to **DLGWINDOWEXTRA**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52b81-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="52b81-113">Remarks</span></span>

<span data-ttu-id="52b81-114">A instrução de **classe** só deve ser usada com casos especiais, porque ela substitui o processamento normal de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="52b81-114">The **CLASS** statement should only be used with special cases, because it overrides the normal processing of a dialog box.</span></span> <span data-ttu-id="52b81-115">A instrução **Class** converte uma caixa de diálogo em uma janela da classe especificada; dependendo da classe, isso pode dar resultados indesejáveis.</span><span class="sxs-lookup"><span data-stu-id="52b81-115">The **CLASS** statement converts a dialog box to a window of the specified class; depending on the class, this could give undesirable results.</span></span> <span data-ttu-id="52b81-116">Não use os nomes de classe de controle redefinidos com esta instrução.</span><span class="sxs-lookup"><span data-stu-id="52b81-116">Do not use the redefined control-class names with this statement.</span></span>

## <a name="examples"></a><span data-ttu-id="52b81-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52b81-117">Examples</span></span>

<span data-ttu-id="52b81-118">O exemplo a seguir demonstra o uso da instrução de **classe** :</span><span class="sxs-lookup"><span data-stu-id="52b81-118">The following example demonstrates the use of the **CLASS** statement:</span></span>

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a><span data-ttu-id="52b81-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="52b81-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b81-120">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="52b81-120">**DefDlgProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="52b81-121">**'**</span><span class="sxs-lookup"><span data-stu-id="52b81-121">**DIALOG**</span></span>](dialog-resource.md)
</dt> </dl>

 

 