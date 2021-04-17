---
description: O método ExtractFilesEx do objeto de mesclagem extrai o arquivo. cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Método Merge. ExtractFilesEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747963"
---
# <a name="mergeextractfilesex-method"></a><span data-ttu-id="d0e22-103">Método Merge. ExtractFilesEx</span><span class="sxs-lookup"><span data-stu-id="d0e22-103">Merge.ExtractFilesEx method</span></span>

<span data-ttu-id="d0e22-104">O método **ExtractFilesEx** do objeto de [**mesclagem**](merge-object.md) extrai o arquivo. cab inserido de um módulo e, em seguida, grava esses arquivos no diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="d0e22-104">The **ExtractFilesEx** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0e22-105">Syntax</span></span>


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="d0e22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0e22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e22-107">*Caminho*</span><span class="sxs-lookup"><span data-stu-id="d0e22-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="d0e22-108">O diretório de destino totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="d0e22-108">The fully qualified destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="d0e22-109">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="d0e22-109">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="d0e22-110">Defina para especificar o uso de nomes de arquivo longos para segmentos de caminho e nomes de arquivo finais.</span><span class="sxs-lookup"><span data-stu-id="d0e22-110">Set to specify using long file names for path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="d0e22-111">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="d0e22-111">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="d0e22-112">Esta é uma lista de caminhos totalmente qualificados para os arquivos que foram extraídos com êxito.</span><span class="sxs-lookup"><span data-stu-id="d0e22-112">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e22-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0e22-113">Return value</span></span>

<span data-ttu-id="d0e22-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d0e22-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0e22-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0e22-115">Remarks</span></span>

<span data-ttu-id="d0e22-116">Todos os arquivos no diretório de destino com o mesmo nome são substituídos.</span><span class="sxs-lookup"><span data-stu-id="d0e22-116">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="d0e22-117">O caminho será criado se ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="d0e22-117">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="d0e22-118">C++</span><span class="sxs-lookup"><span data-stu-id="d0e22-118">C++</span></span>

<span data-ttu-id="d0e22-119">Consulte a função [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) .</span><span class="sxs-lookup"><span data-stu-id="d0e22-119">See [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e22-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0e22-120">Requirements</span></span>



| <span data-ttu-id="d0e22-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e22-121">Requirement</span></span> | <span data-ttu-id="d0e22-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d0e22-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e22-123">Versão</span><span class="sxs-lookup"><span data-stu-id="d0e22-123">Version</span></span><br/> | <span data-ttu-id="d0e22-124">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d0e22-124">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="d0e22-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0e22-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d0e22-126"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0e22-126"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0e22-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d0e22-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0e22-128"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0e22-128"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




