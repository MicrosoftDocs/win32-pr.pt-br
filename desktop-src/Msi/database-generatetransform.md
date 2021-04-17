---
description: O método GenerateTransform do objeto Database cria uma transformação que, quando aplicada ao banco de dados de objeto, resulta no banco de dados de referência. A transformação é armazenada no objeto de armazenamento.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Método Database. GenerateTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747773"
---
# <a name="databasegeneratetransform-method"></a><span data-ttu-id="0bd5a-104">Método Database. GenerateTransform</span><span class="sxs-lookup"><span data-stu-id="0bd5a-104">Database.GenerateTransform method</span></span>

<span data-ttu-id="0bd5a-105">O método **GenerateTransform** do objeto [**Database**](database-object.md) cria uma [*transformação*](t-gly.md) que, quando aplicada ao banco de dados de objeto, resulta no banco de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-105">The **GenerateTransform** method of the [**Database**](database-object.md) object creates a [*transform*](t-gly.md) that, when applied to the object database, results in the reference database.</span></span> <span data-ttu-id="0bd5a-106">A transformação é armazenada no objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-106">The transform is stored in the storage object.</span></span>

<span data-ttu-id="0bd5a-107">Se a transformação for ser aplicada durante uma instalação, você deverá usar o método [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) para popular o fluxo de informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-107">If the transform is to be applied during an installation you must use the [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) method to populate the summary information stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd5a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bd5a-108">Syntax</span></span>


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a><span data-ttu-id="0bd5a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bd5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bd5a-110">*reference*</span><span class="sxs-lookup"><span data-stu-id="0bd5a-110">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd5a-111">Banco de dados necessário que não inclui as alterações.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-111">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="0bd5a-112">*storage*</span><span class="sxs-lookup"><span data-stu-id="0bd5a-112">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd5a-113">O nome do arquivo de transformação gerado.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-113">The name of the generated transform file.</span></span> <span data-ttu-id="0bd5a-114">Isso é opcional.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-114">This is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bd5a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bd5a-115">Return value</span></span>

<span data-ttu-id="0bd5a-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd5a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bd5a-117">Remarks</span></span>

<span data-ttu-id="0bd5a-118">Uma transformação pode adicionar colunas de chave não primárias ao final de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-118">A transform can add non-primary key columns to the end of a table.</span></span> <span data-ttu-id="0bd5a-119">Não é possível criar uma transformação que adiciona colunas de chave primária a uma tabela.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-119">A transform cannot be created that adds primary key columns to a table.</span></span> <span data-ttu-id="0bd5a-120">Não é possível criar uma transformação que altere a ordem, os nomes ou as definições de colunas.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-120">A transform cannot be created that changes the order, names, or definitions of columns.</span></span>

<span data-ttu-id="0bd5a-121">Esse método retorna um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-121">This method returns a Boolean value.</span></span> <span data-ttu-id="0bd5a-122">Retornará TRUE se uma transformação for gerada.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-122">It returns TRUE if a transform is generated.</span></span> <span data-ttu-id="0bd5a-123">Retornará FALSE se uma transformação não for gerada porque não há diferenças entre os dois bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-123">It returns FALSE if a transform is not generated because there are no differences between the two databases.</span></span> <span data-ttu-id="0bd5a-124">Se o método falhar, ele gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-124">If the method fails, it generates an error.</span></span>

<span data-ttu-id="0bd5a-125">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="0bd5a-125">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd5a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bd5a-126">Requirements</span></span>



| <span data-ttu-id="0bd5a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bd5a-127">Requirement</span></span> | <span data-ttu-id="0bd5a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="0bd5a-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd5a-129">Versão</span><span class="sxs-lookup"><span data-stu-id="0bd5a-129">Version</span></span><br/> | <span data-ttu-id="0bd5a-130">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0bd5a-131">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0bd5a-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0bd5a-132">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0bd5a-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0bd5a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0bd5a-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="0bd5a-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bd5a-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0bd5a-135">IID</span><span class="sxs-lookup"><span data-stu-id="0bd5a-135">IID</span></span><br/>     | <span data-ttu-id="0bd5a-136">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0bd5a-136">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0bd5a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bd5a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd5a-138">**Backup de banco de dados**</span><span class="sxs-lookup"><span data-stu-id="0bd5a-138">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="0bd5a-139">Transformações de banco de dados</span><span class="sxs-lookup"><span data-stu-id="0bd5a-139">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




