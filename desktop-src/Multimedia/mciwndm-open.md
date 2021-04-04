---
title: Mensagem de MCIWNDM_OPEN (VFW. h)
description: A mensagem de abertura do MCIWNDM \_ abre um dispositivo MCI e o associa a uma janela MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- Multimídia do Windows de mensagem MCIWNDM_OPEN
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085441"
---
# <a name="mciwndm_open-message"></a><span data-ttu-id="2c389-104">MCIWNDM \_ Abrir mensagem</span><span class="sxs-lookup"><span data-stu-id="2c389-104">MCIWNDM\_OPEN message</span></span>

<span data-ttu-id="2c389-105">A mensagem de **\_ abertura do MCIWNDM** abre um dispositivo MCI e o associa a uma janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="2c389-105">The **MCIWNDM\_OPEN** message opens an MCI device and associates it with an MCIWnd window.</span></span> <span data-ttu-id="2c389-106">Para dispositivos MCI que usam arquivos de dados, essa macro também pode abrir um arquivo de dados especificado, nomear um novo arquivo a ser criado ou exibir uma caixa de diálogo para permitir que o usuário selecione um arquivo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="2c389-106">For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open.</span></span> <span data-ttu-id="2c389-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .</span><span class="sxs-lookup"><span data-stu-id="2c389-107">You can send this message explicitly or by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro.</span></span>


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a><span data-ttu-id="2c389-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c389-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c389-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="2c389-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2c389-110">Sinalizadores associados ao dispositivo ou ao arquivo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="2c389-110">Flags associated with the device or file to open.</span></span> <span data-ttu-id="2c389-111">O \_ novo sinalizador MCIWNDOPENF especifica que um novo arquivo deve ser criado com o nome especificado em **szFile**.</span><span class="sxs-lookup"><span data-stu-id="2c389-111">The MCIWNDOPENF\_NEW flag specifies a new file is to be created with the name specified in **szFile**.</span></span>

</dd> <dt>

<span data-ttu-id="2c389-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span><span class="sxs-lookup"><span data-stu-id="2c389-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span></span>
</dt> <dd>

<span data-ttu-id="2c389-113">Ponteiro para uma cadeia de caracteres terminada em nulo identificando o nome do nome do dispositivo ou do MCI a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="2c389-113">Pointer to a null-terminated string identifying the filename or MCI device name to open.</span></span> <span data-ttu-id="2c389-114">Especifique 1 para esse parâmetro para exibir a caixa de diálogo abrir.</span><span class="sxs-lookup"><span data-stu-id="2c389-114">Specify  1 for this parameter to display the Open dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c389-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2c389-115">Return Value</span></span>

<span data-ttu-id="2c389-116">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="2c389-116">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c389-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c389-117">Requirements</span></span>



| <span data-ttu-id="2c389-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c389-118">Requirement</span></span> | <span data-ttu-id="2c389-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2c389-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c389-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c389-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c389-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c389-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2c389-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c389-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c389-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c389-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2c389-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c389-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c389-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c389-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c389-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c389-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c389-127">**MCIWndOpen**</span><span class="sxs-lookup"><span data-stu-id="2c389-127">**MCIWndOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





