---
description: A tabela MsiFileHash é usada para armazenar um hash de 128 bits de um arquivo de origem fornecido pelo pacote de Windows Installer. O hash é dividido em valores de 4 32 bits e armazenados em colunas separadas da tabela.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Tabela MsiFileHash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780951"
---
# <a name="msifilehash-table"></a><span data-ttu-id="33bbe-104">Tabela MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="33bbe-104">MsiFileHash Table</span></span>

<span data-ttu-id="33bbe-105">A tabela **MsiFileHash** é usada para armazenar um hash de 128 bits de um arquivo de origem fornecido pelo pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="33bbe-105">The **MsiFileHash** table is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span> <span data-ttu-id="33bbe-106">O hash é dividido em valores de 4 32 bits e armazenados em colunas separadas da tabela.</span><span class="sxs-lookup"><span data-stu-id="33bbe-106">The hash is split into four 32-bit values and stored in separate columns of the table.</span></span>

<span data-ttu-id="33bbe-107">Windows Installer pode usar o hash de arquivo como um meio para detectar e eliminar a cópia de arquivo desnecessária.</span><span class="sxs-lookup"><span data-stu-id="33bbe-107">Windows Installer can use file hashing as a means to detect and eliminate unnecessary file copying.</span></span> <span data-ttu-id="33bbe-108">Um hash de arquivo armazenado na tabela **MsiFileHash** pode ser comparado com um hash de um arquivo existente no computador do usuário obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="33bbe-108">A file hash stored in the **MsiFileHash** table may be compared to a hash of an existing file on the user's computer obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="33bbe-109">A tabela **MsiFileHash** só pode ser usada com arquivos sem versão.</span><span class="sxs-lookup"><span data-stu-id="33bbe-109">The **MsiFileHash** table can only be used with unversioned files.</span></span>

<span data-ttu-id="33bbe-110">A tabela **MsiFileHash** tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="33bbe-110">The **MsiFileHash** table has the following columns.</span></span>



