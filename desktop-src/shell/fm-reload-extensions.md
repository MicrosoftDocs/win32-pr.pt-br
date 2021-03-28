---
description: Enviado por uma extensão do Gerenciador de arquivos (ou outro aplicativo) para fazer com que o Gerenciador de arquivos recarregue todas as DLLs de extensão listadas na \[ \] seção Complementos do arquivo de Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Mensagem de FM_RELOAD_EXTENSIONS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967941"
---
# <a name="fm_reload_extensions-message"></a><span data-ttu-id="1b824-103">\_Mensagem de extensões de REcarregamento de FM \_</span><span class="sxs-lookup"><span data-stu-id="1b824-103">FM\_RELOAD\_EXTENSIONS message</span></span>

<span data-ttu-id="1b824-104">Enviado por uma extensão do Gerenciador de arquivos (ou outro aplicativo) para fazer com que o Gerenciador de arquivos recarregue todas as DLLs de extensão listadas na \[ \] seção Complementos do arquivo de Winfile.ini.</span><span class="sxs-lookup"><span data-stu-id="1b824-104">Sent by a File Manager extension (or another application) to cause File Manager to reload all extension DLLs listed in the \[AddOns\] section of the Winfile.ini file.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b824-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b824-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b824-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b824-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b824-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1b824-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1b824-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b824-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b824-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1b824-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b824-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b824-110">Return value</span></span>

<span data-ttu-id="1b824-111">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1b824-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b824-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b824-112">Remarks</span></span>

<span data-ttu-id="1b824-113">Outros aplicativos podem usar a função [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) para enviar essa mensagem ao Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1b824-113">Other applications can use the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to send this message to File Manager.</span></span> <span data-ttu-id="1b824-114">Para obter o identificador apropriado da janela do Gerenciador de arquivos, um aplicativo pode especificar "WFS \_ frame" como o parâmetro *lpszClassName* em uma chamada para a função [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .</span><span class="sxs-lookup"><span data-stu-id="1b824-114">To obtain the appropriate File Manager window handle, an application can specify "WFS\_Frame" as the *lpszClassName* parameter in a call to the [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b824-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b824-115">Requirements</span></span>



| <span data-ttu-id="1b824-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b824-116">Requirement</span></span> | <span data-ttu-id="1b824-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1b824-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b824-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b824-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b824-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1b824-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1b824-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b824-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b824-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1b824-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1b824-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1b824-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b824-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b824-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b824-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b824-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b824-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="1b824-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
