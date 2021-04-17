---
description: O método ApplyTransform do objeto de banco de dados aplica a transformação a esse banco de dados.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Método Database. ApplyTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811850"
---
# <a name="databaseapplytransform-method"></a><span data-ttu-id="57ced-103">Método Database. ApplyTransform</span><span class="sxs-lookup"><span data-stu-id="57ced-103">Database.ApplyTransform method</span></span>

<span data-ttu-id="57ced-104">O método **ApplyTransform** do objeto de [**banco de dados**](database-object.md) aplica a transformação a esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="57ced-104">The **ApplyTransform** method of the [**Database**](database-object.md) object applies the transform to this database.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ced-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57ced-105">Syntax</span></span>


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a><span data-ttu-id="57ced-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57ced-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ced-107">*storage*</span><span class="sxs-lookup"><span data-stu-id="57ced-107">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="57ced-108">Caminho para o arquivo de transformação que está sendo aplicado.</span><span class="sxs-lookup"><span data-stu-id="57ced-108">Path to the transform file being applied.</span></span> <span data-ttu-id="57ced-109">Este parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="57ced-109">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="57ced-110">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="57ced-110">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="57ced-111">Especifica as condições de erro que devem ser suprimidas.</span><span class="sxs-lookup"><span data-stu-id="57ced-111">Specifies the error conditions that are to be suppressed.</span></span> <span data-ttu-id="57ced-112">Especifique como uma combinação dos valores inteiros a seguir.</span><span class="sxs-lookup"><span data-stu-id="57ced-112">Specify as a combination of the following integer values.</span></span>



| <span data-ttu-id="57ced-113">Condição de erro</span><span class="sxs-lookup"><span data-stu-id="57ced-113">Error condition</span></span>                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="57ced-114">Significado</span><span class="sxs-lookup"><span data-stu-id="57ced-114">Meaning</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="57ced-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="57ced-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span></span> </dl>                                 | <span data-ttu-id="57ced-116">Adiciona uma linha que já existe.</span><span class="sxs-lookup"><span data-stu-id="57ced-116">Adds a row that already exists.</span></span><br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="57ced-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="57ced-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="57ced-118">Exclui uma linha que não existe.</span><span class="sxs-lookup"><span data-stu-id="57ced-118">Deletes a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="57ced-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="57ced-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span></span> </dl>                         | <span data-ttu-id="57ced-120">Adiciona uma tabela que já existe.</span><span class="sxs-lookup"><span data-stu-id="57ced-120">Adds a table that already exists.</span></span><br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="57ced-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="57ced-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="57ced-122">Exclui uma tabela que não existe.</span><span class="sxs-lookup"><span data-stu-id="57ced-122">Deletes a table that does not exist.</span></span><br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="57ced-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="57ced-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span></span> </dl>         | <span data-ttu-id="57ced-124">Atualiza uma linha que não existe.</span><span class="sxs-lookup"><span data-stu-id="57ced-124">Updates a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="57ced-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="57ced-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span></span> </dl>                                 | <span data-ttu-id="57ced-126">As páginas de código de transformação e de banco de dados não coincidem e nenhuma página de código neutra.</span><span class="sxs-lookup"><span data-stu-id="57ced-126">Transform and database code pages do not match and neither has a neutral code page.</span></span><br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <span data-ttu-id="57ced-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="57ced-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span></span> </dl>                                     | <span data-ttu-id="57ced-128">Cria a tabela temporária de [ \_ transformview](-transformview-table.md).</span><span class="sxs-lookup"><span data-stu-id="57ced-128">Creates the temporary [\_TransformView table](-transformview-table.md).</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ced-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57ced-129">Return value</span></span>

<span data-ttu-id="57ced-130">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="57ced-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57ced-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="57ced-131">Remarks</span></span>

<span data-ttu-id="57ced-132">O método **ApplyTransform** atrasa a transformação de tabelas até o último momento possível.</span><span class="sxs-lookup"><span data-stu-id="57ced-132">The **ApplyTransform** method delays transforming tables until the last possible moment.</span></span> <span data-ttu-id="57ced-133">As etapas executadas no **ApplyTransform** são transformar imediatamente os catálogos de tabela e de coluna para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="57ced-133">The steps taken in **ApplyTransform** are to immediately transform the table and column catalogs for the database.</span></span> <span data-ttu-id="57ced-134">Os catálogos de tabela e de coluna são atualizados de acordo com qual tabela é adicionada ou excluída e qual coluna é adicionada (nenhuma exclusão de colunas é permitida).</span><span class="sxs-lookup"><span data-stu-id="57ced-134">The table and column catalogs are updated according to which table is added or deleted and which column is added (no deletion of columns is allowed).</span></span> <span data-ttu-id="57ced-135">Se uma tabela estiver atualmente carregada na memória e precisar ser transformada, ela será transformada.</span><span class="sxs-lookup"><span data-stu-id="57ced-135">If a table is currently loaded in memory and needs to be transformed, it is transformed.</span></span> <span data-ttu-id="57ced-136">Caso contrário, o estado da tabela será definido como que exige uma transformação para que, quando a tabela for carregada, ou quando o banco de dados for confirmado, a transformação seja aplicada.</span><span class="sxs-lookup"><span data-stu-id="57ced-136">Otherwise, the table state is set to that requiring a transform so that when the table is loaded, or when the database is committed, the transform is applied.</span></span> <span data-ttu-id="57ced-137">A transformação nessa instância significa que os dados reais (linha) da tabela são adicionados, excluídos ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="57ced-137">Transform in this instance means that the actual (row) data of the table is added, deleted, or updated.</span></span>

<span data-ttu-id="57ced-138">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="57ced-138">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ced-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57ced-139">Requirements</span></span>



| <span data-ttu-id="57ced-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="57ced-140">Requirement</span></span> | <span data-ttu-id="57ced-141">Valor</span><span class="sxs-lookup"><span data-stu-id="57ced-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ced-142">Versão</span><span class="sxs-lookup"><span data-stu-id="57ced-142">Version</span></span><br/> | <span data-ttu-id="57ced-143">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="57ced-143">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="57ced-144">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="57ced-144">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="57ced-145">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="57ced-145">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="57ced-146">DLL</span><span class="sxs-lookup"><span data-stu-id="57ced-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="57ced-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ced-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="57ced-148">IID</span><span class="sxs-lookup"><span data-stu-id="57ced-148">IID</span></span><br/>     | <span data-ttu-id="57ced-149">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="57ced-149">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="57ced-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="57ced-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ced-151">**Backup de banco de dados**</span><span class="sxs-lookup"><span data-stu-id="57ced-151">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="57ced-152">Transformações de banco de dados</span><span class="sxs-lookup"><span data-stu-id="57ced-152">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




