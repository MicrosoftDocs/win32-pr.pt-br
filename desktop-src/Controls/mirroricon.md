---
title: Função MirrorIcon
description: Inverte os ícones (espelhos) para que sejam exibidos corretamente em um contexto de dispositivo espelhado.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Controles do Windows da função MirrorIcon
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008997"
---
# <a name="mirroricon-function"></a><span data-ttu-id="86d2e-104">Função MirrorIcon</span><span class="sxs-lookup"><span data-stu-id="86d2e-104">MirrorIcon function</span></span>

<span data-ttu-id="86d2e-105">\[O **MirrorIcon** está disponível por meio do Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="86d2e-105">\[**MirrorIcon** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="86d2e-106">Ele pode ser alterado ou indisponível nas versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="86d2e-106">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="86d2e-107">Inverte os ícones (espelhos) para que sejam exibidos corretamente em um contexto de dispositivo espelhado.</span><span class="sxs-lookup"><span data-stu-id="86d2e-107">Reverses (mirrors) icons so that they are displayed correctly on a mirrored device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d2e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86d2e-108">Syntax</span></span>


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a><span data-ttu-id="86d2e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86d2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86d2e-110">*phIconSmall* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="86d2e-110">*phIconSmall* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86d2e-111">Tipo: \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="86d2e-111">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="86d2e-112">Um ponteiro para o identificador de ícone que faz referência a uma pequena versão de um ícone.</span><span class="sxs-lookup"><span data-stu-id="86d2e-112">A pointer to the icon handle that references a small version of an icon.</span></span>

</dd> <dt>

<span data-ttu-id="86d2e-113">_phIconLarge \* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="86d2e-113">_phIconLarge\* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86d2e-114">Tipo: \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="86d2e-114">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="86d2e-115">Um ponteiro para o identificador de ícone que faz referência a uma grande versão de um ícone.</span><span class="sxs-lookup"><span data-stu-id="86d2e-115">A pointer to the icon handle that references a large version of an icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86d2e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86d2e-116">Return value</span></span>

<span data-ttu-id="86d2e-117">Tipo: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)*\*</span><span class="sxs-lookup"><span data-stu-id="86d2e-117">Type: _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)*\*</span></span>

<span data-ttu-id="86d2e-118">**Verdadeiro se for** bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="86d2e-118">**TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="86d2e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="86d2e-119">Remarks</span></span>

<span data-ttu-id="86d2e-120">**MirrorIcon** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="86d2e-120">**MirrorIcon** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="86d2e-121">Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 414 de ComCtl32.dll para obter um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="86d2e-121">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 414 from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="86d2e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86d2e-122">Requirements</span></span>



| <span data-ttu-id="86d2e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="86d2e-123">Requirement</span></span> | <span data-ttu-id="86d2e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="86d2e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86d2e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86d2e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="86d2e-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86d2e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="86d2e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86d2e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="86d2e-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="86d2e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="86d2e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="86d2e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86d2e-130"><dt>Comctl32.dll (versão 5,81 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="86d2e-130"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

