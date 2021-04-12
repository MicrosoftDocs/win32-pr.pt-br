---
title: Tipo complexo channelType
description: Define um canal para o qual os provedores podem registrar eventos.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- EventLog tipo complexo de channelType
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455622"
---
# <a name="channeltype-complex-type"></a><span data-ttu-id="1c5d1-104">Tipo complexo channelType</span><span class="sxs-lookup"><span data-stu-id="1c5d1-104">ChannelType Complex Type</span></span>

<span data-ttu-id="1c5d1-105">Define um canal para o qual os provedores podem registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-105">Defines a channel to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1c5d1-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1c5d1-106">Child elements</span></span>



| <span data-ttu-id="1c5d1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1c5d1-107">Element</span></span>                                                                  | <span data-ttu-id="1c5d1-108">Type</span><span class="sxs-lookup"><span data-stu-id="1c5d1-108">Type</span></span>                                                                                   | <span data-ttu-id="1c5d1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c5d1-109">Description</span></span>                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c5d1-110">**logout**</span><span class="sxs-lookup"><span data-stu-id="1c5d1-110">**logging**</span></span>](eventmanifestschema-logging-channeltype-element.md)       | [<span data-ttu-id="1c5d1-111">**ChannelLoggingType**</span><span class="sxs-lookup"><span data-stu-id="1c5d1-111">**ChannelLoggingType**</span></span>](eventmanifestschema-channelloggingtype-complextype.md)       | <span data-ttu-id="1c5d1-112">Define as propriedades do arquivo de log que faz o backup do canal, como sua capacidade e se o arquivo de log é sequencial ou circular.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-112">Defines the properties of the log file that backs the channel, such as its capacity and whether the log file is sequential or circular.</span></span><br/>                                                         |
| [<span data-ttu-id="1c5d1-113">**editor**</span><span class="sxs-lookup"><span data-stu-id="1c5d1-113">**publishing**</span></span>](eventmanifestschema-publishing-channeltype-element.md) | [<span data-ttu-id="1c5d1-114">**ChannelPublishingType**</span><span class="sxs-lookup"><span data-stu-id="1c5d1-114">**ChannelPublishingType**</span></span>](eventmanifestschema-channelpublishingtype-complextype.md) | <span data-ttu-id="1c5d1-115">Define as propriedades de log para a sessão que o canal usa.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-115">Defines the logging properties for the session that the channel uses.</span></span> <span data-ttu-id="1c5d1-116">Somente canais de depuração e de análise e canais que usam o isolamento personalizado podem especificar propriedades de log para sua sessão.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-116">Only Debug and Analytic channels and channels that use Custom isolation can specify logging properties for their session.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="1c5d1-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="1c5d1-117">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c5d1-118">Nome</span><span class="sxs-lookup"><span data-stu-id="1c5d1-118">Name</span></span></th>
<th><span data-ttu-id="1c5d1-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c5d1-119">Type</span></span></th>
<th><span data-ttu-id="1c5d1-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c5d1-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c5d1-121">access</span><span class="sxs-lookup"><span data-stu-id="1c5d1-121">access</span></span></td>
<td><span data-ttu-id="1c5d1-122">string</span><span class="sxs-lookup"><span data-stu-id="1c5d1-122">string</span></span></td>
<td><span data-ttu-id="1c5d1-123">Um descritor de acesso SDDL ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">linguagem de definição de descritor de segurança</a> ) que controla o acesso ao arquivo de log que faz o backup do canal.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-123">A <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL) access descriptor that controls access to the log file that backs the channel.</span></span> <span data-ttu-id="1c5d1-124">Se o atributo de <strong>isolamento</strong> estiver definido como aplicativo ou sistema, o descritor de acesso controlará o acesso de leitura ao arquivo (as permissões de gravação serão ignoradas).</span><span class="sxs-lookup"><span data-stu-id="1c5d1-124">If the <strong>isolation</strong> attribute is set to Application or System, the access descriptor controls read access to the file (the write permissions are ignored).</span></span> <span data-ttu-id="1c5d1-125">Se o atributo de <strong>isolamento</strong> for definido como personalizado, o descritor de acesso controlará o acesso de gravação ao canal e o acesso de leitura ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-125">If the <strong>isolation</strong> attribute is set to Custom, the access descriptor controls write access to the channel and read access to the file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c5d1-126">chid</span><span class="sxs-lookup"><span data-stu-id="1c5d1-126">chid</span></span></td>
<td><span data-ttu-id="1c5d1-127">token</span><span class="sxs-lookup"><span data-stu-id="1c5d1-127">token</span></span></td>
<td><span data-ttu-id="1c5d1-128">Um identificador que identifica exclusivamente o canal na lista de canais que o provedor define ou importa.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-128">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="1c5d1-129">Use esse valor ao referenciar o canal em um evento.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-129">Use this value when referencing the channel in an event.</span></span> <span data-ttu-id="1c5d1-130">Se você não especificar um identificador de canal, use o nome do canal para fazer referência a esse canal em uma definição de evento.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-130">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c5d1-131">Habilitado</span><span class="sxs-lookup"><span data-stu-id="1c5d1-131">enabled</span></span></td>
<td><span data-ttu-id="1c5d1-132">booleano</span><span class="sxs-lookup"><span data-stu-id="1c5d1-132">boolean</span></span></td>
<td><span data-ttu-id="1c5d1-133">Determina se o canal está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-133">Determines whether the channel is enabled.</span></span> <span data-ttu-id="1c5d1-134">Defina como <strong>true</strong> para permitir o registro em log do canal; caso contrário, <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-134">Set to <strong>true</strong> to allow logging to the channel; otherwise, <strong>false</strong>.</span></span> <span data-ttu-id="1c5d1-135">O padrão é <strong>false</strong> (o registro em log está desabilitado).</span><span class="sxs-lookup"><span data-stu-id="1c5d1-135">The default is <strong>false</strong> (logging is disabled).</span></span><br/> <span data-ttu-id="1c5d1-136">Como os tipos de canal de depuração e de análise são canais de alto volume, você deve habilitar o canal somente ao investigar um problema com um componente que grava nesse canal; caso contrário, o canal deve permanecer desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-136">Because Debug and Analytic channel types are high volume channels, you should enable the channel only when investigating an issue with a component that writes to that channel; otherwise, the channel should remain disabled.</span></span><br/> <span data-ttu-id="1c5d1-137">Cada vez que você habilita um canal de depuração e analítica, o serviço limpa os eventos do canal.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-137">Each time you enable a Debug and Analytic channel, the service clears the events from the channel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c5d1-138">isolamento</span><span class="sxs-lookup"><span data-stu-id="1c5d1-138">isolation</span></span></td>
<td><span data-ttu-id="1c5d1-139">string</span><span class="sxs-lookup"><span data-stu-id="1c5d1-139">string</span></span></td>
<td><span data-ttu-id="1c5d1-140">O valor de isolamento define as permissões de acesso padrão para o canal.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-140">The isolation value defines the default access permissions for the channel.</span></span> <span data-ttu-id="1c5d1-141">É possível especificar um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1c5d1-141">You can specify one of the following values:</span></span>
<ul>
<li><span data-ttu-id="1c5d1-142"><strong>Aplicativo</strong></span><span class="sxs-lookup"><span data-stu-id="1c5d1-142"><strong>Application</strong></span></span></li>
<li><span data-ttu-id="1c5d1-143"><strong>System</strong></span><span class="sxs-lookup"><span data-stu-id="1c5d1-143"><strong>System</strong></span></span></li>
<li><span data-ttu-id="1c5d1-144"><strong>Personalizado</strong></span><span class="sxs-lookup"><span data-stu-id="1c5d1-144"><strong>Custom</strong></span></span></li>
</ul>
<span data-ttu-id="1c5d1-145">O isolamento padrão é <strong>aplicativo</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-145">The default isolation is <strong>Application</strong>.</span></span> <span data-ttu-id="1c5d1-146">As permissões padrão para o <strong>aplicativo</strong> são (mostradas usando SDDL):</span><span class="sxs-lookup"><span data-stu-id="1c5d1-146">The default permissions for <strong>Application</strong> are (shown using SDDL):</span></span> <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c5d1-147">Texto</span><span class="sxs-lookup"><span data-stu-id="1c5d1-147">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="1c5d1-148">As permissões padrão para <strong>System</strong> são (mostradas usando SDDL):</span><span class="sxs-lookup"><span data-stu-id="1c5d1-148">The default permissions for <strong>System</strong> are (shown using SDDL):</span></span></p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c5d1-149">Texto</span><span class="sxs-lookup"><span data-stu-id="1c5d1-149">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="1c5d1-150">As permissões padrão para isolamento <strong>personalizado</strong> são as mesmas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-150">The default permissions for <strong>Custom</strong> isolation is the same as Application.</span></span></p>
<p><span data-ttu-id="1c5d1-151">Os canais que especificam o isolamento de <strong>aplicativo</strong> usam a mesma sessão de ETW.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-151">Channels that specify <strong>Application</strong> isolation use the same ETW session.</span></span> <span data-ttu-id="1c5d1-152">O mesmo é verdadeiro para o isolamento do <strong>sistema</strong> .</span><span class="sxs-lookup"><span data-stu-id="1c5d1-152">The same is true for <strong>System</strong> isolation.</span></span> <span data-ttu-id="1c5d1-153">No entanto, se você especificar o isolamento <strong>personalizado</strong> , o serviço criará uma sessão ETW separada para o canal.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-153">However, if you specify <strong>Custom</strong> isolation, the service creates a separate ETW session for the channel.</span></span> <span data-ttu-id="1c5d1-154">Usar o isolamento <strong>personalizado</strong> permite controlar as permissões de acesso para o canal e o arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-154">Using <strong>Custom</strong> isolation lets you control the access permissions for the channel and backing file.</span></span> <span data-ttu-id="1c5d1-155">Como há apenas 64 sessões de ETW disponíveis, você deve limitar o uso de isolamento <strong>personalizado</strong> .</span><span class="sxs-lookup"><span data-stu-id="1c5d1-155">Because there are only 64 ETW sessions available, you should limit your use of <strong>Custom</strong> isolation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c5d1-156">message</span><span class="sxs-lookup"><span data-stu-id="1c5d1-156">message</span></span></td>
<td><span data-ttu-id="1c5d1-157">string</span><span class="sxs-lookup"><span data-stu-id="1c5d1-157">string</span></span></td>
<td><p><span data-ttu-id="1c5d1-158">O nome de exibição localizado para o canal.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-158">The localized display name for the channel.</span></span> <span data-ttu-id="1c5d1-159">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> do manifesto.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-159">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c5d1-160">name</span><span class="sxs-lookup"><span data-stu-id="1c5d1-160">name</span></span></td>
<td><span data-ttu-id="1c5d1-161">anyURI</span><span class="sxs-lookup"><span data-stu-id="1c5d1-161">anyURI</span></span></td>
<td><p><span data-ttu-id="1c5d1-162">O nome do canal.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-162">The name of the channel.</span></span> <span data-ttu-id="1c5d1-163">O nome deve ser exclusivo na lista de canais que o provedor usa.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-163">The name must be unique within the list of channels that the provider uses.</span></span> <span data-ttu-id="1c5d1-164">A Convenção de nomenclatura de canais é acrescentar o tipo de canal ao nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-164">The convention for naming channels is to append the channel type to the provider's name.</span></span> <span data-ttu-id="1c5d1-165">Por exemplo.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-165">For example.</span></span> <span data-ttu-id="1c5d1-166">Se o nome do provedor for empresa-produto-componente e você estiver definindo um canal operacional, o nome será empresa-produto-componente/operacional.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-166">if the provider's name is Company-Product-Component and you are defining an operational channel, the name would be Company-Product-Component/Operational.</span></span></p>
<p><span data-ttu-id="1c5d1-167">Os nomes de canal devem ter menos de 255 caracteres e não podem conter os seguintes caracteres: ' > ', '</span><span class="sxs-lookup"><span data-stu-id="1c5d1-167">Channel names must be less that 255 characters and cannot contain the following characters: '>', '</span></span><', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c5d1-168">símbolo</span><span class="sxs-lookup"><span data-stu-id="1c5d1-168">symbol</span></span></td>
<td><span data-ttu-id="1c5d1-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="1c5d1-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="1c5d1-170">O símbolo a ser usado para referenciar o canal em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-170">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="1c5d1-171">O <a href="message-compiler--mc-exe-.md"><strong>compilador de mensagem (MC.exe)</strong></a> usa o símbolo para criar uma constante para o canal no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-171">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="1c5d1-172">Se você não especificar um símbolo, o compilador gerará o nome para você.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-172">If you do not specify a symbol, the compiler generates the name for you.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c5d1-173">tipo</span><span class="sxs-lookup"><span data-stu-id="1c5d1-173">type</span></span></td>
<td><span data-ttu-id="1c5d1-174">string</span><span class="sxs-lookup"><span data-stu-id="1c5d1-174">string</span></span></td>
<td><p><span data-ttu-id="1c5d1-175">Identifica o tipo do canal.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-175">Identifies the channel's type.</span></span> <span data-ttu-id="1c5d1-176">Você pode especificar um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="1c5d1-176">You can specify one of the following types:</span></span></p>
<ul>
<li><span data-ttu-id="1c5d1-177"><strong>Administrador</strong></span><span class="sxs-lookup"><span data-stu-id="1c5d1-177"><strong>Admin</strong></span></span></li>
<li><span data-ttu-id="1c5d1-178"><strong>Operacional</strong></span><span class="sxs-lookup"><span data-stu-id="1c5d1-178"><strong>Operational</strong></span></span></li>
<li><span data-ttu-id="1c5d1-179"><strong>Analítico</strong></span><span class="sxs-lookup"><span data-stu-id="1c5d1-179"><strong>Analytic</strong></span></span></li>
<li><span data-ttu-id="1c5d1-180"><strong>Depurar</strong></span><span class="sxs-lookup"><span data-stu-id="1c5d1-180"><strong>Debug</strong></span></span></li>
</ul>
<p><span data-ttu-id="1c5d1-181">Os canais de tipo de administrador dão suporte a eventos que visam usuários finais, administradores e equipe de suporte.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-181">Admin type channels support events that target end users, administrators, and support personnel.</span></span> <span data-ttu-id="1c5d1-182">Os eventos gravados nos canais de administração devem ter uma solução bem definida na qual o administrador possa agir. Um exemplo de um evento de administrador é um evento que ocorre quando um aplicativo não consegue se conectar a uma impressora.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-182">Events written to the Admin channels should have a well-defined solution on which the administrator can act. An example of an admin event is an event that occurs when an application fails to connect to a printer.</span></span> <span data-ttu-id="1c5d1-183">Esses eventos são bem documentados ou têm uma mensagem associada a eles que fornecem instruções de leitura direta sobre o que deve ser feito para retificar o problema.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-183">These events are either well-documented or have a message associated with them that gives the reader direct instructions of what must be done to rectify the problem.</span></span></p>
<p><span data-ttu-id="1c5d1-184">Os canais de tipo operacional dão suporte a eventos que são usados para analisar e diagnosticar um problema ou ocorrência.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-184">Operational type channels support events that are used for analyzing and diagnosing a problem or occurrence.</span></span> <span data-ttu-id="1c5d1-185">Eles podem ser usados para disparar ferramentas ou tarefas com base no problema ou na ocorrência.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-185">They can be used to trigger tools or tasks based on the problem or occurrence.</span></span> <span data-ttu-id="1c5d1-186">Um exemplo de evento operacional é um evento que ocorre quando uma impressora é adicionada ou removida de um sistema.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-186">An example of an operational event is an event that occurs when a printer is added or removed from a system.</span></span></p>
<p><span data-ttu-id="1c5d1-187">Os canais de tipo analítico dão suporte a eventos que são publicados em alto volume.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-187">Analytic type channels support events that are published in high volume.</span></span> <span data-ttu-id="1c5d1-188">Eles descrevem a operação do programa e indicam os problemas que não podem ser tratados por intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-188">They describe program operation and indicate problems that cannot be handled by user intervention.</span></span></p>
<p><span data-ttu-id="1c5d1-189">Os canais de tipo de depuração dão suporte a eventos que são usados exclusivamente por desenvolvedores para diagnosticar um problema de depuração.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-189">Debug type channels support events that are used solely by developers to diagnose a problem for debugging.</span></span></p>
<p><span data-ttu-id="1c5d1-190">Os canais analíticos e de depuração são desabilitados por padrão e só devem ser habilitados para determinar a causa de um problema.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-190">Analytic and debug channels are disabled by default and should only enabled to determine the cause of an issue.</span></span> <span data-ttu-id="1c5d1-191">Por exemplo, você deve habilitar o canal, executar o cenário que está causando o problema, desabilitar o canal e, em seguida, consultar os eventos.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-191">For example, you would enable the channel, run the scenario that is causing the issue, disable the channel, and then query the events.</span></span> <span data-ttu-id="1c5d1-192">Observe que a habilitação do canal limpa o canal de eventos existentes.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-192">Note that enabling the channel clears the channel of existing events.</span></span> <span data-ttu-id="1c5d1-193">Se o canal analítico e de depuração usar um arquivo de backup circular, você deverá desabilitar o canal para consultar seus eventos.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-193">If the analytic and debug channel uses a circular backing file, you must disable the channel to query its events.</span></span></p>
<p><span data-ttu-id="1c5d1-194">Todos os canais de administração usam a mesma sessão de ETW; o mesmo é verdadeiro para canais operacionais.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-194">All Admin channels use the same ETW session; the same is true for Operational channels.</span></span> <span data-ttu-id="1c5d1-195">No entanto, cada canal analítico e de depuração usa uma sessão ETW separada, que é outro motivo para habilitar esses tipos de canal apenas quando necessário (há um número limitado de sessões de ETW disponíveis).</span><span class="sxs-lookup"><span data-stu-id="1c5d1-195">However, each Analytic and Debug channel uses a separate ETW session, which is another reason to only enable these channel types when needed (there is a limited number of ETW sessions available).</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c5d1-196">value</span><span class="sxs-lookup"><span data-stu-id="1c5d1-196">value</span></span></td>
<td><span data-ttu-id="1c5d1-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="1c5d1-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span></span></td>
<td><p><span data-ttu-id="1c5d1-198">Um identificador numérico que identifica exclusivamente o canal dentro da lista de canais que o provedor define.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-198">A numeric identifier that uniquely identifies the channel within the list of channels that the provider defines.</span></span> <span data-ttu-id="1c5d1-199">O compilador de mensagem atribui o valor, se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-199">The message compiler assigns the value if not specified.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="1c5d1-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c5d1-200">Remarks</span></span>

