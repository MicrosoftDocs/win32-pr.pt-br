---
title: Função MrmDumpPriFile (MrmResourceIndexer. h)
description: Despeja um arquivo PRI (que é binário) para seu equivalente XML (como um arquivo no disco) para torná-lo mais fácil de ler.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Menus de função MrmDumpPriFile e outros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644731"
---
# <a name="mrmdumpprifile-function"></a><span data-ttu-id="20b08-104">Função MrmDumpPriFile</span><span class="sxs-lookup"><span data-stu-id="20b08-104">MrmDumpPriFile function</span></span>

<span data-ttu-id="20b08-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="20b08-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="20b08-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="20b08-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="20b08-107">Despeja um arquivo PRI (que é binário) para seu equivalente XML (como um arquivo no disco) para torná-lo mais fácil de ler.</span><span class="sxs-lookup"><span data-stu-id="20b08-107">Dumps a PRI file (which is binary) to its XML equivalent (as a file on disk), in order to make it more easily readable.</span></span> <span data-ttu-id="20b08-108">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="20b08-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="20b08-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20b08-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="20b08-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20b08-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20b08-111">*indexFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20b08-111">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20b08-112">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="20b08-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="20b08-113">Um caminho de arquivo completo para um arquivo PRI.</span><span class="sxs-lookup"><span data-stu-id="20b08-113">A full file path to a PRI file.</span></span> <span data-ttu-id="20b08-114">Esse é o arquivo PRI que será despejado em XML.</span><span class="sxs-lookup"><span data-stu-id="20b08-114">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="20b08-115">*schemaPriFile* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="20b08-115">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20b08-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="20b08-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="20b08-117">Um caminho de arquivo completo opcional para um arquivo de esquema (ou para um arquivo PRI que representa um esquema; consulte comentários).</span><span class="sxs-lookup"><span data-stu-id="20b08-117">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="20b08-118">*dumptype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20b08-118">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20b08-119">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="20b08-119">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="20b08-120">Especifica o quão detalhado o despejo de XML deve ser ou se um esquema deve ser despejado.</span><span class="sxs-lookup"><span data-stu-id="20b08-120">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="20b08-121">*outputXmlFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20b08-121">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20b08-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="20b08-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="20b08-123">O caminho de um arquivo XML a ser criado.</span><span class="sxs-lookup"><span data-stu-id="20b08-123">The path of an XML file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20b08-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20b08-124">Return value</span></span>

<span data-ttu-id="20b08-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="20b08-125">Type: **HRESULT**</span></span>

<span data-ttu-id="20b08-126">S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="20b08-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="20b08-127">Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="20b08-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="20b08-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="20b08-128">Remarks</span></span>

<span data-ttu-id="20b08-129">Um pacote de recursos sem esquema é aquele criado com o argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passado para [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou com a opção *omitSchemaFromResourcePacks* no arquivo de configuração PRI).</span><span class="sxs-lookup"><span data-stu-id="20b08-129">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="20b08-130">Para despejar um pacote de recursos sem esquema, passe o caminho para os dados PRI do pacote principal como o argumento para o parâmetro *schemaPriFile* .</span><span class="sxs-lookup"><span data-stu-id="20b08-130">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="20b08-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20b08-131">Requirements</span></span>



| <span data-ttu-id="20b08-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="20b08-132">Requirement</span></span> | <span data-ttu-id="20b08-133">Valor</span><span class="sxs-lookup"><span data-stu-id="20b08-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b08-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20b08-134">Minimum supported client</span></span><br/> | <span data-ttu-id="20b08-135">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="20b08-135">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="20b08-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20b08-136">Minimum supported server</span></span><br/> | <span data-ttu-id="20b08-137">\[Somente aplicativos da área de trabalho do Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="20b08-137">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20b08-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20b08-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="20b08-139"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="20b08-139"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="20b08-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20b08-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="20b08-141"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20b08-141"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="20b08-142">DLL</span><span class="sxs-lookup"><span data-stu-id="20b08-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b08-143"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b08-143"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="20b08-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="20b08-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b08-145">APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados</span><span class="sxs-lookup"><span data-stu-id="20b08-145">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

