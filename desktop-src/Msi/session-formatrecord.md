---
description: O método FormatRecord do objeto Session retorna uma cadeia de caracteres formatada de um modelo e dados de registro.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Método Session. FormatRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775701"
---
# <a name="sessionformatrecord-method"></a><span data-ttu-id="15a39-103">Método Session. FormatRecord</span><span class="sxs-lookup"><span data-stu-id="15a39-103">Session.FormatRecord method</span></span>

<span data-ttu-id="15a39-104">O método **FormatRecord** do objeto [**Session**](session-object.md) retorna uma cadeia de caracteres formatada de um modelo e dados de registro.</span><span class="sxs-lookup"><span data-stu-id="15a39-104">The **FormatRecord** method of the [**Session**](session-object.md) object returns a formatted string from a template and record data.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a39-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15a39-105">Syntax</span></span>


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="15a39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15a39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a39-107">*gravável*</span><span class="sxs-lookup"><span data-stu-id="15a39-107">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="15a39-108">Objeto de **registro** necessário contendo um modelo e dados a serem formatados.</span><span class="sxs-lookup"><span data-stu-id="15a39-108">Required **Record** object containing a template and data to be formatted.</span></span> <span data-ttu-id="15a39-109">A cadeia de caracteres do modelo deve ser definida no campo 0 seguido por quaisquer parâmetros de dados referenciados.</span><span class="sxs-lookup"><span data-stu-id="15a39-109">The template string must be set in field 0 followed by any referenced data parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a39-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15a39-110">Return value</span></span>

<span data-ttu-id="15a39-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="15a39-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a39-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="15a39-112">Remarks</span></span>

<span data-ttu-id="15a39-113">O método **FormatRecord** usa o seguinte processo de formato.</span><span class="sxs-lookup"><span data-stu-id="15a39-113">The **FormatRecord** method uses the following format process.</span></span>

<span data-ttu-id="15a39-114">Os parâmetros a serem [formatados](formatted.md) são colocados entre colchetes \[ .. \] .</span><span class="sxs-lookup"><span data-stu-id="15a39-114">Parameters to be [formatted](formatted.md) are enclosed in square brackets \[..\].</span></span> <span data-ttu-id="15a39-115">Os colchetes podem ser iterados porque as substituições são resolvidas de dentro para fora.</span><span class="sxs-lookup"><span data-stu-id="15a39-115">The square brackets can be iterated because the substitutions are resolved from inside out.</span></span>

<span data-ttu-id="15a39-116">Se uma parte da cadeia de caracteres estiver entre chaves {} e não contiver colchetes, a parte permanecerá inalterada, incluindo as chaves.</span><span class="sxs-lookup"><span data-stu-id="15a39-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, the part is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="15a39-117">Se uma parte da cadeia de caracteres estiver entre chaves e contiver um ou mais nomes de propriedade, e se todas as propriedades forem encontradas, o texto (com as substituições resolvidas) será exibido sem as chaves.</span><span class="sxs-lookup"><span data-stu-id="15a39-117">If a part of the string is enclosed in curly braces and contains one or more property names, and if all the properties are found, the text (with the resolved substitutions) is displayed without the curly braces.</span></span> <span data-ttu-id="15a39-118">Se qualquer uma das propriedades não for encontrada, todo o texto entre chaves e as chaves serão removidos.</span><span class="sxs-lookup"><span data-stu-id="15a39-118">If any of the properties are not found, all the text in the curly braces and the braces themselves are removed.</span></span>

<span data-ttu-id="15a39-119">**Para formatar Cadeias de caracteres usando o método FormatRecord**</span><span class="sxs-lookup"><span data-stu-id="15a39-119">**To format strings using the FormatRecord method**</span></span>