| <span data-ttu-id="33bbe-111">Coluna</span><span class="sxs-lookup"><span data-stu-id="33bbe-111">Column</span></span>    | <span data-ttu-id="33bbe-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="33bbe-112">Type</span></span>                               | <span data-ttu-id="33bbe-113">Chave</span><span class="sxs-lookup"><span data-stu-id="33bbe-113">Key</span></span> | <span data-ttu-id="33bbe-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="33bbe-114">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="33bbe-115">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="33bbe-115">File\_</span></span>    | [<span data-ttu-id="33bbe-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="33bbe-116">Identifier</span></span>](identifier.md)       | <span data-ttu-id="33bbe-117">S</span><span class="sxs-lookup"><span data-stu-id="33bbe-117">Y</span></span>   | <span data-ttu-id="33bbe-118">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-118">N</span></span>        |
| <span data-ttu-id="33bbe-119">Opções</span><span class="sxs-lookup"><span data-stu-id="33bbe-119">Options</span></span>   | [<span data-ttu-id="33bbe-120">Inteiro</span><span class="sxs-lookup"><span data-stu-id="33bbe-120">Integer</span></span>](integer.md)             | <span data-ttu-id="33bbe-121">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-121">N</span></span>   | <span data-ttu-id="33bbe-122">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-122">N</span></span>        |
| <span data-ttu-id="33bbe-123">HashPart1</span><span class="sxs-lookup"><span data-stu-id="33bbe-123">HashPart1</span></span> | [<span data-ttu-id="33bbe-124">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="33bbe-124">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="33bbe-125">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-125">N</span></span>   | <span data-ttu-id="33bbe-126">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-126">N</span></span>        |
| <span data-ttu-id="33bbe-127">HashPart2</span><span class="sxs-lookup"><span data-stu-id="33bbe-127">HashPart2</span></span> | [<span data-ttu-id="33bbe-128">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="33bbe-128">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="33bbe-129">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-129">N</span></span>   | <span data-ttu-id="33bbe-130">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-130">N</span></span>        |
| <span data-ttu-id="33bbe-131">HashPart3</span><span class="sxs-lookup"><span data-stu-id="33bbe-131">HashPart3</span></span> | [<span data-ttu-id="33bbe-132">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="33bbe-132">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="33bbe-133">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-133">N</span></span>   | <span data-ttu-id="33bbe-134">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-134">N</span></span>        |
| <span data-ttu-id="33bbe-135">Hashpart4</span><span class="sxs-lookup"><span data-stu-id="33bbe-135">Hashpart4</span></span> | [<span data-ttu-id="33bbe-136">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="33bbe-136">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="33bbe-137">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-137">N</span></span>   | <span data-ttu-id="33bbe-138">N</span><span class="sxs-lookup"><span data-stu-id="33bbe-138">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="33bbe-139">Colunas</span><span class="sxs-lookup"><span data-stu-id="33bbe-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="33bbe-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="33bbe-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="33bbe-141">Chave estrangeira para [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="33bbe-141">Foreign key to [File table](file-table.md).</span></span> <span data-ttu-id="33bbe-142">Cadeia de caracteres de 72 caracteres.</span><span class="sxs-lookup"><span data-stu-id="33bbe-142">72 char string.</span></span>

</dd> <dt>

<span data-ttu-id="33bbe-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opções</span><span class="sxs-lookup"><span data-stu-id="33bbe-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="33bbe-144">Essa coluna deve ser 0 e reservada para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="33bbe-144">This column must be 0 and is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="33bbe-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span><span class="sxs-lookup"><span data-stu-id="33bbe-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span></span>
</dt> <dd>

<span data-ttu-id="33bbe-146">Primeiros 32 bits de hash.</span><span class="sxs-lookup"><span data-stu-id="33bbe-146">First 32 bits of hash.</span></span> <span data-ttu-id="33bbe-147">O hash de arquivo inserido neste campo deve ser obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou o [**método FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="33bbe-147">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="33bbe-148">Não use outros métodos.</span><span class="sxs-lookup"><span data-stu-id="33bbe-148">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="33bbe-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span><span class="sxs-lookup"><span data-stu-id="33bbe-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span></span>
</dt> <dd>

<span data-ttu-id="33bbe-150">Segundo 32 bits de hash.</span><span class="sxs-lookup"><span data-stu-id="33bbe-150">Second 32 bits of hash.</span></span> <span data-ttu-id="33bbe-151">O hash de arquivo inserido neste campo deve ser obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou o [**método FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="33bbe-151">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="33bbe-152">Não use outros métodos de hash.</span><span class="sxs-lookup"><span data-stu-id="33bbe-152">Do not use other hashing methods.</span></span>

</dd> <dt>

<span data-ttu-id="33bbe-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span><span class="sxs-lookup"><span data-stu-id="33bbe-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span></span>
</dt> <dd>

<span data-ttu-id="33bbe-154">Terceiro 32 bits de hash.</span><span class="sxs-lookup"><span data-stu-id="33bbe-154">Third 32 bits of hash.</span></span> <span data-ttu-id="33bbe-155">O hash de arquivo inserido neste campo deve ser obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou o [**método FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="33bbe-155">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="33bbe-156">Não use outros métodos.</span><span class="sxs-lookup"><span data-stu-id="33bbe-156">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="33bbe-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span><span class="sxs-lookup"><span data-stu-id="33bbe-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span></span>
</dt> <dd>

<span data-ttu-id="33bbe-158">Quarto 32 bits de hash.</span><span class="sxs-lookup"><span data-stu-id="33bbe-158">Fourth 32 bits of hash.</span></span> <span data-ttu-id="33bbe-159">O hash de arquivo inserido neste campo deve ser obtido chamando [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou o [**método FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="33bbe-159">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="33bbe-160">Não use outros métodos.</span><span class="sxs-lookup"><span data-stu-id="33bbe-160">Do not use other methods.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="33bbe-161">Validação</span><span class="sxs-lookup"><span data-stu-id="33bbe-161">Validation</span></span>

<dl>

[<span data-ttu-id="33bbe-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="33bbe-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="33bbe-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="33bbe-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="33bbe-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="33bbe-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="33bbe-165">ICE60</span><span class="sxs-lookup"><span data-stu-id="33bbe-165">ICE60</span></span>](ice60.md)  
[<span data-ttu-id="33bbe-166">ICE66</span><span class="sxs-lookup"><span data-stu-id="33bbe-166">ICE66</span></span>](ice66.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="33bbe-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33bbe-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33bbe-168">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="33bbe-168">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[<span data-ttu-id="33bbe-169">Controle de versão de arquivo padrão</span><span class="sxs-lookup"><span data-stu-id="33bbe-169">Default File Versioning</span></span>](default-file-versioning.md)
</dt> </dl>

 

 