<span data-ttu-id="1c5d1-201">Se o nome do canal seguir a Convenção de nomenclatura de canal, o Visualizador de Eventos do Windows listará o canal usando a cadeia de caracteres que segue a barra invertida.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-201">If the channel's name follows the channel naming convention, the Windows Event Viewer will list the channel using the string that follows the backslash.</span></span> <span data-ttu-id="1c5d1-202">Por exemplo, se o nome do canal for empresa-produto-componente/operacional, a Visualizador de Eventos listará o canal como operacional no provedor da empresa-produto-componente.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-202">For example, if the channel name is Company-Product-Component/Operational, then the Event Viewer will list the channel as Operational under the Company-Product-Component provider.</span></span> <span data-ttu-id="1c5d1-203">Caso contrário, o nome inteiro do canal será mostrado no provedor.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-203">Otherwise, the entire channel name is shown under the provider.</span></span> <span data-ttu-id="1c5d1-204">O nome de exibição localizado é usado, se fornecido.</span><span class="sxs-lookup"><span data-stu-id="1c5d1-204">The localized display name is used if provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5d1-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c5d1-205">Requirements</span></span>



| <span data-ttu-id="1c5d1-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c5d1-206">Requirement</span></span> | <span data-ttu-id="1c5d1-207">Valor</span><span class="sxs-lookup"><span data-stu-id="1c5d1-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c5d1-208">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c5d1-208">Minimum supported client</span></span><br/> | <span data-ttu-id="1c5d1-209">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c5d1-209">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1c5d1-210">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c5d1-210">Minimum supported server</span></span><br/> | <span data-ttu-id="1c5d1-211">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c5d1-211">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




`
