---
description: O método de importação do objeto de banco de dados importa uma tabela de banco de dados de arquivos mortos de texto, descartando qualquer tabela existente.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Método Database. Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756733"
---
# <a name="databaseimport-method"></a><span data-ttu-id="83a37-103">Método Database. Import</span><span class="sxs-lookup"><span data-stu-id="83a37-103">Database.Import method</span></span>

<span data-ttu-id="83a37-104">O método de **importação** do objeto de [**banco de dados**](database-object.md) importa uma tabela de banco de dados de [arquivos mortos de texto](text-archive-files.md), descartando qualquer tabela existente.</span><span class="sxs-lookup"><span data-stu-id="83a37-104">The **Import** method of the [**Database**](database-object.md) object imports a database table from a [text archive files](text-archive-files.md), dropping any existing table.</span></span>

## <a name="syntax"></a><span data-ttu-id="83a37-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83a37-105">Syntax</span></span>


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="83a37-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83a37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83a37-107">*path*</span><span class="sxs-lookup"><span data-stu-id="83a37-107">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="83a37-108">Pasta necessária onde o arquivo de texto está presente.</span><span class="sxs-lookup"><span data-stu-id="83a37-108">Required folder where the text file is present.</span></span>

</dd> <dt>

<span data-ttu-id="83a37-109">*file*</span><span class="sxs-lookup"><span data-stu-id="83a37-109">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="83a37-110">Nome necessário do arquivo a ser importado.</span><span class="sxs-lookup"><span data-stu-id="83a37-110">Required name of the file to be imported.</span></span> <span data-ttu-id="83a37-111">Isso não inclui a pasta, pois ela deve ser definida no objeto Path.</span><span class="sxs-lookup"><span data-stu-id="83a37-111">This does not include the folder, as that must be set in the path object.</span></span> <span data-ttu-id="83a37-112">O nome da tabela é especificado dentro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="83a37-112">The table name is specified within the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83a37-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83a37-113">Return value</span></span>

<span data-ttu-id="83a37-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="83a37-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83a37-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="83a37-115">Remarks</span></span>

<span data-ttu-id="83a37-116">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="83a37-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="83a37-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83a37-117">Requirements</span></span>



| <span data-ttu-id="83a37-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83a37-118">Requirement</span></span> | <span data-ttu-id="83a37-119">Valor</span><span class="sxs-lookup"><span data-stu-id="83a37-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a37-120">Versão</span><span class="sxs-lookup"><span data-stu-id="83a37-120">Version</span></span><br/> | <span data-ttu-id="83a37-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="83a37-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="83a37-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="83a37-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="83a37-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="83a37-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="83a37-124">DLL</span><span class="sxs-lookup"><span data-stu-id="83a37-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="83a37-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83a37-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="83a37-126">IID</span><span class="sxs-lookup"><span data-stu-id="83a37-126">IID</span></span><br/>     | <span data-ttu-id="83a37-127">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="83a37-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="83a37-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="83a37-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a37-129">**Backup de banco de dados**</span><span class="sxs-lookup"><span data-stu-id="83a37-129">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="83a37-130">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="83a37-130">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