1.  <span data-ttu-id="15a39-120">Os parâmetros numéricos são substituídos substituindo o marcador pelo valor do campo de registro correspondente, com valores ausentes ou nulos que não produzem nenhum texto.</span><span class="sxs-lookup"><span data-stu-id="15a39-120">The numeric parameters are substituted by replacing the marker with the value of the corresponding record field, with missing or Null values producing no text.</span></span>
2.  <span data-ttu-id="15a39-121">A cadeia de caracteres que resulta é processada substituindo os parâmetros que não são de registro pelos valores correspondentes, conforme observado nas descrições a seguir.</span><span class="sxs-lookup"><span data-stu-id="15a39-121">The string that results is processed by replacing the non-record parameters with the corresponding values, as noted in the following descriptions.</span></span>
    -   <span data-ttu-id="15a39-122">Se uma subcadeia de caracteres do formato " \[ PropertyName \] " for encontrada, ela será substituída pelo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="15a39-122">If a substring of the form "\[propertyname\]" is encountered, it is replaced by the value of the property.</span></span>
    -   <span data-ttu-id="15a39-123">Se uma subcadeia de caracteres do formulário " \[ % environmentvariable \] " for encontrada, o valor da variável de ambiente será substituído.</span><span class="sxs-lookup"><span data-stu-id="15a39-123">If a substring of the form "\[%environmentvariable\]" is found, the value of the environment variable is substituted.</span></span>
    -   <span data-ttu-id="15a39-124">Se uma subcadeia de caracteres do formulário \[ \# *FileKey* \] for encontrada, ela será substituída pelo caminho completo do arquivo, com o valor *FileKey* usado como uma chave na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="15a39-124">If a substring of the form \[\#*filekey*\] is found, it is replaced by the full path of the file, with the value *filekey* used as a key into the [File table](file-table.md).</span></span> <span data-ttu-id="15a39-125">O valor de \[ \# *FileKey* \] permanece em branco e não é substituído por um caminho até que o instalador execute a ação [CostInitialize](costinitialize-action.md), a ação de [filecusto](filecost-action.md)e a ação [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="15a39-125">The value of \[\#*filekey*\] remains blank and is not replaced by a path until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="15a39-126">O valor de \[ \# *FileKey* \] depende do estado da instalação do componente ao qual o arquivo pertence.</span><span class="sxs-lookup"><span data-stu-id="15a39-126">The value of \[\#*filekey*\] depends upon the installation state of the component to which the file belongs.</span></span> <span data-ttu-id="15a39-127">Se o componente estiver sendo executado da origem, o valor será o caminho para o local de origem do arquivo.</span><span class="sxs-lookup"><span data-stu-id="15a39-127">If the component is being run from source, the value is the path to the source location of the file.</span></span> <span data-ttu-id="15a39-128">Se o componente estiver sendo executado localmente, o valor será o caminho para o local de destino do arquivo após a instalação.</span><span class="sxs-lookup"><span data-stu-id="15a39-128">If the component is being run locally, the value is the path to the target location of the file after installation.</span></span> <span data-ttu-id="15a39-129">Se o componente estiver ausente, o caminho ficará em branco.</span><span class="sxs-lookup"><span data-stu-id="15a39-129">If the component is absent, the path is blank.</span></span> <span data-ttu-id="15a39-130">Para obter mais informações sobre como verificar o estado de instalação dos componentes, consulte [verificando a instalação de recursos, componentes e arquivos](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="15a39-130">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="15a39-131">Se uma subcadeia de caracteres do formulário \[ *$componentkey* \] for encontrada, ela será substituída pelo diretório de instalação do componente, com o valor *componentkey* usado como uma chave na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="15a39-131">If a substring of the form \[*$componentkey*\] is found, it is replaced by the install directory of the component, with the value *componentkey* used as a key into the [Component table](component-table.md).</span></span> <span data-ttu-id="15a39-132">O valor de \[ $ *componentkey* \] permanece em branco e não é substituído por um diretório até que o instalador execute a ação [CostInitialize](costinitialize-action.md), a ação de [filecusto](filecost-action.md)e a ação [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="15a39-132">The value of \[$*componentkey*\] remains blank and is not replaced by a directory until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="15a39-133">O valor de \[ $ *componentkey* \] depende do estado de instalação do componente.</span><span class="sxs-lookup"><span data-stu-id="15a39-133">The value of \[$*componentkey*\] depends upon the installation state of the component.</span></span> <span data-ttu-id="15a39-134">Se o componente estiver sendo executado da origem, o valor será o diretório de origem do arquivo.</span><span class="sxs-lookup"><span data-stu-id="15a39-134">If the component is being run from source, the value is the source directory of the file.</span></span> <span data-ttu-id="15a39-135">Se o componente estiver sendo executado localmente, o valor será o diretório de destino após a instalação.</span><span class="sxs-lookup"><span data-stu-id="15a39-135">If the component is being run locally, the value is the target directory after installation.</span></span> <span data-ttu-id="15a39-136">Se o componente estiver ausente, o valor será deixado em branco.</span><span class="sxs-lookup"><span data-stu-id="15a39-136">If the component is absent, the value is left blank.</span></span> <span data-ttu-id="15a39-137">Para obter mais informações sobre como verificar o estado de instalação dos componentes, consulte [verificando a instalação de recursos, componentes e arquivos](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="15a39-137">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="15a39-138">Se uma subcadeia de caracteres no formato " \[ \\ c \] " for encontrada, ela será substituída pelo caractere sem nenhum processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="15a39-138">If a substring of the form "\[\\c\]" is found, it is replaced by the character without any further processing.</span></span> <span data-ttu-id="15a39-139">Somente o primeiro caractere após a barra invertida é mantido; Tudo o mais é removido.</span><span class="sxs-lookup"><span data-stu-id="15a39-139">Only the first character after the backslash is kept; everything else is removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a39-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15a39-140">Requirements</span></span>



| <span data-ttu-id="15a39-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="15a39-141">Requirement</span></span> | <span data-ttu-id="15a39-142">Valor</span><span class="sxs-lookup"><span data-stu-id="15a39-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a39-143">Versão</span><span class="sxs-lookup"><span data-stu-id="15a39-143">Version</span></span><br/> | <span data-ttu-id="15a39-144">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="15a39-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="15a39-145">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15a39-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="15a39-146">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="15a39-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="15a39-147">DLL</span><span class="sxs-lookup"><span data-stu-id="15a39-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="15a39-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15a39-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="15a39-149">IID</span><span class="sxs-lookup"><span data-stu-id="15a39-149">IID</span></span><br/>     | <span data-ttu-id="15a39-150">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="15a39-150">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="15a39-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="15a39-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a39-152">Binário</span><span class="sxs-lookup"><span data-stu-id="15a39-152">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="15a39-153">Tipos de dados de coluna</span><span class="sxs-lookup"><span data-stu-id="15a39-153">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




