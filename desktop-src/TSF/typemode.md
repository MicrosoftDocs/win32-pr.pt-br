---
title: Enumeração TYPEmode (Softkbdc. h)
description: Elementos da enumeração TYPEmode são usados para especificar modos de tipo que estão disponíveis para um teclado virtual.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Estrutura de serviços de texto de enumeração do TIPOmode
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757230"
---
# <a name="typemode-enumeration"></a><span data-ttu-id="4ae97-104">Enumeração TYPEmode</span><span class="sxs-lookup"><span data-stu-id="4ae97-104">TYPEMODE enumeration</span></span>

<span data-ttu-id="4ae97-105">Elementos da enumeração **typemode** são usados para especificar modos de tipo que estão disponíveis para um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="4ae97-105">Elements of the **TYPEMODE** enumeration are used to specify type modes that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae97-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae97-106">Syntax</span></span>


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a><span data-ttu-id="4ae97-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="4ae97-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4ae97-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span><span class="sxs-lookup"><span data-stu-id="4ae97-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span></span>
</dt> <dd>

<span data-ttu-id="4ae97-109">O usuário pode clicar nas chaves na tela para digitar o texto.</span><span class="sxs-lookup"><span data-stu-id="4ae97-109">The user can click the on-screen keys to type text.</span></span>

</dd> <dt>

<span data-ttu-id="4ae97-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Operação**</span><span class="sxs-lookup"><span data-stu-id="4ae97-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hover**</span></span>
</dt> <dd>

<span data-ttu-id="4ae97-111">O usuário pode apontar para uma chave por um período de tempo predefinido e o caractere selecionado é digitado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4ae97-111">The user can point to a key for a predefined period of time, and the selected character is typed automatically.</span></span>

</dd> <dt>

<span data-ttu-id="4ae97-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Varredura**</span><span class="sxs-lookup"><span data-stu-id="4ae97-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Scanning**</span></span>
</dt> <dd>

<span data-ttu-id="4ae97-113">O teclado virtual verifica continuamente a área de entrada e realça as regiões em que o usuário pode pressionar uma tecla de atalho ou usar um dispositivo de entrada de interruptor.</span><span class="sxs-lookup"><span data-stu-id="4ae97-113">The soft keyboard continually scans the input area and highlights regions where the user can press a shortcut key or use a switch-input device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ae97-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ae97-114">Requirements</span></span>



| <span data-ttu-id="4ae97-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae97-115">Requirement</span></span> | <span data-ttu-id="4ae97-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4ae97-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae97-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ae97-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ae97-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ae97-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4ae97-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ae97-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ae97-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ae97-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4ae97-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4ae97-121">Redistributable</span></span><br/>          | <span data-ttu-id="4ae97-122">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4ae97-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="4ae97-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ae97-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ae97-124"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae97-124"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="4ae97-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="4ae97-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ae97-126"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ae97-126"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





