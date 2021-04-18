---
title: Enumeração de TITLEBAR_TYPE (Softkbdc. h)
description: Os elementos da \_ enumeração de tipo TITLEBAR são usados para especificar tipos de titlebars que estão disponíveis para uma janela de teclado flexível.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- Estrutura de serviços de texto de enumeração TITLEBAR_TYPE
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105792635"
---
# <a name="titlebar_type-enumeration"></a><span data-ttu-id="d2aef-104">\_Enumeração de tipo TITLEBAR</span><span class="sxs-lookup"><span data-stu-id="d2aef-104">TITLEBAR\_TYPE enumeration</span></span>

<span data-ttu-id="d2aef-105">Os elementos da enumeração de **\_ tipo TITLEBAR** são usados para especificar tipos de titlebars que estão disponíveis para uma janela de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="d2aef-105">Elements of the **TITLEBAR\_TYPE** enumeration are used to specify types of titlebars that are available for a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2aef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2aef-106">Syntax</span></span>


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="d2aef-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="d2aef-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d2aef-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="d2aef-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="d2aef-109">A janela teclado soft não usa nenhuma TitleBar.</span><span class="sxs-lookup"><span data-stu-id="d2aef-109">The soft keyboard window uses no titlebar.</span></span>

</dd> <dt>

<span data-ttu-id="d2aef-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**\_garra da TITLEBAR \_ \_ somente horizontal**</span><span class="sxs-lookup"><span data-stu-id="d2aef-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR\_GRIPPER\_HORIZ\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="d2aef-111">A janela teclado soft usa apenas uma barra de garra horizontal.</span><span class="sxs-lookup"><span data-stu-id="d2aef-111">The soft keyboard window uses a horizontal gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="d2aef-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**\_garra da TITLEBAR \_ somente verticalmente \_**</span><span class="sxs-lookup"><span data-stu-id="d2aef-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR\_GRIPPER\_VERTI\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="d2aef-113">A janela teclado soft usa apenas uma barra vertical.</span><span class="sxs-lookup"><span data-stu-id="d2aef-113">The soft keyboard window uses a vertical gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="d2aef-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**botão de garra da TITLEBAR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d2aef-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TITLEBAR\_GRIPPER\_BUTTON**</span></span>
</dt> <dd>

<span data-ttu-id="d2aef-115">A janela teclado soft usa apenas um botão de garra.</span><span class="sxs-lookup"><span data-stu-id="d2aef-115">The soft keyboard window uses a gripper button only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2aef-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2aef-116">Requirements</span></span>



| <span data-ttu-id="d2aef-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2aef-117">Requirement</span></span> | <span data-ttu-id="d2aef-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d2aef-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2aef-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2aef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2aef-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2aef-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d2aef-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2aef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2aef-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d2aef-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d2aef-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d2aef-123">Redistributable</span></span><br/>          | <span data-ttu-id="d2aef-124">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d2aef-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="d2aef-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2aef-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2aef-126"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2aef-126"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="d2aef-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="d2aef-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2aef-128"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2aef-128"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





