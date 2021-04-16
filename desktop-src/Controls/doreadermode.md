---
title: Função doreadermode
description: Habilita o modo de leitura em uma janela.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Controles do Windows da função doreadermode
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456061"
---
# <a name="doreadermode-function"></a><span data-ttu-id="37783-104">Função doreadermode</span><span class="sxs-lookup"><span data-stu-id="37783-104">DoReaderMode function</span></span>

<span data-ttu-id="37783-105">\[O **Doreadermode** está disponível por meio do Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="37783-105">\[**DoReaderMode** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="37783-106">Ele pode não estar disponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="37783-106">It may be unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="37783-107">Habilita o modo de leitura em uma janela.</span><span class="sxs-lookup"><span data-stu-id="37783-107">Enables reader mode in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="37783-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37783-108">Syntax</span></span>


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a><span data-ttu-id="37783-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37783-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37783-110">*prmi* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37783-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37783-111">Tipo: **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="37783-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="37783-112">Um ponteiro para uma estrutura [**READERMODEINFO**](readermodeinfo.md) que contém informações de inicialização para o modo leitor.</span><span class="sxs-lookup"><span data-stu-id="37783-112">A pointer to a [**READERMODEINFO**](readermodeinfo.md) structure that contains initialization information for the reader mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37783-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37783-113">Return value</span></span>

<span data-ttu-id="37783-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="37783-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37783-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="37783-115">Remarks</span></span>

<span data-ttu-id="37783-116">O modo leitor é ativado por meio de dispositivos com suporte com um clique do mouse, normalmente usando um terceiro botão do mouse ou roda de rolagem.</span><span class="sxs-lookup"><span data-stu-id="37783-116">Reader mode is activated through supported devices by a mouse click, typically using a third mouse button or scroll wheel.</span></span> <span data-ttu-id="37783-117">O movimento subsequente do mouse em uma área especificada rola o conteúdo dessa área em vez de mover um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37783-117">Subsequent mouse movement in a specified area scrolls that area's contents rather than moving a pointer.</span></span> <span data-ttu-id="37783-118">Fora dessa área, o ponteiro do mouse é exibido e opera normalmente.</span><span class="sxs-lookup"><span data-stu-id="37783-118">Outside of that area, the mouse pointer is displayed and operates normally.</span></span> <span data-ttu-id="37783-119">Um segundo clique no botão ou na roda de rolagem libera o dispositivo do modo leitor.</span><span class="sxs-lookup"><span data-stu-id="37783-119">A second click of the button or scroll wheel releases the device from reader mode.</span></span>

> [!Note]  
> <span data-ttu-id="37783-120">Essa função não é declarada em nenhum cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="37783-120">This function is not declared in any public header.</span></span> <span data-ttu-id="37783-121">Para usá-lo, você deve acessá-lo como ordinal 383 de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="37783-121">To use it, you must access it as ordinal 383 from Comctl32.dll.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37783-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37783-122">Requirements</span></span>



| <span data-ttu-id="37783-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="37783-123">Requirement</span></span> | <span data-ttu-id="37783-124">Valor</span><span class="sxs-lookup"><span data-stu-id="37783-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37783-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37783-125">Minimum supported client</span></span><br/> | <span data-ttu-id="37783-126">Windows Vista, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37783-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="37783-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37783-127">Minimum supported server</span></span><br/> | <span data-ttu-id="37783-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37783-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="37783-129">DLL</span><span class="sxs-lookup"><span data-stu-id="37783-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37783-130"><dt>Comctl32.dll (versão 4,72 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="37783-130"><dt>Comctl32.dll (version 4.72 or later)</dt></span></span> </dl> |



 

 





