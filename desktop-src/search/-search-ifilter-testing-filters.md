---
description: O conjunto de testes do IFilter valida seus manipuladores de filtro.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Testando manipuladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090078"
---
# <a name="testing-filter-handlers"></a><span data-ttu-id="7aa0d-103">Testando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="7aa0d-103">Testing Filter Handlers</span></span>

<span data-ttu-id="7aa0d-104">O conjunto de testes do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) valida seus manipuladores de filtro.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-104">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite validates your filter handlers.</span></span> <span data-ttu-id="7aa0d-105">O conjunto de testes faz isso: chamando métodos [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e verificando os valores retornados quanto à conformidade com a especificação da interface **IFilter** ; e verificar se os identificadores de partes são exclusivos e crescentes, se a interface do **IFilter** se comporta consistentemente após a reinicialização e se as chamadas de método **IFilter** com parâmetros inválidos retornam os códigos de erro esperados.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-105">The test suite does so by: calling [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) methods and checking the returned values for compliance with the **IFilter** interface specification; and checking that chunk identifiers are unique and increasing, that the **IFilter** interface behaves consistently after re-initialization, and that any **IFilter** method calls with invalid parameters return expected error codes.</span></span> <span data-ttu-id="7aa0d-106">Os programas do conjunto de testes também despejam a saída de um arquivo filtrado por um manipulador de filtro e verificam as informações de registro do **IFilter** no registro.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-106">The test suite programs also dump the output of a file filtered by a filter handler, and check the **IFilter** registration information in the registry.</span></span>

