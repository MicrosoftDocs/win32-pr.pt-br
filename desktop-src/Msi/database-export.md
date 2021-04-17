---
description: O método Export do objeto Database copia a estrutura e os dados de uma tabela especificada para um arquivo morto de texto.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Método Database. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748780"
---
# <a name="databaseexport-method"></a><span data-ttu-id="6812a-103">Método Database. Export</span><span class="sxs-lookup"><span data-stu-id="6812a-103">Database.Export method</span></span>

<span data-ttu-id="6812a-104">O método **Export** do objeto [**Database**](database-object.md) copia a estrutura e os dados de uma tabela especificada para um [arquivo morto de texto](text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="6812a-104">The **Export** method of the [**Database**](database-object.md) object copies the structure and data from a specified table to a [text archive file](text-archive-files.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6812a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6812a-105">Syntax</span></span>


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="6812a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6812a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6812a-107">*table*</span><span class="sxs-lookup"><span data-stu-id="6812a-107">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="6812a-108">Nome necessário da tabela de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6812a-108">Required name of the database table.</span></span> <span data-ttu-id="6812a-109">Diferenciar maiúsculas de minúsculas se usar o banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="6812a-109">Case-sensitive if using the installer database.</span></span>

</dd> <dt>

<span data-ttu-id="6812a-110">*path*</span><span class="sxs-lookup"><span data-stu-id="6812a-110">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="6812a-111">Cadeia de caracteres necessária que é o caminho para a pasta onde o arquivo de texto é colocado.</span><span class="sxs-lookup"><span data-stu-id="6812a-111">Required string that is the path to the folder where the text file is placed.</span></span>

</dd> <dt>

<span data-ttu-id="6812a-112">*file*</span><span class="sxs-lookup"><span data-stu-id="6812a-112">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="6812a-113">Nome necessário do arquivo a ser criado.</span><span class="sxs-lookup"><span data-stu-id="6812a-113">Required name of the file to be created.</span></span> <span data-ttu-id="6812a-114">Isso não inclui a pasta, pois ela deve ser definida no objeto Path.</span><span class="sxs-lookup"><span data-stu-id="6812a-114">This does not include the folder, as that must be set in the path object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6812a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6812a-115">Return value</span></span>

<span data-ttu-id="6812a-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6812a-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6812a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6812a-117">Remarks</span></span>

<span data-ttu-id="6812a-118">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="6812a-118">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6812a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6812a-119">Requirements</span></span>



| <span data-ttu-id="6812a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6812a-120">Requirement</span></span> | <span data-ttu-id="6812a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6812a-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6812a-122">Versão</span><span class="sxs-lookup"><span data-stu-id="6812a-122">Version</span></span><br/> | <span data-ttu-id="6812a-123">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6812a-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6812a-124">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6812a-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6812a-125">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6812a-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6812a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6812a-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="6812a-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6812a-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6812a-128">IID</span><span class="sxs-lookup"><span data-stu-id="6812a-128">IID</span></span><br/>     | <span data-ttu-id="6812a-129">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6812a-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




