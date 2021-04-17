---
description: O método Execute do objeto View usa o token de ponto de interrogação para representar parâmetros em uma instrução SQL. Para obter mais informações, consulte sintaxe SQL. Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exemétodo graciosos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748752"
---
# <a name="viewexecute-method"></a><span data-ttu-id="e1e8f-105">View.Exemétodo graciosos</span><span class="sxs-lookup"><span data-stu-id="e1e8f-105">View.Execute method</span></span>

<span data-ttu-id="e1e8f-106">O método **Execute** do objeto [**View**](view-object.md) usa o token de ponto de interrogação para representar parâmetros em uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="e1e8f-106">The **Execute** method of the [**View**](view-object.md) object uses the question mark token to represent parameters in an SQL statement.</span></span> <span data-ttu-id="e1e8f-107">Para obter mais informações, consulte [sintaxe SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e1e8f-107">For more information, see [SQL Syntax](sql-syntax.md).</span></span> <span data-ttu-id="e1e8f-108">Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1e8f-108">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e8f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1e8f-109">Syntax</span></span>


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="e1e8f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1e8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1e8f-111">*gravável*</span><span class="sxs-lookup"><span data-stu-id="e1e8f-111">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="e1e8f-112">Objetos de [**registro**](record-object.md) opcionais que contêm os valores que substituem os tokens de parâmetro (?) na consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="e1e8f-112">Optional [**Record**](record-object.md) objects that contains the values that replace the parameter tokens (?) in the SQL query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1e8f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1e8f-113">Return value</span></span>

<span data-ttu-id="e1e8f-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e1e8f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1e8f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1e8f-115">Remarks</span></span>

<span data-ttu-id="e1e8f-116">Esse método deve ser chamado antes de qualquer chamada para o método [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="e1e8f-116">This method must be called before any calls to the [**Fetch**](view-fetch.md) method.</span></span>

<span data-ttu-id="e1e8f-117">Se a consulta SQL especificar valores com marcadores de parâmetro (?), um registro deve ser fornecido contendo todos os valores de substituição, que devem estar na mesma ordem e no mesmo tipo de dados que os marcadores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1e8f-117">If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values, which must be in the same order and of the same data type as the parameter markers.</span></span> <span data-ttu-id="e1e8f-118">Quando esse método é usado com consultas INSERT e UPDATE, os tokens de ponto de interrogação devem preceder todos os valores não parametrizados.</span><span class="sxs-lookup"><span data-stu-id="e1e8f-118">When this method is used with INSERT and UPDATE queries, the question mark tokens must precede all the non-parameterized values.</span></span>

<span data-ttu-id="e1e8f-119">Por exemplo, essas consultas são válidas:</span><span class="sxs-lookup"><span data-stu-id="e1e8f-119">For example, these queries are valid:</span></span>

<span data-ttu-id="e1e8f-120">ATUALIZAR {Table-List} conjunto {Column} =?</span><span class="sxs-lookup"><span data-stu-id="e1e8f-120">UPDATE {table-list} SET {column}= ?</span></span> <span data-ttu-id="e1e8f-121">, {coluna} = {constante}</span><span class="sxs-lookup"><span data-stu-id="e1e8f-121">, {column}= {constant}</span></span>

<span data-ttu-id="e1e8f-122">INSERT em {Table} ({Column-List}) valores (?, {Constant-List})</span><span class="sxs-lookup"><span data-stu-id="e1e8f-122">INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})</span></span>

<span data-ttu-id="e1e8f-123">No entanto, essas consultas são inválidas:</span><span class="sxs-lookup"><span data-stu-id="e1e8f-123">However these queries are invalid:</span></span>

<span data-ttu-id="e1e8f-124">ATUALIZAR {Table-List} conjunto {Column} = {constante}, {Column} =?</span><span class="sxs-lookup"><span data-stu-id="e1e8f-124">UPDATE {table-list} SET {column}= {constant}, {column}=?</span></span>

<span data-ttu-id="e1e8f-125">INSERIR em valores de {Table} ({Column-List}) ({lista de constantes},?</span><span class="sxs-lookup"><span data-stu-id="e1e8f-125">INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ?</span></span> <span data-ttu-id="e1e8f-126">)</span><span class="sxs-lookup"><span data-stu-id="e1e8f-126">)</span></span>

<span data-ttu-id="e1e8f-127">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="e1e8f-127">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1e8f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1e8f-128">Requirements</span></span>



| <span data-ttu-id="e1e8f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1e8f-129">Requirement</span></span> | <span data-ttu-id="e1e8f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e1e8f-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e8f-131">Versão</span><span class="sxs-lookup"><span data-stu-id="e1e8f-131">Version</span></span><br/> | <span data-ttu-id="e1e8f-132">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1e8f-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e1e8f-133">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1e8f-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e1e8f-134">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1e8f-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e1e8f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e1e8f-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1e8f-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1e8f-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e1e8f-137">IID</span><span class="sxs-lookup"><span data-stu-id="e1e8f-137">IID</span></span><br/>     | <span data-ttu-id="e1e8f-138">IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e1e8f-138">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




