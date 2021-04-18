---
description: O método FileHash do objeto instalador usa o caminho para um arquivo e retorna um hash de 128 bits desse arquivo. As informações de hash do arquivo são retornadas como um objeto de registro. O hash do arquivo de 128 bits inteiro é retornado como campos de propriedade IntegerData de 4 32 bits.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Método Installer. FileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750612"
---
# <a name="installerfilehash-method"></a><span data-ttu-id="144e1-105">Método Installer. FileHash</span><span class="sxs-lookup"><span data-stu-id="144e1-105">Installer.FileHash method</span></span>

<span data-ttu-id="144e1-106">O método **FileHash** do [**objeto instalador**](installer-object.md) usa o caminho para um arquivo e retorna um hash de 128 bits desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="144e1-106">The **FileHash** method of the [**Installer Object**](installer-object.md) takes the path to a file and returns a 128-bit hash of that file.</span></span> <span data-ttu-id="144e1-107">As informações de hash do arquivo são retornadas como um [**objeto de registro**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="144e1-107">The file hash information is returned as a [**Record Object**](record-object.md).</span></span> <span data-ttu-id="144e1-108">O hash do arquivo de 128 bits inteiro é retornado como campos de propriedade [**IntegerData**](record-integerdata.md) de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="144e1-108">The entire 128-bit file hash is returned as four 32-bit [**IntegerData**](record-integerdata.md) property fields.</span></span>

<span data-ttu-id="144e1-109">Os valores retornados no [**objeto de registro**](record-object.md) correspondem aos quatro campos da estrutura [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) retornados por [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="144e1-109">The values returned in the [**Record Object**](record-object.md) correspond to the four fields of the [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) structure returned by [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="144e1-110">A numeração de quatro campos é baseada em 1 na [tabela MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="144e1-110">The numbering of four fields is 1-based in the [MsiFileHash Table](msifilehash-table.md).</span></span>

-   <span data-ttu-id="144e1-111">O campo 1 corresponde à coluna HashPart1.</span><span class="sxs-lookup"><span data-stu-id="144e1-111">Field 1 corresponds to the HashPart1 column.</span></span>
-   <span data-ttu-id="144e1-112">O campo 2 corresponde à coluna HashPart2.</span><span class="sxs-lookup"><span data-stu-id="144e1-112">Field 2 corresponds to the HashPart2 column.</span></span>
-   <span data-ttu-id="144e1-113">O campo 3 corresponde à coluna HashPart3.</span><span class="sxs-lookup"><span data-stu-id="144e1-113">Field 3 corresponds to the HashPart3 column.</span></span>
-   <span data-ttu-id="144e1-114">O campo 4 corresponde à coluna HashPart4.</span><span class="sxs-lookup"><span data-stu-id="144e1-114">Field 4 corresponds to the HashPart4 column.</span></span>

## <a name="syntax"></a><span data-ttu-id="144e1-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="144e1-115">Syntax</span></span>


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a><span data-ttu-id="144e1-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="144e1-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="144e1-117">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="144e1-117">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="144e1-118">Caminho para o arquivo cujo hash deve ser feito.</span><span class="sxs-lookup"><span data-stu-id="144e1-118">Path to the file that is to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="144e1-119">*Opções*</span><span class="sxs-lookup"><span data-stu-id="144e1-119">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="144e1-120">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="144e1-120">Reserved for future use.</span></span>

<span data-ttu-id="144e1-121">O valor desse parâmetro deve ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="144e1-121">The value of this parameter must be 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="144e1-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="144e1-122">Return value</span></span>

<span data-ttu-id="144e1-123">Se for bem-sucedido, esse método retornará um [**objeto de registro**](record-object.md) que contém o hash do arquivo.</span><span class="sxs-lookup"><span data-stu-id="144e1-123">If successful, this method returns a [**Record Object**](record-object.md) that contains the hash of the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="144e1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="144e1-124">Requirements</span></span>



| <span data-ttu-id="144e1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="144e1-125">Requirement</span></span> | <span data-ttu-id="144e1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="144e1-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="144e1-127">Versão</span><span class="sxs-lookup"><span data-stu-id="144e1-127">Version</span></span><br/> | <span data-ttu-id="144e1-128">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="144e1-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="144e1-129">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="144e1-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="144e1-130">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="144e1-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="144e1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="144e1-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="144e1-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="144e1-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="144e1-133">IID</span><span class="sxs-lookup"><span data-stu-id="144e1-133">IID</span></span><br/>     | <span data-ttu-id="144e1-134">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="144e1-134">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="144e1-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="144e1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144e1-136">Controle de versão de arquivo padrão</span><span class="sxs-lookup"><span data-stu-id="144e1-136">Default File Versioning</span></span>](default-file-versioning.md)
</dt> <dt>

[<span data-ttu-id="144e1-137">Gerenciar tamanhos e versões de arquivo</span><span class="sxs-lookup"><span data-stu-id="144e1-137">Manage File Sizes and Versions</span></span>](manage-file-sizes-and-versions.md)
</dt> <dt>

[<span data-ttu-id="144e1-138">Tabela MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="144e1-138">MsiFileHash Table</span></span>](msifilehash-table.md)
</dt> <dt>

[<span data-ttu-id="144e1-139">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="144e1-139">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




