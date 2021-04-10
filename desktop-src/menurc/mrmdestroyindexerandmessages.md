---
title: Função MrmDestroyIndexerAndMessages (MrmResourceIndexer. h)
description: Libera recursos de máquina associados a um indexador de recurso.
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- Menus de função MrmDestroyIndexerAndMessages e outros recursos
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e351c4d9e43bbb094d9738a6fef1b90c657b01e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009741"
---
# <a name="mrmdestroyindexerandmessages-function"></a><span data-ttu-id="0cc21-104">Função MrmDestroyIndexerAndMessages</span><span class="sxs-lookup"><span data-stu-id="0cc21-104">MrmDestroyIndexerAndMessages function</span></span>

<span data-ttu-id="0cc21-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0cc21-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0cc21-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0cc21-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0cc21-107">Libera recursos de máquina associados a um indexador de recurso.</span><span class="sxs-lookup"><span data-stu-id="0cc21-107">Releases machine resources associated with a resource indexer.</span></span> <span data-ttu-id="0cc21-108">Destrói o identificador, libera o indexador e exclui todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="0cc21-108">Destroys the handle, frees the indexer, and deletes any messages.</span></span> <span data-ttu-id="0cc21-109">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="0cc21-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc21-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cc21-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a><span data-ttu-id="0cc21-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cc21-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cc21-112">*indexador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cc21-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cc21-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="0cc21-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="0cc21-114">Um identificador que identifica o indexador de recursos a ser destruído.</span><span class="sxs-lookup"><span data-stu-id="0cc21-114">A handle identifying the resource indexer to destroy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cc21-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0cc21-115">Return value</span></span>

<span data-ttu-id="0cc21-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0cc21-116">Type: **HRESULT**</span></span>

<span data-ttu-id="0cc21-117">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="0cc21-117">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="0cc21-118">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="0cc21-118">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc21-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cc21-119">Requirements</span></span>



| <span data-ttu-id="0cc21-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cc21-120">Requirement</span></span> | <span data-ttu-id="0cc21-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0cc21-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc21-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cc21-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc21-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="0cc21-123">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0cc21-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cc21-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc21-125">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="0cc21-125">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0cc21-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cc21-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cc21-127"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cc21-127"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="0cc21-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cc21-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cc21-129"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cc21-129"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="0cc21-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0cc21-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cc21-131"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cc21-131"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0cc21-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cc21-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc21-133">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="0cc21-133">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

