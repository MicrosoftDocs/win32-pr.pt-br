---
description: O método ExtractFiles do objeto de mesclagem extrai o arquivo. cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Método Merge. ExtractFiles (Advpub. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783269"
---
# <a name="mergeextractfiles-method"></a><span data-ttu-id="bb5a7-103">Método Merge. ExtractFiles</span><span class="sxs-lookup"><span data-stu-id="bb5a7-103">Merge.ExtractFiles method</span></span>

<span data-ttu-id="bb5a7-104">O método **ExtractFiles** do objeto de [**mesclagem**](merge-object.md) extrai o arquivo. cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="bb5a7-104">The **ExtractFiles** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5a7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb5a7-105">Syntax</span></span>


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="bb5a7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb5a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb5a7-107">*Caminho*</span><span class="sxs-lookup"><span data-stu-id="bb5a7-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="bb5a7-108">O diretório de destino totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="bb5a7-108">The fully qualified destination directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb5a7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb5a7-109">Return value</span></span>

<span data-ttu-id="bb5a7-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bb5a7-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb5a7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb5a7-111">Remarks</span></span>

<span data-ttu-id="bb5a7-112">Todos os arquivos no diretório de destino com o mesmo nome são substituídos.</span><span class="sxs-lookup"><span data-stu-id="bb5a7-112">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="bb5a7-113">O caminho será criado se ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="bb5a7-113">The path is created if it does not already exist.</span></span>

<span data-ttu-id="bb5a7-114">O **ExtractFiles** sempre extrai arquivos usando nomes de arquivo curtos para o caminho.</span><span class="sxs-lookup"><span data-stu-id="bb5a7-114">**ExtractFiles** always extracts files using short file names for the path.</span></span> <span data-ttu-id="bb5a7-115">Para usar nomes de arquivo longos para o caminho, use o [**método ExtractFilesEx**](merge-extractfilesex.md).</span><span class="sxs-lookup"><span data-stu-id="bb5a7-115">To use long file names for the path, use the [**ExtractFilesEx method**](merge-extractfilesex.md).</span></span>

### <a name="c"></a><span data-ttu-id="bb5a7-116">C++</span><span class="sxs-lookup"><span data-stu-id="bb5a7-116">C++</span></span>

<span data-ttu-id="bb5a7-117">Consulte a função [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) .</span><span class="sxs-lookup"><span data-stu-id="bb5a7-117">See [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb5a7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb5a7-118">Requirements</span></span>



| <span data-ttu-id="bb5a7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb5a7-119">Requirement</span></span> | <span data-ttu-id="bb5a7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bb5a7-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5a7-121">Versão</span><span class="sxs-lookup"><span data-stu-id="bb5a7-121">Version</span></span><br/> | <span data-ttu-id="bb5a7-122">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="bb5a7-122">Mergemod.dll 1.0 or later</span></span><br/>                                                                     |
| <span data-ttu-id="bb5a7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb5a7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bb5a7-124"><dt>Advpub. h (incluir Mergemod. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb5a7-124"><dt>Advpub.h (include Mergemod.h)</dt></span></span> </dl> |
| <span data-ttu-id="bb5a7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bb5a7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="bb5a7-126"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb5a7-126"><dt>Mergemod.dll</dt></span></span> </dl>                  |



 

 
