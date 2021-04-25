---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core. h)
description: Cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 43e43e00385e10f0da0ba459cdc16e84562b72ec
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955019"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="fde90-103">Função DWriteCoreCreateFactory (dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="fde90-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="fde90-104">Cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.</span><span class="sxs-lookup"><span data-stu-id="fde90-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fde90-105">Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fde90-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="fde90-106">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="fde90-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="fde90-107">Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/directwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="fde90-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="fde90-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fde90-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="fde90-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fde90-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="fde90-110">Tipo: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="fde90-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="fde90-111">Um valor que especifica se o objeto de fábrica será compartilhado, isolado ou restrito.</span><span class="sxs-lookup"><span data-stu-id="fde90-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="fde90-112">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="fde90-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="fde90-113">Um valor de GUID que identifica a interface de fábrica DirectWrite, como __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span><span class="sxs-lookup"><span data-stu-id="fde90-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="fde90-114">Tipo: <b>IUnknown \* \*</b></span><span class="sxs-lookup"><span data-stu-id="fde90-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="fde90-115">Um endereço de um ponteiro para o objeto da fábrica DirectWrite recém-criado.</span><span class="sxs-lookup"><span data-stu-id="fde90-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="fde90-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fde90-116">Return value</span></span>

<span data-ttu-id="fde90-117">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="fde90-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="fde90-118">Se esse método tiver sucesso, ele retornará <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="fde90-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="fde90-119">Caso contrário, ele retorna um código de erro <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="fde90-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="fde90-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fde90-120">Examples</span></span>

<span data-ttu-id="fde90-121">Consulte o tópico [visão geral do DWriteCore](/windows/win32/directwrite/dwritecore-overview) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="fde90-121">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde90-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="fde90-122">Remarks</span></span>

<span data-ttu-id="fde90-123">Isso é funcionalmente o mesmo que a função [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada pela versão do sistema do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="fde90-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="fde90-124">A função DWriteCore tem um nome diferente para evitar ambigüidade.</span><span class="sxs-lookup"><span data-stu-id="fde90-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde90-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde90-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fde90-126">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="fde90-126">**Minimum supported client**</span></span> | <span data-ttu-id="fde90-127">Windows 10, reunião do projeto [aplicativos Win32]</span><span class="sxs-lookup"><span data-stu-id="fde90-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="fde90-128">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="fde90-128">**Header**</span></span> | <span data-ttu-id="fde90-129">dwrite. h (incluir dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="fde90-129">dwrite.h (include dwrite_core.h)</span></span> |
