---
title: Função MrmFreeMemory (MrmResourceIndexer. h)
description: Libera memória alocada por MrmCreateConfigInMemory, MrmCreateResourceFileInMemory, MrmDumpPriFileInMemory e MrmDumpPriDataInMemory.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Menus de função MrmFreeMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757572"
---
# <a name="mrmfreememory-function"></a><span data-ttu-id="aa53f-104">Função MrmFreeMemory</span><span class="sxs-lookup"><span data-stu-id="aa53f-104">MrmFreeMemory function</span></span>

<span data-ttu-id="aa53f-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="aa53f-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aa53f-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="aa53f-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aa53f-107">Libera memória alocada por [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)e [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="aa53f-107">Frees memory allocated by [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), and [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="aa53f-108">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="aa53f-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa53f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa53f-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a><span data-ttu-id="aa53f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa53f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa53f-111">*dados* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="aa53f-111">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa53f-112">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="aa53f-112">Type: \**BYTE\** _</span></span>

<span data-ttu-id="aa53f-113">Um ponteiro para a memória alocada e retornada por [_ *MrmCreateConfigInMemory* \*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)ou [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="aa53f-113">A pointer to memory allocated and returned by [_ *MrmCreateConfigInMemory*\*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa53f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa53f-114">Return value</span></span>

<span data-ttu-id="aa53f-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aa53f-115">Type: **HRESULT**</span></span>

<span data-ttu-id="aa53f-116">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="aa53f-116">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="aa53f-117">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="aa53f-117">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa53f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa53f-118">Requirements</span></span>



| <span data-ttu-id="aa53f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa53f-119">Requirement</span></span> | <span data-ttu-id="aa53f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="aa53f-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa53f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa53f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aa53f-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="aa53f-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aa53f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa53f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aa53f-124">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="aa53f-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aa53f-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa53f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa53f-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa53f-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="aa53f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa53f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa53f-128"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa53f-128"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="aa53f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="aa53f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa53f-130"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa53f-130"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="aa53f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa53f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa53f-132">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="aa53f-132">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

