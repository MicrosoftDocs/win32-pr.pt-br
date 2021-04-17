---
description: 'Saiba mais sobre: arquivos do mecanismo de armazenamento extensível'
title: Arquivos do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105785214"
---
# <a name="extensible-storage-engine-files"></a><span data-ttu-id="f9685-103">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="f9685-103">Extensible Storage Engine Files</span></span>


<span data-ttu-id="f9685-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f9685-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-files"></a><span data-ttu-id="f9685-105">Arquivos do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="f9685-105">Extensible Storage Engine Files</span></span>

<span data-ttu-id="f9685-106">O mecanismo de armazenamento extensível usa os seguintes tipos de arquivos:</span><span class="sxs-lookup"><span data-stu-id="f9685-106">The Extensible Storage Engine uses the following types of files:</span></span>

- [<span data-ttu-id="f9685-107">Arquivos de log de transações</span><span class="sxs-lookup"><span data-stu-id="f9685-107">Transaction Log Files</span></span>](#transaction-log-files)

- [<span data-ttu-id="f9685-108">Arquivos de log de transações temporários</span><span class="sxs-lookup"><span data-stu-id="f9685-108">Temporary Transaction Log Files</span></span>](#temporary-transaction-log-files)

- [<span data-ttu-id="f9685-109">Arquivos de log de transações reservados</span><span class="sxs-lookup"><span data-stu-id="f9685-109">Reserved Transaction Log Files</span></span>](#reserved-transaction-log-files)

- [<span data-ttu-id="f9685-110">Arquivos de ponto de verificação</span><span class="sxs-lookup"><span data-stu-id="f9685-110">Checkpoint Files</span></span>](#checkpoint-files)

- [<span data-ttu-id="f9685-111">Arquivos do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f9685-111">Database Files</span></span>](#database-files)

- [<span data-ttu-id="f9685-112">Bancos de dados temporários</span><span class="sxs-lookup"><span data-stu-id="f9685-112">Temporary Databases</span></span>](#temporary-databases)

- [<span data-ttu-id="f9685-113">Liberar arquivos de mapa</span><span class="sxs-lookup"><span data-stu-id="f9685-113">Flush Map Files</span></span>](#flush-map-files)

<span data-ttu-id="f9685-114">Esta tabela contém uma visão geral dos nomes de arquivo de dados que são gerenciados pelo ESE.</span><span class="sxs-lookup"><span data-stu-id="f9685-114">This table contains an overview of the data file names that are managed by ESE.</span></span> <span data-ttu-id="f9685-115">Para o Windows Vista e posterior, a configuração JET_paramLegacyNames Impacta os nomes de arquivo usados.</span><span class="sxs-lookup"><span data-stu-id="f9685-115">For Windows Vista and later, the JET_paramLegacyNames setting impacts the file names that are used.</span></span>

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p><span data-ttu-id="f9685-116">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f9685-116">Operating System</span></span></p>
    </th>
    <th>
      <p><span data-ttu-id="f9685-117">Windows Server 2003 e anterior</span><span class="sxs-lookup"><span data-stu-id="f9685-117">Windows Server 2003 and earlier</span></span><br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p><span data-ttu-id="f9685-118">Windows Vista e posterior (cliente)</span><span class="sxs-lookup"><span data-stu-id="f9685-118">Windows Vista and later (client)</span></span> <br />
<span data-ttu-id="f9685-119">Windows Server 2008 e posterior (servidor)</span><span class="sxs-lookup"><span data-stu-id="f9685-119">Windows Server 2008 and later (server)</span></span>
</p>
    </th>
    <th>
      <p><span data-ttu-id="f9685-120">Atualização de aniversário do Windows 10 e posterior (cliente)</span><span class="sxs-lookup"><span data-stu-id="f9685-120">Windows 10 Anniversary Update and later (client)</span></span> <br />
<span data-ttu-id="f9685-121">Windows Server 2016 e posterior (servidor)</span><span class="sxs-lookup"><span data-stu-id="f9685-121">Windows Server 2016 and later (server)</span></span>
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-122">
        <strong>JET_paramLegacyNames configuração</strong>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-122">
        <strong>JET_paramLegacyNames setting</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-123">
        <strong>N/A</strong>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-123">
        <strong>N/A</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-124">
        <strong>Nenhum</strong>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-124">
        <strong>None</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-125">
        <strong>JET_bitESE98FileNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-125">
        <strong>JET_bitESE98FileNames</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-126">
        <strong>O mesmo que o Windows Vista/Server 2008</strong>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-126">
        <strong>Same as Windows Vista/Server 2008</strong>
      </span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-127">Log atual</span><span class="sxs-lookup"><span data-stu-id="f9685-127">Current Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-128">&lt;Inst &gt; . log</span><span class="sxs-lookup"><span data-stu-id="f9685-128">&lt;inst&gt;.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-129">&lt;Inst &gt; . jtx</span><span class="sxs-lookup"><span data-stu-id="f9685-129">&lt;inst&gt;.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-130">&lt;Inst &gt; . log</span><span class="sxs-lookup"><span data-stu-id="f9685-130">&lt;inst&gt;.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-131">Log de pré-inicialização</span><span class="sxs-lookup"><span data-stu-id="f9685-131">Pre-Init Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-132">&lt;Inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="f9685-132">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-133">&lt;Inst &gt; tmp. jtx</span><span class="sxs-lookup"><span data-stu-id="f9685-133">&lt;inst&gt;tmp.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-134">&lt;Inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="f9685-134">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-135">Logs girados</span><span class="sxs-lookup"><span data-stu-id="f9685-135">Rotated Logs</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-136">&lt;Inst &gt; xxxxx. log</span><span class="sxs-lookup"><span data-stu-id="f9685-136">&lt;inst&gt;XXXXX.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-137">&lt;Inst &gt; xxxxx. jtx após FFFFF mudar para &lt; Inst &gt; xxxxxxxx. jtx</span><span class="sxs-lookup"><span data-stu-id="f9685-137">&lt;inst&gt;XXXXX.jtx after FFFFF switch to &lt;inst&gt;XXXXXXXX.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-138">&lt;Inst &gt; xxxxx. log após FFFFF mudar para &lt; Inst &gt; xxxxxxxx. log.</span><span class="sxs-lookup"><span data-stu-id="f9685-138">&lt;inst&gt;XXXXX.log after FFFFF switch to &lt;inst&gt;XXXXXXXX.log.</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-139">
        <a href="gg294069(v=exchg.10).md">Arquivos de ponto de verificação</a>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-139">
        <a href="gg294069(v=exchg.10).md">Checkpoint Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-140">&lt;Inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="f9685-140">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-141">&lt;Inst &gt; . JCP</span><span class="sxs-lookup"><span data-stu-id="f9685-141">&lt;inst&gt;.jcp</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-142">&lt;Inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="f9685-142">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-143">
        <a href="gg294069(v=exchg.10).md">Bancos de dados temporários</a>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-143">
        <a href="gg294069(v=exchg.10).md">Temporary Databases</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-144">&lt;padrão de nome de arquivo do BD temp &gt; : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="f9685-144">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-145">&lt;padrão de nome de arquivo do BD temp &gt; : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="f9685-145">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-146">&lt;padrão de nome de arquivo do BD temp &gt; : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="f9685-146">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-147">
        <a href="gg294069(v=exchg.10).md">Arquivos de log de transações reservados</a>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-147">
        <a href="gg294069(v=exchg.10).md">Reserved Transaction Log Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-148">res1. log &amp; res2. log</span><span class="sxs-lookup"><span data-stu-id="f9685-148">res1.log &amp; res2.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-149">&lt;Inst &gt; RESXXXXX. jrs</span><span class="sxs-lookup"><span data-stu-id="f9685-149">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
    <td colspan="2">
      <p><span data-ttu-id="f9685-150">&lt;Inst &gt; RESXXXXX. jrs</span><span class="sxs-lookup"><span data-stu-id="f9685-150">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-151">
        <a href="gg294069(v=exchg.10).md">Arquivos de banco de dados</a>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-151">
        <a href="gg294069(v=exchg.10).md">Database Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-152">&lt;nome do arquivo de BD&gt;</span><span class="sxs-lookup"><span data-stu-id="f9685-152">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-153">&lt;nome do arquivo de BD&gt;</span><span class="sxs-lookup"><span data-stu-id="f9685-153">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-154">&lt;nome do arquivo de BD&gt;</span><span class="sxs-lookup"><span data-stu-id="f9685-154">&lt;db file name&gt;</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="f9685-155">
        <a href="gg294069(v=exchg.10).md">Liberar arquivos de mapa</a>
      </span><span class="sxs-lookup"><span data-stu-id="f9685-155">
        <a href="gg294069(v=exchg.10).md">Flush Map Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-156">N/D</span><span class="sxs-lookup"><span data-stu-id="f9685-156">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-157">N/D</span><span class="sxs-lookup"><span data-stu-id="f9685-157">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-158">N/D</span><span class="sxs-lookup"><span data-stu-id="f9685-158">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="f9685-159">&lt;nome do arquivo de BD sem extensão &gt; . JFM</span><span class="sxs-lookup"><span data-stu-id="f9685-159">&lt;db file name without extension&gt;.jfm</span></span></p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a><span data-ttu-id="f9685-160">Arquivos de log de transações</span><span class="sxs-lookup"><span data-stu-id="f9685-160">Transaction Log Files</span></span>

<span data-ttu-id="f9685-161">Os arquivos de log de transações contêm operações em arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-161">Transaction log files contain operations on database files.</span></span> <span data-ttu-id="f9685-162">Elas contêm informações suficientes para colocar um banco de dados em um estado logicamente consistente após uma terminação de processo inesperada ou um desligamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="f9685-162">They contain enough information to bring a database to a logically consistent state after an unexpected process termination or system shutdown.</span></span>

<span data-ttu-id="f9685-163">Os nomes dos arquivos de log dependem de um nome de base de três letras, que pode ser definido com [JET_paramBaseName](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f9685-163">The names of the log files are dependent on a three-letter base name, which can be set with [JET_paramBaseName](./transaction-log-parameters.md).</span></span> <span data-ttu-id="f9685-164">Os exemplos a seguir usam um nome de base de "edb", porque esse é o nome de base padrão.</span><span class="sxs-lookup"><span data-stu-id="f9685-164">The examples below use a base name of "edb", because that is the default base name.</span></span> <span data-ttu-id="f9685-165">A extensão dos arquivos de log de transações será. log ou. jtx, dependendo se o JET_bitESE98FileNames está definido no parâmetro JET_paramLegacyFileNames.</span><span class="sxs-lookup"><span data-stu-id="f9685-165">The extension for the transaction log files will be either .log or .jtx depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter.</span></span> <span data-ttu-id="f9685-166">Para obter mais informações, consulte [parâmetros do sistema do mecanismo de armazenamento extensível](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f9685-166">For more information, see [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="f9685-167">Os arquivos de log de transações são nomeados \<base\> \<generation-number\> . log, começando com 1.</span><span class="sxs-lookup"><span data-stu-id="f9685-167">Transaction log files are named \<base\>\<generation-number\>.log, beginning with 1.</span></span> <span data-ttu-id="f9685-168">O número de geração de log está em formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="f9685-168">The log generation number is in hexadecimal format.</span></span> <span data-ttu-id="f9685-169">Por exemplo, edb00001. log é o primeiro log, e edb000ff. log é o log 255th.</span><span class="sxs-lookup"><span data-stu-id="f9685-169">For example, edb00001.log is the first log, and edb000ff.log is the 255th log.</span></span> <span data-ttu-id="f9685-170">Os arquivos de log têm cinco dígitos hexadecimais no nome do arquivo de log, até o arquivo de log 1048576th, no ponto em que os arquivos de log começam a ser nomeados em um formato 11,3 (por exemplo, edb00100000. log).</span><span class="sxs-lookup"><span data-stu-id="f9685-170">The log files have five hexadecimal digits in the log file name, until the 1048576th log file, at which point the log files start being named in an 11.3 format (for example, edb00100000.log).</span></span> <span data-ttu-id="f9685-171">\<base\>. log é sempre o arquivo de log que está sendo usado no momento.</span><span class="sxs-lookup"><span data-stu-id="f9685-171">\<base\>.log is always the log file that is currently being used.</span></span> <span data-ttu-id="f9685-172">Se o mecanismo de banco de dados não estiver ativo, a geração de edb. log poderá ser identificada usando o seguinte comando: **esentutl.exe-ml edb. log**.</span><span class="sxs-lookup"><span data-stu-id="f9685-172">If the database engine is not active, the generation of edb.log can be identified using the following command: **esentutl.exe -ml edb.log**.</span></span>

<span data-ttu-id="f9685-173">Embora os arquivos de log de transações tenham o. Extensão de LOG normalmente associada a arquivos de texto, os arquivos de log de transações estão em um formato binário e nunca devem ser editados por um usuário. As operações de banco de dados são gravadas primeiro no log.</span><span class="sxs-lookup"><span data-stu-id="f9685-173">Although transaction log files have the .LOG extension commonly associated with text files, transaction log files are in a binary format and should never be edited by a user.Database operations are written to the log first.</span></span> <span data-ttu-id="f9685-174">Os dados podem ser gravados no arquivo de banco de dado mais tarde; possivelmente de imediato, possivelmente muito mais tarde.</span><span class="sxs-lookup"><span data-stu-id="f9685-174">The data can be written to the database file later; possibly immediately, potentially much later.</span></span> <span data-ttu-id="f9685-175">No caso de um processo inesperado ou encerramento do sistema, as operações ainda estão presentes nos arquivos de log, e as transações incompletas podem ser revertidas.</span><span class="sxs-lookup"><span data-stu-id="f9685-175">In the event of unexpected process or system termination, the operations are still present in the log files, and incomplete transactions can be rolled back.</span></span> <span data-ttu-id="f9685-176">O ato de reproduzir arquivos de log de transações é chamado de *recuperação simples* e é feito automaticamente quando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="f9685-176">The act of replaying transaction log files is called *soft recovery*, and it is done automatically when [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md) is called.</span></span> <span data-ttu-id="f9685-177">A recuperação simples também pode ser executada manualmente com a opção "-r" do programa Esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="f9685-177">Soft recovery can also be performed manually with the "-r" option of the Esentutl.exe program.</span></span> <span data-ttu-id="f9685-178">O ato de reproduzir arquivos de log de transações em um banco de dados restaurado de um backup é chamado de *recuperação complexa*.</span><span class="sxs-lookup"><span data-stu-id="f9685-178">The act of replaying transaction log files on a database that is restored from a backup is called *hard recovery*.</span></span>

<span data-ttu-id="f9685-179">Os arquivos de log têm um tamanho fixo, personalizável com [JET_paramLogFileSize](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f9685-179">Log files are of a fixed size, customizable with [JET_paramLogFileSize](./transaction-log-parameters.md).</span></span> <span data-ttu-id="f9685-180">Quando o arquivo de log atual (ou seja, edb. log) é preenchido, ele é renomeado para \<base\> \<generation-number\> . log e um novo arquivo de log de transações é necessário no fluxo do log de transações.</span><span class="sxs-lookup"><span data-stu-id="f9685-180">When the current log file (that is, edb.log) gets filled, it gets renamed to \<base\>\<generation-number\>.log, and a new transaction log file is needed in the transaction log stream.</span></span>

<span data-ttu-id="f9685-181">Cada instância de banco de dados tem uma única sequência de arquivo de log associada a ela.</span><span class="sxs-lookup"><span data-stu-id="f9685-181">Each database instance has a single log file sequence associated with it.</span></span> <span data-ttu-id="f9685-182">O Windows XP introduziu o [JetCreateInstance](./jetcreateinstance-function.md), permitindo que várias sequências de arquivos de log de transações sejam usadas por um único processo.</span><span class="sxs-lookup"><span data-stu-id="f9685-182">Windows XP introduced [JetCreateInstance](./jetcreateinstance-function.md), allowing multiple transaction log file sequences to be used by a single process.</span></span> <span data-ttu-id="f9685-183">No entanto, várias sequências do arquivo de log de transações não podem existir no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="f9685-183">Multiple transaction log file sequences cannot exist in the same directory, however.</span></span>

<span data-ttu-id="f9685-184">Os arquivos de log de transações quase nunca devem ser manipulados manualmente, renomeados, movidos ou excluídos porque os dados corrompidos podem resultar.</span><span class="sxs-lookup"><span data-stu-id="f9685-184">Transaction log files should almost never be manually manipulated, renamed, moved, or deleted because data corruption can result.</span></span>

<span data-ttu-id="f9685-185">Os arquivos de log de transações serão excluídos pelo mecanismo de banco de dados durante um backup completo (consulte [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) ou durante operações normais, se o log circular estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="f9685-185">Transaction log files will be deleted by the database engine during a full backup (see [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), or during normal operations, if circular logging is enabled.</span></span>

<span data-ttu-id="f9685-186">Depois que um arquivo de log de transações é preenchido, o mecanismo de banco de dados precisa criar um novo arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="f9685-186">After a transaction log file is filled up, the database engine needs to create a new log file.</span></span> <span data-ttu-id="f9685-187">O log circular é um meio pelo qual os arquivos de log podem ser limpos automaticamente pelo mecanismo de banco de dados quando não são mais necessários para a recuperação de falhas.</span><span class="sxs-lookup"><span data-stu-id="f9685-187">Circular logging is a means by which log files can be automatically cleaned up by the database engine when they are no longer required for crash recovery.</span></span> <span data-ttu-id="f9685-188">Esse processo é uma alternativa à remoção de arquivos de log como um produto de execução de um backup.</span><span class="sxs-lookup"><span data-stu-id="f9685-188">This process is an alternative to removing log files as a by-product of performing a backup.</span></span> <span data-ttu-id="f9685-189">O log circular pode ser controlado com o parâmetro do sistema [JET_paramCircularLog](./transaction-log-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="f9685-189">Circular logging can be controlled with the [JET_paramCircularLog](./transaction-log-parameters.md) system parameter.</span></span> <span data-ttu-id="f9685-190">Os arquivos de log de transações não devem ser excluídos usando qualquer outro método.</span><span class="sxs-lookup"><span data-stu-id="f9685-190">Transaction log files should not be deleted using any other method.</span></span>

### <a name="temporary-transaction-log-files"></a><span data-ttu-id="f9685-191">Arquivos de log de transações temporários</span><span class="sxs-lookup"><span data-stu-id="f9685-191">Temporary Transaction Log Files</span></span>

<span data-ttu-id="f9685-192">Quando o edb. log é preenchido, o ESE precisa criar um novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="f9685-192">When edb.log fills up, ESE needs to create a new file.</span></span> <span data-ttu-id="f9685-193">O novo arquivo de transação de log é conhecido como um arquivo de log de transações temporário antes de seu uso pelo ESE.</span><span class="sxs-lookup"><span data-stu-id="f9685-193">The new log transaction file is known as a temporary transaction log file prior to its use by ESE.</span></span>

<span data-ttu-id="f9685-194">Enquanto um novo arquivo de log é criado e seu tamanho estendido, ele será chamado de \<base\> tmp. log.</span><span class="sxs-lookup"><span data-stu-id="f9685-194">While a new log file is created and its size extended, it will be called \<base\>tmp.log.</span></span> <span data-ttu-id="f9685-195">A criação de um novo arquivo pode ser uma operação potencialmente dispendiosa, portanto, o ESE criará o próximo arquivo de log proativamente como uma tarefa em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f9685-195">Creating a new file can be a potentially costly operation, so ESE will create the next log file proactively as a background task.</span></span>

<span data-ttu-id="f9685-196">Como o arquivo de log de transações temporários é criado na antecipação de necessidade de um novo arquivo de log de transações, ele não contém informações úteis.</span><span class="sxs-lookup"><span data-stu-id="f9685-196">Because the temporary transaction log file is created in anticipation of need for a new transaction log file, it does not contain any useful information.</span></span>

### <a name="reserved-transaction-log-files"></a><span data-ttu-id="f9685-197">Arquivos de log de transações reservados</span><span class="sxs-lookup"><span data-stu-id="f9685-197">Reserved Transaction Log Files</span></span>

<span data-ttu-id="f9685-198">Os arquivos de log de transações reservados são criados quando o mecanismo começa a permitir que operações importantes sejam registradas para obter um desligamento normal.</span><span class="sxs-lookup"><span data-stu-id="f9685-198">The reserved transaction log files are created when the engine starts to allow important operations to be logged to get a clean shutdown.</span></span>

<span data-ttu-id="f9685-199">**Windows Vista:** No Windows Vista e posterior, os arquivos de log de transações reservados são nomeados \<base\> RESXXXXX. jrs.</span><span class="sxs-lookup"><span data-stu-id="f9685-199">**Windows Vista:** In Windows Vista and later, the Reserved Transaction Log Files are named \<base\>RESXXXXX.jrs.</span></span>

<span data-ttu-id="f9685-200">**Windows Server 2003:** No Windows Server 2003 e versões anteriores, os arquivos de log de transações reservados são nomeados res1. log e res2. log.</span><span class="sxs-lookup"><span data-stu-id="f9685-200">**Windows Server 2003:** In Windows Server 2003 and earlier, The Reserved Transaction Log Files are named res1.log and res2.log.</span></span>

<span data-ttu-id="f9685-201">Quando o mecanismo de banco de dados fica sem espaço em disco, ele não pode criar um novo arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="f9685-201">When the database engine runs out of disk space it cannot create a new log file.</span></span> <span data-ttu-id="f9685-202">A coisa mais segura a fazer é desligar corretamente, mas algumas operações (como operações de reversão) ainda devem ser registradas em log.</span><span class="sxs-lookup"><span data-stu-id="f9685-202">The safest thing to do is to shut down cleanly, but some operations (such as rollback operations) must still be logged.</span></span> <span data-ttu-id="f9685-203">A maioria das operações de banco de dados falhará durante esse estágio.</span><span class="sxs-lookup"><span data-stu-id="f9685-203">Most database operations will fail during this stage.</span></span>

<span data-ttu-id="f9685-204">Como os arquivos de log de transações reservados são criados na antecipação de necessidade de arquivos de log de transações em um cenário de fora de disco, eles não contêm nenhuma informação útil.</span><span class="sxs-lookup"><span data-stu-id="f9685-204">Because the reserved transaction log files are created in anticipation of need for transaction log files in an out-of-disk scenario, they do not contain any useful information.</span></span>

### <a name="checkpoint-files"></a><span data-ttu-id="f9685-205">arquivos de ponto de verificação</span><span class="sxs-lookup"><span data-stu-id="f9685-205">Checkpoint Files</span></span>

<span data-ttu-id="f9685-206">O arquivo de ponto de verificação armazena o ponto de verificação para uma sequência de arquivo de log de transação específica.</span><span class="sxs-lookup"><span data-stu-id="f9685-206">The checkpoint file stores the checkpoint for a particular transaction log file sequence.</span></span> <span data-ttu-id="f9685-207">O arquivo de ponto de verificação é chamado \<base\> . chk ou \<base\> . JCP, dependendo se o JET_bitESE98FileNames está definido no parâmetro JET_paramLegacyFileNames e sua localização é fornecida por [JET_paramSystemPath](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f9685-207">The checkpoint file is named \<base\>.chk or \<base\>.jcp, depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter, and its location is given by [JET_paramSystemPath](./transaction-log-parameters.md).</span></span>

<span data-ttu-id="f9685-208">As operações de banco de dados são primeiro gravadas nos arquivos de log e, em seguida, armazenadas em cache na memória.</span><span class="sxs-lookup"><span data-stu-id="f9685-208">Database operations are first written to the log files and then cached in memory.</span></span> <span data-ttu-id="f9685-209">Em algum momento posterior, as operações são gravadas no arquivo de banco de dados, mas por motivos de desempenho, a ordem na qual as operações são gravadas no arquivo de banco de dados pode não corresponder à ordem em que foram registradas originalmente.</span><span class="sxs-lookup"><span data-stu-id="f9685-209">At some later point, the operations get written to the database file, but for performance reasons, the order in which operations are written to the database file might not match the order in which they were originally logged.</span></span> <span data-ttu-id="f9685-210">As operações gravadas no arquivo de log de transações estarão em um dos dois Estados:</span><span class="sxs-lookup"><span data-stu-id="f9685-210">Operations written to the transaction log file will be in one of two states:</span></span>

  - <span data-ttu-id="f9685-211">Gravado no arquivo de log de transações e no arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-211">Written to the transaction log file and the database file.</span></span>

  - <span data-ttu-id="f9685-212">Gravado no arquivo de log de transações e ainda não gravados no arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-212">Written to the transaction log file and not yet written to the database file.</span></span>

<span data-ttu-id="f9685-213">Muitas operações de banco de dados podem ser armazenadas em um único arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="f9685-213">Many database operations can be stored in a single transaction log file.</span></span> <span data-ttu-id="f9685-214">Um determinado arquivo de log pode consistir nos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="f9685-214">A given log file can consist of the following items:</span></span>

  - <span data-ttu-id="f9685-215">Todas as operações gravadas no arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-215">All operations written to the database file.</span></span>

  - <span data-ttu-id="f9685-216">Nenhuma operação gravada no arquivo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="f9685-216">No operations written to the database file</span></span>

  - <span data-ttu-id="f9685-217">Uma mistura de operações gravadas no arquivo de banco de dados e operações ainda não gravadas no arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-217">A mix of operations written to the database file and operations not yet written to the database file.</span></span>

<span data-ttu-id="f9685-218">O ponto de verificação refere-se ao ponto no tempo no fluxo de log de transações, em que todas as operações anteriores ao ponto de verificação foram gravadas no arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-218">The checkpoint refers to the point in time in the transaction log stream where all operations prior to the checkpoint have been written to the database file.</span></span> <span data-ttu-id="f9685-219">Não há nenhuma garantia sobre as operações que ocorrem após o ponto de verificação; Alguns podem estar na memória e alguns podem ser gravados no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-219">There is no guarantee about the operations that occur after the checkpoint; some might be in memory, and some might be written to the database.</span></span>

<span data-ttu-id="f9685-220">Como todas as operações nos arquivos de log antes do ponto de verificação são representadas no arquivo de banco de dados, somente os arquivos de log de transações após o ponto de verificação são necessários para a recuperação simples para colocar um determinado banco de dados em um estado limpo.</span><span class="sxs-lookup"><span data-stu-id="f9685-220">Since all the operations in the log files prior to the checkpoint are represented in the database file, only the transaction log files after the checkpoint are needed for soft recovery to bring a particular database into a clean state.</span></span>

### <a name="database-files"></a><span data-ttu-id="f9685-221">Arquivos do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f9685-221">Database Files</span></span>

<span data-ttu-id="f9685-222">O arquivo de banco de dados contém o esquema para todas as tabelas no banco de dados, os registros de todas as tabelas no banco de dados e os índices nas tabelas.</span><span class="sxs-lookup"><span data-stu-id="f9685-222">The database file contains the schema for all of the tables in the database, the records for all of the tables in the database, and the indexes over the tables.</span></span> <span data-ttu-id="f9685-223">Seu local é fornecido usando [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)ou [JetAttachDatabase2](./jetattachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="f9685-223">Its location is given using [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md), or [JetAttachDatabase2](./jetattachdatabase2-function.md).</span></span>

<span data-ttu-id="f9685-224">Um banco de dados é desligado corretamente somente após uma chamada bem-sucedida para [JetTerm](./jetterm-function.md) ou [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="f9685-224">A database is cleanly shut down only after a successful call to [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="f9685-225">O programa Esentutl.exe pode detectar se um banco de dados é desligado corretamente com a opção "-MH".</span><span class="sxs-lookup"><span data-stu-id="f9685-225">The Esentutl.exe program can detect whether a database is shut down cleanly with the "-mh" option.</span></span> <span data-ttu-id="f9685-226">Por exemplo, "esentutl.exe-MH Sample. edb" lerá o cabeçalho do banco de dados de um banco de dados chamado Sample. edb e imprimirá o estado de Sample. edb.</span><span class="sxs-lookup"><span data-stu-id="f9685-226">For example, "esentutl.exe -mh sample.edb" will read the database header of a database named sample.edb, and print out the state of sample.edb.</span></span> <span data-ttu-id="f9685-227">Ele pode imprimir "Estado: limpar desligamento" ou "Estado: desligamento anormal".</span><span class="sxs-lookup"><span data-stu-id="f9685-227">It may print out "State: Clean Shutdown" or "State: Dirty Shutdown".</span></span>

<span data-ttu-id="f9685-228">Um banco de dados que não foi desligado corretamente está em um estado de desligamento anormal.</span><span class="sxs-lookup"><span data-stu-id="f9685-228">A database that has not been cleanly shut down is in a dirty shutdown state.</span></span> <span data-ttu-id="f9685-229">Antes do Windows XP, esse estado era chamado *inconsistente*.</span><span class="sxs-lookup"><span data-stu-id="f9685-229">Prior to Windows XP, this state was called *inconsistent*.</span></span> <span data-ttu-id="f9685-230">Um banco de dados sujo (inconsistente) pode ser levado a um estado limpo com a recuperação simples.</span><span class="sxs-lookup"><span data-stu-id="f9685-230">A dirty (inconsistent) database can be brought to a clean state with soft recovery.</span></span> <span data-ttu-id="f9685-231">Um banco de dados corrompido não é o mesmo que um banco de dados sujo ("inconsistente").</span><span class="sxs-lookup"><span data-stu-id="f9685-231">A corrupt database is not the same as a dirty ("inconsistent") database.</span></span>

<span data-ttu-id="f9685-232">Um banco de dados corrompido refere-se a uma corrupção física ou lógica e não pode ser corrigido com a recuperação simples.</span><span class="sxs-lookup"><span data-stu-id="f9685-232">A corrupt database refers to a physical or logical corruption, and cannot be fixed with soft recovery.</span></span> <span data-ttu-id="f9685-233">As corrupções físicas podem ser invertidas de bits, que frequentemente serão detectadas pelas somas de verificação nas páginas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-233">Physical corruptions can be bit flips, which will frequently be caught by the checksums on the database pages.</span></span> <span data-ttu-id="f9685-234">Uma soma de verificação com falha em um arquivo de banco de dados se manifesta como um erro JET_errReadVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="f9685-234">A failed checksum in a database file manifests itself as a JET_errReadVerifyFailure error.</span></span>

<span data-ttu-id="f9685-235">Somente os bancos de dados desligados de forma limpa podem ser movidos com segurança ou renomeados.</span><span class="sxs-lookup"><span data-stu-id="f9685-235">Only cleanly shut down databases can be safely moved around or renamed.</span></span> <span data-ttu-id="f9685-236">Se um banco de dados não tiver sido desligado corretamente, ele não poderá ser movido ou renomeado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f9685-236">If a database was not cleanly shut down, it cannot be automatically safely moved or renamed.</span></span>

<span data-ttu-id="f9685-237">Vários bancos de dados podem ser associados a uma única sequência de arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="f9685-237">Multiple databases can be associated with a single transaction log file sequence.</span></span>

### <a name="temporary-databases"></a><span data-ttu-id="f9685-238">Bancos de dados temporários</span><span class="sxs-lookup"><span data-stu-id="f9685-238">Temporary Databases</span></span>

<span data-ttu-id="f9685-239">O banco de dados temporário é usado como um repositório de backup para temptables e também é usado durante a criação de índices.</span><span class="sxs-lookup"><span data-stu-id="f9685-239">The temporary database is used as a backing store for temptables and it is also used when creating indices.</span></span>

<span data-ttu-id="f9685-240">O nome e o local são configurados com [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f9685-240">The name and location is configured with [JET_paramTempPath](./temporary-database-parameters.md).</span></span>

<span data-ttu-id="f9685-241">Temptables são criados com [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="f9685-241">Temptables are created with [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span> <span data-ttu-id="f9685-242">Eles também são criados por algumas chamadas à API e usados para retornar informações de esquema (como [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="f9685-242">They are also created by some API calls and used to return schema information (such as [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span></span>

## <a name="flush-map-files"></a><span data-ttu-id="f9685-243">Liberar arquivos de mapa</span><span class="sxs-lookup"><span data-stu-id="f9685-243">Flush Map Files</span></span>

<span data-ttu-id="f9685-244">A partir da atualização de aniversário do Windows 10 (cliente) e do Windows Server 2016 (servidor), o ESE adicionou um nível adicional de proteção contra gravações perdidas (ou liberações perdidas) 1, permitindo que ele detecte tais eventos de reinitialization2ção entre processos.</span><span class="sxs-lookup"><span data-stu-id="f9685-244">Starting with the Windows 10 Anniversary Update (client) and Windows Server 2016 (server), ESE added an additional level of protection against lost writes (or lost flushes) 1, allowing it to detect such events cross-process re-initialization2.</span></span> <span data-ttu-id="f9685-245">Esse recurso requer a persistência de metadados em um arquivo separado chamado de arquivo de "mapa de liberação".</span><span class="sxs-lookup"><span data-stu-id="f9685-245">This feature requires persisting metadata to a separate file called a "flush map" file.</span></span>

<span data-ttu-id="f9685-246">Um arquivo de mapa de liberação é criado para cada arquivo de banco de dados e está localizado no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="f9685-246">One flush map file is created for each database file, and is located in the same directory.</span></span> <span data-ttu-id="f9685-247">O arquivo é nomeado de forma semelhante ao arquivo de banco de dados, mas com uma extensão diferente.</span><span class="sxs-lookup"><span data-stu-id="f9685-247">The file is named similarly to the database file, but with a different extension.</span></span> <span data-ttu-id="f9685-248">Por exemplo, se o aplicativo cliente criar um banco de dados com o caminho completo C: \\ mydirectory \\ MyDabatase. edb, seu arquivo de mapa de liberação correspondente será C: \\ mydirectory \\ MyDabatase. JFM.</span><span class="sxs-lookup"><span data-stu-id="f9685-248">For example, if the client application creates a database with the full path C:\\MyDirectory\\MyDabatase.edb, its corresponding flush map file is C:\\MyDirectory\\MyDabatase.jfm.</span></span>

<span data-ttu-id="f9685-249">Esse aprimoramento apresenta dois requisitos de como os arquivos de banco de dados devem ser nomeados:</span><span class="sxs-lookup"><span data-stu-id="f9685-249">This enhancement introduces two requirements for how database files must be named:</span></span>

  - <span data-ttu-id="f9685-250">Dois bancos de dados no mesmo diretório não devem ter o mesmo nome de arquivo com extensões diferentes.</span><span class="sxs-lookup"><span data-stu-id="f9685-250">Two databases in the same directory must not have the same filename with different extensions.</span></span> <span data-ttu-id="f9685-251">Por exemplo: C: \\ mydirectory \\ MyDabatase. db1 e C: \\ mydirectory \\ MyDabatase. DB2.</span><span class="sxs-lookup"><span data-stu-id="f9685-251">For example: C:\\MyDirectory\\MyDabatase.db1 and C:\\MyDirectory\\MyDabatase.db2.</span></span>

  - <span data-ttu-id="f9685-252">2 \.</span><span class="sxs-lookup"><span data-stu-id="f9685-252">2\.</span></span> <span data-ttu-id="f9685-253">Um banco de dados não deve ter uma extensão. JFM.</span><span class="sxs-lookup"><span data-stu-id="f9685-253">A database must not have a .jfm extension.</span></span>

<span data-ttu-id="f9685-254">Quando você copia ou move um arquivo de banco de dados manualmente, seu arquivo de mapa de liberação correspondente também deve ser, respectivamente, copiado ou movido para o mesmo diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="f9685-254">When you manually copy or move a database file, its corresponding flush map file should also be, respectively, copied or moved to the same destination directory.</span></span> <span data-ttu-id="f9685-255">Se um arquivo de mapa de liberação não estiver presente no momento de um novo anexo de banco de dados (via [JetAttachDatabase](./jetattachdatabase-function.md), um novo será criado e preenchido novamente sob demanda, pois as páginas são lidas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-255">If a flush map file is not present at the time of a new database attachment (via [JetAttachDatabase](./jetattachdatabase-function.md), a new one will be created and re-populated on-demand as pages are read in from the database.</span></span> <span data-ttu-id="f9685-256">Misturar bancos de dados incompatíveis e arquivos de mapa de liberação é manipulado pelo ESE e força o mapa de liberação incompatível a ser excluído e recriado do zero.</span><span class="sxs-lookup"><span data-stu-id="f9685-256">Mixing mismatching database and flush map files is handled by ESE, and forces the mismatched flush map to be deleted and re-created from scratch.</span></span>

<span data-ttu-id="f9685-257">O tamanho de um arquivo de mapa de liberação é diretamente proporcional ao seu arquivo de banco de dados associado e aproximadamente igual a (todos os tamanhos em bytes, o resultado deve ser arredondado para o próximo múltiplo de 8.192):</span><span class="sxs-lookup"><span data-stu-id="f9685-257">The size of a flush map file is directly proportional to its associated database file and approximately equal to (all sizes in bytes, result must be rounded up to the next multiple of 8,192):</span></span>

`8,192 + ((<database file size> / <database page size>) / 4)`

<span data-ttu-id="f9685-258">Por exemplo: para um banco de dados de 1,5 GB usando um tamanho de página 32 KB, o tamanho aproximado do mapa de liberação é 24.576 bytes (ou 24KB).</span><span class="sxs-lookup"><span data-stu-id="f9685-258">For example: for a 1.5GB database using a 32KB page size, the approximate size of the flush map is 24,576 bytes (or 24KB).</span></span>

<span data-ttu-id="f9685-259">O arquivo do mapa de liberação precisa ser atualizado, pois as páginas do banco de dados são liberadas.</span><span class="sxs-lookup"><span data-stu-id="f9685-259">The flush map file needs to be refreshed as database pages are flushed.</span></span> <span data-ttu-id="f9685-260">Se o registro em log transacional estiver habilitado (por exemplo, [JET_paramRecovery](./transaction-log-parameters.md) definido como "ativado", o padrão), a atualização do mapa de liberação será executada à medida que o aplicativo cliente fizer modificações no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9685-260">If transactional logging is enabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "on", the default), refreshing the flush map is performed as the client application makes modifications to the database.</span></span> <span data-ttu-id="f9685-261">Em média, todo o mapa de liberação é gravado na mídia não volátil uma vez para cada 20% de [JET_paramCheckpointDepthMax](./database-cache-parameters.md) (em bytes) de logs transacionais gerados.</span><span class="sxs-lookup"><span data-stu-id="f9685-261">On average, the entire flush map is written to the non-volatile media once for every 20% of [JET_paramCheckpointDepthMax](./database-cache-parameters.md) -worth (in bytes) of transactional logs generated.</span></span> <span data-ttu-id="f9685-262">O número de operações de gravação depende de quão distribuído em todo o banco de dados as modificações são.</span><span class="sxs-lookup"><span data-stu-id="f9685-262">The number of write operations depends on how distributed throughout the database the modifications are.</span></span> <span data-ttu-id="f9685-263">Mas é, no máximo, aproximadamente (todos os tamanhos em bytes):</span><span class="sxs-lookup"><span data-stu-id="f9685-263">But it is at most, approximately (all sizes in bytes):</span></span>

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

<span data-ttu-id="f9685-264">Se o registro em log transacional estiver desabilitado (por exemplo, [JET_paramRecovery](./transaction-log-parameters.md) definido como "desativado"), o mapa de liberação será atualizado apenas uma vez quando o banco de dados for explicitamente desanexado (via [JetDetachDatabase](./jetdetachdatabase-function.md), ou desanexado implicitamente, encerrando sua instância do ESE associada (por meio de qualquer uma das funções de [JetTerm](./jetterm-function.md) , desde que [JET_bitTermDirty](./jetterm2-function.md) não seja passado).</span><span class="sxs-lookup"><span data-stu-id="f9685-264">If transactional logging is disabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "off"), the flush map gets refreshed only once when the database is explicitly detached cleanly (via [JetDetachDatabase](./jetdetachdatabase-function.md), or implicitly detached cleanly by terminating its associated ESE instance (via any of the [JetTerm](./jetterm-function.md) functions, as long as [JET_bitTermDirty](./jetterm2-function.md) is not passed).</span></span>

<span data-ttu-id="f9685-265">1 uma gravação perdida (ou liberação perdida) é definida como uma operação de gravação que retorna com êxito do sistema operacional para o mecanismo de banco de dados ESE, mas os dados reais nunca são mantidos no arquivo de banco de dados na mídia não volátil.</span><span class="sxs-lookup"><span data-stu-id="f9685-265">1 A lost write (or lost flush) is defined as a write operation that returns successfully from the operating system to the ESE database engine but the actual data never gets persisted to the database file in the non-volatile media.</span></span> <span data-ttu-id="f9685-266">Geralmente, isso é causado por uma pilha de armazenamento mal configurada ou defeituosa (software ou hardware).</span><span class="sxs-lookup"><span data-stu-id="f9685-266">It is usually caused by a malfunctioning or misconfigured storage stack (software or hardware).</span></span> <span data-ttu-id="f9685-267">Os aplicativos cliente podem receber um erro [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) de funções do ESE que exigem a leitura de dados do banco de dados se eles estiverem localizados em uma região que sofreu um evento de gravação perdido.</span><span class="sxs-lookup"><span data-stu-id="f9685-267">Client applications may receive a [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) error from ESE functions that require reading data from the database if the data is located in a region that underwent a lost write event.</span></span>

<span data-ttu-id="f9685-268">2 a capacidade de detectar gravações perdidas no tempo de vida de um processo vem presente desde o Windows 8 (cliente) e o Windows Server 2012 (Server).</span><span class="sxs-lookup"><span data-stu-id="f9685-268">2 The ability to detect lost writes within a process's lifetime has been present since Windows 8 (client) and Windows Server 2012 (server).</span></span>