<span data-ttu-id="7aa0d-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7aa0d-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="7aa0d-108">Invocação de linha de comando</span><span class="sxs-lookup"><span data-stu-id="7aa0d-108">Command-Line Invocation</span></span>](#command-line-invocation)
  - [<span data-ttu-id="7aa0d-109">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="7aa0d-109">ifilttst.exe</span></span>](#ifilttstexe)
  - [<span data-ttu-id="7aa0d-110">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="7aa0d-110">filtdump.exe</span></span>](#filtdumpexe)
  - [<span data-ttu-id="7aa0d-111">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="7aa0d-111">filtreg.exe</span></span>](#filtregexe)
  - [<span data-ttu-id="7aa0d-112">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="7aa0d-112">ifilttst.ini</span></span>](#ifilttstini)
- [<span data-ttu-id="7aa0d-113">Procedimento de teste do IFilter</span><span class="sxs-lookup"><span data-stu-id="7aa0d-113">IFilter Test Procedure</span></span>](#ifilter-test-procedure)
  - [<span data-ttu-id="7aa0d-114">Teste de validação</span><span class="sxs-lookup"><span data-stu-id="7aa0d-114">Validation Test</span></span>](#validation-test)
  - [<span data-ttu-id="7aa0d-115">Teste de consistência</span><span class="sxs-lookup"><span data-stu-id="7aa0d-115">Consistency Test</span></span>](#consistency-test)
  - [<span data-ttu-id="7aa0d-116">Teste de entrada inválido</span><span class="sxs-lookup"><span data-stu-id="7aa0d-116">Invalid Input Test</span></span>](#invalid-input-test)
  - [<span data-ttu-id="7aa0d-117">Testando diferentes configurações de IFilter</span><span class="sxs-lookup"><span data-stu-id="7aa0d-117">Testing Different IFilter Configurations</span></span>](#testing-different-ifilter-configurations)
- [<span data-ttu-id="7aa0d-118">Garantindo que os itens registrados sejam indexados</span><span class="sxs-lookup"><span data-stu-id="7aa0d-118">Ensuring Registered Items Get Indexed</span></span>](#ensuring-registered-items-get-indexed)
  - [<span data-ttu-id="7aa0d-119">Arquivo de log de exemplo</span><span class="sxs-lookup"><span data-stu-id="7aa0d-119">Sample Log File</span></span>](#sample-log-file)
  - [<span data-ttu-id="7aa0d-120">Exemplo de arquivo de despejo</span><span class="sxs-lookup"><span data-stu-id="7aa0d-120">Sample Dump File</span></span>](#sample-dump-file)
- [<span data-ttu-id="7aa0d-121">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7aa0d-121">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="7aa0d-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7aa0d-122">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="7aa0d-123">Se um novo manipulador de filtro para um tipo de arquivo estiver sendo instalado como uma substituição para um registro de filtro existente, o instalador deverá salvar o registro atual e restaurá-lo se o novo manipulador de filtro for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="7aa0d-124">Não há nenhum mecanismo para encadear filtros.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="7aa0d-125">Portanto, o novo manipulador de filtro é responsável por replicar qualquer funcionalidade necessária do filtro antigo.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="command-line-invocation"></a><span data-ttu-id="7aa0d-126">Invocação de Command-Line</span><span class="sxs-lookup"><span data-stu-id="7aa0d-126">Command-Line Invocation</span></span>

<span data-ttu-id="7aa0d-127">O conjunto de testes do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) consiste em três aplicativos de linha de comando – [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)e [filtreg.exe](#filtregexe) e um arquivo de inicialização [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-127">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite consists of three command-line applications - [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe), and [filtreg.exe](#filtregexe) and an initialization file, [ifilttst.ini](#ifilttstini).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7aa0d-128">No Windows 7 e posterior, os filtros gravados em código gerenciado são explicitamente bloqueados.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-128">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="7aa0d-129">Os filtros devem ser escritos em código nativo devido a problemas de controle de versão do CLR (Common Language Runtime potencial) com o processo em que vários suplementos são executados.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-129">Filters MUST be written in native code due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="ifilttstexe"></a><span data-ttu-id="7aa0d-130">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="7aa0d-130">ifilttst.exe</span></span>

<span data-ttu-id="7aa0d-131">O programa de ifilttst.exe executa vários testes para validar um manipulador de filtro.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-131">The ifilttst.exe program runs several tests to validate a filter handler.</span></span> <span data-ttu-id="7aa0d-132">O exemplo a seguir ilustra como invocar o programa de ifilttst.exe da linha de comando:</span><span class="sxs-lookup"><span data-stu-id="7aa0d-132">The following example illustrates how to invoke the ifilttst.exe program from the command line:</span></span>


```
ifilttst /i test.htm /l /d /v 1
```

<span data-ttu-id="7aa0d-133">O exemplo executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="7aa0d-133">The example performs the following tasks:</span></span>

- <span data-ttu-id="7aa0d-134">Direciona o programa para filtrar o arquivo test.htm</span><span class="sxs-lookup"><span data-stu-id="7aa0d-134">Directs the program to filter the file test.htm</span></span>
- <span data-ttu-id="7aa0d-135">Redireciona as mensagens de log para test.htm. log</span><span class="sxs-lookup"><span data-stu-id="7aa0d-135">Redirects the log messages to test.htm.log</span></span>
- <span data-ttu-id="7aa0d-136">Redireciona as mensagens de despejo para test.htm. dmp</span><span class="sxs-lookup"><span data-stu-id="7aa0d-136">Redirects the dump messages to test.htm.dmp</span></span>
- <span data-ttu-id="7aa0d-137">Define o detalhamento como 1</span><span class="sxs-lookup"><span data-stu-id="7aa0d-137">Sets the verbosity to 1</span></span>

<span data-ttu-id="7aa0d-138">Para que o comando anterior funcione, três arquivos devem estar localizados no diretório de trabalho atual: `test.htm` , [ifilttst.exe](#ifilttstexe)e [ifilttst.ini](#ifilttstini).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-138">For the preceding command to work, three files must be located in the current working directory: `test.htm`, [ifilttst.exe](#ifilttstexe), and [ifilttst.ini](#ifilttstini).</span></span> <span data-ttu-id="7aa0d-139">As opções de linha de comando são listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-139">Command-line switches are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aa0d-140">Switch e variáveis possíveis</span><span class="sxs-lookup"><span data-stu-id="7aa0d-140">Switch and possible variables</span></span></th>
<th><span data-ttu-id="7aa0d-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aa0d-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7aa0d-142"><strong>/i nome do arquivo</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0d-142"><strong>/i file name</strong></span></span></td>
<td><span data-ttu-id="7aa0d-143">O arquivo ou diretório de entrada a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-143">The input file or directory to be filtered.</span></span> <span data-ttu-id="7aa0d-144">O nome do arquivo pode conter os caracteres curinga <code>\*</code> e <code>?</code> .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-144">The file name can contain the wildcard characters <code>\*</code> and <code>?</code>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aa0d-145"><strong>/l</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0d-145"><strong>/l</strong></span></span></td>
<td><span data-ttu-id="7aa0d-146">As mensagens de log são direcionadas para um arquivo em vez da tela.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-146">Log messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="7aa0d-147">As mensagens de log descrevem os testes individuais executados e os resultados de aprovação/reprovação dos testes.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-147">Log messages describe the individual tests performed and the pass/fail results of the tests.</span></span> <span data-ttu-id="7aa0d-148">O nome do arquivo de log é o mesmo que o nome do arquivo de entrada, mas com uma extensão. log.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-148">The log file name is the same as the input file name but with a .log extension.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aa0d-149"><strong>/d</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0d-149"><strong>/d</strong></span></span></td>
<td><span data-ttu-id="7aa0d-150">Mensagens de despejo são direcionadas para um arquivo em vez da tela.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-150">Dump messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="7aa0d-151">Mensagens de despejo descrevem o conteúdo das partes.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-151">Dump messages describe the contents of the chunks.</span></span> <span data-ttu-id="7aa0d-152">A estrutura da parte é despejada quando o nível de detalhes é 3.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-152">The chunk structure is dumped when the verbosity level is 3.</span></span> <span data-ttu-id="7aa0d-153">O nome do arquivo de despejo é o mesmo que o nome do arquivo de entrada, mas com uma extensão. dmp.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-153">The dump file name is the same as the input file name but with a .dmp extension.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aa0d-154"><strong>/-l</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0d-154"><strong>/-l</strong></span></span></td>
<td><span data-ttu-id="7aa0d-155">Desabilite o registro em log.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-155">Disable logging.</span></span> <span data-ttu-id="7aa0d-156">Esse sinalizador substitui a <code>/l</code> opção.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-156">This flag overrides the <code>/l</code> switch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aa0d-157"><strong>/-d</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0d-157"><strong>/-d</strong></span></span></td>
<td><span data-ttu-id="7aa0d-158">Desabilitar despejo.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-158">Disable dumping.</span></span> <span data-ttu-id="7aa0d-159">Esse sinalizador substitui a <code>/d</code> opção.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-159">This flag overrides the <code>/d</code> switch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aa0d-160"><strong>/v inteiro</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0d-160"><strong>/v integer</strong></span></span></td>
<td><span data-ttu-id="7aa0d-161">O nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-161">The verbosity level.</span></span> <span data-ttu-id="7aa0d-162">O padrão é 3.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-162">The default is 3.</span></span>
<ul>
<li><span data-ttu-id="7aa0d-163">0-o teste registra somente as mensagens relacionadas a falhas de interface <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> específicas.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-163">0 - The test logs only messages concerning specific <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> interface failures.</span></span> <span data-ttu-id="7aa0d-164">O teste despeja o conteúdo da parte.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-164">The test dumps the chunk contents.</span></span></li>
<li><span data-ttu-id="7aa0d-165">1-o teste Registra mensagens de aviso, bem como aquelas para o nível 0.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-165">1 - The test logs warning messages as well as those for level 0.</span></span></li>
<li><span data-ttu-id="7aa0d-166">2-o teste registra as mensagens relacionadas a testes que passaram e para o nível 1.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-166">2 - The test logs messages concerning tests that passed as well as those for level 1.</span></span></li>
<li><span data-ttu-id="7aa0d-167">3-o teste Registra mensagens informativas, bem como aquelas para o nível 2.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-167">3 - The test logs informational messages as well as those for level 2.</span></span> <span data-ttu-id="7aa0d-168">Além disso, o teste despeja a estrutura da parte.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-168">In addition, the test dumps the structure of the chunk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aa0d-169"><strong>/t inteiro</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0d-169"><strong>/t integer</strong></span></span></td>
<td><span data-ttu-id="7aa0d-170">O número de threads a serem iniciados.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-170">The number of threads to launch.</span></span> <span data-ttu-id="7aa0d-171">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-171">The default is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aa0d-172"><strong>/r inteiro</strong>]</span><span class="sxs-lookup"><span data-stu-id="7aa0d-172"><strong>/r integer</strong>]</span></span></td>
<td><span data-ttu-id="7aa0d-173">Filtra recursivamente os subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-173">Recursively filters subdirectories.</span></span> <span data-ttu-id="7aa0d-174">O parâmetro inteiro opcional especifica a profundidade para a recursão de exercício.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-174">The optional integer parameter specifies the depth to which to exercise recursion.</span></span> <span data-ttu-id="7aa0d-175">Se nenhum inteiro for especificado, ou se o inteiro for 0, a recursão completa será assumida.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-175">If no integer is specified, or if the integer is 0, full recursion is assumed.</span></span> <span data-ttu-id="7aa0d-176">Por padrão, a profundidade da recursão é 1.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-176">By default, the recursion depth is 1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aa0d-177"><strong>/c inteiro</strong></span><span class="sxs-lookup"><span data-stu-id="7aa0d-177"><strong>/c integer</strong></span></span></td>
<td><span data-ttu-id="7aa0d-178">O número de vezes para o loop.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-178">The number of times to loop.</span></span> <span data-ttu-id="7aa0d-179">Se o inteiro for 0, o teste fará o loop infinitamente.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-179">If the integer is 0, the test loops infinitely.</span></span> <span data-ttu-id="7aa0d-180">Por padrão, o teste executa um loop apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-180">By default, the test loops only once.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]  
> <span data-ttu-id="7aa0d-181">Você deve incluir um espaço entre a opção de linha de comando e o valor.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-181">You must include a space between the command line switch and the value.</span></span>

### <a name="filtdumpexe"></a><span data-ttu-id="7aa0d-182">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="7aa0d-182">filtdump.exe</span></span>

<span data-ttu-id="7aa0d-183">O programa filtdump.exe carrega um manipulador de filtro para um documento especificado e imprime a saída produzida pela DLL do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-183">The filtdump.exe program loads a filter handler for a specified document and prints the output produced by the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL.</span></span> <span data-ttu-id="7aa0d-184">O exemplo a seguir ilustra como invocar o programa filtdump.exe.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-184">The following example illustrates how to invoke the filtdump.exe program.</span></span>

```
filtdump filename.ext
```
<span data-ttu-id="7aa0d-185">Filtdump.exe usa o método [ILoadFilter:: loadifilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) para carregar a DLL do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) apropriada para a extensão de nome de arquivo especificada e imprime os resultados.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-185">Filtdump.exe uses the [ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) method to load the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL appropriate for the specified file name extension and prints the results.</span></span> <span data-ttu-id="7aa0d-186">Por exemplo, o comando a seguir instrui filtdump.exe a carregar o manipulador de filtro de smpfilt.dll para a extensão. SMP, extrair todo o texto e as propriedades do arquivo MyFile. SMP e imprimir os resultados.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-186">For example, the following command instructs filtdump.exe to load the smpfilt.dll filter handler for the extension .smp, extract all text and properties from the file myfile.smp, and print the results.</span></span>

```
filtdump myfile.smp
```

### <a name="filtregexe"></a><span data-ttu-id="7aa0d-187">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="7aa0d-187">filtreg.exe</span></span>

<span data-ttu-id="7aa0d-188">O programa de filtreg.exe inspeciona as informações de instalação do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no registro.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-188">The filtreg.exe program inspects [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) installation information in the registry.</span></span> <span data-ttu-id="7aa0d-189">Você invoca o programa filtreg.exe na linha de comando, digitando seu nome, como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-189">You invoke the filtreg.exe program from the command line by typing its name, as in the following example.</span></span>

```
filtreg
```

<span data-ttu-id="7aa0d-190">Filtreg.exe enumera todas as extensões de nome de arquivo que têm manipuladores de filtro associados a elas, imprimindo a extensão de nome de arquivo e o nome da dll do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para a extensão.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-190">Filtreg.exe enumerates all file name extensions that have filter handlers associated with them by printing the file name extension and the name of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL for the extension.</span></span> <span data-ttu-id="7aa0d-191">Essa é uma maneira simples de verificar a instalação correta de um **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-191">This is a simple way to verify the correct installation of an **IFilter**.</span></span>

### <a name="ifilttstini"></a><span data-ttu-id="7aa0d-192">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="7aa0d-192">ifilttst.ini</span></span>

<span data-ttu-id="7aa0d-193">Uma interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é inicializada chamando o método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-193">An [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface is initialized by calling the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="7aa0d-194">O método **IFilter:: init** usa os quatro parâmetros a seguir:</span><span class="sxs-lookup"><span data-stu-id="7aa0d-194">The **IFilter::Init** method takes the following four parameters:</span></span>

1. <span data-ttu-id="7aa0d-195">*grfFlags*</span><span class="sxs-lookup"><span data-stu-id="7aa0d-195">*grfFlags*</span></span>
2. <span data-ttu-id="7aa0d-196">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="7aa0d-196">*cAttributes*</span></span>
3. <span data-ttu-id="7aa0d-197">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="7aa0d-197">*aAttributes*</span></span>
4. <span data-ttu-id="7aa0d-198">*pdwFlags*</span><span class="sxs-lookup"><span data-stu-id="7aa0d-198">*pdwFlags*</span></span>

<span data-ttu-id="7aa0d-199">O usuário do programa de ifilttst.exe do conjunto de testes do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pode especificar os valores para esses parâmetros em um arquivo chamado ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-199">The user of the ifilttst.exe program of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite can specify the values for these parameters in a file called ifilttst.ini.</span></span> <span data-ttu-id="7aa0d-200">A tabela a seguir descreve as entradas no arquivo de ifilttst.ini que especificam os três primeiros parâmetros (os parâmetros de entrada).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-200">The following table describes the entries in the ifilttst.ini file that specify the first three parameters(the input parameters).</span></span> <span data-ttu-id="7aa0d-201">Para obter um arquivo de exemplo, consulte [arquivo de ifilttst.ini de exemplo](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-201">For a sample file, see [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span>

> [!NOTE]  
> <span data-ttu-id="7aa0d-202">Não há nenhuma entrada de tabela para o parâmetro *pdwFlags* porque ele é um parâmetro de saída; Ele não precisa ter nenhum valor especial antes da chamada para o método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-202">There is no table entry for the *pdwFlags* parameter because it is an output parameter; it does not need to have any special value prior to the call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

 | <span data-ttu-id="7aa0d-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="7aa0d-203">Entry</span></span>         | <span data-ttu-id="7aa0d-204">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aa0d-204">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa0d-205">Flags</span><span class="sxs-lookup"><span data-stu-id="7aa0d-205">Flags</span></span>         | <span data-ttu-id="7aa0d-206">Os nomes dos sinalizadores [**de \_ inicialização do IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) que devem ser Unidos pelo operador OR para formar o parâmetro *grfFlags* do método [**IFILTER:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-206">The names of the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) flags that are to be joined by the OR operator to form the *grfFlags* parameter of the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="7aa0d-207">Os nomes dos sinalizadores devem estar em letras maiúsculas e na mesma linha.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-207">The flag names must all be uppercase, and on the same line.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7aa0d-208">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="7aa0d-208">*cAttributes*</span></span> | <span data-ttu-id="7aa0d-209">Um inteiro decimal que representa o valor do parâmetro *cAttributes* .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-209">A decimal integer representing the value of the *cAttributes* parameter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7aa0d-210">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="7aa0d-210">*aAttributes*</span></span> | <span data-ttu-id="7aa0d-211">Essa entrada deve começar com *aAttributes* e deve ser diferente das outras entradas de *aAttributes* na seção.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-211">This entry must start with *aAttributes* and must be different from the other *aAttributes* entries within the section.</span></span> <span data-ttu-id="7aa0d-212">Os nomes válidos para a entrada *aAttributes* são: *aAttributes*, *aAttributes1*, *aAttributes2* e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-212">Legal names for the *aAttributes* entry are: *aAttributes*, *aAttributes1*, *aAttributes2*, and so forth.</span></span> <span data-ttu-id="7aa0d-213">O primeiro token deve ser um GUID.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-213">The first token must be a GUID.</span></span> <span data-ttu-id="7aa0d-214">O GUID deve ser formatado exatamente conforme ilustrado na `[Test3]` seção do [arquivo de ifilttst.ini de exemplo](#sample-ifilttstini-file).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-214">The GUID must be formatted exactly as illustrated in the `[Test3]` section of the [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span> <span data-ttu-id="7aa0d-215">O segundo token pode ser um identificador de propriedade (PID) que consiste em um número em notação hexadecimal ou um ponteiro para uma grande cadeia de caracteres (LPWSTR).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-215">The second token can be either a property identifier (PID) consisting of a number in hexadecimal notation, or a pointer to a wide character string (lpwstr).</span></span> <span data-ttu-id="7aa0d-216">Um LPWStr pode ser especificado ao colocar a cadeia de caracteres entre aspas duplas, conforme ilustrado na `[Test6]` seção do arquivo de ifilttst.ini de exemplo.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-216">A lpwstr can be specified by enclosing the string in double quotes, as illustrated in the `[Test6]` section of the Sample ifilttst.ini File.</span></span> |

<span data-ttu-id="7aa0d-217">Se as entradas flags e *cAttributes* não forem especificadas, elas serão padronizadas como 0.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-217">If the Flags and *cAttributes* entries are not specified, they default to 0.</span></span> <span data-ttu-id="7aa0d-218">Se você definir *cAttributes* igual a 2, deverá especificar dois nomes de *aAttributes* .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-218">If you set *cAttributes* equal to 2, you should specify two *aAttributes* names.</span></span> <span data-ttu-id="7aa0d-219">Na `[Test5]` seção do exemplo, *cAttributes* é 1, mas nenhum *aAttributes* foi especificado.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-219">In the `[Test5]` section of the sample, *cAttributes* is 1, but no *aAttributes* have been specified.</span></span> <span data-ttu-id="7aa0d-220">Em seguida, o teste chama o método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) com *cAttributes* igual a 1 e *aAttributes* igual a **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-220">The test then calls the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method with *cAttributes* equal to 1 and *aAttributes* equal to **NULL**.</span></span> <span data-ttu-id="7aa0d-221">Esse é um caso de teste útil porque provavelmente causará uma violação de acesso no método **IFilter:: init** .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-221">This is a useful test case because it is likely to cause an access violation in the **IFilter::Init** method.</span></span>

<span data-ttu-id="7aa0d-222">Se ifilttst.exe não conseguir encontrar um arquivo chamado ifilttst.ini no diretório de trabalho, uma configuração padrão será usada para inicializar o objeto [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-222">If ifilttst.exe cannot find a file named ifilttst.ini in the working directory, a default configuration is used to initialize the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) object.</span></span> <span data-ttu-id="7aa0d-223">O exemplo a seguir ilustra a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-223">The following example illustrates the default configuration.</span></span>

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a><span data-ttu-id="7aa0d-224">Arquivo de ifilttst.ini de exemplo</span><span class="sxs-lookup"><span data-stu-id="7aa0d-224">Sample ifilttst.ini File</span></span>

<span data-ttu-id="7aa0d-225">O arquivo de ifilttst.ini é organizado em seções, com o nome da seção entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-225">The ifilttst.ini file is organized in sections, with the section name enclosed in square brackets.</span></span> <span data-ttu-id="7aa0d-226">No exemplo, as seções são nomeadas `[Test1]` , `[Test2]` e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-226">In the example, the sections are named `[Test1]`, `[Test2]`, and so forth.</span></span> <span data-ttu-id="7aa0d-227">Todos os nomes de seção devem ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-227">All section names must be unique.</span></span> <span data-ttu-id="7aa0d-228">O teste lê os valores da primeira seção e inicializa o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) com esses valores.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-228">The test reads the values from the first section and initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) with those values.</span></span> <span data-ttu-id="7aa0d-229">Em seguida, todos os testes são executados usando essa configuração de **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-229">Then all the tests are run using this **IFilter** configuration.</span></span> <span data-ttu-id="7aa0d-230">Em seguida, o **IFilter** é liberado e reinicializado, usando parâmetros listados acima.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-230">Then the **IFilter** is released and reinitialized, using parameters that are listed above.</span></span> <span data-ttu-id="7aa0d-231">O processo é repetido até que todas as configurações sejam testadas.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-231">The process is repeated until all configurations are tested.</span></span>

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a><span data-ttu-id="7aa0d-232">Procedimento de teste do IFilter</span><span class="sxs-lookup"><span data-stu-id="7aa0d-232">IFilter Test Procedure</span></span>

<span data-ttu-id="7aa0d-233">Depois que o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) tiver sido inicializado, o programa de ifilttst.exe conduzirá uma série de testes no **IFilter**.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-233">After the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) has been initialized, the ifilttst.exe program conducts a series of tests on the **IFilter**.</span></span> <span data-ttu-id="7aa0d-234">Além de seguir os procedimentos de teste do **IFilter** , certifique-se de que sua implementação do **IFilter** empregue práticas de código seguras.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-234">In addition to following the **IFilter** test procedures, ensure that your **IFilter** implementation employs secure code practices.</span></span> <span data-ttu-id="7aa0d-235">Consulte "práticas de código de segurança para o Windows Search" em [implementando manipuladores de filtro no Windows Search](-search-ifilter-constructing-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-235">See "Secure Code Practices for Windows Search" in [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md).</span></span>

### <a name="validation-test"></a><span data-ttu-id="7aa0d-236">Teste de validação</span><span class="sxs-lookup"><span data-stu-id="7aa0d-236">Validation Test</span></span>

<span data-ttu-id="7aa0d-237">O teste de validação percorre o objeto uma parte por vez, verificando cada parte individual e todos os códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-237">The validation test steps through the object one chunk at a time, verifying each individual chunk and all return codes.</span></span> <span data-ttu-id="7aa0d-238">O teste de validação salva todas as estruturas de [**\_ partes de estatística**](/windows/win32/api/filter/ns-filter-stat_chunk) retornadas em uma lista.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-238">The validation test saves all returned [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structures in a list.</span></span>

<span data-ttu-id="7aa0d-239">O teste de validação verifica as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="7aa0d-239">The validation test verifies the following conditions:</span></span>

- <span data-ttu-id="7aa0d-240">A [**\_ parte de stat**](/windows/win32/api/filter/ns-filter-stat_chunk).\*\* as IDs de partes do idChunk devem ser exclusivas e crescentes.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-240">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunk* chunk IDs must be unique and increasing.</span></span>
- <span data-ttu-id="7aa0d-241">A [**\_ parte de stat**](/windows/win32/api/filter/ns-filter-stat_chunk).\*\* o parâmetro flags é um estado de parte reconhecido, como o [**bloco**](/windows/win32/api/filter/ne-filter-chunkstate)de partes, o texto da parte \_ ou as constantes de valor CenabledHUNK \_ .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-241">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*flags* parameter is a recognized chunk state, such as [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), CHUNK\_TEXT, or CenabledHUNK\_VALUE constants.</span></span>
- <span data-ttu-id="7aa0d-242">A [**\_ parte de stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*o parâmetro breaktype* é um tipo de quebra reconhecido (0, 1, 2, 3, 4).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-242">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*breakType* parameter is a recognized break type (0, 1, 2, 3, 4).</span></span>
- <span data-ttu-id="7aa0d-243">Se os atributos de inicialização do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) especificarem que o **IFilter** deve retornar apenas partes que contêm propriedades de tipo de valor interno, *idChunkSource* deverá ser igual a 0.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-243">If the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialization attributes specify that the **IFilter** should return only chunks containing internal value-type properties, then *idChunkSource* must equal 0.</span></span>
- <span data-ttu-id="7aa0d-244">Se a parte não for derivada, isto é, se não for uma propriedade de tipo de valor interno, então a [**\_ parte de stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* deve ser igual à **\_ parte de stat**.*idChunk*.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-244">If the chunk is not derived that is, if it is not an internal value-type property, then [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* must equal **STAT\_CHUNK**.*idChunk*.</span></span>
- <span data-ttu-id="7aa0d-245">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retorna S \_ OK ou outro valor de retorno aceitável, como filtrar \_ e \_ terminar \_ de \_ partes, filtrar \_ e \_ vincular \_ não disponível e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-245">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>
- <span data-ttu-id="7aa0d-246">Se a parte contiver texto, [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornará s \_ OK, filtre o \_ \_ último \_ texto ou filtre \_ E \_ não \_ mais \_ texto.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-246">If the chunk contains text, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns S\_OK, FILTER\_S\_LAST\_TEXT, or FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="7aa0d-247">Se [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornar o filtro \_ S \_ Last Text \_ , a próxima chamada para **IFILTER:: gettext** retornará Filter \_ E \_ não \_ mais \_ texto.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-247">If [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_S\_LAST\_TEXT, the next call to **IFilter::GetText** returns FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="7aa0d-248">Se a parte contiver um valor, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retornará S \_ OK ou filtrar \_ E \_ não \_ mais \_ valores.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-248">If the chunk contains a value, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns S\_OK or FILTER\_E\_NO\_MORE\_VALUES.</span></span>

### <a name="consistency-test"></a><span data-ttu-id="7aa0d-249">Teste de consistência</span><span class="sxs-lookup"><span data-stu-id="7aa0d-249">Consistency Test</span></span>

<span data-ttu-id="7aa0d-250">O programa ifilttxt.exe reinicializa a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) com os mesmos parâmetros do teste de validação e executa um teste de consistência.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-250">The ifilttxt.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters as in the validation test and performs a consistency test.</span></span> <span data-ttu-id="7aa0d-251">Se a implementação do **IFilter** tiver sido inicializada com o sinalizador [**IFilter \_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFilter \_ init \_ somente a indexação \_ , o teste liberará a interface **IFilter** e a associará novamente antes de fazer outra chamada para o método [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-251">If the **IFilter** implementation has been initialized with the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFILTER\_INIT\_INDEXING\_ONLY flag, the test releases the **IFilter** interface and re-binds it before making another call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

<span data-ttu-id="7aa0d-252">O teste de consistência verifica as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="7aa0d-252">The consistency test verifies the following conditions:</span></span>

- <span data-ttu-id="7aa0d-253">Cada estrutura de [**\_ parte de estatística**](/windows/win32/api/filter/ns-filter-stat_chunk) retornada pelo método [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) é idêntica à **\_ parte de stat** correspondente retornada no teste de validação.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-253">Each [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structure returned by the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method is identical to the corresponding **STAT\_CHUNK** returned in the validation test.</span></span>
- <span data-ttu-id="7aa0d-254">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retorna S \_ OK ou outro valor de retorno aceitável, como filtrar \_ e \_ terminar \_ de \_ partes, filtrar \_ e \_ vincular \_ não disponível e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-254">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>

### <a name="invalid-input-test"></a><span data-ttu-id="7aa0d-255">Teste de entrada inválido</span><span class="sxs-lookup"><span data-stu-id="7aa0d-255">Invalid Input Test</span></span>

<span data-ttu-id="7aa0d-256">O programa ifilttst.exe reinicializa a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) com os mesmos parâmetros e executa um teste de entrada inválido.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-256">The ifilttst.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters,and performs an invalid input test.</span></span> <span data-ttu-id="7aa0d-257">Este teste percorre o documento uma parte de cada vez fazendo chamadas de função incorretamente, como chamar o método [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) quando o Chuck atual contiver texto.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-257">This test steps through the document one chunk at a time making function calls incorrectly, such as calling the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method when the current chuck contains text.</span></span> <span data-ttu-id="7aa0d-258">O teste verifica todos os códigos de retorno quanto à conformidade com a especificação do **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-258">The test checks all return codes for compliance with the **IFilter** specification.</span></span>

<span data-ttu-id="7aa0d-259">O teste de entrada inválido verifica as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="7aa0d-259">The invalid input test verifies the following conditions:</span></span>

- <span data-ttu-id="7aa0d-260">Se a parte atual contiver texto, [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retornará \_ um filtro e \_ nenhum valor \_ , e uma chamada para [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-260">If the current chunk contains text, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns FILTER\_E\_NO\_VALUES, and a call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) succeeds.</span></span>
- <span data-ttu-id="7aa0d-261">Se a parte atual contiver um valor, [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornará Filter \_ E \_ nenhum \_ texto e uma chamada para [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-261">If the current chunk contains a value, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_E\_NO\_TEXT, and a call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) succeeds.</span></span>
- <span data-ttu-id="7aa0d-262">Se a chamada anterior para [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornou \_ um filtro e \_ não \_ mais \_ texto, chamadas sucessivas para **IFilter:: gettext** retornarão o filtro \_ e \_ não \_ mais \_ texto.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-262">If the previous call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returned FILTER\_E\_NO\_MORE\_TEXT, successive calls to **IFilter::GetText** return FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="7aa0d-263">Se a chamada anterior para [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retornou \_ um filtro e \_ não \_ mais \_ valores, as chamadas sucessivas para **IFilter:: GetValue** retornarão o filtro \_ e \_ não \_ mais \_ valores.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-263">If the previous call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returned FILTER\_E\_NO\_MORE\_VALUES, successive calls to **IFilter::GetValue** return FILTER\_E\_NO\_MORE\_VALUES.</span></span>
- <span data-ttu-id="7aa0d-264">Se a chamada anterior para [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retornou o filtro \_ e o \_ final \_ de \_ partes, chamadas sucessivas para **IFilter:: GetChunk** filtro \_ de retorno e \_ final \_ das \_ partes.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-264">If the previous call to [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returned FILTER\_E\_END\_OF\_CHUNKS, successive calls to **IFilter::GetChunk** return FILTER\_E\_END\_OF\_CHUNKS.</span></span>

> [!NOTE]  
> <span data-ttu-id="7aa0d-265">O teste de entrada inválido compara as estruturas de partes atuais com as retornadas no teste de validação para garantir que elas sejam idênticas.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-265">The invalid input test compares the current chunk structures to those returned in the validation test to make sure they are identical.</span></span>

### <a name="testing-different-ifilter-configurations"></a><span data-ttu-id="7aa0d-266">Testando diferentes configurações de IFilter</span><span class="sxs-lookup"><span data-stu-id="7aa0d-266">Testing Different IFilter Configurations</span></span>

<span data-ttu-id="7aa0d-267">O programa ifilttst.exe libera a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e religa, desta vez inicializando-a com o próximo conjunto de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-267">The ifilttst.exe program releases the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface and rebinds, this time initializing it with the next set of parameters.</span></span> <span data-ttu-id="7aa0d-268">O teste repete o ciclo: teste de validação, teste de consistência e teste de entrada inválido, até que todas as configurações de **IFilter** desejadas especificadas no arquivo de [ifilttst.ini](#ifilttstini) tenham sido testadas.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-268">The test repeats the cycle: validation test, consistency test, and invalid input test, until all the desired **IFilter** configurations specified in [ifilttst.ini](#ifilttstini) file have been tested.</span></span>

## <a name="ensuring-registered-items-get-indexed"></a><span data-ttu-id="7aa0d-269">Garantindo que os itens registrados sejam indexados</span><span class="sxs-lookup"><span data-stu-id="7aa0d-269">Ensuring Registered Items Get Indexed</span></span>

<span data-ttu-id="7aa0d-270">O teste final de seu [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garante que o **IFilter** seja registrado corretamente e que seja invocado para indexar os itens que você registrou para usá-lo.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-270">The final test of your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ensures that your **IFilter** is properly registered and that it is invoked to index the items that you registered to use it.</span></span> <span data-ttu-id="7aa0d-271">Você pode usar o Gerenciador de catálogo para iniciar a reindexação ou usar o Gerenciador de escopo de rastreamento (CSM) para configurar as regras padrão que indicam as URLs que você deseja que o indexador rastreie.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-271">You can use the Catalog Manager to initiate re-indexing, or use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl.</span></span> <span data-ttu-id="7aa0d-272">Após a conclusão da indexação, use a interface do usuário do Windows Search para procurar uma cadeia de caracteres no conteúdo ou nas propriedades de itens.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-272">After indexing is complete, use the Windows Search UI to search for a string in the content or properties of items.</span></span> <span data-ttu-id="7aa0d-273">Se os itens foram indexados, eles serão exibidos nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-273">If the items were indexed, they will appear in the search results.</span></span>

<span data-ttu-id="7aa0d-274">Para obter mais informações sobre a reindexação, consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-274">For more information about re-indexing, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span> <span data-ttu-id="7aa0d-275">O exemplo de código ReindexMatchingUrls demonstra maneiras de especificar quais arquivos reindexar e como.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-275">The ReindexMatchingUrls code sample demonstrates ways to specify which files to re-index and how.</span></span> <span data-ttu-id="7aa0d-276">O exemplo de código CrawlScopeCommandLine demonstra como definir opções de linha de comando para operações de indexação do Gerenciador de escopo de rastreamento (CSM).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-276">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span> <span data-ttu-id="7aa0d-277">Ambos os exemplos de código estão disponíveis no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-277">Both code samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

### <a name="sample-log-file"></a><span data-ttu-id="7aa0d-278">Arquivo de log de exemplo</span><span class="sxs-lookup"><span data-stu-id="7aa0d-278">Sample Log File</span></span>

<span data-ttu-id="7aa0d-279">Mediante solicitação, o programa de Ifilttst.exe pode produzir um log contendo uma descrição das etapas que ele executa durante a execução.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-279">Upon request, the Ifilttst.exe program can produce a log containing a description of the steps it takes during execution.</span></span> <span data-ttu-id="7aa0d-280">Os exemplos a seguir são trechos de um arquivo de log, com o detalhamento definido para o valor 3 mais alto possível.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-280">The following examples are excerpts from a log file, with the verbosity set to the highest possible value 3.</span></span>

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

<span data-ttu-id="7aa0d-281">A primeira linha é uma mensagem informativa, indicando que uma nova configuração foi carregada a partir do arquivo de ifilttst.ini.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-281">The first line is an informational message, indicating that a new configuration has been loaded from the ifilttst.ini file.</span></span> <span data-ttu-id="7aa0d-282">Linha (3) indica o nome da seção no arquivo de ifilttst.ini do qual a configuração atual foi lida.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-282">Line (3) indicates the section name in the ifilttst.ini file from which the current configuration has been read.</span></span> <span data-ttu-id="7aa0d-283">Linhas (4) a (7) liste os parâmetros para [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-283">Lines (4) through (7) list the parameters to [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span></span> <span data-ttu-id="7aa0d-284">As linhas que começam com `INFO` são mensagens informativas sobre a associação do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e o início do teste de validação.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-284">The lines starting with `INFO` are informational messages about the binding of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and the start of the validation test.</span></span> <span data-ttu-id="7aa0d-285">As linhas que começam com `PASS` são mensagens relacionadas a testes específicos que passaram.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-285">Lines starting with `PASS` are messages regarding specific tests that have passed.</span></span>

<span data-ttu-id="7aa0d-286">A linha no exemplo de log a seguir é um aviso.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-286">The line in the following log example is a warning.</span></span> <span data-ttu-id="7aa0d-287">Os avisos chamam a atenção para o comportamento do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que é problemático, embora seja legal.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-287">Warnings call attention to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) behavior that is problematic, although legal.</span></span> <span data-ttu-id="7aa0d-288">Esse aviso indica que o método [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retornou uma parte de texto que não contém texto.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-288">This warning indicates that the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method has returned a text chunk that contains no text.</span></span>

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

<span data-ttu-id="7aa0d-289">O exemplo de mensagem de erro a seguir indica que o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitiu uma parte que não foi solicitada.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-289">The following example error message indicates that the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk that was not requested.</span></span>

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

<span data-ttu-id="7aa0d-290">No caso desse exemplo de mensagem de erro, o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitiu uma parte com um PID de `0x5` .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-290">In the case of this example error message, the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk with a PID of `0x5`.</span></span> <span data-ttu-id="7aa0d-291">A inspeção da seção `[Test1]` no ifilttst.ini mostraria que o **IFilter** foi configurado para não emitir partes com esse PID.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-291">Inspection of section `[Test1]` in ifilttst.ini would show that the **IFilter** was configured to not emit chunks with this PID.</span></span> <span data-ttu-id="7aa0d-292">Por exemplo, se nenhum IFILTER \_ init \_ aplicar \_ \_ atributos de índice nem o IFilter \_ init \_ aplicar \_ outros \_ atributos foram especificados na entrada flags e, se *cAttributes* fosse 0, o **IFILTER** emitiria apenas partes com um PID `0x13` e correspondente ao \_ conteúdo PID STG \_ .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-292">For example, if neither IFILTER\_INIT\_APPLY\_INDEX\_ATTRIBUTES nor IFILTER\_INIT\_APPLY\_OTHER\_ATTRIBUTES were specified in the Flags entry and if *cAttributes* were 0, then **IFilter** would emit only chunks with a PID of `0x13` and corresponding to PID\_STG\_CONTENTS.</span></span>

### <a name="sample-dump-file"></a><span data-ttu-id="7aa0d-293">Exemplo de arquivo de despejo</span><span class="sxs-lookup"><span data-stu-id="7aa0d-293">Sample Dump File</span></span>

<span data-ttu-id="7aa0d-294">Mediante solicitação, o programa de Ifilttst.exe pode produzir um despejo contendo as partes encontradas e seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-294">Upon request, the Ifilttst.exe program can produce a dump containing the chunks it finds and their content.</span></span> <span data-ttu-id="7aa0d-295">O exemplo a seguir é um trecho desse arquivo de despejo.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-295">The following example is an excerpt from such a dump file.</span></span>

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

<span data-ttu-id="7aa0d-296">As nove primeiras linhas descrevem a estrutura da parte atual.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-296">The first nine lines describe the current chunk structure.</span></span> <span data-ttu-id="7aa0d-297">O GUID e o PID correspondem ao \_ conteúdo do armazenamento PSGUID/PID \_ STG \_ .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-297">The GUID and the PID correspond to PSGUID\_STORAGE / PID\_STG\_CONTENTS.</span></span> <span data-ttu-id="7aa0d-298">Esta é uma parte que contém texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-298">This is a chunk containing plain text.</span></span> <span data-ttu-id="7aa0d-299">O texto está na seguinte estrutura de partes:</span><span class="sxs-lookup"><span data-stu-id="7aa0d-299">The text is in the following chunk structure:</span></span>

```
10. This is an HTML IFilter test page
```

<span data-ttu-id="7aa0d-300">A próxima parte, começando na linha 11, tem um GUID diferente, correspondente ao `HTML IFilter` e um PID diferente, correspondente a um href HTML.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-300">The next chunk, starting at line 11, has a different GUID, corresponding to the `HTML IFilter`, and a different PID, corresponding to an HTML HREF.</span></span> <span data-ttu-id="7aa0d-301">Essa é uma propriedade interna de tipo de valor, exportada pelo `HTML IFilter` .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-301">This is an internal value-type property, exported by the `HTML IFilter`.</span></span>

<span data-ttu-id="7aa0d-302">A próxima parte, começando na linha 21, tem o mesmo GUID e PID, mas seu estado de bloco é `VALUE` em vez de `TEXT` .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-302">The next chunk, starting at line 21, has the same GUID and PID, but its chunk state is `VALUE` instead of `TEXT`.</span></span> <span data-ttu-id="7aa0d-303">Observe que o texto nessas duas últimas partes é o mesmo que para a primeira parte.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-303">Note that the text in these last two chunks is the same as for the first chunk.</span></span> <span data-ttu-id="7aa0d-304">Mas como o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) foi projetado para três atributos (texto sem formatação, href HTML como texto e href HTML como um valor) a serem aplicados a essa frase, os resultados são emitidos em três partes separadas.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-304">But because the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is designed for three attributes (plain text, HTML HREF as text, and HTML HREF as a value) to be applied to this phrase, the results are emitted in three separate chunks.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7aa0d-305">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="7aa0d-305">Additional Resources</span></span>

- <span data-ttu-id="7aa0d-306">O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="7aa0d-306">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="7aa0d-307">Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-307">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="7aa0d-308">Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-308">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="7aa0d-309">Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-309">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aa0d-310">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7aa0d-310">Related topics</span></span>

[<span data-ttu-id="7aa0d-311">Desenvolvendo manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="7aa0d-311">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="7aa0d-312">Sobre manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="7aa0d-312">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="7aa0d-313">Práticas recomendadas para a criação de manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="7aa0d-313">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="7aa0d-314">Retornando Propriedades de um manipulador de filtro</span><span class="sxs-lookup"><span data-stu-id="7aa0d-314">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="7aa0d-315">Manipuladores de filtro que acompanham o Windows</span><span class="sxs-lookup"><span data-stu-id="7aa0d-315">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="7aa0d-316">Implementando manipuladores de filtro no Windows Search</span><span class="sxs-lookup"><span data-stu-id="7aa0d-316">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="7aa0d-317">Registrando manipuladores de filtro</span><span class="sxs-lookup"><span data-stu-id="7aa0d-317">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
