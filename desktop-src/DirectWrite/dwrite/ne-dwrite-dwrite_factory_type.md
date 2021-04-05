---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Especifica o tipo de objeto de fábrica DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
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
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2020
ms.locfileid: "104008788"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="ae77e-103">Enumeração de DWRITE_FACTORY_TYPE (DWRITE. h)</span><span class="sxs-lookup"><span data-stu-id="ae77e-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="ae77e-104">Especifica o tipo de objeto de fábrica DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ae77e-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae77e-105">Essa API está disponível como parte da implementação DWriteCore do [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ae77e-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="ae77e-106">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="ae77e-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="ae77e-107">Para obter mais informações e exemplos de código, consulte [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="ae77e-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae77e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae77e-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a><span data-ttu-id="ae77e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="ae77e-109">Constants</span></span>

| <span data-ttu-id="ae77e-110">Nome</span><span class="sxs-lookup"><span data-stu-id="ae77e-110">Name</span></span> | <span data-ttu-id="ae77e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae77e-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="ae77e-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="ae77e-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="ae77e-113">Indica que a fábrica DirectWrite é uma fábrica compartilhada e que permite a reutilização de dados de fontes armazenados em cache em vários componentes em processo.</span><span class="sxs-lookup"><span data-stu-id="ae77e-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="ae77e-114">Essas fábricas também aproveitam os componentes de cache de fonte de processo cruzado para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="ae77e-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="ae77e-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="ae77e-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="ae77e-116">Indica que o objeto de fábrica DirectWrite está isolado.</span><span class="sxs-lookup"><span data-stu-id="ae77e-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="ae77e-117">Os objetos criados a partir da fábrica isolada não interagem com o estado interno do DirectWrite de outros componentes.</span><span class="sxs-lookup"><span data-stu-id="ae77e-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="ae77e-118">DWRITE_FACTORY_TYPE_RESTRICTED</span><span class="sxs-lookup"><span data-stu-id="ae77e-118">DWRITE_FACTORY_TYPE_RESTRICTED</span></span> | <span data-ttu-id="ae77e-119">Os objetos criados a partir de uma fábrica restrita não usam nem modificam os dados de estado interno ou armazenados em cache usados por outras fábricas.</span><span class="sxs-lookup"><span data-stu-id="ae77e-119">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="ae77e-120">Além disso, a coleção de fontes do sistema contém apenas fontes conhecidas.</span><span class="sxs-lookup"><span data-stu-id="ae77e-120">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="ae77e-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae77e-121">Examples</span></span>

<span data-ttu-id="ae77e-122">Consulte o tópico [visão geral do DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e o aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="ae77e-122">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae77e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae77e-123">Remarks</span></span>

<span data-ttu-id="ae77e-124">Um objeto de fábrica DirectWrite contém informações sobre seu estado interno, como registro de carregador de fonte e dados de fonte em cache.</span><span class="sxs-lookup"><span data-stu-id="ae77e-124">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="ae77e-125">Na maioria dos casos, você deve usar o objeto de fábrica compartilhado, pois ele permite que vários componentes usem o DirectWrite para compartilhar informações de estado DirectWrite internas, reduzindo assim o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="ae77e-125">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="ae77e-126">No entanto, há casos em que é desejável reduzir o impacto de um componente no restante do processo, como um plug-in de uma fonte não confiável, na área restrita e no isolamento do restante dos componentes do processo.</span><span class="sxs-lookup"><span data-stu-id="ae77e-126">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="ae77e-127">Nesses casos, você deve usar uma fábrica isolada para o componente de área restrita.</span><span class="sxs-lookup"><span data-stu-id="ae77e-127">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="ae77e-128">Uma fábrica restrita é mais bloqueada do que uma fábrica isolada.</span><span class="sxs-lookup"><span data-stu-id="ae77e-128">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="ae77e-129">Ele não interage com um cache de fontes entre processos e persistentes de nenhuma forma.</span><span class="sxs-lookup"><span data-stu-id="ae77e-129">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="ae77e-130">Além disso, a coleção de fontes do sistema retornada por essa fábrica inclui apenas fontes conhecidas.</span><span class="sxs-lookup"><span data-stu-id="ae77e-130">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="ae77e-131">Se você passar **DWRITE_FACTORY_TYPE_RESTRICTED** para uma versão de DWRITE mais antiga que DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) retornará **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="ae77e-131">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae77e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae77e-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ae77e-133">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="ae77e-133">**Minimum supported client**</span></span> | <span data-ttu-id="ae77e-134">Windows 10, versão 0,1 de pré-lançamento do projeto [aplicativos Win32]</span><span class="sxs-lookup"><span data-stu-id="ae77e-134">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="ae77e-135">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="ae77e-135">**Header**</span></span> | <span data-ttu-id="ae77e-136">dwrite. h (incluir dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="ae77e-136">dwrite.h (include dwrite_core.h)</span></span> |
