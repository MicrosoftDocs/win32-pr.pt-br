---
description: As tarefas do WMI para o registro criam e modificam valores e chaves do registro. Para obter outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: 0785189e-9638-4776-8414-1414d7b02524
ms.tgt_platform: multiple
title: 'Tarefas do WMI: registro'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df6ae73d41c9cbfd6cd303b72e1b9207f3191c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753846"
---
# <a name="wmi-tasks-registry"></a><span data-ttu-id="ed0af-104">Tarefas do WMI: registro</span><span class="sxs-lookup"><span data-stu-id="ed0af-104">WMI Tasks: Registry</span></span>

<span data-ttu-id="ed0af-105">As tarefas do WMI para o registro criam e modificam valores e chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="ed0af-105">WMI tasks for the registry create and modify registry keys and values.</span></span> <span data-ttu-id="ed0af-106">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ed0af-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="ed0af-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="ed0af-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="ed0af-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="ed0af-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="ed0af-109">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="ed0af-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="ed0af-110">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="ed0af-110">**To run a script**</span></span>

1.  <span data-ttu-id="ed0af-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="ed0af-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="ed0af-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="ed0af-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="ed0af-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ed0af-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="ed0af-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="ed0af-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="ed0af-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="ed0af-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="ed0af-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="ed0af-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="ed0af-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="ed0af-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="ed0af-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="ed0af-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="ed0af-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="ed0af-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="ed0af-120">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="ed0af-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-121">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="ed0af-121">How do I...</span></span></th>
<th><span data-ttu-id="ed0af-122">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="ed0af-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed0af-123">... ler valores de chave do registro usando o WMI?</span><span class="sxs-lookup"><span data-stu-id="ed0af-123">...read registry key values using WMI?</span></span></td>
<td><span data-ttu-id="ed0af-124">Use a classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , localizada no namespace root\default.</span><span class="sxs-lookup"><span data-stu-id="ed0af-124">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace.</span></span> <span data-ttu-id="ed0af-125">Você não pode obter nenhuma instância dessa classe porque o <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">provedor de registro do sistema</a> é apenas um método e provedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="ed0af-125">You cannot get any instances of this class because the <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registry Provider</a> is a method and event provider only.</span></span> <span data-ttu-id="ed0af-126">No entanto, você pode obter dados do registro por meio de métodos como <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> ou <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ed0af-126">However, you can get registry data through methods such as <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> or <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span></span> <span data-ttu-id="ed0af-127">O <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, localizado no namespace root\cimv2, obtém dados sobre o registro como um todo, como o tamanho do seu.</span><span class="sxs-lookup"><span data-stu-id="ed0af-127">The <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, located in root\cimv2 namespace, gets data about the registry as a whole, such as how large it is.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-128">VB</span><span class="sxs-lookup"><span data-stu-id="ed0af-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER,strKeyPath,strValueName,dwValue
WScript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed0af-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_CURRENT_USER =2147483649
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key = &quot;Console&quot;
$Value = &quot;HistoryBufferSize&quot;
$results = $reg.GetDWORDValue($HKEY_CURRENT_USER, $Key, $value)
&quot;Current History Buffer Size: {0}&quot; -f $results.uValue</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed0af-130">... criar uma nova chave do registro?</span><span class="sxs-lookup"><span data-stu-id="ed0af-130">...create a new registry key?</span></span></td>
<td><p><span data-ttu-id="ed0af-131">Use a classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , localizada no namespace root\default e o método <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-131">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-132">VB</span><span class="sxs-lookup"><span data-stu-id="ed0af-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)

