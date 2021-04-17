---
title: Mensagem de ICM_CONFIGURE (VFW. h)
description: A mensagem de configuração de ICM \_ Notifica um driver de compactação de vídeo para exibir sua caixa de diálogo de configuração ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo de configuração.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- Multimídia do Windows de mensagem ICM_CONFIGURE
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770165"
---
# <a name="icm_configure-message"></a><span data-ttu-id="98303-104">Mensagem de configuração de ICM \_</span><span class="sxs-lookup"><span data-stu-id="98303-104">ICM\_CONFIGURE message</span></span>

<span data-ttu-id="98303-105">A mensagem de **\_ configuração de ICM** notifica um driver de compactação de vídeo para exibir sua caixa de diálogo de configuração ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="98303-105">The **ICM\_CONFIGURE** message notifies a video compression driver to display its configuration dialog box or queries a video compression driver to determine if it has a configuration dialog box.</span></span> <span data-ttu-id="98303-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) .</span><span class="sxs-lookup"><span data-stu-id="98303-106">You can send this message explicitly or by using the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro.</span></span>


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="98303-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98303-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98303-108"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="98303-108"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="98303-109">Identificador para a janela pai da caixa de diálogo exibida.</span><span class="sxs-lookup"><span data-stu-id="98303-109">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="98303-110">Você pode determinar se um driver tem uma caixa de diálogo de configuração especificando 1 nesse parâmetro, como na macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) .</span><span class="sxs-lookup"><span data-stu-id="98303-110">You can determine if a driver has a configuration dialog box by specifying  1 in this parameter, as in the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98303-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="98303-111">Return Value</span></span>

<span data-ttu-id="98303-112">Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="98303-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="98303-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="98303-113">Remarks</span></span>

<span data-ttu-id="98303-114">Essa mensagem é diferente da mensagem [**de \_ configuração de drv**](drv-configure.md) usada para configuração de hardware.</span><span class="sxs-lookup"><span data-stu-id="98303-114">This message is different from the [**DRV\_CONFIGURE**](drv-configure.md) message used for hardware configuration.</span></span> <span data-ttu-id="98303-115">A caixa de diálogo dessa mensagem deve permitir que o usuário defina e edite o estado interno referenciado pelas mensagens [**ICM \_ GetState**](icm-getstate.md) e [**ICM \_ SetState**](icm-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="98303-115">The dialog box for this message should let the user set and edit the internal state referenced by the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages.</span></span> <span data-ttu-id="98303-116">Por exemplo, essa caixa de diálogo pode permitir que o usuário altere os parâmetros que afetam o nível de qualidade e outras opções de compactação semelhantes.</span><span class="sxs-lookup"><span data-stu-id="98303-116">For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.</span></span>

## <a name="requirements"></a><span data-ttu-id="98303-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98303-117">Requirements</span></span>



| <span data-ttu-id="98303-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="98303-118">Requirement</span></span> | <span data-ttu-id="98303-119">Valor</span><span class="sxs-lookup"><span data-stu-id="98303-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="98303-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98303-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98303-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="98303-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="98303-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98303-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98303-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="98303-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98303-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="98303-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="98303-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="98303-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98303-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="98303-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98303-127">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="98303-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="98303-128">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="98303-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





