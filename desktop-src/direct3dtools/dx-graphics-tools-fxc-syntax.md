---
title: Sintaxe
description: Aqui está a sintaxe para chamar FXC.exe, a ferramenta de compilador de efeito. Para obter um exemplo, consulte compilando offline.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- FXC, sintaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105781560"
---
# <a name="syntax"></a><span data-ttu-id="dd375-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd375-105">Syntax</span></span>

<span data-ttu-id="dd375-106">Aqui está a sintaxe para chamar FXC.exe, a ferramenta de compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="dd375-106">Here is the syntax for calling FXC.exe, the effect-compiler tool.</span></span> <span data-ttu-id="dd375-107">Para obter um exemplo, consulte [compilando offline](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="dd375-107">For an example, see [Offline Compiling](dx-graphics-tools-fxc-using.md).</span></span>

-   [<span data-ttu-id="dd375-108">Usage</span><span class="sxs-lookup"><span data-stu-id="dd375-108">Usage</span></span>](#usage)
-   [<span data-ttu-id="dd375-109">Argumentos</span><span class="sxs-lookup"><span data-stu-id="dd375-109">Arguments</span></span>](#arguments)
-   [<span data-ttu-id="dd375-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd375-110">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="dd375-111">Perfis</span><span class="sxs-lookup"><span data-stu-id="dd375-111">Profiles</span></span>](#profiles)
-   [<span data-ttu-id="dd375-112">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="dd375-112">Version notes</span></span>](#version-notes)
-   [<span data-ttu-id="dd375-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd375-113">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="dd375-114">Uso</span><span class="sxs-lookup"><span data-stu-id="dd375-114">Usage</span></span>

<span data-ttu-id="dd375-115">*nomes* de **FXC** do *switchoptions*</span><span class="sxs-lookup"><span data-stu-id="dd375-115">**fxc** *SwitchOptions* *Filenames*</span></span>

## <a name="arguments"></a><span data-ttu-id="dd375-116">Argumentos</span><span class="sxs-lookup"><span data-stu-id="dd375-116">Arguments</span></span>
<span data-ttu-id="dd375-117">Separe cada opção de comutador com um espaço ou dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="dd375-117">Separate each switch option with a space or a colon.</span></span>

### <a name="switchoptions"></a><span data-ttu-id="dd375-118">*Switchoptions*</span><span class="sxs-lookup"><span data-stu-id="dd375-118">*SwitchOptions*</span></span>
<span data-ttu-id="dd375-119">\[em \] Opções de compilação.</span><span class="sxs-lookup"><span data-stu-id="dd375-119">\[in\] Compile options.</span></span> <span data-ttu-id="dd375-120">Há apenas uma opção necessária e muito mais que são opcionais.</span><span class="sxs-lookup"><span data-stu-id="dd375-120">There is just one required option, and many more that are optional.</span></span> <span data-ttu-id="dd375-121">Separe cada um com um ou dois espaços.</span><span class="sxs-lookup"><span data-stu-id="dd375-121">Separate each with a space or colon.</span></span>

#### <a name="required-option"></a><span data-ttu-id="dd375-122">Opção necessária</span><span class="sxs-lookup"><span data-stu-id="dd375-122">Required option</span></span>
##### <a name="t-profile"></a><span data-ttu-id="dd375-123">/T <*perfil*></span><span class="sxs-lookup"><span data-stu-id="dd375-123">/T <*profile*></span></span>
<span data-ttu-id="dd375-124">Modelo de sombreador (consulte [perfis](#profiles)).</span><span class="sxs-lookup"><span data-stu-id="dd375-124">Shader model (see [Profiles](#profiles)).</span></span>

#### <a name="optional-options"></a><span data-ttu-id="dd375-125">Opções opcionais</span><span class="sxs-lookup"><span data-stu-id="dd375-125">Optional options</span></span>
##### <a name="-help"></a><span data-ttu-id="dd375-126">/?, /help</span><span class="sxs-lookup"><span data-stu-id="dd375-126">/?, /help</span></span>
<span data-ttu-id="dd375-127">Imprimir ajuda para `FXC.exe` .</span><span class="sxs-lookup"><span data-stu-id="dd375-127">Print help for `FXC.exe`.</span></span>

##### <a name="commandoptionfile"></a><span data-ttu-id="dd375-128">@<*comando. Option. File*></span><span class="sxs-lookup"><span data-stu-id="dd375-128">@<*command.option.file*></span></span>
<span data-ttu-id="dd375-129">Arquivo que contém opções de compilação adicionais.</span><span class="sxs-lookup"><span data-stu-id="dd375-129">File that contains additional compile options.</span></span> <span data-ttu-id="dd375-130">Essa opção pode ser combinada com outras opções de compilação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="dd375-130">This option can be mixed with other command line compile options.</span></span> <span data-ttu-id="dd375-131">O *comando. Option. File* deve conter apenas uma opção por linha.</span><span class="sxs-lookup"><span data-stu-id="dd375-131">The *command.option.file* must contain only one option per line.</span></span> <span data-ttu-id="dd375-132">O *comando. Option. File* não pode conter nenhuma linha em branco.</span><span class="sxs-lookup"><span data-stu-id="dd375-132">The *command.option.file* cannot contain any blank lines.</span></span> <span data-ttu-id="dd375-133">As opções especificadas no arquivo não devem conter espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="dd375-133">Options specified in the file must not contain any leading or trailing spaces.</span></span>

##### <a name="all_resources_bound"></a><span data-ttu-id="dd375-134">/all_resources_bound</span><span class="sxs-lookup"><span data-stu-id="dd375-134">/all_resources_bound</span></span>
<span data-ttu-id="dd375-135">Habilite o nivelamento agressivo no SM 5.1 +.</span><span class="sxs-lookup"><span data-stu-id="dd375-135">Enable aggressive flattening in SM5.1+.</span></span> <span data-ttu-id="dd375-136">Novo para o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="dd375-136">New for Direct3D 12.</span></span>

##### <a name="cc"></a><span data-ttu-id="dd375-137">/CC</span><span class="sxs-lookup"><span data-stu-id="dd375-137">/Cc</span></span>
<span data-ttu-id="dd375-138">Assembly com código de cor de saída.</span><span class="sxs-lookup"><span data-stu-id="dd375-138">Output color-coded assembly.</span></span>

##### <a name="compress"></a><span data-ttu-id="dd375-139">/compress</span><span class="sxs-lookup"><span data-stu-id="dd375-139">/compress</span></span>
<span data-ttu-id="dd375-140">Compacte o código de bytes do sombreador DX10 dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="dd375-140">Compress DX10 shader bytecode from files.</span></span>

##### <a name="d-idtext"></a><span data-ttu-id="dd375-141">/D < >=< *texto* da ID></span><span class="sxs-lookup"><span data-stu-id="dd375-141">/D <*id*>=<*text*></span></span>
<span data-ttu-id="dd375-142">Definir macro.</span><span class="sxs-lookup"><span data-stu-id="dd375-142">Define macro.</span></span>

##### <a name="decompress"></a><span data-ttu-id="dd375-143">/decompress</span><span class="sxs-lookup"><span data-stu-id="dd375-143">/decompress</span></span>
<span data-ttu-id="dd375-144">Descompacte o código de bytes do sombreador DX10 do primeiro arquivo.</span><span class="sxs-lookup"><span data-stu-id="dd375-144">Decompress DX10 shader bytecode from first file.</span></span> <span data-ttu-id="dd375-145">Os arquivos de saída devem ser listados na ordem em que estavam durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="dd375-145">Output files should be listed in the order they were in during compression.</span></span>

##### <a name="dumpbin"></a><span data-ttu-id="dd375-146">/dumpbin</span><span class="sxs-lookup"><span data-stu-id="dd375-146">/dumpbin</span></span>
<span data-ttu-id="dd375-147">Carrega um arquivo binário em vez de compilar um sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-147">Loads a binary file rather than compiling a shader.</span></span>

##### <a name="e-name"></a><span data-ttu-id="dd375-148">/E <name></span><span class="sxs-lookup"><span data-stu-id="dd375-148">/E <name></span></span>
<span data-ttu-id="dd375-149">Ponto de entrada do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-149">Shader entry point.</span></span> <span data-ttu-id="dd375-150">Se nenhum ponto de entrada for fornecido, **Main** será considerado o nome da entrada do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-150">If no entry point is given, **main** is considered to be the shader entry name.</span></span>

##### <a name="enable_unbounded_descriptor_tables"></a><span data-ttu-id="dd375-151">/enable_unbounded_descriptor_tables</span><span class="sxs-lookup"><span data-stu-id="dd375-151">/enable_unbounded_descriptor_tables</span></span>
<span data-ttu-id="dd375-152">Habilita tabelas de descritor não associadas.</span><span class="sxs-lookup"><span data-stu-id="dd375-152">Enables unbounded descriptor tables.</span></span> <span data-ttu-id="dd375-153">Novo para o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="dd375-153">New for Direct3D 12.</span></span>

##### <a name="extractrootsignature-file"></a><span data-ttu-id="dd375-154">*arquivo* de </extractrootsignature></span><span class="sxs-lookup"><span data-stu-id="dd375-154">/extractrootsignature <*file*></span></span>
<span data-ttu-id="dd375-155">Extraia a assinatura raiz do código de bytes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-155">Extract root signature from shader bytecode.</span></span> <span data-ttu-id="dd375-156">Novo para o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="dd375-156">New for Direct3D 12.</span></span>

##### <a name="fc-file"></a><span data-ttu-id="dd375-157">*Arquivo* de </FC></span><span class="sxs-lookup"><span data-stu-id="dd375-157">/Fc <*file*></span></span>
<span data-ttu-id="dd375-158">Arquivo de listagem de código de assembly de saída.</span><span class="sxs-lookup"><span data-stu-id="dd375-158">Output assembly code listing file.</span></span>

##### <a name="fd-file"></a><span data-ttu-id="dd375-159">*Arquivo* de </FD></span><span class="sxs-lookup"><span data-stu-id="dd375-159">/Fd <*file*></span></span>
<span data-ttu-id="dd375-160">Extraia informações de PDB (banco de dados do programa do sombreador) e grave no arquivo fornecido. Ao compilar o sombreador, use/FD para gerar um arquivo PDB com informações de depuração do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-160">Extract shader program database (PDB) info and write to the given file.When you compile the shader, use /Fd to generate a PDB file with shader debugging info.</span></span>

##### <a name="fe-file"></a><span data-ttu-id="dd375-161">*Arquivo* de </FE></span><span class="sxs-lookup"><span data-stu-id="dd375-161">/Fe <*file*></span></span>
<span data-ttu-id="dd375-162">Avisos de saída e erros para o arquivo fornecido.</span><span class="sxs-lookup"><span data-stu-id="dd375-162">Output warnings and errors to the given file.</span></span>

##### <a name="fh-file"></a><span data-ttu-id="dd375-163">*Arquivo* de </FH></span><span class="sxs-lookup"><span data-stu-id="dd375-163">/Fh <*file*></span></span>
<span data-ttu-id="dd375-164">Arquivo de cabeçalho de saída que contém o código do objeto.</span><span class="sxs-lookup"><span data-stu-id="dd375-164">Output header file containing object code.</span></span>

##### <a name="fl-file"></a><span data-ttu-id="dd375-165">*Arquivo* de </FL</span><span class="sxs-lookup"><span data-stu-id="dd375-165">/Fl <*file*</span></span>
<span data-ttu-id="dd375-166">Saída de uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="dd375-166">Output a library.</span></span> <span data-ttu-id="dd375-167">Requer o \_47.dll D3dcompiler ou uma versão posterior da dll.</span><span class="sxs-lookup"><span data-stu-id="dd375-167">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="fo-file"></a><span data-ttu-id="dd375-168">/Fo <*arquivo*></span><span class="sxs-lookup"><span data-stu-id="dd375-168">/Fo <*file*></span></span>
<span data-ttu-id="dd375-169">Arquivo de objeto de saída.</span><span class="sxs-lookup"><span data-stu-id="dd375-169">Output object file.</span></span> <span data-ttu-id="dd375-170">Geralmente, dada a extensão &quot; . fxc &quot; , embora outras extensões sejam usadas, como &quot; . o &quot; , &quot; . obj &quot; ou &quot; . dxbc &quot; .</span><span class="sxs-lookup"><span data-stu-id="dd375-170">Often given the extension &quot;.fxc&quot;, though other extensions are used, such as &quot;.o&quot;, &quot;.obj&quot; or &quot;.dxbc&quot;.</span></span>

##### <a name="fx-file"></a><span data-ttu-id="dd375-171">*Arquivo* de </FX></span><span class="sxs-lookup"><span data-stu-id="dd375-171">/Fx <*file*></span></span>
<span data-ttu-id="dd375-172">Código do assembly de saída e arquivo de listagem Hex.</span><span class="sxs-lookup"><span data-stu-id="dd375-172">Output assembly code and hex listing file.</span></span>

##### <a name="gch"></a><span data-ttu-id="dd375-173">/Gch</span><span class="sxs-lookup"><span data-stu-id="dd375-173">/Gch</span></span>
<span data-ttu-id="dd375-174">Compile como um efeito filho para perfis de fx_4_x.</span><span class="sxs-lookup"><span data-stu-id="dd375-174">Compile as a child effect for fx_4_x profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="dd375-175">O suporte para perfis de efeitos herdados foi preterido.</span><span class="sxs-lookup"><span data-stu-id="dd375-175">Support for legacy Effects profiles is deprecated.</span></span>

##### <a name="gdp"></a><span data-ttu-id="dd375-176">/Gdp</span><span class="sxs-lookup"><span data-stu-id="dd375-176">/Gdp</span></span>
<span data-ttu-id="dd375-177">Desabilitar o modo de desempenho de efeito.</span><span class="sxs-lookup"><span data-stu-id="dd375-177">Disable effect performance mode.</span></span>

##### <a name="gec"></a><span data-ttu-id="dd375-178">/Gec</span><span class="sxs-lookup"><span data-stu-id="dd375-178">/Gec</span></span>
<span data-ttu-id="dd375-179">Habilitar o modo de compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="dd375-179">Enable backward compatibility mode.</span></span>

##### <a name="ges"></a><span data-ttu-id="dd375-180">/Ges</span><span class="sxs-lookup"><span data-stu-id="dd375-180">/Ges</span></span>
<span data-ttu-id="dd375-181">Habilite o modo estrito.</span><span class="sxs-lookup"><span data-stu-id="dd375-181">Enable strict mode.</span></span>

##### <a name="getprivate-file"></a><span data-ttu-id="dd375-182">*arquivo* de </GetPrivate></span><span class="sxs-lookup"><span data-stu-id="dd375-182">/getprivate <*file*></span></span>
<span data-ttu-id="dd375-183">Salve dados privados do blob de sombreador (binário de sombreador compilado) no arquivo fornecido.</span><span class="sxs-lookup"><span data-stu-id="dd375-183">Save private data from the shader blob (compiled shader binary) to the given file.</span></span> <span data-ttu-id="dd375-184">Extrai dados privados, anteriormente inseridos por/SetPrivate, do blob de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-184">Extracts private data, previously embedded by /setprivate, from the shader blob.</span></span>

<span data-ttu-id="dd375-185">Você deve especificar a opção/DUMPBIN com/GetPrivate.</span><span class="sxs-lookup"><span data-stu-id="dd375-185">You must specify the /dumpbin option with /getprivate.</span></span> <span data-ttu-id="dd375-186">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dd375-186">For example:</span></span>

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a><span data-ttu-id="dd375-187">/Gfa</span><span class="sxs-lookup"><span data-stu-id="dd375-187">/Gfa</span></span>
<span data-ttu-id="dd375-188">Evite construções de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="dd375-188">Avoid flow control constructs.</span></span>

##### <a name="gfp"></a><span data-ttu-id="dd375-189">/GFP,</span><span class="sxs-lookup"><span data-stu-id="dd375-189">/Gfp</span></span>
<span data-ttu-id="dd375-190">Prefira construções de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="dd375-190">Prefer flow control constructs.</span></span>

##### <a name="gis"></a><span data-ttu-id="dd375-191">/Gis</span><span class="sxs-lookup"><span data-stu-id="dd375-191">/Gis</span></span>
<span data-ttu-id="dd375-192">Forçar restrição de IEEE.</span><span class="sxs-lookup"><span data-stu-id="dd375-192">Force IEEE strictness.</span></span>

##### <a name="gpp"></a><span data-ttu-id="dd375-193">/Gpp</span><span class="sxs-lookup"><span data-stu-id="dd375-193">/Gpp</span></span>
<span data-ttu-id="dd375-194">Forçar a precisão parcial.</span><span class="sxs-lookup"><span data-stu-id="dd375-194">Force partial precision.</span></span>
    
##### <a name="i-include"></a><span data-ttu-id="dd375-195">/I <*incluir*></span><span class="sxs-lookup"><span data-stu-id="dd375-195">/I <*include*></span></span>
<span data-ttu-id="dd375-196">Caminho de inclusão adicional.</span><span class="sxs-lookup"><span data-stu-id="dd375-196">Additional include path.</span></span>

##### <a name="lx"></a><span data-ttu-id="dd375-197">/Lx</span><span class="sxs-lookup"><span data-stu-id="dd375-197">/Lx</span></span>
<span data-ttu-id="dd375-198">Literais hexadecimais de saída.</span><span class="sxs-lookup"><span data-stu-id="dd375-198">Output hexadecimal literals.</span></span> <span data-ttu-id="dd375-199">Requer o \_47.dll D3dcompiler ou uma versão posterior da dll.</span><span class="sxs-lookup"><span data-stu-id="dd375-199">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="matchuavs"></a><span data-ttu-id="dd375-200">/matchUAVs</span><span class="sxs-lookup"><span data-stu-id="dd375-200">/matchUAVs</span></span>
<span data-ttu-id="dd375-201">Corresponder as alocações do slot do UAV do sombreador de modelo no sombreador atual.</span><span class="sxs-lookup"><span data-stu-id="dd375-201">Match template shader UAV slot allocations in the current shader.</span></span> <span data-ttu-id="dd375-202">Para obter mais informações, consulte <a href="#remarks">comentários</a>.</span><span class="sxs-lookup"><span data-stu-id="dd375-202">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="mergeuavs"></a><span data-ttu-id="dd375-203">/mergeUAVs</span><span class="sxs-lookup"><span data-stu-id="dd375-203">/mergeUAVs</span></span>
<span data-ttu-id="dd375-204">Mescle as alocações do slot UAV do sombreador de modelo e o sombreador atual.</span><span class="sxs-lookup"><span data-stu-id="dd375-204">Merge UAV slot allocations of template shader and the current shader.</span></span> <span data-ttu-id="dd375-205">Para obter mais informações, consulte <a href=""></a> <a href="#remarks">comentários</a>.</span><span class="sxs-lookup"><span data-stu-id="dd375-205">For more info, see <a href=""></a><a href="#remarks">Remarks</a>.</span></span>

##### <a name="ni"></a><span data-ttu-id="dd375-206">/Ni</span><span class="sxs-lookup"><span data-stu-id="dd375-206">/Ni</span></span>
<span data-ttu-id="dd375-207">Números de instrução de saída em listagens de assembly.</span><span class="sxs-lookup"><span data-stu-id="dd375-207">Output instruction numbers in assembly listings.</span></span>

##### <a name="no"></a><span data-ttu-id="dd375-208">/</span><span class="sxs-lookup"><span data-stu-id="dd375-208">/No</span></span>
<span data-ttu-id="dd375-209">Deslocamento de byte de instrução de saída em listagens de assembly.</span><span class="sxs-lookup"><span data-stu-id="dd375-209">Output instruction byte offset in assembly listings.</span></span> <span data-ttu-id="dd375-210">Quando você produzir o assembly, use////para anotar com o deslocamento de bytes para cada instrução.</span><span class="sxs-lookup"><span data-stu-id="dd375-210">When you produce assembly, use /No to annotate it with the byte offset for each instruction.</span></span>

##### <a name="nologo"></a><span data-ttu-id="dd375-211">/nologo</span><span class="sxs-lookup"><span data-stu-id="dd375-211">/nologo</span></span>
<span data-ttu-id="dd375-212">Suprime uma mensagem de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="dd375-212">Suppress copyright message.</span></span>

##### <a name="od"></a><span data-ttu-id="dd375-213">/Od</span><span class="sxs-lookup"><span data-stu-id="dd375-213">/Od</span></span>
<span data-ttu-id="dd375-214">Desabilitar otimizações.</span><span class="sxs-lookup"><span data-stu-id="dd375-214">Disable optimizations.</span></span> <span data-ttu-id="dd375-215">/OD implica/GFP,, mas a saída pode não ser idêntica a/OD/GFP.</span><span class="sxs-lookup"><span data-stu-id="dd375-215">/Od implies /Gfp, though output may not be identical to /Od /Gfp.</span></span>

##### <a name="op"></a><span data-ttu-id="dd375-216">/Op</span><span class="sxs-lookup"><span data-stu-id="dd375-216">/Op</span></span>
<span data-ttu-id="dd375-217">Desabilitar preshaders (preterido).</span><span class="sxs-lookup"><span data-stu-id="dd375-217">Disable preshaders (deprecated).</span></span>

##### <a name="o0-o1-o2-o3"></a><span data-ttu-id="dd375-218">/O0/O1,/O2,/O3</span><span class="sxs-lookup"><span data-stu-id="dd375-218">/O0 /O1, /O2, /O3</span></span>
<span data-ttu-id="dd375-219">Níveis de otimização.</span><span class="sxs-lookup"><span data-stu-id="dd375-219">Optimization levels.</span></span> <span data-ttu-id="dd375-220">O1 é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="dd375-220">O1 is the default setting.</span></span>
- <span data-ttu-id="dd375-221">O0-desabilita a reordenação de instrução.</span><span class="sxs-lookup"><span data-stu-id="dd375-221">O0 - Disables instruction reordering.</span></span> <span data-ttu-id="dd375-222">Isso ajuda a reduzir a carga de registro e permite uma simulação de loop mais rápida.</span><span class="sxs-lookup"><span data-stu-id="dd375-222">This helps reduce register load and enables faster loop simulation.</span></span>
- <span data-ttu-id="dd375-223">O1-desabilita a reordenação de instrução para ps_3_0 e para cima.</span><span class="sxs-lookup"><span data-stu-id="dd375-223">O1 - Disables instruction reordering for ps_3_0 and up.</span></span>
- <span data-ttu-id="dd375-224">O2-igual a O1.</span><span class="sxs-lookup"><span data-stu-id="dd375-224">O2 - Same as O1.</span></span> <span data-ttu-id="dd375-225">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="dd375-225">Reserved for future use.</span></span>
- <span data-ttu-id="dd375-226">O3-igual a O1.</span><span class="sxs-lookup"><span data-stu-id="dd375-226">O3 - Same as O1.</span></span> <span data-ttu-id="dd375-227">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="dd375-227">Reserved for future use.</span></span>

##### <a name="p-file"></a><span data-ttu-id="dd375-228">/P <*arquivo*></span><span class="sxs-lookup"><span data-stu-id="dd375-228">/P <*file*></span></span>
<span data-ttu-id="dd375-229">Pré-processar para o arquivo (deve ser usado sozinho).</span><span class="sxs-lookup"><span data-stu-id="dd375-229">Preprocess to file (must be used alone).</span></span>

##### <a name="qstrip_debug"></a><span data-ttu-id="dd375-230">/Qstrip_debug</span><span class="sxs-lookup"><span data-stu-id="dd375-230">/Qstrip_debug</span></span>
<span data-ttu-id="dd375-231">Remova os dados de depuração do código de bytes do sombreador para 4_0 + perfis.</span><span class="sxs-lookup"><span data-stu-id="dd375-231">Strip debug data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_priv"></a><span data-ttu-id="dd375-232">/Qstrip_priv</span><span class="sxs-lookup"><span data-stu-id="dd375-232">/Qstrip_priv</span></span>
<span data-ttu-id="dd375-233">Remova os dados privados do código de bytes 4_0 + Shader.</span><span class="sxs-lookup"><span data-stu-id="dd375-233">Strip the private data from 4_0+ shader bytecode.</span></span> <span data-ttu-id="dd375-234">Remove dados privados (sequência arbitrária de bytes) do blob de sombreador (binário de sombreador compilado) que você inseriu anteriormente com a `/setprivate <file>` opção.</span><span class="sxs-lookup"><span data-stu-id="dd375-234">Removes private data (arbitrary sequence of bytes) from the shader blob (compiled shader binary) that you previously embedded with the `/setprivate <file>` option.</span></span>

<span data-ttu-id="dd375-235">Você deve especificar a opção/DUMPBIN com/Qstrip_priv.</span><span class="sxs-lookup"><span data-stu-id="dd375-235">You must specify the /dumpbin option with /Qstrip_priv.</span></span> <span data-ttu-id="dd375-236">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dd375-236">For example:</span></span>

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a><span data-ttu-id="dd375-237">/Qstrip_reflect</span><span class="sxs-lookup"><span data-stu-id="dd375-237">/Qstrip_reflect</span></span>
<span data-ttu-id="dd375-238">Remova os dados de reflexo do código de bytes do sombreador para 4_0 + perfis.</span><span class="sxs-lookup"><span data-stu-id="dd375-238">Strip reflection data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_rootsignature"></a><span data-ttu-id="dd375-239">/Qstrip_rootsignature</span><span class="sxs-lookup"><span data-stu-id="dd375-239">/Qstrip_rootsignature</span></span>
<span data-ttu-id="dd375-240">Remova a assinatura raiz do código de bytes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-240">Strip root signature from shader bytecode.</span></span> <span data-ttu-id="dd375-241">Novo para o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="dd375-241">New for Direct3D 12.</span></span>

##### <a name="res_may_alias"></a><span data-ttu-id="dd375-242">/res_may_alias</span><span class="sxs-lookup"><span data-stu-id="dd375-242">/res_may_alias</span></span>
<span data-ttu-id="dd375-243">Suponha que UAVs/SRVs possa alias para cs_5_0 +.</span><span class="sxs-lookup"><span data-stu-id="dd375-243">Assume that UAVs/SRVs may alias for cs_5_0+.</span></span> <span data-ttu-id="dd375-244">Requer o \_47.dll D3dcompiler ou uma versão posterior da dll.</span><span class="sxs-lookup"><span data-stu-id="dd375-244">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="setprivate-file"></a><span data-ttu-id="dd375-245">*arquivo* de </SetPrivate></span><span class="sxs-lookup"><span data-stu-id="dd375-245">/setprivate <*file*></span></span>
<span data-ttu-id="dd375-246">Adicione dados privados no arquivo fornecido ao blob de sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="dd375-246">Add private data in the given file to the compiled shader blob.</span></span> <span data-ttu-id="dd375-247">Insere o arquivo fornecido, que é tratado como um buffer bruto, para o blob de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-247">Embeds the given file, which is treated as a raw buffer, to the shader blob.</span></span> <span data-ttu-id="dd375-248">Use/SetPrivate para adicionar dados privados ao compilar um sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-248">Use /setprivate to add private data when you compile a shader.</span></span> <span data-ttu-id="dd375-249">Ou use a opção/DUMPBIN com/SetPrivate para carregar um objeto de sombreador existente e, depois que o objeto estiver na memória, para adicionar o blob de dados privados.</span><span class="sxs-lookup"><span data-stu-id="dd375-249">Or, use the /dumpbin option with /setprivate to load an existing shader object, and then after the object is in memory, to add the private data blob.</span></span> <span data-ttu-id="dd375-250">Por exemplo, use um único comando com/SetPrivate para adicionar dados privados a um blob de sombreador compilado:</span><span class="sxs-lookup"><span data-stu-id="dd375-250">For example, use either a single command with /setprivate to add private data to a compiled shader blob:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
<span data-ttu-id="dd375-251">Ou use dois comandos em que o segundo comando carrega um objeto de sombreador e, em seguida, adiciona dados privados:</span><span class="sxs-lookup"><span data-stu-id="dd375-251">Or, use two commands where the second command loads a shader object and then adds private data:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a><span data-ttu-id="dd375-252">*arquivo* de </setrootsignature></span><span class="sxs-lookup"><span data-stu-id="dd375-252">/setrootsignature <*file*></span></span>
<span data-ttu-id="dd375-253">Anexe a assinatura raiz ao código de bytes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd375-253">Attach root signature to shader bytecode.</span></span> <span data-ttu-id="dd375-254">Novo para o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="dd375-254">New for Direct3D 12.</span></span>

##### <a name="shtemplate-file"></a><span data-ttu-id="dd375-255">*arquivo* de </shtemplate></span><span class="sxs-lookup"><span data-stu-id="dd375-255">/shtemplate <*file*></span></span>
<span data-ttu-id="dd375-256">Use o arquivo de sombreador de modelo fornecido para recursos de mesclagem (/mergeUAVs) e correspondentes (/matchUAVs).</span><span class="sxs-lookup"><span data-stu-id="dd375-256">Use given template shader file for merging (/mergeUAVs) and matching (/matchUAVs) resources.</span></span> <span data-ttu-id="dd375-257">Para obter mais informações, consulte <a href="#remarks">comentários</a>.</span><span class="sxs-lookup"><span data-stu-id="dd375-257">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="vd"></a><span data-ttu-id="dd375-258">/Vd</span><span class="sxs-lookup"><span data-stu-id="dd375-258">/Vd</span></span>
<span data-ttu-id="dd375-259">Desabilitar validação.</span><span class="sxs-lookup"><span data-stu-id="dd375-259">Disable validation.</span></span>

##### <a name="verifyrootsignature-file"></a><span data-ttu-id="dd375-260">*arquivo* de </verifyrootsignature></span><span class="sxs-lookup"><span data-stu-id="dd375-260">/verifyrootsignature <*file*></span></span>
<span data-ttu-id="dd375-261">Verifique o código de bytes do sombreador em relação à assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="dd375-261">Verify shader bytecode against root signature.</span></span> <span data-ttu-id="dd375-262">Novo para o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="dd375-262">New for Direct3D 12.</span></span>

##### <a name="vi"></a><span data-ttu-id="dd375-263">/Vi</span><span class="sxs-lookup"><span data-stu-id="dd375-263">/Vi</span></span>
<span data-ttu-id="dd375-264">Exibir detalhes sobre o processo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="dd375-264">Display details about the include process.</span></span>

##### <a name="vn-name"></a><span data-ttu-id="dd375-265">*Nome* </vn></span><span class="sxs-lookup"><span data-stu-id="dd375-265">/Vn <*name*></span></span>
<span data-ttu-id="dd375-266">Use nome como nome da variável no arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="dd375-266">Use name as variable name in header file.</span></span>

##### <a name="wx"></a><span data-ttu-id="dd375-267">/WX</span><span class="sxs-lookup"><span data-stu-id="dd375-267">/WX</span></span>
<span data-ttu-id="dd375-268">Tratar avisos como erros.</span><span class="sxs-lookup"><span data-stu-id="dd375-268">Treat warnings as errors.</span></span>

##### <a name="zi"></a><span data-ttu-id="dd375-269">/Zi</span><span class="sxs-lookup"><span data-stu-id="dd375-269">/Zi</span></span>
<span data-ttu-id="dd375-270">Habilitar informações de depuração.</span><span class="sxs-lookup"><span data-stu-id="dd375-270">Enable debugging information.</span></span>

##### <a name="zpc"></a><span data-ttu-id="dd375-271">/Zpc</span><span class="sxs-lookup"><span data-stu-id="dd375-271">/Zpc</span></span>
<span data-ttu-id="dd375-272">Matrizes de pacote na ordem de coluna principal.</span><span class="sxs-lookup"><span data-stu-id="dd375-272">Pack matrices in column-major order.</span></span>

##### <a name="zpr"></a><span data-ttu-id="dd375-273">/Zpr</span><span class="sxs-lookup"><span data-stu-id="dd375-273">/Zpr</span></span>
<span data-ttu-id="dd375-274">Matrizes de pacote na ordem de linha principal.</span><span class="sxs-lookup"><span data-stu-id="dd375-274">Pack matrices in row-major order.</span></span>

### <a name="filenames"></a><span data-ttu-id="dd375-275">*Nomes de arquivos*</span><span class="sxs-lookup"><span data-stu-id="dd375-275">*Filenames*</span></span>

<span data-ttu-id="dd375-276">\[nos \] arquivos que contêm o (s) sombreador (es) e/ou os efeitos.</span><span class="sxs-lookup"><span data-stu-id="dd375-276">\[in\] The files that contains the shader(s) and/or the effect(s).</span></span>

## <a name="remarks"></a><span data-ttu-id="dd375-277">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd375-277">Remarks</span></span>

<span data-ttu-id="dd375-278">Use as `/mergeUAVs` `/matchUAVs` Opções, e `/shtemplate` para alinhar os slots de associação UAV para uma cadeia de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="dd375-278">Use the `/mergeUAVs`, `/matchUAVs`, and `/shtemplate` options to align the UAV binding slots for a chain of shaders.</span></span>

<span data-ttu-id="dd375-279">Suponha que você tenha sombreadores A. FX, B. FX e C. FX.</span><span class="sxs-lookup"><span data-stu-id="dd375-279">Suppose you have shaders A.fx, B.fx, and C.fx.</span></span> <span data-ttu-id="dd375-280">Para alinhar os slots de associação de UAV para essa cadeia de sombreadores, você precisa de duas passagens de compilação:</span><span class="sxs-lookup"><span data-stu-id="dd375-280">To align the UAV binding slots for this chain of shaders, you need two passes of compilation:</span></span>

<span data-ttu-id="dd375-281">**Para alinhar os slots de associação de UAV para uma cadeia de sombreadores**</span><span class="sxs-lookup"><span data-stu-id="dd375-281">**To align the UAV binding slots for a chain of shaders**</span></span>

1.  <span data-ttu-id="dd375-282">Use/mergeUAVs para compilar sombreadores e especifique um blob de sombreador compilado anteriormente com/shtemplate.</span><span class="sxs-lookup"><span data-stu-id="dd375-282">Use /mergeUAVs to compile shaders, and specify a previously-compiled shader blob with /shtemplate.</span></span> <span data-ttu-id="dd375-283">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dd375-283">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  <span data-ttu-id="dd375-284">Use/matchUAVs para compilar sombreadores e especifique o último blob de sombreador da primeira passagem com/shtemplate.</span><span class="sxs-lookup"><span data-stu-id="dd375-284">Use /matchUAVs to compile shaders, and specify the last shader blob from the first pass with /shtemplate.</span></span> <span data-ttu-id="dd375-285">Você pode compilar em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="dd375-285">You can compile in any order.</span></span> <span data-ttu-id="dd375-286">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dd375-286">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
<span data-ttu-id="dd375-287">Você não precisa recompilar o C. FX na segunda passagem.</span><span class="sxs-lookup"><span data-stu-id="dd375-287">You don't have to recompile C.fx in the second pass.</span></span>

<span data-ttu-id="dd375-288">Depois de executar as duas etapas de compilação anteriores, você pode usar um. o, B. o e o C. o como BLOBs de sombreador final com slots UAV alinhados.</span><span class="sxs-lookup"><span data-stu-id="dd375-288">After you perform the preceding two compilation passes, you can use A.o, B.o, and C.o as final shader blobs with aligned UAV slots.</span></span>

## <a name="profiles"></a><span data-ttu-id="dd375-289">Perfis</span><span class="sxs-lookup"><span data-stu-id="dd375-289">Profiles</span></span>

<span data-ttu-id="dd375-290">Cada modelo de sombreador é rotulado com um perfil HLSL.</span><span class="sxs-lookup"><span data-stu-id="dd375-290">Each shader model is labeled with an HLSL profile.</span></span> <span data-ttu-id="dd375-291">Para compilar um sombreador em um modelo de sombreador específico, escolha o perfil de sombreador apropriado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dd375-291">To compile a shader against a particular shader model, choose the appropriate shader profile from the following table.</span></span>

<table><thead><tr class="header"><th><span data-ttu-id="dd375-292">Tipo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="dd375-292">Shader Type</span></span></th><th><span data-ttu-id="dd375-293">Perfis</span><span class="sxs-lookup"><span data-stu-id="dd375-293">Profiles</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="dd375-294">Sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="dd375-294">Compute Shader</span></span></td><td><dl> <span data-ttu-id="dd375-295">cs_4_0</span><span class="sxs-lookup"><span data-stu-id="dd375-295">cs_4_0</span></span><br />
<span data-ttu-id="dd375-296">cs_4_1</span><span class="sxs-lookup"><span data-stu-id="dd375-296">cs_4_1</span></span><br />
<span data-ttu-id="dd375-297">cs_5_0</span><span class="sxs-lookup"><span data-stu-id="dd375-297">cs_5_0</span></span><br />
<span data-ttu-id="dd375-298">cs_5_1</span><span class="sxs-lookup"><span data-stu-id="dd375-298">cs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="dd375-299">Sombreador de domínio</span><span class="sxs-lookup"><span data-stu-id="dd375-299">Domain Shader</span></span></td><td><dl> <span data-ttu-id="dd375-300">ds_5_0</span><span class="sxs-lookup"><span data-stu-id="dd375-300">ds_5_0</span></span><br />
<span data-ttu-id="dd375-301">ds_5_1</span><span class="sxs-lookup"><span data-stu-id="dd375-301">ds_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="dd375-302">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="dd375-302">Geometry Shader</span></span></td><td><dl> <span data-ttu-id="dd375-303">gs_4_0</span><span class="sxs-lookup"><span data-stu-id="dd375-303">gs_4_0</span></span><br />
<span data-ttu-id="dd375-304">gs_4_1</span><span class="sxs-lookup"><span data-stu-id="dd375-304">gs_4_1</span></span><br />
<span data-ttu-id="dd375-305">gs_5_0</span><span class="sxs-lookup"><span data-stu-id="dd375-305">gs_5_0</span></span><br />
<span data-ttu-id="dd375-306">gs_5_1</span><span class="sxs-lookup"><span data-stu-id="dd375-306">gs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="dd375-307">Vinculação de sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="dd375-307">HLSL shader linking</span></span> </td><td><dl> <span data-ttu-id="dd375-308">lib_4_0</span><span class="sxs-lookup"><span data-stu-id="dd375-308">lib_4_0</span></span><br />
<span data-ttu-id="dd375-309">lib_4_1</span><span class="sxs-lookup"><span data-stu-id="dd375-309">lib_4_1</span></span><br />
<span data-ttu-id="dd375-310">lib_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="dd375-310">lib_4_0_level_9_1</span></span><br />
<span data-ttu-id="dd375-311">lib_4_0_level_9_1_vs_only</span><span class="sxs-lookup"><span data-stu-id="dd375-311">lib_4_0_level_9_1_vs_only</span></span><br />
<span data-ttu-id="dd375-312">lib_4_0_level_9_1_ps_only</span><span class="sxs-lookup"><span data-stu-id="dd375-312">lib_4_0_level_9_1_ps_only</span></span><br />
<span data-ttu-id="dd375-313">lib_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="dd375-313">lib_4_0_level_9_3</span></span><br />
<span data-ttu-id="dd375-314">lib_4_0_level_9_3_vs_only</span><span class="sxs-lookup"><span data-stu-id="dd375-314">lib_4_0_level_9_3_vs_only</span></span><br />
<span data-ttu-id="dd375-315">lib_4_0_level_9_3_ps_only</span><span class="sxs-lookup"><span data-stu-id="dd375-315">lib_4_0_level_9_3_ps_only</span></span><br />
<span data-ttu-id="dd375-316">lib_5_0</span><span class="sxs-lookup"><span data-stu-id="dd375-316">lib_5_0</span></span><br />
</dl> <span data-ttu-id="dd375-317">Para obter mais informações sobre a vinculação de sombreador, consulte <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> e <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dd375-317">For more info about shader linking, see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> and <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span></span> <br/></td></tr><tr class="odd"><td><span data-ttu-id="dd375-318">{1&gt;Sombreador Hull&lt;1}</span><span class="sxs-lookup"><span data-stu-id="dd375-318">Hull Shader</span></span></td><td><dl> <span data-ttu-id="dd375-319">hs_5_0</span><span class="sxs-lookup"><span data-stu-id="dd375-319">hs_5_0</span></span><br />
<span data-ttu-id="dd375-320">hs_5_1</span><span class="sxs-lookup"><span data-stu-id="dd375-320">hs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="dd375-321">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="dd375-321">Pixel Shader</span></span></td><td><dl> <span data-ttu-id="dd375-322">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="dd375-322">ps_2_0</span></span><br />
<span data-ttu-id="dd375-323">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="dd375-323">ps_2_a</span></span><br />
<span data-ttu-id="dd375-324">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="dd375-324">ps_2_b</span></span><br />
<span data-ttu-id="dd375-325">ps_2_sw</span><span class="sxs-lookup"><span data-stu-id="dd375-325">ps_2_sw</span></span><br />
<span data-ttu-id="dd375-326">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="dd375-326">ps_3_0</span></span><br />
<span data-ttu-id="dd375-327">ps_3_sw</span><span class="sxs-lookup"><span data-stu-id="dd375-327">ps_3_sw</span></span><br />
<span data-ttu-id="dd375-328">ps_4_0</span><span class="sxs-lookup"><span data-stu-id="dd375-328">ps_4_0</span></span><br />
<span data-ttu-id="dd375-329">ps_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="dd375-329">ps_4_0_level_9_0</span></span><br />
<span data-ttu-id="dd375-330">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="dd375-330">ps_4_0_level_9_1</span></span><br />
<span data-ttu-id="dd375-331">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="dd375-331">ps_4_0_level_9_3</span></span><br />
<span data-ttu-id="dd375-332">ps_4_1</span><span class="sxs-lookup"><span data-stu-id="dd375-332">ps_4_1</span></span><br />
<span data-ttu-id="dd375-333">ps_5_0</span><span class="sxs-lookup"><span data-stu-id="dd375-333">ps_5_0</span></span><br />
<span data-ttu-id="dd375-334">ps_5_1</span><span class="sxs-lookup"><span data-stu-id="dd375-334">ps_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="dd375-335">Assinatura de raiz</span><span class="sxs-lookup"><span data-stu-id="dd375-335">Root Signature</span></span></td><td><dl> <span data-ttu-id="dd375-336">rootsig_1_0</span><span class="sxs-lookup"><span data-stu-id="dd375-336">rootsig_1_0</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="dd375-337">Sombreador de textura</span><span class="sxs-lookup"><span data-stu-id="dd375-337">Texture Shader</span></span></td><td><dl> <span data-ttu-id="dd375-338">tx_1_0</span><span class="sxs-lookup"><span data-stu-id="dd375-338">tx_1_0</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="dd375-339">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="dd375-339">Vertex Shader</span></span></td><td><dl> <span data-ttu-id="dd375-340">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="dd375-340">vs_1_1</span></span><br />
<span data-ttu-id="dd375-341">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="dd375-341">vs_2_0</span></span><br />
<span data-ttu-id="dd375-342">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="dd375-342">vs_2_a</span></span><br />
<span data-ttu-id="dd375-343">vs_2_sw</span><span class="sxs-lookup"><span data-stu-id="dd375-343">vs_2_sw</span></span><br />
<span data-ttu-id="dd375-344">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="dd375-344">vs_3_0</span></span><br />
<span data-ttu-id="dd375-345">vs_3_sw</span><span class="sxs-lookup"><span data-stu-id="dd375-345">vs_3_sw</span></span><br />
<span data-ttu-id="dd375-346">vs_4_0</span><span class="sxs-lookup"><span data-stu-id="dd375-346">vs_4_0</span></span><br />
<span data-ttu-id="dd375-347">vs_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="dd375-347">vs_4_0_level_9_0</span></span><br />
<span data-ttu-id="dd375-348">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="dd375-348">vs_4_0_level_9_1</span></span><br />
<span data-ttu-id="dd375-349">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="dd375-349">vs_4_0_level_9_3</span></span><br />
<span data-ttu-id="dd375-350">vs_4_1</span><span class="sxs-lookup"><span data-stu-id="dd375-350">vs_4_1</span></span><br />
<span data-ttu-id="dd375-351">vs_5_0</span><span class="sxs-lookup"><span data-stu-id="dd375-351">vs_5_0</span></span><br />
<span data-ttu-id="dd375-352">vs_5_1</span><span class="sxs-lookup"><span data-stu-id="dd375-352">vs_5_1</span></span><br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a><span data-ttu-id="dd375-353">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="dd375-353">Version notes</span></span>

<span data-ttu-id="dd375-354">Para o Direct3D 12, consulte [especificando assinaturas raiz no HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Associação de recursos em HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) e [indexação dinâmica usando HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span><span class="sxs-lookup"><span data-stu-id="dd375-354">For Direct3D 12 refer to [Specifying Root Signatures in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Resource Binding in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) and [Dynamic Indexing using HLSL 5.1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span></span>

<span data-ttu-id="dd375-355">No Direct3D 10, use a API para obter o vértice, a geometria e o perfil do pixel-shader mais adequado para um determinado dispositivo chamando essas funções: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)e [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="dd375-355">In Direct3D 10 use the API to get the vertex, geometry, and pixel-shader profile best suited to a given device by calling these functions: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile), and [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span></span>

<span data-ttu-id="dd375-356">No Direct3D 9, use os métodos [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) ou [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) para recuperar os perfis de vértice e pixel shader com suporte de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd375-356">In Direct3D 9 use the [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) or [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) methods to retrieve the vertex and pixel-shader profiles supported by a device.</span></span> <span data-ttu-id="dd375-357">A estrutura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) retornada por esses métodos indica os perfis de vértice e pixel shader com suporte de um dispositivo em seus membros **VertexShaderVersion** e **PixelShaderVersion** .</span><span class="sxs-lookup"><span data-stu-id="dd375-357">The [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure returned by those methods indicates the vertex and pixel-shader profiles supported by a device in its **VertexShaderVersion** and **PixelShaderVersion** members.</span></span>

<span data-ttu-id="dd375-358">Para obter exemplos, consulte [compilando com o compilador atual](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="dd375-358">For examples, see [Compiling with the Current Compiler](dx-graphics-tools-fxc-using.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd375-359">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd375-359">Related topics</span></span>

* [<span data-ttu-id="dd375-360">Efeito-ferramenta do compilador</span><span class="sxs-lookup"><span data-stu-id="dd375-360">Effect-Compiler Tool</span></span>](fxc.md)