---
description: O método CreateSourceImage do objeto Merge permite que o cliente Extraia os arquivos de um módulo para uma imagem de origem no disco após uma mesclagem, levando em conta as alterações ao módulo que podem ter sido feitas durante a configuração do módulo.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Método Merge. CreateSourceImage (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756727"
---
# <a name="mergecreatesourceimage-method"></a><span data-ttu-id="8dc86-103">Método Merge. CreateSourceImage</span><span class="sxs-lookup"><span data-stu-id="8dc86-103">Merge.CreateSourceImage method</span></span>

<span data-ttu-id="8dc86-104">O método **CreateSourceImage** do objeto [**Merge**](merge-object.md) permite que o cliente Extraia os arquivos de um módulo para uma imagem de origem no disco após uma mesclagem, levando em conta as alterações ao módulo que podem ter sido feitas durante a configuração do módulo.</span><span class="sxs-lookup"><span data-stu-id="8dc86-104">The **CreateSourceImage** method of the [**Merge**](merge-object.md) object allows the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.</span></span> <span data-ttu-id="8dc86-105">A lista de arquivos a serem extraídos é obtida da tabela de arquivos do módulo durante o processo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8dc86-105">The list of files to be extracted is taken from the file table of the module during the merge process.</span></span> <span data-ttu-id="8dc86-106">A lista de arquivos consiste em cada arquivo copiado com êxito da tabela de arquivos do módulo para o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="8dc86-106">The list of files consists of every file successfully copied from the file table of the module to the target database.</span></span> <span data-ttu-id="8dc86-107">As entradas de tabela de arquivo que não foram copiadas devido a conflitos de chave primária com linhas existentes no banco de dados não fazem parte dessa lista.</span><span class="sxs-lookup"><span data-stu-id="8dc86-107">File table entries that were not copied due to primary key conflicts with existing rows in the database are not a part of this list.</span></span> <span data-ttu-id="8dc86-108">No momento da criação da imagem, o diretório de cada um desses arquivos é proveniente do banco de dados aberto (post-Merge).</span><span class="sxs-lookup"><span data-stu-id="8dc86-108">At image creation time, the directory for each of these files comes from the open (post-merge) database.</span></span> <span data-ttu-id="8dc86-109">O caminho especificado no parâmetro *path* é a raiz da imagem de origem para a instalação.</span><span class="sxs-lookup"><span data-stu-id="8dc86-109">The path specified in the *Path* parameter is the root of the source image for the install.</span></span> <span data-ttu-id="8dc86-110">*fLongFileNames* determina se nomes de arquivo longos são ou não usados para segmentos de caminho e nomes de arquivo finais.</span><span class="sxs-lookup"><span data-stu-id="8dc86-110">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span> <span data-ttu-id="8dc86-111">A função falhará se nenhum banco de dados estiver aberto, nenhum módulo estiver aberto ou nenhuma mesclagem tiver sido executada.</span><span class="sxs-lookup"><span data-stu-id="8dc86-111">The function fails if no database is open, no module is open, or no merge has been performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc86-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dc86-112">Syntax</span></span>


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="8dc86-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dc86-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dc86-114">*Caminho*</span><span class="sxs-lookup"><span data-stu-id="8dc86-114">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc86-115">O caminho da raiz da imagem de origem para a instalação.</span><span class="sxs-lookup"><span data-stu-id="8dc86-115">The path of the root of the source image for the install.</span></span>

</dd> <dt>

<span data-ttu-id="8dc86-116">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="8dc86-116">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc86-117">*fLongFileNames* determina se nomes de arquivo longos são ou não usados para segmentos de caminho e nomes de arquivo finais.</span><span class="sxs-lookup"><span data-stu-id="8dc86-117">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="8dc86-118">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="8dc86-118">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc86-119">Esta é uma lista de caminhos totalmente qualificados para os arquivos que foram extraídos com êxito.</span><span class="sxs-lookup"><span data-stu-id="8dc86-119">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dc86-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8dc86-120">Return value</span></span>

<span data-ttu-id="8dc86-121">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8dc86-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dc86-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dc86-122">Remarks</span></span>

<span data-ttu-id="8dc86-123">Todos os arquivos no diretório de destino com o mesmo nome são substituídos.</span><span class="sxs-lookup"><span data-stu-id="8dc86-123">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="8dc86-124">O caminho será criado se ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="8dc86-124">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="8dc86-125">C++</span><span class="sxs-lookup"><span data-stu-id="8dc86-125">C++</span></span>

<span data-ttu-id="8dc86-126">Consulte a função [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .</span><span class="sxs-lookup"><span data-stu-id="8dc86-126">See [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dc86-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dc86-127">Requirements</span></span>



| <span data-ttu-id="8dc86-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dc86-128">Requirement</span></span> | <span data-ttu-id="8dc86-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8dc86-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc86-130">Versão</span><span class="sxs-lookup"><span data-stu-id="8dc86-130">Version</span></span><br/> | <span data-ttu-id="8dc86-131">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8dc86-131">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="8dc86-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8dc86-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8dc86-133"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dc86-133"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="8dc86-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8dc86-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="8dc86-135"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dc86-135"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




