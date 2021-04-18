---
description: O método CreateTransformSummaryInfo do objeto Database cria e popula o fluxo de informações resumidas de um arquivo de transformação existente. Esse método preenche as propriedades com o ProductCode base e de referência e ProductVersion.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Método Database. CreateTransformSummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780960"
---
# <a name="databasecreatetransformsummaryinfo-method"></a><span data-ttu-id="fa89e-104">Método Database. CreateTransformSummaryInfo</span><span class="sxs-lookup"><span data-stu-id="fa89e-104">Database.CreateTransformSummaryInfo method</span></span>

<span data-ttu-id="fa89e-105">O método **CreateTransformSummaryInfo** do objeto [**Database**](database-object.md) cria e popula o fluxo de informações resumidas de um arquivo de transformação existente.</span><span class="sxs-lookup"><span data-stu-id="fa89e-105">The **CreateTransformSummaryInfo** method of the [**Database**](database-object.md) object creates and populates the summary information stream of an existing transform file.</span></span> <span data-ttu-id="fa89e-106">Esse método preenche as propriedades com o [**ProductCode**](productcode.md) base e de referência e [**ProductVersion**](productversion.md).</span><span class="sxs-lookup"><span data-stu-id="fa89e-106">This method fills in the properties with the base and reference [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa89e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa89e-107">Syntax</span></span>


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a><span data-ttu-id="fa89e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa89e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa89e-109">*reference*</span><span class="sxs-lookup"><span data-stu-id="fa89e-109">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="fa89e-110">Banco de dados necessário que não inclui as alterações.</span><span class="sxs-lookup"><span data-stu-id="fa89e-110">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="fa89e-111">*storage*</span><span class="sxs-lookup"><span data-stu-id="fa89e-111">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="fa89e-112">O nome do arquivo de transformação gerado.</span><span class="sxs-lookup"><span data-stu-id="fa89e-112">The name of the generated transform file.</span></span> <span data-ttu-id="fa89e-113">Isso é opcional.</span><span class="sxs-lookup"><span data-stu-id="fa89e-113">This is optional.</span></span>

</dd> <dt>

<span data-ttu-id="fa89e-114">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="fa89e-114">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="fa89e-115">Condições de erro necessárias que devem ser suprimidas quando a transformação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="fa89e-115">Required error conditions that should be suppressed when the transform is applied.</span></span> <span data-ttu-id="fa89e-116">Combine um ou mais dos seguintes valores de condição de erro.</span><span class="sxs-lookup"><span data-stu-id="fa89e-116">Combine one or more of the following error condition values.</span></span>



| <span data-ttu-id="fa89e-117">Nome da condição de erro</span><span class="sxs-lookup"><span data-stu-id="fa89e-117">Error condition name</span></span>                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="fa89e-118">Significado</span><span class="sxs-lookup"><span data-stu-id="fa89e-118">Meaning</span></span>                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <span data-ttu-id="fa89e-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span></span> </dl>                                                                         | <span data-ttu-id="fa89e-120">Nenhuma das condições a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa89e-120">None of the following conditions.</span></span><br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="fa89e-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span></span> </dl>                                 | <span data-ttu-id="fa89e-122">Adiciona uma linha que já existe.</span><span class="sxs-lookup"><span data-stu-id="fa89e-122">Adds a row that already exists.</span></span><br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="fa89e-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="fa89e-124">Exclui uma linha que não existe.</span><span class="sxs-lookup"><span data-stu-id="fa89e-124">Deletes a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="fa89e-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="fa89e-126">Adiciona uma tabela que já existe.</span><span class="sxs-lookup"><span data-stu-id="fa89e-126">Adds a table that already exists.</span></span><br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="fa89e-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="fa89e-128">Exclui uma tabela que não existe.</span><span class="sxs-lookup"><span data-stu-id="fa89e-128">Deletes a table that does not exist.</span></span><br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="fa89e-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span></span> </dl>        | <span data-ttu-id="fa89e-130">Atualiza uma linha que não existe.</span><span class="sxs-lookup"><span data-stu-id="fa89e-130">Updates a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="fa89e-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span></span> </dl>                                | <span data-ttu-id="fa89e-132">As páginas de código de transformação e de banco de dados não coincidem e nenhuma página de código é neutra.</span><span class="sxs-lookup"><span data-stu-id="fa89e-132">Transform and database code pages do not match and neither code page is neutral.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fa89e-133">*validation*</span><span class="sxs-lookup"><span data-stu-id="fa89e-133">*validation*</span></span> 
</dt> <dd>

<span data-ttu-id="fa89e-134">Necessário quando a transformação é aplicada a um banco de dados; mostra quais propriedades devem ser validadas para verificar se essa transformação pode ser aplicada ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa89e-134">Required when the transform is applied to a database; shows which properties should be validated to verify that this transform can be applied to the database.</span></span> <span data-ttu-id="fa89e-135">As propriedades estão todas contidas no [conjunto de propriedades fluxo de informações de resumo](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="fa89e-135">The properties are all contained in the [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="fa89e-136">Combine um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa89e-136">Combine one or more of the following values.</span></span>



| <span data-ttu-id="fa89e-137">Sinalizador de validação</span><span class="sxs-lookup"><span data-stu-id="fa89e-137">Validation flag</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="fa89e-138">Significado</span><span class="sxs-lookup"><span data-stu-id="fa89e-138">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <span data-ttu-id="fa89e-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="fa89e-140">Nenhuma validação feita.</span><span class="sxs-lookup"><span data-stu-id="fa89e-140">No validation done.</span></span><br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <span data-ttu-id="fa89e-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="fa89e-142">O idioma padrão deve corresponder ao banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="fa89e-142">Default language must match base database.</span></span><br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <span data-ttu-id="fa89e-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="fa89e-144">O produto deve corresponder ao banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="fa89e-144">Product must match base database.</span></span><br/>          |



 

<span data-ttu-id="fa89e-145">Para validar a versão do produto, primeiro escolha um ou mais desses três sinalizadores para indicar a quantidade de verificação da versão.</span><span class="sxs-lookup"><span data-stu-id="fa89e-145">To validate product version, first choose one or more of these three flags to indicate how much of the version is to be verified.</span></span>



| <span data-ttu-id="fa89e-146">Sinalizador de validação</span><span class="sxs-lookup"><span data-stu-id="fa89e-146">Validation flag</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="fa89e-147">Significado</span><span class="sxs-lookup"><span data-stu-id="fa89e-147">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <span data-ttu-id="fa89e-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span></span> </dl>      | <span data-ttu-id="fa89e-149">Verifica somente a versão principal.</span><span class="sxs-lookup"><span data-stu-id="fa89e-149">Checks major version only.</span></span><br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <span data-ttu-id="fa89e-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span></span> </dl>     | <span data-ttu-id="fa89e-151">Verifica apenas a versão principal e secundária.</span><span class="sxs-lookup"><span data-stu-id="fa89e-151">Checks major and minor version only.</span></span><br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <span data-ttu-id="fa89e-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span></span> </dl> | <span data-ttu-id="fa89e-153">Verifica as versões principal, secundária e de atualização.</span><span class="sxs-lookup"><span data-stu-id="fa89e-153">Checks major, minor, and update versions.</span></span><br/> |



 

<span data-ttu-id="fa89e-154">Em seguida, escolha uma das opções a seguir para indicar a relação necessária entre a versão do produto do banco de dados à qual a transformação está sendo aplicada e a do banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="fa89e-154">Then choose one of the following to indicate the required relationship between the product version of the database the transform is being applied to and that of the base database.</span></span>



| <span data-ttu-id="fa89e-155">Sinalizador de validação</span><span class="sxs-lookup"><span data-stu-id="fa89e-155">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="fa89e-156">Significado</span><span class="sxs-lookup"><span data-stu-id="fa89e-156">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <span data-ttu-id="fa89e-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span></span> </dl>                                          | <span data-ttu-id="fa89e-158">Versão aplicada < versão base</span><span class="sxs-lookup"><span data-stu-id="fa89e-158">Applied version < base version</span></span><br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <span data-ttu-id="fa89e-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span></span> </dl>             | <span data-ttu-id="fa89e-160">Versão aplicada <= versão base</span><span class="sxs-lookup"><span data-stu-id="fa89e-160">Applied version <= base version</span></span><br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <span data-ttu-id="fa89e-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span></span> </dl>                                     | <span data-ttu-id="fa89e-162">Versão aplicada = versão base</span><span class="sxs-lookup"><span data-stu-id="fa89e-162">Applied version = base version</span></span><br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <span data-ttu-id="fa89e-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span></span> </dl> | <span data-ttu-id="fa89e-164">Versão aplicada >= versão base</span><span class="sxs-lookup"><span data-stu-id="fa89e-164">Applied version >= base version</span></span><br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <span data-ttu-id="fa89e-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span></span> </dl>                            | <span data-ttu-id="fa89e-166">Versão aplicada > versão base</span><span class="sxs-lookup"><span data-stu-id="fa89e-166">Applied version > base version</span></span><br/>  |



 

<span data-ttu-id="fa89e-167">Para validar que a transformação está sendo aplicada a um pacote com o [**UpgradeCode**](upgradecode.md)apropriado, defina o sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa89e-167">To validate that the transform is being applied to a package having the appropriate [**UpgradeCode**](upgradecode.md), set the following flag.</span></span>



| <span data-ttu-id="fa89e-168">Sinalizador de validação</span><span class="sxs-lookup"><span data-stu-id="fa89e-168">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="fa89e-169">Significado</span><span class="sxs-lookup"><span data-stu-id="fa89e-169">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <span data-ttu-id="fa89e-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span></span> </dl> | <span data-ttu-id="fa89e-171">Valida que a transformação é o [**UpgradeCode**](upgradecode.md)apropriado.</span><span class="sxs-lookup"><span data-stu-id="fa89e-171">Validates that the transform is the appropriate [**UpgradeCode**](upgradecode.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa89e-172">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa89e-172">Return value</span></span>

<span data-ttu-id="fa89e-173">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fa89e-173">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa89e-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa89e-174">Remarks</span></span>

<span data-ttu-id="fa89e-175">Para criar um fluxo de informações de resumo para uma transformação, as propriedades [**ProductCode**](productcode.md) e [**ProductVersion**](productversion.md) devem ser definidas nas tabelas de [Propriedades](property-table.md) dos bancos de dados base e de referência.</span><span class="sxs-lookup"><span data-stu-id="fa89e-175">To create a summary information stream for a transform, the [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md) properties must be defined in the [Property](property-table.md) tables of both the base and reference databases.</span></span> <span data-ttu-id="fa89e-176">Se msiTransformValidationUpgradeCode for usado, a propriedade [**UpgradeCode**](upgradecode.md) deverá ser definida em ambos os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="fa89e-176">If msiTransformValidationUpgradeCode is used, the [**UpgradeCode**](upgradecode.md) property must be defined in both databases.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa89e-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa89e-177">Requirements</span></span>



| <span data-ttu-id="fa89e-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa89e-178">Requirement</span></span> | <span data-ttu-id="fa89e-179">Valor</span><span class="sxs-lookup"><span data-stu-id="fa89e-179">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa89e-180">Versão</span><span class="sxs-lookup"><span data-stu-id="fa89e-180">Version</span></span><br/> | <span data-ttu-id="fa89e-181">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fa89e-181">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fa89e-182">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fa89e-182">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fa89e-183">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa89e-183">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fa89e-184">DLL</span><span class="sxs-lookup"><span data-stu-id="fa89e-184">DLL</span></span><br/>     | <dl> <span data-ttu-id="fa89e-185"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa89e-185"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fa89e-186">IID</span><span class="sxs-lookup"><span data-stu-id="fa89e-186">IID</span></span><br/>     | <span data-ttu-id="fa89e-187">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fa89e-187">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="fa89e-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa89e-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa89e-189">Transformações de banco de dados</span><span class="sxs-lookup"><span data-stu-id="fa89e-189">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




