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
ms.openlocfilehash: 6606ad884fd65195e9922d348cc4fe565b95f2ee
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107882130"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="6b170-103">Função DWriteCoreCreateFactory (dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="6b170-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="6b170-104">Cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.</span><span class="sxs-lookup"><span data-stu-id="6b170-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b170-105">Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6b170-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="6b170-106">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="6b170-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="6b170-107">Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="6b170-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b170-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b170-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="6b170-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b170-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="6b170-110">Tipo: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="6b170-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="6b170-111">Um valor que especifica se o objeto de fábrica será compartilhado, isolado ou restrito.</span><span class="sxs-lookup"><span data-stu-id="6b170-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="6b170-112">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="6b170-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="6b170-113">Um valor de GUID que identifica a interface de fábrica DirectWrite, como __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span><span class="sxs-lookup"><span data-stu-id="6b170-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="6b170-114">Tipo: <b>IUnknown \* \*</b></span><span class="sxs-lookup"><span data-stu-id="6b170-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="6b170-115">Um endereço de um ponteiro para o objeto da fábrica DirectWrite recém-criado.</span><span class="sxs-lookup"><span data-stu-id="6b170-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b170-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b170-116">Return value</span></span>

<span data-ttu-id="6b170-117">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="6b170-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="6b170-118">Se esse método tiver sucesso, ele retornará <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="6b170-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="6b170-119">Caso contrário, ele retorna um código de erro <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="6b170-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="6b170-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b170-120">Examples</span></span>

<span data-ttu-id="6b170-121">Consulte o tópico [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="6b170-121">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b170-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b170-122">Remarks</span></span>

<span data-ttu-id="6b170-123">Isso é funcionalmente o mesmo que a função [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada pela versão do sistema do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="6b170-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="6b170-124">A função DWriteCore tem um nome diferente para evitar ambigüidade.</span><span class="sxs-lookup"><span data-stu-id="6b170-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b170-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b170-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6b170-126">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="6b170-126">**Minimum supported client**</span></span> | <span data-ttu-id="6b170-127">Windows 10, reunião do projeto [aplicativos Win32]</span><span class="sxs-lookup"><span data-stu-id="6b170-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="6b170-128">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="6b170-128">**Header**</span></span> | <span data-ttu-id="6b170-129">dwrite. h (incluir dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="6b170-129">dwrite.h (include dwrite_core.h)</span></span> |
