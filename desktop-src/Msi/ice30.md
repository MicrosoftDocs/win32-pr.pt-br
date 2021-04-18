---
description: ICE30 valida que a instalação de componentes que contém o mesmo arquivo nunca instala o arquivo mais de uma vez no mesmo diretório.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769317"
---
# <a name="ice30"></a><span data-ttu-id="193e2-103">ICE30</span><span class="sxs-lookup"><span data-stu-id="193e2-103">ICE30</span></span>

<span data-ttu-id="193e2-104">ICE30 valida que a instalação de componentes que contém o mesmo arquivo nunca instala o arquivo mais de uma vez no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="193e2-104">ICE30 validates that the installation of components containing the same file never installs the file more than once in the same directory.</span></span>

<span data-ttu-id="193e2-105">ICE30 vai para todos os componentes na [tabela de componentes](component-table.md) e determina o diretório de destino do componente da [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="193e2-105">ICE30 goes to every component in the [Component table](component-table.md) and then determines the component's target directory from the [Directory table](directory-table.md).</span></span> <span data-ttu-id="193e2-106">Em seguida, ele verifica para ver quais desses componentes são instalados no mesmo diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="193e2-106">It then checks to see which of these components install to the same target directory.</span></span> <span data-ttu-id="193e2-107">Por fim, ele usa a [tabela de arquivos](file-table.md) para verificar se nenhum dos arquivos nesses componentes tem o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="193e2-107">Finally, it uses the [File table](file-table.md) to verify that none of the files in these components have the same name.</span></span>

<span data-ttu-id="193e2-108">ICE30 verifica nomes de arquivo longos (LFN) e nomes de arquivo curtos (SFN).</span><span class="sxs-lookup"><span data-stu-id="193e2-108">ICE30 checks both long file names (LFN) and short file names (SFN).</span></span>

<span data-ttu-id="193e2-109">ICE30 não avalia as propriedades na resolução de diretórios porque essas propriedades podem ser alteradas em tempo de execução e alterar o esquema de resolução de diretório.</span><span class="sxs-lookup"><span data-stu-id="193e2-109">ICE30 does not evaluate properties in the resolution of directories because these properties can change at runtime and alter the directory resolution scheme.</span></span> <span data-ttu-id="193e2-110">Isso significa que o ICE30 pode detectar colisões de arquivo devido a diretórios com a mesma propriedade em seus caminhos, mas não detecta colisões resultantes de duas propriedades com o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="193e2-110">This means ICE30 can detect file collisions due to directories with the same property in their paths, but does not detect collisions resulting from two properties having the same value.</span></span>

## <a name="result"></a><span data-ttu-id="193e2-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="193e2-111">Result</span></span>

<span data-ttu-id="193e2-112">O ICE30 posta uma mensagem de erro para cada par de componentes que instala o mesmo arquivo no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="193e2-112">ICE30 posts an error message for each pair of components that installs the same file to the same directory.</span></span>

## <a name="example"></a><span data-ttu-id="193e2-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="193e2-113">Example</span></span>

<span data-ttu-id="193e2-114">O exemplo mostrado retorna cada um dos seguintes erros duas vezes.</span><span class="sxs-lookup"><span data-stu-id="193e2-114">The example shown returns each of the following errors twice.</span></span>



| <span data-ttu-id="193e2-115">Erro ou aviso do ICE30</span><span class="sxs-lookup"><span data-stu-id="193e2-115">ICE30 error or warning</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="193e2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="193e2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="193e2-117">ERRO: o arquivo de destino ' README. 1o ' está instalado em ' TARGETDIR \\ Product ' por dois componentes diferentes em um sistema SFN: ' Component1 ' e ' Component2 '.</span><span class="sxs-lookup"><span data-stu-id="193e2-117">ERROR: The target file 'README.1st' is installed in 'TARGETDIR\\PRODUCT' by two different components on an SFN system: 'Component1' and 'Component2'.</span></span> <span data-ttu-id="193e2-118">Essa contagem de referência de componente de quebras.</span><span class="sxs-lookup"><span data-stu-id="193e2-118">This breaks component reference counting.</span></span>                                                                                           | <span data-ttu-id="193e2-119">Component1 e Component2 têm um arquivo chamado ' READEME. 1o '.</span><span class="sxs-lookup"><span data-stu-id="193e2-119">Component1 and Component2 both have a file named 'READEME.1st'.</span></span> <span data-ttu-id="193e2-120">Ao usar nomes de arquivo curtos, o instalador instala dir1 e dir2 no mesmo diretório, produto TARGETDIR \\ .</span><span class="sxs-lookup"><span data-stu-id="193e2-120">When using short file names, the installer installs both Dir1 and Dir2 to the same directory, TARGETDIR\\PRODUCT.</span></span><br/> <span data-ttu-id="193e2-121">ICE30 gera dois erros, um para cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="193e2-121">ICE30 generate two errors, one for each file.</span></span> <span data-ttu-id="193e2-122">Em um ambiente de criação que exibe locais de erro, o primeiro erro está na entrada de um arquivo na [tabela de arquivos](file-table.md)e o segundo no local do outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="193e2-122">In an authoring environment that displays error locations, the first error is at one file's entry in the [File Table](file-table.md), and the second at the location of the other file.</span></span><br/> |
| <span data-ttu-id="193e2-123">ERRO: a instalação de um componente condicional faria com que o arquivo de destino ' README. 1o ' fosse instalado em ' TARGETDIR \\ Common Tools ' por dois componentes diferentes em um sistema LFN: ' Component3 ' e ' Component4 '.</span><span class="sxs-lookup"><span data-stu-id="193e2-123">ERROR: Installation of a conditionalized component would cause the target file 'README.1st' to be installed in 'TARGETDIR\\COMMON TOOLS' by two different components on an LFN system: 'Component3' and 'Component4'.</span></span> <span data-ttu-id="193e2-124">Isso interromperia a contagem de referências de componentes.</span><span class="sxs-lookup"><span data-stu-id="193e2-124">This would break component reference counting.</span></span>                      | <span data-ttu-id="193e2-125">Component4 tem uma entrada na coluna Condition da [tabela Component](component-table.md) e Component3 não.</span><span class="sxs-lookup"><span data-stu-id="193e2-125">Component4 has an entry in the Condition column of the [Component table](component-table.md) and Component3 does not.</span></span> <span data-ttu-id="193e2-126">Se [**VersionNT**](versionnt.md) for true, Component4 será instalado e haverá uma colisão com o README. 1o sempre instalado pelo Component3.</span><span class="sxs-lookup"><span data-stu-id="193e2-126">If [**VersionNT**](versionnt.md) is True, Component4 is installed, and there a collision with the Readme.1st always installed by Component3.</span></span><br/> <span data-ttu-id="193e2-127">O ICE30 gera 4 erros, um par para SFN, um para LFN.</span><span class="sxs-lookup"><span data-stu-id="193e2-127">ICE30 generates 4 errors, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |
| <span data-ttu-id="193e2-128">Aviso: o arquivo de destino ' README. 1o ' pode ser instalado em ' TARGETDIR \\ Common Tools ' por dois componentes condicionais diferentes em um sistema SFN: ' Component4 ' e ' Component5 '.</span><span class="sxs-lookup"><span data-stu-id="193e2-128">WARNING: The target file 'README.1st' might be installed in 'TARGETDIR\\COMMON TOOLS' by two different conditionalized components on an SFN system: 'Component4' and 'Component5'.</span></span> <span data-ttu-id="193e2-129">Se as condições não forem mutuamente exclusivas, isso interromperá o sistema de contagem de referência do componente.</span><span class="sxs-lookup"><span data-stu-id="193e2-129">If the conditions are not mutually exclusive, this will break the component reference counting system.</span></span> | <span data-ttu-id="193e2-130">Como Component4 e Component5 têm entradas na coluna condição da [tabela de componentes](component-table.md) , essa colisão de arquivo pode não ocorrer.</span><span class="sxs-lookup"><span data-stu-id="193e2-130">Because Component4 and Component5 both have entries in the Condition column of the [Component table](component-table.md) this file collision may not occur.</span></span> <span data-ttu-id="193e2-131">O ICE30 posta apenas um aviso porque as condições devem ser determinadas no momento da instalação.</span><span class="sxs-lookup"><span data-stu-id="193e2-131">ICE30 only posts a warning because the conditions must be determined at the time of the installation.</span></span><br/> <span data-ttu-id="193e2-132">O ICE30 gera 4 avisos, um par para SFN, um para LFN.</span><span class="sxs-lookup"><span data-stu-id="193e2-132">ICE30 generates 4 warnings, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |



 

<span data-ttu-id="193e2-133">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="193e2-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="193e2-134">Componente</span><span class="sxs-lookup"><span data-stu-id="193e2-134">Component</span></span>  | <span data-ttu-id="193e2-135">Diretório</span><span class="sxs-lookup"><span data-stu-id="193e2-135">Directory</span></span> | <span data-ttu-id="193e2-136">Condição</span><span class="sxs-lookup"><span data-stu-id="193e2-136">Condition</span></span> |
|------------|-----------|-----------|
| <span data-ttu-id="193e2-137">Component1</span><span class="sxs-lookup"><span data-stu-id="193e2-137">Component1</span></span> | <span data-ttu-id="193e2-138">Dir1</span><span class="sxs-lookup"><span data-stu-id="193e2-138">Dir1</span></span>      |           |
| <span data-ttu-id="193e2-139">Component2</span><span class="sxs-lookup"><span data-stu-id="193e2-139">Component2</span></span> | <span data-ttu-id="193e2-140">Dir2</span><span class="sxs-lookup"><span data-stu-id="193e2-140">Dir2</span></span>      |           |
| <span data-ttu-id="193e2-141">Component3</span><span class="sxs-lookup"><span data-stu-id="193e2-141">Component3</span></span> | <span data-ttu-id="193e2-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="193e2-142">Dir3</span></span>      |           |
| <span data-ttu-id="193e2-143">Component4</span><span class="sxs-lookup"><span data-stu-id="193e2-143">Component4</span></span> | <span data-ttu-id="193e2-144">Dir3</span><span class="sxs-lookup"><span data-stu-id="193e2-144">Dir3</span></span>      | <span data-ttu-id="193e2-145">VersionNT</span><span class="sxs-lookup"><span data-stu-id="193e2-145">VersionNT</span></span> |
| <span data-ttu-id="193e2-146">Component5</span><span class="sxs-lookup"><span data-stu-id="193e2-146">Component5</span></span> | <span data-ttu-id="193e2-147">Dir3</span><span class="sxs-lookup"><span data-stu-id="193e2-147">Dir3</span></span>      | <span data-ttu-id="193e2-148">Version9X</span><span class="sxs-lookup"><span data-stu-id="193e2-148">Version9X</span></span> |



 

[<span data-ttu-id="193e2-149">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="193e2-149">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="193e2-150">Diretório</span><span class="sxs-lookup"><span data-stu-id="193e2-150">Directory</span></span> | <span data-ttu-id="193e2-151">\_Diretório pai</span><span class="sxs-lookup"><span data-stu-id="193e2-151">Parent\_Directory</span></span> | <span data-ttu-id="193e2-152">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="193e2-152">DefaultDir</span></span>                    |
|-----------|-------------------|-------------------------------|
| <span data-ttu-id="193e2-153">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="193e2-153">SOURCEDIR</span></span> |                   | <span data-ttu-id="193e2-154">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="193e2-154">TARGETDIR</span></span>                     |
| <span data-ttu-id="193e2-155">Dir1</span><span class="sxs-lookup"><span data-stu-id="193e2-155">Dir1</span></span>      | <span data-ttu-id="193e2-156">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="193e2-156">SOURCEDIR</span></span>         | <span data-ttu-id="193e2-157">Produto \| Component1 produto:.</span><span class="sxs-lookup"><span data-stu-id="193e2-157">Product\|Component1 Product:.</span></span> |
| <span data-ttu-id="193e2-158">Dir2</span><span class="sxs-lookup"><span data-stu-id="193e2-158">Dir2</span></span>      | <span data-ttu-id="193e2-159">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="193e2-159">SOURCEDIR</span></span>         | <span data-ttu-id="193e2-160">Produto:.</span><span class="sxs-lookup"><span data-stu-id="193e2-160">Product:.</span></span>                     |
| <span data-ttu-id="193e2-161">Dir3</span><span class="sxs-lookup"><span data-stu-id="193e2-161">Dir3</span></span>      | <span data-ttu-id="193e2-162">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="193e2-162">SOURCEDIR</span></span>         | <span data-ttu-id="193e2-163">\|Ferramentas comuns comuns:</span><span class="sxs-lookup"><span data-stu-id="193e2-163">Common\|Common Tools:</span></span>         |



 

<span data-ttu-id="193e2-164">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="193e2-164">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="193e2-165">Arquivo</span><span class="sxs-lookup"><span data-stu-id="193e2-165">File</span></span>  | <span data-ttu-id="193e2-166">Componente\_</span><span class="sxs-lookup"><span data-stu-id="193e2-166">Component\_</span></span> | <span data-ttu-id="193e2-167">FileName</span><span class="sxs-lookup"><span data-stu-id="193e2-167">FileName</span></span>   |
|-------|-------------|------------|
| <span data-ttu-id="193e2-168">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="193e2-168">File1</span></span> | <span data-ttu-id="193e2-169">Component1</span><span class="sxs-lookup"><span data-stu-id="193e2-169">Component1</span></span>  | <span data-ttu-id="193e2-170">LEIAme. 1º</span><span class="sxs-lookup"><span data-stu-id="193e2-170">README.1st</span></span> |
| <span data-ttu-id="193e2-171">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="193e2-171">File2</span></span> | <span data-ttu-id="193e2-172">Component2</span><span class="sxs-lookup"><span data-stu-id="193e2-172">Component2</span></span>  | <span data-ttu-id="193e2-173">LEIAme. 1º</span><span class="sxs-lookup"><span data-stu-id="193e2-173">README.1st</span></span> |
| <span data-ttu-id="193e2-174">Arquivo3</span><span class="sxs-lookup"><span data-stu-id="193e2-174">File3</span></span> | <span data-ttu-id="193e2-175">Component3</span><span class="sxs-lookup"><span data-stu-id="193e2-175">Component3</span></span>  | <span data-ttu-id="193e2-176">LEIAme. 1º</span><span class="sxs-lookup"><span data-stu-id="193e2-176">README.1st</span></span> |
| <span data-ttu-id="193e2-177">Arquivo4</span><span class="sxs-lookup"><span data-stu-id="193e2-177">File4</span></span> | <span data-ttu-id="193e2-178">Component4</span><span class="sxs-lookup"><span data-stu-id="193e2-178">Component4</span></span>  | <span data-ttu-id="193e2-179">LEIAme. 1º</span><span class="sxs-lookup"><span data-stu-id="193e2-179">README.1st</span></span> |
| <span data-ttu-id="193e2-180">Arquivo5</span><span class="sxs-lookup"><span data-stu-id="193e2-180">File5</span></span> | <span data-ttu-id="193e2-181">Component5</span><span class="sxs-lookup"><span data-stu-id="193e2-181">Component5</span></span>  | <span data-ttu-id="193e2-182">LEIAme. 1º</span><span class="sxs-lookup"><span data-stu-id="193e2-182">README.1st</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="193e2-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="193e2-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="193e2-184">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="193e2-184">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