strKeyPath = &quot;SOFTWARE\NewKey&quot;
objReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
WScript.Echo &quot;Created registry key HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed0af-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.CreateKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key created&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed0af-134">... criar um novo valor de registro em uma chave?</span><span class="sxs-lookup"><span data-stu-id="ed0af-134">...create a new registry value under a key?</span></span></td>
<td><p><span data-ttu-id="ed0af-135">Use a classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , localizada no namespace root\default e no método <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-135">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in the root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span> <span data-ttu-id="ed0af-136">Em seguida, use um dos métodos set, dependendo de qual tipo de dados de registro o valor é, como <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SETdwordvalue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ed0af-136">Then use one of the Set methods, depending on what registry datatype the value is, such as the <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span></span> <span data-ttu-id="ed0af-137">Os métodos set criam um valor se ele ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="ed0af-137">The Set methods create a value if it does not already exist.</span></span> <span data-ttu-id="ed0af-138">Para obter mais informações, consulte <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mapeando um tipo de dados do registro para um tipo de dados do WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="ed0af-138">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-139">VB</span><span class="sxs-lookup"><span data-stu-id="ed0af-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strValueName = &quot;Example_Expanded_String_Value&quot;
strValue = &quot;%PATHEXT%&quot;
objReg.SetExpandedStringValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,strValue
WScript.Echo &quot;Example expanded_String_Value at &quot; & &quot;HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed0af-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example_Expanded_String_Value&quot;
$Value     = &quot;%PATHEXT%&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetExpandedStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Value)
If ($results.Returnvalue -eq 0) {&quot;Value created&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed0af-141">... Evite obter um erro de classe inválido ao tentar gravar um script para ler o registro?</span><span class="sxs-lookup"><span data-stu-id="ed0af-141">...avoid getting an Invalid Class error when trying to write a script to read the registry?</span></span></td>
<td><p><span data-ttu-id="ed0af-142">Use o namespace root\default ao acessar a classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-142">Use the root\default namespace when accessing the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class.</span></span> <span data-ttu-id="ed0af-143"><strong>StdRegProv</strong> não faz parte do namespace CIMV2, que é o motivo pelo qual um &quot; erro de classe inválido &quot; é gerado se você tentar se conectar a &quot; root\cimv2: StdRegProv &quot; .</span><span class="sxs-lookup"><span data-stu-id="ed0af-143"><strong>StdRegProv</strong> is not part of the cimv2 namespace, which is why an &quot;Invalid Class&quot; error is generated if you try to connect to &quot;root\cimv2:StdRegProv&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-144">VB</span><span class="sxs-lookup"><span data-stu-id="ed0af-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;) 
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER, strKeyPath, strValueName, dwValue
Wscript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed0af-145">... verificar a segurança em uma chave de Registro específica?</span><span class="sxs-lookup"><span data-stu-id="ed0af-145">...check security on a specific registry key?</span></span></td>
<td><p><span data-ttu-id="ed0af-146">Use a classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , localizada no namespace root\default e no método <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-146">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> method.</span></span> <span data-ttu-id="ed0af-147">Você só pode verificar os direitos de acesso para o usuário atual que está executando o script ou o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed0af-147">You can only check the access rights for the current user that is running the script or application.</span></span> <span data-ttu-id="ed0af-148">Você não pode verificar os direitos de acesso de outro usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="ed0af-148">You cannot check the access rights for another specified user.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed0af-149">... ler e gravar valores de registro binários?</span><span class="sxs-lookup"><span data-stu-id="ed0af-149">...read and write binary registry values?</span></span></td>
<td><p><span data-ttu-id="ed0af-150">Use a classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , localizada no &quot; &quot; namespace Root\Default e os métodos <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>Getbinaryvalue</strong></a> e <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-150">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in &quot;Root\Default&quot; namespace and the <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> methods.</span></span> <span data-ttu-id="ed0af-151">Os valores do registro que aparecem no utilitário RegEdt32 como uma série de valores hexadecimais de bytes estão no formato de dados <strong>REG_BINARY</strong> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-151">Registry values that appear in the RegEdt32 utility as a series of byte hexadecimal values are in the <strong>REG_BINARY</strong> data format.</span></span> <span data-ttu-id="ed0af-152">Para obter mais informações, consulte <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mapeando um tipo de dados do registro para um tipo de dados do WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="ed0af-152">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="ed0af-153">O exemplo de código VBScript a seguir cria uma nova chave com um valor binário.</span><span class="sxs-lookup"><span data-stu-id="ed0af-153">The following VBScript code example creates a new key with a binary value.</span></span> <span data-ttu-id="ed0af-154">O valor binário é fornecido na matriz de bytes <em>iValues</em> especificada em Hex.</span><span class="sxs-lookup"><span data-stu-id="ed0af-154">The binary value is supplied in the <em>iValues</em> byte array specified in Hex.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-155">VB</span><span class="sxs-lookup"><span data-stu-id="ed0af-155">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&H01,&Ha2,&H10)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
strKeyPath = &quot;SOFTWARE\NewKey&quot;
BinaryValueName = &quot;Example Binary Value&quot;

oReg.SetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,BinaryValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="ed0af-156">O script a seguir lê o valor binário.</span><span class="sxs-lookup"><span data-stu-id="ed0af-156">The following script reads the binary value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-157">VB</span><span class="sxs-lookup"><span data-stu-id="ed0af-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002 
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strValueName = &quot;Example Binary Value&quot;
strComputer = &quot;.&quot;
dim iValues(3)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.GetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,iValues
For i = lBound(iValues) to uBound(iValues)
Wscript.Echo iValues(i)
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-158">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed0af-158">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example Binary Value&quot;
$Values     = @(0x54, 0x46, 0x4C)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.GetBinaryValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
Foreach ($byte in $results.uvalue) {&quot;{0}&quot; -f $byte.tostring(&quot;x&quot;)}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed0af-159">... ler e gravar valores de registro que contêm várias cadeias de caracteres?</span><span class="sxs-lookup"><span data-stu-id="ed0af-159">...read and write registry values that contain multiple strings?</span></span></td>
<td><p><span data-ttu-id="ed0af-160">Use a classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , localizada no namespace root\default e nos métodos <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> e <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-160">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> methods.</span></span> <span data-ttu-id="ed0af-161">As chaves do registro que aparecem no utilitário RegEdt32 como uma série de cadeias de caracteres separadas por espaços estão no formato de dados <strong>REG_MULTI_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-161">Registry keys that appear in the RegEdt32 utility as a series of strings separated by spaces are in the <strong>REG_MULTI_SZ</strong> data format.</span></span> <span data-ttu-id="ed0af-162">Para obter mais informações, consulte <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mapeando um tipo de dados do registro para um tipo de dados do WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="ed0af-162">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="ed0af-163">O exemplo de código VBScript a seguir cria uma nova chave e um novo valor multistring.</span><span class="sxs-lookup"><span data-stu-id="ed0af-163">The following VBScript code example creates a new key and a new multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-164">VB</span><span class="sxs-lookup"><span data-stu-id="ed0af-164">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
MultValueName = &quot;Example Multistring Value&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
oReg.SetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-165">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed0af-165">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$Values     = @(&quot;Thomas&quot;, &quot;Susan&quot;, &quot;Rebecca&quot;)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Values)
If ($results.Returnvalue -eq 0) {&quot;Value Set&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="ed0af-166">O script a seguir lê o valor de multistring.</span><span class="sxs-lookup"><span data-stu-id="ed0af-166">The following script reads the multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-167">VB</span><span class="sxs-lookup"><span data-stu-id="ed0af-167">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
MultValueName = &quot;Example Multistring Value&quot;
oReg.GetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues
For Each strValue In iValues
WScript.echo strValue
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-168">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed0af-168">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Define Constants
$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$results   = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
$results.svalue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed0af-169">... remover uma chave do registro?</span><span class="sxs-lookup"><span data-stu-id="ed0af-169">...remove a registry key?</span></span></td>
<td><p><span data-ttu-id="ed0af-170">Use a classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , localizada no namespace root\default e nos métodos <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed0af-170">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed0af-171">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed0af-171">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.DeleteKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key Removed&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ed0af-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed0af-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed0af-173">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="ed0af-173">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="ed0af-174">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="ed0af-174">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="ed0af-175">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="ed0af-175">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> <dt>

[<span data-ttu-id="ed0af-176">Modificando o registro do sistema</span><span class="sxs-lookup"><span data-stu-id="ed0af-176">Modifying the System Registry</span></span>](modifying-the-system-registry.md)
</dt> <dt>

[<span data-ttu-id="ed0af-177">**StdRegProv**</span><span class="sxs-lookup"><span data-stu-id="ed0af-177">**StdRegProv**</span></span>](/previous-versions/windows/desktop/regprov/stdregprov)
</dt> </dl>
