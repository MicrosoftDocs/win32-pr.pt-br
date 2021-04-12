---
title: Compilador de mensagem (MC.exe)
description: Usado para compilar manifestos de instrumentação e arquivos de texto de mensagem.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Log de mensagens (MC.exe) EventLog
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501097"
---
# <a name="message-compiler-mcexe"></a><span data-ttu-id="9a938-104">Compilador de mensagem (MC.exe)</span><span class="sxs-lookup"><span data-stu-id="9a938-104">Message Compiler (MC.exe)</span></span>

<span data-ttu-id="9a938-105">Usado para compilar manifestos de instrumentação e arquivos de texto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9a938-105">Used to compile instrumentation manifests and message text files.</span></span> <span data-ttu-id="9a938-106">O compilador gera os arquivos de recurso de mensagem para os quais seu aplicativo se vincula.</span><span class="sxs-lookup"><span data-stu-id="9a938-106">The compiler generates the message resource files to which your application links.</span></span>

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [<span data-ttu-id="9a938-107">Argumentos comuns a arquivos de texto de mensagem e arquivos de manifesto</span><span class="sxs-lookup"><span data-stu-id="9a938-107">Arguments common to both message text files and manifest files</span></span>](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [<span data-ttu-id="9a938-108">Argumentos específicos para arquivos de manifesto</span><span class="sxs-lookup"><span data-stu-id="9a938-108">Arguments specific to manifest files</span></span>](#arguments-specific-to-manifest-files)
-   [<span data-ttu-id="9a938-109">Argumentos específicos para gerar código que seu provedor usaria para registrar eventos</span><span class="sxs-lookup"><span data-stu-id="9a938-109">Arguments specific to generating code that your provider would use to log events</span></span>](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [<span data-ttu-id="9a938-110">Argumentos específicos para arquivos de texto de mensagem</span><span class="sxs-lookup"><span data-stu-id="9a938-110">Arguments specific to message text files</span></span>](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a><span data-ttu-id="9a938-111">Argumentos comuns a arquivos de texto de mensagem e arquivos de manifesto</span><span class="sxs-lookup"><span data-stu-id="9a938-111">Arguments common to both message text files and manifest files</span></span>

<dl> <dt>

<span data-ttu-id="9a938-112"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="9a938-112"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-113">Exibe as informações de uso para o compilador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9a938-113">Displays the usage information for the Message Compiler.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-114"><span id="-c"></span><span id="-C"></span>**-c**</span><span class="sxs-lookup"><span data-stu-id="9a938-114"><span id="-c"></span><span id="-C"></span>**-c**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-115">Use este argumento para fazer com que o compilador defina o bit do cliente (bit 28) em todas as IDs de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9a938-115">Use this argument to have the compiler set the customer bit (bit 28) in all message IDs.</span></span> <span data-ttu-id="9a938-116">Para obter informações sobre o bit do cliente, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9a938-116">For information on the customer bit, see winerror.h.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-117"><span id="-cp"></span><span id="-CP"></span>**-CP** *Encoding*</span><span class="sxs-lookup"><span data-stu-id="9a938-117"><span id="-cp"></span><span id="-CP"></span>**-cp** *encoding*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-118">Use este argumento para especificar a codificação de caracteres usada para todos os arquivos de texto gerados.</span><span class="sxs-lookup"><span data-stu-id="9a938-118">Use this argument to specify the character encoding used for all generated text files.</span></span> <span data-ttu-id="9a938-119">Os nomes válidos incluem "ANSI" (padrão), "UTF-8" e "UTF-16".</span><span class="sxs-lookup"><span data-stu-id="9a938-119">Valid names include "ansi" (default), "utf-8", and "utf-16".</span></span> <span data-ttu-id="9a938-120">As codificações Unicode adicionarão uma marca de ordem de byte.</span><span class="sxs-lookup"><span data-stu-id="9a938-120">The Unicode encodings will add a byte order mark.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>*extensão* **-e**</span><span class="sxs-lookup"><span data-stu-id="9a938-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *extension*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-122">Use este argumento para especificar a extensão a ser usada para o arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9a938-122">Use this argument to specify the extension to use for the header file.</span></span> <span data-ttu-id="9a938-123">Você pode especificar até uma extensão de três caracteres, não incluindo o período.</span><span class="sxs-lookup"><span data-stu-id="9a938-123">You can specify up to a three characters extension, not including the period.</span></span> <span data-ttu-id="9a938-124">O padrão é. h.</span><span class="sxs-lookup"><span data-stu-id="9a938-124">The default is .h.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *caminho*</span><span class="sxs-lookup"><span data-stu-id="9a938-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *path*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-126">Use este argumento para especificar a pasta na qual você deseja que o compilador Coloque o arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="9a938-126">Use this argument to specify the folder into which you want the compiler to place the generated header file.</span></span> <span data-ttu-id="9a938-127">O padrão é o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="9a938-127">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *comprimento*</span><span class="sxs-lookup"><span data-stu-id="9a938-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *length*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-129">Use este argumento para que o compilador gere um aviso se a mensagem exceder caracteres de *comprimento* .</span><span class="sxs-lookup"><span data-stu-id="9a938-129">Use this argument to have the compiler generate a warning if the any message exceeds *length* characters.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *caminho*</span><span class="sxs-lookup"><span data-stu-id="9a938-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-131">Use este argumento para especificar a pasta na qual você deseja que o compilador Coloque o script do compilador de recurso gerado (arquivo. rc) e os arquivos. bin gerados (recursos binários) que o script do compilador de recurso inclui.</span><span class="sxs-lookup"><span data-stu-id="9a938-131">Use this argument to specify the folder into which you want the compiler to place the generated resource compiler script (.rc file) and the generated .bin files (binary resources) that the resource compiler script includes.</span></span> <span data-ttu-id="9a938-132">O padrão é o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="9a938-132">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *nome*</span><span class="sxs-lookup"><span data-stu-id="9a938-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *name*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-134">Use este argumento para substituir o nome de base padrão que o compilador usa para os arquivos que ele gera.</span><span class="sxs-lookup"><span data-stu-id="9a938-134">Use this argument to override the default base name that the compiler uses for the files that it generates.</span></span> <span data-ttu-id="9a938-135">O padrão é usar o nome de base do arquivo de entrada *filename* .</span><span class="sxs-lookup"><span data-stu-id="9a938-135">The default is to use the base name of the *filename* input file.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-136"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="9a938-136"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-137">O arquivo de manifesto de instrumentação ou o arquivo de texto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9a938-137">The instrumentation manifest file or message text file.</span></span> <span data-ttu-id="9a938-138">O arquivo deve existir no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="9a938-138">The file must exist in the current directory.</span></span> <span data-ttu-id="9a938-139">Você pode especificar um arquivo de manifesto, um arquivo de texto de mensagem ou ambos.</span><span class="sxs-lookup"><span data-stu-id="9a938-139">You can specify a manifest file, message text file, or both.</span></span> <span data-ttu-id="9a938-140">O nome do arquivo deve incluir a extensão.</span><span class="sxs-lookup"><span data-stu-id="9a938-140">The file name must include the extension.</span></span> <span data-ttu-id="9a938-141">A Convenção é usar uma extensão. Man para arquivos de manifesto e uma extensão. MC para arquivos de texto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9a938-141">The convention is to use a .man extension for manifest files and a .mc extension for message text files.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a><span data-ttu-id="9a938-142">Argumentos específicos para arquivos de manifesto</span><span class="sxs-lookup"><span data-stu-id="9a938-142">Arguments specific to manifest files</span></span>

<dl> <dt>

<span data-ttu-id="9a938-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *caminho*</span><span class="sxs-lookup"><span data-stu-id="9a938-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *path*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-144">Use este argumento para criar uma linha de base de sua instrumentação.</span><span class="sxs-lookup"><span data-stu-id="9a938-144">Use this argument to create a baseline of your instrumentation.</span></span> <span data-ttu-id="9a938-145">Especifique o caminho para a pasta que contém os arquivos de manifesto de linha de base.</span><span class="sxs-lookup"><span data-stu-id="9a938-145">Specify the path to the folder that contains your baseline manifest files.</span></span> <span data-ttu-id="9a938-146">Para versões subsequentes, você usará o argumento **-t** para verificar o novo manifesto em relação à linha de base para problemas de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="9a938-146">For subsequent releases, you would then use the **-t** argument to check the new manifest against the baseline for compatibility issues.</span></span>

<span data-ttu-id="9a938-147">**Antes do MC versão 1.12.7051:** Não disponível</span><span class="sxs-lookup"><span data-stu-id="9a938-147">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="9a938-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *caminho*</span><span class="sxs-lookup"><span data-stu-id="9a938-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *path*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-149">Use esse argumento quando você criar uma nova versão do seu manifesto e quiser verificá-la para compatibilidade de aplicativos em relação à linha de base que você criou usando o argumento **-s** .</span><span class="sxs-lookup"><span data-stu-id="9a938-149">Use this argument when you create a new version of your manifest and want to check it for application compatibility against the baseline that you created using the **-s** argument.</span></span> <span data-ttu-id="9a938-150">O caminho deve apontar para a pasta que contém o. Arquivos BIN que a operação de linha de base criou (consulte a opção **-s** ).</span><span class="sxs-lookup"><span data-stu-id="9a938-150">The path must point to the folder that contains the .BIN files that the baseline operation created (see the **-s** switch).</span></span>

<span data-ttu-id="9a938-151">**Antes do MC versão 1.12.7051:** Não disponível</span><span class="sxs-lookup"><span data-stu-id="9a938-151">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="9a938-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *caminho*</span><span class="sxs-lookup"><span data-stu-id="9a938-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *path*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-153">O compilador ignora esse argumento e valida automaticamente o manifesto.</span><span class="sxs-lookup"><span data-stu-id="9a938-153">The compiler ignores this argument and automatically validates the manifest.</span></span>

<span data-ttu-id="9a938-154">**Antes do MC versão 1.12.7051:** Use este argumento para especificar a pasta que contém o arquivo de esquema eventer. xsd, que o compilador usa para validar seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="9a938-154">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Eventman.xsd schema file, which the compiler uses to validate your manifest.</span></span> <span data-ttu-id="9a938-155">A SDK do Windows inclui o arquivo de esquema eventer. xsd na \\ pasta include.</span><span class="sxs-lookup"><span data-stu-id="9a938-155">The Windows SDK includes the Eventman.xsd schema file in the \\Include folder.</span></span> <span data-ttu-id="9a938-156">Se você não especificar esse argumento, o compilador não validará seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="9a938-156">If you do not specify this argument, the compiler does not validate your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *caminho*</span><span class="sxs-lookup"><span data-stu-id="9a938-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *path*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-158">O compilador ignora esse argumento.</span><span class="sxs-lookup"><span data-stu-id="9a938-158">The compiler ignores this argument.</span></span>

<span data-ttu-id="9a938-159">**Antes do MC versão 1.12.7051:** Use este argumento para especificar a pasta que contém o arquivo de Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="9a938-159">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Winmeta.xml file.</span></span> <span data-ttu-id="9a938-160">O arquivo de Winmeta.xml contém os tipos de entrada e saída reconhecidos, bem como os canais, níveis e opcodes predefinidos.</span><span class="sxs-lookup"><span data-stu-id="9a938-160">The Winmeta.xml file contains the recognized input and output types as well as the predefined channels, levels, and opcodes.</span></span> <span data-ttu-id="9a938-161">A SDK do Windows inclui o arquivo de Winmeta.xml na \\ pasta include.</span><span class="sxs-lookup"><span data-stu-id="9a938-161">The Windows SDK includes the Winmeta.xml file in the \\Include folder.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a><span data-ttu-id="9a938-162">Argumentos específicos para gerar código que seu provedor usaria para registrar eventos</span><span class="sxs-lookup"><span data-stu-id="9a938-162">Arguments specific to generating code that your provider would use to log events</span></span>

<span data-ttu-id="9a938-163">Você pode usar os seguintes argumentos do compilador para gerar o código do modo kernel ou do modo de usuário que você pode usar para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="9a938-163">You can use the following compiler arguments to generate kernel-mode or user-mode code that you can use to log events.</span></span> <span data-ttu-id="9a938-164">Você também pode solicitar que o compilador gere código para dar suporte à gravação de eventos em computadores anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a938-164">You can also request that the compiler generate code to support writing events on computers prior to Windows Vista.</span></span> <span data-ttu-id="9a938-165">Se seu aplicativo for escrito em C#, o compilador poderá gerar uma classe C# que você pode usar para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="9a938-165">If your application is written C#, the compiler can generate a C# class that you can use to log events.</span></span> <span data-ttu-id="9a938-166">Esses argumentos estão disponíveis a partir do MC versão 1.12.7051 que acompanha a versão do Windows 7 do SDK do Window.</span><span class="sxs-lookup"><span data-stu-id="9a938-166">These arguments are available beginning with MC version 1.12.7051 that ships with the Windows 7 version of the Window SDK.</span></span>

<dl> <dt>

<span data-ttu-id="9a938-167"><span id="-co"></span><span id="-CO"></span>**-co**</span><span class="sxs-lookup"><span data-stu-id="9a938-167"><span id="-co"></span><span id="-CO"></span>**-co**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-168">Use este argumento para fazer com que o serviço de log chame sua função definida pelo usuário para cada evento que você registrar (a função é chamada após o registro do evento).</span><span class="sxs-lookup"><span data-stu-id="9a938-168">Use this argument to have the logging service call your user-defined function for each event that you log (the function is called after the event has been logged).</span></span> <span data-ttu-id="9a938-169">Sua função definida pelo usuário deve ter a assinatura a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a938-169">Your user-defined function must have the following signature.</span></span>


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



<span data-ttu-id="9a938-170">Você também deve incluir a diretiva a seguir em seu código.</span><span class="sxs-lookup"><span data-stu-id="9a938-170">You must also include the following directive in your code.</span></span>

`#define MCGEN_CALLOUT pFnUserFunction`

<span data-ttu-id="9a938-171">Você deve manter sua implementação o mais curta possível para evitar problemas de log; o serviço não registrará mais os eventos até que a função seja retornada.</span><span class="sxs-lookup"><span data-stu-id="9a938-171">You should keep your implementation as short as possible to prevent logging issues; the service will not log anymore of your events until the function returns.</span></span>

<span data-ttu-id="9a938-172">Você pode usar esse argumento com o argumento **-km** ou **-um** .</span><span class="sxs-lookup"><span data-stu-id="9a938-172">You can use this argument with the **-km** or **-um** argument.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*</span><span class="sxs-lookup"><span data-stu-id="9a938-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-174">Use este argumento para que o compilador gere uma classe C# com base na classe .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="9a938-174">Use this argument to have the compiler generate a C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-namespace de CSS** </span><span class="sxs-lookup"><span data-stu-id="9a938-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-176">Use este argumento para que o compilador gere uma classe C# estática com base na classe .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="9a938-176">Use this argument to have the compiler generate a static C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-177"><span id="-km"></span><span id="-KM"></span>**-km**</span><span class="sxs-lookup"><span data-stu-id="9a938-177"><span id="-km"></span><span id="-KM"></span>**-km**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-178">Use este argumento para que o compilador gere o código do modo kernel que você usaria para registrar os eventos definidos em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="9a938-178">Use this argument to have the compiler generate the kernel-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-179"><span id="-mof"></span><span id="-MOF"></span>**-MOF**</span><span class="sxs-lookup"><span data-stu-id="9a938-179"><span id="-mof"></span><span id="-MOF"></span>**-mof**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-180">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9a938-180">DEPRECATED.</span></span> <span data-ttu-id="9a938-181">Use este argumento para que o compilador gere código que você pode usar para registrar eventos em computadores anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a938-181">Use this argument to have the compiler generate code that you can use to log events on computers prior to Windows Vista.</span></span> <span data-ttu-id="9a938-182">Essa opção também cria um arquivo MOF que contém as classes MOF para cada evento definido no manifesto.</span><span class="sxs-lookup"><span data-stu-id="9a938-182">This option also creates a MOF file that contains the MOF classes for each event defined in the manifest.</span></span> <span data-ttu-id="9a938-183">Para registrar as classes no arquivo MOF para que os consumidores possam decodificar os eventos, use o compilador MOF (Mofcomp.exe).</span><span class="sxs-lookup"><span data-stu-id="9a938-183">To register the classes in the MOF file so that consumers can decode the events, use the MOF compiler (Mofcomp.exe).</span></span> <span data-ttu-id="9a938-184">Para obter detalhes sobre como usar o compilador MOF, consulte [formato MOF](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9a938-184">For details on using the MOF compiler, see [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

<span data-ttu-id="9a938-185">Para usar essa opção, você deve aderir às seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="9a938-185">To use this switch, you must adhere to the following restrictions:</span></span>

-   <span data-ttu-id="9a938-186">Cada definição de evento deve incluir a tarefa e os atributos de opcode</span><span class="sxs-lookup"><span data-stu-id="9a938-186">Every event definition must include the task and opcode attributes</span></span>
-   <span data-ttu-id="9a938-187">Cada tarefa deve incluir o atributo eventGuid</span><span class="sxs-lookup"><span data-stu-id="9a938-187">Every task must include the eventGuid attribute</span></span>
-   <span data-ttu-id="9a938-188">Os dados do modelo que as referências do evento não podem conter:</span><span class="sxs-lookup"><span data-stu-id="9a938-188">The template data that the event references cannot contain:</span></span>
    -   <span data-ttu-id="9a938-189">Itens de dados que especificam os tipos de entrada Win: binary ou Win: SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="9a938-189">Data items that specify the win:Binary or win:SYSTEMTIME input types</span></span>
    -   <span data-ttu-id="9a938-190">Estruturas</span><span class="sxs-lookup"><span data-stu-id="9a938-190">Structures</span></span>
    -   <span data-ttu-id="9a938-191">Matrizes de tamanho variável; no entanto, você pode especificar matrizes de comprimento fixo</span><span class="sxs-lookup"><span data-stu-id="9a938-191">Variable sized arrays; however, you can specify fixed length arrays</span></span>
    -   <span data-ttu-id="9a938-192">Tipos de dados de cadeia de caracteres não podem especificar o atributo de comprimento</span><span class="sxs-lookup"><span data-stu-id="9a938-192">String data types cannot specify the length attribute</span></span>

<span data-ttu-id="9a938-193">Você deve usar esse argumento com o argumento **-um**, **-cs**, **-CSS** ou **-km**</span><span class="sxs-lookup"><span data-stu-id="9a938-193">You must use this argument with the **-um**, **-cs**, **-css**, or **-km** argument</span></span>

</dd> <dt>

<span data-ttu-id="9a938-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefixo*</span><span class="sxs-lookup"><span data-stu-id="9a938-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-195">Use este argumento para substituir o prefixo padrão que o compilador usa para os nomes de macro e nomes de método de registro em log.</span><span class="sxs-lookup"><span data-stu-id="9a938-195">Use this argument to override the default prefix that the compiler uses for the logging macro names and method names.</span></span> <span data-ttu-id="9a938-196">O prefixo padrão é "EventWrite".</span><span class="sxs-lookup"><span data-stu-id="9a938-196">The default prefix is "EventWrite".</span></span> <span data-ttu-id="9a938-197">A cadeia de caracteres diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9a938-197">The string is case-sensitive.</span></span>

<span data-ttu-id="9a938-198">Você pode usar esse argumento com o argumento **-um**, **-cs**, **-CSS** ou **-km** .</span><span class="sxs-lookup"><span data-stu-id="9a938-198">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefixo*</span><span class="sxs-lookup"><span data-stu-id="9a938-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-200">Use este argumento para remover os caracteres do início do nome simbólico que você especificou para o evento.</span><span class="sxs-lookup"><span data-stu-id="9a938-200">Use this argument to remove characters from the beginning of the symbolic name that you specified for the event.</span></span> <span data-ttu-id="9a938-201">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9a938-201">The comparison is case-insensitive.</span></span> <span data-ttu-id="9a938-202">O compilador usa o nome simbólico para formar os nomes de macro e nomes de método de registro em log.</span><span class="sxs-lookup"><span data-stu-id="9a938-202">The compiler uses the symbolic name to form the logging macro names and method names.</span></span>

<span data-ttu-id="9a938-203">O nome padrão de uma macro de registro em log é EventWrite *symbolname*, em que *symbolname* é o nome simbólico que você especificou para o evento.</span><span class="sxs-lookup"><span data-stu-id="9a938-203">The default name for a logging macro is EventWrite *SymbolName*, where *SymbolName* is the symbolic name that you specified for the event.</span></span> <span data-ttu-id="9a938-204">Por exemplo, se você definir o atributo Symbol do evento como PrinterConnection, o nome da macro será EventWritePrinterConnection.</span><span class="sxs-lookup"><span data-stu-id="9a938-204">For example, if you set the symbol attribute of the event to PrinterConnection, the macro name would be EventWritePrinterConnection.</span></span> <span data-ttu-id="9a938-205">Para remover a impressora do nome, use **-P** **Printer**, que resulta em EventWriteConnection.</span><span class="sxs-lookup"><span data-stu-id="9a938-205">To remove Printer from the name, use **-P** **Printer**, which results in EventWriteConnection.</span></span>

<span data-ttu-id="9a938-206">Você pode usar esse argumento com o argumento **-um**, **-cs**, **-CSS** ou **-km** .</span><span class="sxs-lookup"><span data-stu-id="9a938-206">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-207"><span id="-um"></span><span id="-UM"></span>**-um**</span><span class="sxs-lookup"><span data-stu-id="9a938-207"><span id="-um"></span><span id="-UM"></span>**-um**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-208">Use este argumento para que o compilador gere o código de modo de usuário que você usaria para registrar os eventos definidos em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="9a938-208">Use this argument to have the compiler generate the user-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> </dl>

<span data-ttu-id="9a938-209">Para que o compilador gere o código de registro em log, você deve especificar o argumento **-um**, **-cs**, **-CSS** ou **-km** ; esses argumentos são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="9a938-209">To have the compiler generate logging code, you must specify the **-um**, **-cs**, **-css**, or **-km** argument; these arguments are mutually exclusive.</span></span>

<span data-ttu-id="9a938-210">Para especificar onde posicionar os arquivos. h,. cs e. mof gerados pelo compilador, use o argumento **-h** .</span><span class="sxs-lookup"><span data-stu-id="9a938-210">To specify where to place the .h, .cs, and .mof files that the compiler generates, use the **-h** argument.</span></span> <span data-ttu-id="9a938-211">Se você não especificar o argumento **-h** , os arquivos serão colocados na pasta atual.</span><span class="sxs-lookup"><span data-stu-id="9a938-211">If you do not specify the **-h** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="9a938-212">Para especificar onde posicionar o arquivo. rc e os arquivos binários (que contêm os recursos de metadados) gerados pelo compilador, use o argumento **-r** .</span><span class="sxs-lookup"><span data-stu-id="9a938-212">To specify where to place the .rc file and binary files (that contain the metadata resources) that the compiler generates, use the **-r** argument.</span></span> <span data-ttu-id="9a938-213">Se você não especificar o argumento **-r** , os arquivos serão colocados na pasta atual.</span><span class="sxs-lookup"><span data-stu-id="9a938-213">If you do not specify the **-r** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="9a938-214">O compilador usa o nome base do arquivo de entrada como o nome base dos arquivos que ele gera.</span><span class="sxs-lookup"><span data-stu-id="9a938-214">The compiler uses the base name of the input file as the base name of the files that it generates.</span></span> <span data-ttu-id="9a938-215">Para especificar um nome de base, use o argumento **-z** .</span><span class="sxs-lookup"><span data-stu-id="9a938-215">To specify a base name, use the **-z** argument.</span></span>

### <a name="arguments-specific-to-message-text-files"></a><span data-ttu-id="9a938-216">Argumentos específicos para arquivos de texto de mensagem</span><span class="sxs-lookup"><span data-stu-id="9a938-216">Arguments specific to message text files</span></span>

<dl> <dt>

<span data-ttu-id="9a938-217"><span id="-a"></span><span id="-A"></span>**-a**</span><span class="sxs-lookup"><span data-stu-id="9a938-217"><span id="-a"></span><span id="-A"></span>**-a**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-218">Use este argumento para especificar que o arquivo de entrada de *nome* de arquivos contenha conteúdo na página de código ANSI padrão do Windows (CP_ACP).</span><span class="sxs-lookup"><span data-stu-id="9a938-218">Use this argument to specify that the *filename* input file contains content in the system-default Windows ANSI code page (CP_ACP).</span></span> <span data-ttu-id="9a938-219">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="9a938-219">This is the default.</span></span> <span data-ttu-id="9a938-220">Use **-u** para Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a938-220">Use **-u** for Unicode.</span></span> <span data-ttu-id="9a938-221">Se o arquivo de entrada contiver uma BOM, esse argumento será ignorado.</span><span class="sxs-lookup"><span data-stu-id="9a938-221">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-222"><span id="-A"></span><span id="-a"></span>**-A**</span><span class="sxs-lookup"><span data-stu-id="9a938-222"><span id="-A"></span><span id="-a"></span>**-A**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-223">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9a938-223">DEPRECATED.</span></span> <span data-ttu-id="9a938-224">Use este argumento para especificar que as mensagens no arquivo output. bin devem ser ANSI.</span><span class="sxs-lookup"><span data-stu-id="9a938-224">Use this argument to specify that the messages in the output .bin file should be ANSI.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-225"><span id="-b"></span><span id="-B"></span>**-b**</span><span class="sxs-lookup"><span data-stu-id="9a938-225"><span id="-b"></span><span id="-B"></span>**-b**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-226">Use este argumento para fazer com que o compilador use o nome base do arquivo de entrada de *nome* de arquivo para os nomes de arquivos. bin.</span><span class="sxs-lookup"><span data-stu-id="9a938-226">Use this argument to have the compiler use the base name of the *filename* input file for the .bin file names.</span></span> <span data-ttu-id="9a938-227">O padrão é usar "MSG".</span><span class="sxs-lookup"><span data-stu-id="9a938-227">The default is to use "MSG".</span></span>

</dd> <dt>

<span data-ttu-id="9a938-228"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="9a938-228"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-229">Use este argumento para usar valores decimais para as constantes de severidade e instalação no arquivo de cabeçalho em vez de valores hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="9a938-229">Use this argument to use decimal values for the Severity and Facility constants in the header file instead of hexadecimal values.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-230"><span id="-n"></span><span id="-N"></span>**-n**</span><span class="sxs-lookup"><span data-stu-id="9a938-230"><span id="-n"></span><span id="-N"></span>**-n**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-231">Use este argumento para especificar que as mensagens sejam encerradas imediatamente após o corpo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="9a938-231">Use this argument to specify that messages terminate immediately after the message body.</span></span> <span data-ttu-id="9a938-232">O padrão é encerrar o corpo da mensagem com uma CR/LF.</span><span class="sxs-lookup"><span data-stu-id="9a938-232">The default is to terminate the message body with a CR/LF.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-233"><span id="-o"></span><span id="-O"></span>**-o**</span><span class="sxs-lookup"><span data-stu-id="9a938-233"><span id="-o"></span><span id="-O"></span>**-o**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-234">Use este argumento para fazer com que o compilador gere um arquivo de cabeçalho OLE2 usando definições **HRESULT** em vez de códigos de status.</span><span class="sxs-lookup"><span data-stu-id="9a938-234">Use this argument to have the compiler generate an OLE2 header file using **HRESULT** definitions instead of status codes.</span></span> <span data-ttu-id="9a938-235">O uso de códigos de status é o padrão.</span><span class="sxs-lookup"><span data-stu-id="9a938-235">Using status codes is the default.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-236"><span id="-u"></span><span id="-U"></span>**-u**</span><span class="sxs-lookup"><span data-stu-id="9a938-236"><span id="-u"></span><span id="-U"></span>**-u**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-237">Use este argumento para especificar que o arquivo de entrada *filename* contém conteúdo UTF-16LE.</span><span class="sxs-lookup"><span data-stu-id="9a938-237">Use this argument to specify that the *filename* input file contains UTF-16LE content.</span></span> <span data-ttu-id="9a938-238">O padrão é o conteúdo ANSI.</span><span class="sxs-lookup"><span data-stu-id="9a938-238">The default is ANSI content.</span></span> <span data-ttu-id="9a938-239">Se o arquivo de entrada contiver uma BOM, esse argumento será ignorado.</span><span class="sxs-lookup"><span data-stu-id="9a938-239">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-240"><span id="-U"></span><span id="-u"></span>**-U**</span><span class="sxs-lookup"><span data-stu-id="9a938-240"><span id="-U"></span><span id="-u"></span>**-U**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-241">Use este argumento para especificar que as mensagens no arquivo output. bin devem ser Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a938-241">Use this argument to specify that the messages in the output .bin file should be Unicode.</span></span> <span data-ttu-id="9a938-242">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="9a938-242">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-243"><span id="-v"></span><span id="-V"></span>**-v**</span><span class="sxs-lookup"><span data-stu-id="9a938-243"><span id="-v"></span><span id="-V"></span>**-v**</span></span>
</dt> <dd>

<span data-ttu-id="9a938-244">Use este argumento para gerar saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="9a938-244">Use this argument to generate verbose output.</span></span>

</dd> <dt>

<span data-ttu-id="9a938-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *caminho*</span><span class="sxs-lookup"><span data-stu-id="9a938-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*</span></span>
</dt> <dd>

<span data-ttu-id="9a938-246">Use este argumento para especificar a pasta na qual você deseja que o compilador Coloque o arquivo de inclusão C. dbg.</span><span class="sxs-lookup"><span data-stu-id="9a938-246">Use this argument to specify the folder into which you want the compiler to place the .dbg C include file.</span></span> <span data-ttu-id="9a938-247">O arquivo. dbg mapeia IDs de mensagem para seus nomes simbólicos.</span><span class="sxs-lookup"><span data-stu-id="9a938-247">The .dbg file maps message IDs to their symbolic names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a938-248">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a938-248">Remarks</span></span>

<span data-ttu-id="9a938-249">Os argumentos **-** a e **-MOF** são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="9a938-249">The **-A** and **-mof** arguments are deprecated and will be removed in the future.</span></span>

<span data-ttu-id="9a938-250">O compilador aceita como entrada um arquivo de manifesto (. Man) ou um arquivo de texto de mensagem (. MC) e gera os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="9a938-250">The compiler accepts as input a manifest (.man) file or a message text (.mc) file and generates the following files:</span></span>

-   <span data-ttu-id="9a938-251">*nome do arquivo*. h</span><span class="sxs-lookup"><span data-stu-id="9a938-251">*filename*.h</span></span>

    <span data-ttu-id="9a938-252">Um arquivo de cabeçalho C/C++ que contém os descritores de eventos, o GUID do provedor e os nomes de símbolo que você faz referência em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a938-252">A C/C++ header file that contains the event descriptors, provider GUID, and symbol names that you reference in your application.</span></span>

-   <span data-ttu-id="9a938-253">*nome do arquivo* TEMP. bin</span><span class="sxs-lookup"><span data-stu-id="9a938-253">*filename* TEMP.bin</span></span>

    <span data-ttu-id="9a938-254">Um arquivo de recurso binário que contém os metadados do provedor e do evento.</span><span class="sxs-lookup"><span data-stu-id="9a938-254">A binary resource file that contains the provider and event metadata.</span></span> <span data-ttu-id="9a938-255">Esse é o recurso de modelo, que é representado pelo sufixo temporário do nome de base do arquivo.</span><span class="sxs-lookup"><span data-stu-id="9a938-255">This is the template resource, which is signified by the TEMP suffix of the base name of the file.</span></span>

-   <span data-ttu-id="9a938-256">Msg00001. bin</span><span class="sxs-lookup"><span data-stu-id="9a938-256">Msg00001.bin</span></span>

    <span data-ttu-id="9a938-257">Um arquivo de recurso binário para cada idioma que você especificar (por exemplo, se o seu manifesto contiver cadeias de caracteres de mensagem em en-US e fr-FR, o compilador geraria Msg00001. bin e Msg00002. bin).</span><span class="sxs-lookup"><span data-stu-id="9a938-257">A binary resource file for each language that you specify (for example, if your manifest contains message strings in en-US and fr-FR, the compiler would generate Msg00001.bin and Msg00002.bin).</span></span>

-   <span data-ttu-id="9a938-258">*nome do arquivo*. rc</span><span class="sxs-lookup"><span data-stu-id="9a938-258">*filename*.rc</span></span>

    <span data-ttu-id="9a938-259">Um script de compilador de recurso que contém as instruções para incluir cada arquivo. bin como um recurso.</span><span class="sxs-lookup"><span data-stu-id="9a938-259">A resource compiler script that contains the statements to include each .bin file as a resource.</span></span>

<span data-ttu-id="9a938-260">Para argumentos que usam um caminho, o caminho pode ser um caminho absoluto, relativo ou UNC e pode conter variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="9a938-260">For arguments that take a path, the path can be an absolute, relative, or UNC path and it can contain environment variables.</span></span>

<span data-ttu-id="9a938-261">**Antes do MC versão 1.12.7051:** O compilador não permite caminhos relativos ou variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="9a938-261">**Prior to MC version 1.12.7051:** The compiler does not allow relative paths or environment variables.</span></span>

<span data-ttu-id="9a938-262">A SDK do Windows inclui o compilador (mc.exe) na \\ pasta bin.</span><span class="sxs-lookup"><span data-stu-id="9a938-262">The Windows SDK includes the compiler (mc.exe) in the \\Bin folder.</span></span>

## <a name="examples"></a><span data-ttu-id="9a938-263">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a938-263">Examples</span></span>

<span data-ttu-id="9a938-264">O exemplo a seguir compila um manifesto usando os padrões do compilador.</span><span class="sxs-lookup"><span data-stu-id="9a938-264">The following example compiles a manifest using the compiler defaults.</span></span>

``` syntax
mc spooler.man
```

<span data-ttu-id="9a938-265">O exemplo a seguir compila o manifesto e coloca os arquivos de cabeçalho e de recurso nas pastas especificadas.</span><span class="sxs-lookup"><span data-stu-id="9a938-265">The following example compiles the manifest and places the header and resource files in the specified folders.</span></span>

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a><span data-ttu-id="9a938-266">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a938-266">Requirements</span></span>

| <span data-ttu-id="9a938-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a938-267">Requirement</span></span> | <span data-ttu-id="9a938-268">Valor</span><span class="sxs-lookup"><span data-stu-id="9a938-268">Value</span></span> |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="9a938-269">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a938-269">Minimum supported client</span></span> | <span data-ttu-id="9a938-270">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a938-270">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="9a938-271">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a938-271">Minimum supported server</span></span> | <span data-ttu-id="9a938-272">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a938-272">Windows 2000 Server \[desktop apps only\]</span></span>       |
