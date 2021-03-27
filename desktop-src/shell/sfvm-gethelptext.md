---
description: 'Permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda para itens de menu ou botões da barra de ferramentas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_GETHELPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662602"
---
# <a name="sfvm_gethelptext-message"></a><span data-ttu-id="c8fdf-104">\_Mensagem SFVM GEThelptext</span><span class="sxs-lookup"><span data-stu-id="c8fdf-104">SFVM\_GETHELPTEXT message</span></span>

<span data-ttu-id="c8fdf-105">Permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda para itens de menu ou botões da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-105">Allows the callback object to specify a help text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="c8fdf-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="c8fdf-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="c8fdf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8fdf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8fdf-108">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="c8fdf-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8fdf-109">A palavra de ordem inferior desse parâmetro contém a ID de comando.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="c8fdf-110">A palavra de ordem superior contém o número de caracteres no buffer *pszText* .</span><span class="sxs-lookup"><span data-stu-id="c8fdf-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c8fdf-111">*pszText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c8fdf-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8fdf-112">Uma cadeia de caracteres terminada em nulo que contém o texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="c8fdf-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8fdf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8fdf-113">Requirements</span></span>



| <span data-ttu-id="c8fdf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8fdf-114">Requirement</span></span> | <span data-ttu-id="c8fdf-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c8fdf-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c8fdf-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8fdf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8fdf-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c8fdf-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c8fdf-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8fdf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8fdf-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c8fdf-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c8fdf-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c8fdf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8fdf-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8fdf-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
