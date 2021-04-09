---
title: Mensagem de MCIWNDM_NOTIFYMODE (VFW. h)
description: A \_ mensagem MCIWNDM notifymode notifica a janela pai de um aplicativo de que o modo operacional do dispositivo MCI foi alterado.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NOTIFYMODE
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008834"
---
# <a name="mciwndm_notifymode-message"></a><span data-ttu-id="3a020-104">\_Mensagem MCIWNDM notifymode</span><span class="sxs-lookup"><span data-stu-id="3a020-104">MCIWNDM\_NOTIFYMODE message</span></span>

<span data-ttu-id="3a020-105">A mensagem **MCIWNDM \_ notifymode** notifica a janela pai de um aplicativo de que o modo operacional do dispositivo MCI foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3a020-105">The **MCIWNDM\_NOTIFYMODE** message notifies the parent window of an application that the operating mode of the MCI device has changed.</span></span>


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a><span data-ttu-id="3a020-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a020-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a020-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="3a020-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="3a020-108">Manipule a janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3a020-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="3a020-109"><span id="mode"></span><span id="MODE"></span>*moda*</span><span class="sxs-lookup"><span data-stu-id="3a020-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="3a020-110">Inteiro correspondente ao modo MCI.</span><span class="sxs-lookup"><span data-stu-id="3a020-110">Integer corresponding to the MCI mode.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a020-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a020-111">Remarks</span></span>

<span data-ttu-id="3a020-112">Você pode habilitar a notificação de alterações no modo de um dispositivo MCI especificando o \_ estilo de janela MCIWNDF notifymode.</span><span class="sxs-lookup"><span data-stu-id="3a020-112">You can enable notification of mode changes of an MCI device by specifying the MCIWNDF\_NOTIFYMODE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a020-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a020-113">Requirements</span></span>



| <span data-ttu-id="3a020-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a020-114">Requirement</span></span> | <span data-ttu-id="3a020-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3a020-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3a020-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a020-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3a020-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a020-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3a020-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a020-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3a020-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a020-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3a020-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a020-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a020-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a020-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





