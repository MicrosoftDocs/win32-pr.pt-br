---
description: O método OpenView do objeto Database retorna um objeto View que representa a consulta especificada por uma cadeia de caracteres SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Método Database. OpenView (Certview. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752857"
---
# <a name="databaseopenview-method"></a><span data-ttu-id="aaad8-103">Método Database. OpenView</span><span class="sxs-lookup"><span data-stu-id="aaad8-103">Database.OpenView method</span></span>

<span data-ttu-id="aaad8-104">O método **OpenView** do objeto [**Database**](database-object.md) retorna um objeto [**View**](view-object.md) que representa a consulta especificada por uma cadeia de caracteres SQL.</span><span class="sxs-lookup"><span data-stu-id="aaad8-104">The **OpenView** method of the [**Database**](database-object.md) object returns a [**View**](view-object.md) object that represents the query specified by a SQL string.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaad8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aaad8-105">Syntax</span></span>


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a><span data-ttu-id="aaad8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaad8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaad8-107">*sql*</span><span class="sxs-lookup"><span data-stu-id="aaad8-107">*sql*</span></span> 
</dt> <dd>

<span data-ttu-id="aaad8-108">Cadeia de caracteres de consulta SQL necessária.</span><span class="sxs-lookup"><span data-stu-id="aaad8-108">Required SQL query string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaad8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aaad8-109">Return value</span></span>

<span data-ttu-id="aaad8-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="aaad8-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaad8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="aaad8-111">Remarks</span></span>

<span data-ttu-id="aaad8-112">Para obter informações sobre a sintaxe SQL implementada no instalador, consulte [sintaxe SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="aaad8-112">For information about SQL syntax implemented in the installer, see [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="aaad8-113">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="aaad8-113">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaad8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaad8-114">Requirements</span></span>



| <span data-ttu-id="aaad8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaad8-115">Requirement</span></span> | <span data-ttu-id="aaad8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="aaad8-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaad8-117">Versão</span><span class="sxs-lookup"><span data-stu-id="aaad8-117">Version</span></span><br/> | <span data-ttu-id="aaad8-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aaad8-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="aaad8-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aaad8-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="aaad8-120">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="aaad8-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="aaad8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aaad8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="aaad8-122"><dt>Certview. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaad8-122"><dt>Certview.h</dt></span></span> </dl>                                                                                                                                                                   |
| <span data-ttu-id="aaad8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="aaad8-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="aaad8-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaad8-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="aaad8-125">IID</span><span class="sxs-lookup"><span data-stu-id="aaad8-125">IID</span></span><br/>     | <span data-ttu-id="aaad8-126">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="aaad8-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="aaad8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="aaad8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaad8-128">**Backup de banco de dados**</span><span class="sxs-lookup"><span data-stu-id="aaad8-128">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="aaad8-129">Sintaxe SQL</span><span class="sxs-lookup"><span data-stu-id="aaad8-129">SQL Syntax</span></span>](sql-syntax.md)
</dt> </dl>

 

 




