---
description: Enviado para a função CPlApplet de um aplicativo de painel de controle para solicitar que ele execute a inicialização global, especialmente a alocação de memória.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Mensagem de CPL_INIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967351"
---
# <a name="cpl_init-message"></a><span data-ttu-id="c60b1-103">CPL \_ mensagem de inicialização</span><span class="sxs-lookup"><span data-stu-id="c60b1-103">CPL\_INIT message</span></span>

<span data-ttu-id="c60b1-104">Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo de painel de controle para solicitar que ele execute a inicialização global, especialmente a alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="c60b1-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to prompt it to perform global initialization, especially memory allocation.</span></span>


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a><span data-ttu-id="c60b1-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c60b1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c60b1-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c60b1-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c60b1-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c60b1-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c60b1-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c60b1-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c60b1-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c60b1-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c60b1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c60b1-110">Return value</span></span>

<span data-ttu-id="c60b1-111">Se a inicialização for realizada com sucesso, a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deverá retornar diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c60b1-111">If initialization succeeds, the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function should return nonzero.</span></span> <span data-ttu-id="c60b1-112">Caso contrário, ele deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="c60b1-112">Otherwise, it should return zero.</span></span>

<span data-ttu-id="c60b1-113">Se [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) retornar zero, o aplicativo de controle terminará a comunicação e liberará a DLL que contém o aplicativo do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c60b1-113">If [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) returns zero, the controlling application ends communication and releases the DLL containing the Control Panel application.</span></span>

## <a name="remarks"></a><span data-ttu-id="c60b1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c60b1-114">Remarks</span></span>

<span data-ttu-id="c60b1-115">Como essa é a única maneira como um aplicativo do painel de controle pode sinalizar uma condição de erro, o aplicativo deve alocar memória em resposta a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c60b1-115">Because this is the only way a Control Panel application can signal an error condition, the application should allocate memory in response to this message.</span></span>

<span data-ttu-id="c60b1-116">Essa mensagem é enviada imediatamente depois que a DLL que contém o aplicativo é carregada.</span><span class="sxs-lookup"><span data-stu-id="c60b1-116">This message is sent immediately after the DLL containing the application is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="c60b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c60b1-117">Requirements</span></span>



| <span data-ttu-id="c60b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c60b1-118">Requirement</span></span> | <span data-ttu-id="c60b1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c60b1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c60b1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c60b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c60b1-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c60b1-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c60b1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c60b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c60b1-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c60b1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c60b1-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c60b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c60b1-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c60b1-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c60b1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c60b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60b1-127">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="c60b1-127">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
