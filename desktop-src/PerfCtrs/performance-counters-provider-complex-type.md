---
description: Define um provedor e os contadores que ele fornece.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: Tipo complexo do provedor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828378"
---
# <a name="provider-complex-type"></a><span data-ttu-id="d225a-103">Tipo complexo do provedor</span><span class="sxs-lookup"><span data-stu-id="d225a-103">provider Complex Type</span></span>

<span data-ttu-id="d225a-104">Define um provedor e os contadores que ele fornece.</span><span class="sxs-lookup"><span data-stu-id="d225a-104">Defines a provider and the counters that it provides.</span></span>

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d225a-105">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d225a-105">Child elements</span></span>



| <span data-ttu-id="d225a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="d225a-106">Element</span></span>        | <span data-ttu-id="d225a-107">Type</span><span class="sxs-lookup"><span data-stu-id="d225a-107">Type</span></span>                                                                   | <span data-ttu-id="d225a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d225a-108">Description</span></span>                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d225a-109">**counterSet**</span><span class="sxs-lookup"><span data-stu-id="d225a-109">**counterSet**</span></span> | [<span data-ttu-id="d225a-110">**Man: CounterSet**</span><span class="sxs-lookup"><span data-stu-id="d225a-110">**man:counterSet**</span></span>](performance-counters-counterset-complex-type.md) | <span data-ttu-id="d225a-111">Identifica o conjunto de contadores que contém um ou mais contadores logicamente relacionados.</span><span class="sxs-lookup"><span data-stu-id="d225a-111">Identifies the counter set that contains one or more logically related counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="d225a-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="d225a-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d225a-113">Nome</span><span class="sxs-lookup"><span data-stu-id="d225a-113">Name</span></span></th>
<th><span data-ttu-id="d225a-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="d225a-114">Type</span></span></th>
<th><span data-ttu-id="d225a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d225a-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d225a-116">applicationIdentity</span><span class="sxs-lookup"><span data-stu-id="d225a-116">applicationIdentity</span></span></td>
<td><span data-ttu-id="d225a-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="d225a-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="d225a-118">O nome do arquivo binário que contém as cadeias de caracteres de recurso localizado, um arquivo. exe ou. dll (não inclua o caminho para o binário).</span><span class="sxs-lookup"><span data-stu-id="d225a-118">The name of the binary file that contains the localized resource strings, either an .exe or .dll file (do not include the path to the binary).</span></span><br/> <span data-ttu-id="d225a-119">O utilitário Lodctr.exe usa o caminho do parâmetro opcional [<em>path</em>] para pesquisar o arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="d225a-119">The Lodctr.exe utility uses the path from the optional [<em>path</em>] parameter to search for the binary file.</span></span> <span data-ttu-id="d225a-120">Por exemplo, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>caminho</em>]].</span><span class="sxs-lookup"><span data-stu-id="d225a-120">For example, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]].</span></span> <span data-ttu-id="d225a-121">Se você não incluir o parâmetro [<em>path</em>], Lodctr.exe pesquisará a pasta que contém o manifesto.</span><span class="sxs-lookup"><span data-stu-id="d225a-121">If you do not include the [<em>path</em>] parameter, Lodctr.exe searches the folder that contains the manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d225a-122">retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="d225a-122">callback</span></span></td>

<td><span data-ttu-id="d225a-123">Esse atributo indica que você deseja receber a notificação quando um consumidor executa determinadas ações.</span><span class="sxs-lookup"><span data-stu-id="d225a-123">This attribute indicates that you want to receive notification when a consumer performs certain actions.</span></span> <br/> <span data-ttu-id="d225a-124">Se você incluir esse atributo, a ferramenta CTRPP usará a assinatura de função <a href="counterinitialize.md"><strong>myinitialize</strong></a> alternativa, que você usará para passar o nome da função que implementa a função de retorno de chamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d225a-124">If you include this attribute, the CTRPP tool uses the alternate <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> function signature, which you use to pass in the name of your function that implements the <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span><br/> <span data-ttu-id="d225a-125">Como alternativa para especificar esse atributo, você pode usar o argumento <strong>-NotificationCallback</strong><a href="ctrpp.md">ctrpp</a> .</span><span class="sxs-lookup"><span data-stu-id="d225a-125">As an alternative to specifying this attribute, you can use the <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> argument.</span></span><br/> <span data-ttu-id="d225a-126"><strong>Windows Vista:</strong> O único valor válido para esse atributo é &quot; personalizado &quot; .</span><span class="sxs-lookup"><span data-stu-id="d225a-126"><strong>Windows Vista:</strong> The only valid value for this attribute is &quot;custom&quot;.</span></span> <span data-ttu-id="d225a-127">O utilitário <a href="ctrpp.md">ctrpp</a> gera o modelo para uma função de retorno de chamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d225a-127">The <a href="ctrpp.md">CTRPP</a> utility generates the template for a <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span> <span data-ttu-id="d225a-128">O modelo é incluído no arquivo. c que CTRPP gerou.</span><span class="sxs-lookup"><span data-stu-id="d225a-128">The template is included in the .c file that CTRPP generated.</span></span> <br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d225a-129">providerGuid</span><span class="sxs-lookup"><span data-stu-id="d225a-129">providerGuid</span></span></td>
<td><span data-ttu-id="d225a-130"><a href="performance-counters-guidtype-simple-type.md"><strong>Man: GUIDtype</strong></a></span><span class="sxs-lookup"><span data-stu-id="d225a-130"><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></span></span></td>
<td><span data-ttu-id="d225a-131">GUID de cadeia de caracteres que identifica exclusivamente o provedor no manifesto.</span><span class="sxs-lookup"><span data-stu-id="d225a-131">String GUID that uniquely identifies the provider in the manifest.</span></span> <span data-ttu-id="d225a-132">O GUID deve ser exclusivo no manifesto.</span><span class="sxs-lookup"><span data-stu-id="d225a-132">The GUID must be unique within the manifest.</span></span><br/> <span data-ttu-id="d225a-133">Você precisa fornecer um novo GUID somente quando a versão do aplicativo for alterada (se você oferecer suporte a instalações lado a lado).</span><span class="sxs-lookup"><span data-stu-id="d225a-133">You need to provide a new GUID only when the version of the application changes (if you support side-by-side installations).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d225a-134">providerName</span><span class="sxs-lookup"><span data-stu-id="d225a-134">providerName</span></span></td>
<td><span data-ttu-id="d225a-135"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="d225a-135"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="d225a-136">O nome usado para criar o WMI Win32_PerfRawData nome da classe.</span><span class="sxs-lookup"><span data-stu-id="d225a-136">The name that is used to create the WMI Win32_PerfRawData class name.</span></span> <span data-ttu-id="d225a-137">Se você não especificar um nome, &quot; os contadores &quot; serão usados como o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="d225a-137">If you do not specify a name, &quot;Counters&quot; is used as the name of the class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d225a-138">providerType</span><span class="sxs-lookup"><span data-stu-id="d225a-138">providerType</span></span></td>

<td><span data-ttu-id="d225a-139">Identifica se o provedor é um provedor de modo de usuário, provedor de modo kernel ou provedor de driver.</span><span class="sxs-lookup"><span data-stu-id="d225a-139">Identifies whether the provider is a user-mode provider, kernel-mode provider, or driver provider.</span></span> <span data-ttu-id="d225a-140">Os valores possíveis são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="d225a-140">Possible values are as follows.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d225a-141">Termo</span><span class="sxs-lookup"><span data-stu-id="d225a-141">Term</span></span></th>
<th><span data-ttu-id="d225a-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="d225a-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d225a-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>Modo</span><span class="sxs-lookup"><span data-stu-id="d225a-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span></span><br/></td>
<td><span data-ttu-id="d225a-144">Especifique esse modo para um componente de modo de usuário, como um aplicativo, uma DLL ou um driver de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="d225a-144">Specify this mode for a user-mode component such as an application, a DLL, or a user-mode driver.</span></span> <span data-ttu-id="d225a-145">As extensões típicas para os componentes do modo de usuário são. exe ou. dll.</span><span class="sxs-lookup"><span data-stu-id="d225a-145">The typical extensions for user-mode components are .exe or .dll.</span></span> <span data-ttu-id="d225a-146">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="d225a-146">This is the default.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d225a-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span><span class="sxs-lookup"><span data-stu-id="d225a-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span></span><br/></td>
<td><span data-ttu-id="d225a-148">Especifique esse modo para um componente do modo kernel, como um driver WDM ou WDF.</span><span class="sxs-lookup"><span data-stu-id="d225a-148">Specify this mode for a kernel-mode component such as a WDM or WDF driver.</span></span> <span data-ttu-id="d225a-149">A extensão típica para componentes do modo kernel é. sys.</span><span class="sxs-lookup"><span data-stu-id="d225a-149">The typical extension for kernel-mode components is .sys.</span></span><br/> <span data-ttu-id="d225a-150"><strong>Windows Vista e Windows Server 2008:</strong> Esse valor não tem suporte até o Windows 7 e o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="d225a-150"><strong>Windows Vista and Windows Server 2008:</strong> This value is not supported until Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d225a-151">resourceBase</span><span class="sxs-lookup"><span data-stu-id="d225a-151">resourceBase</span></span></td>
<td><span data-ttu-id="d225a-152"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32type</strong></a></span><span class="sxs-lookup"><span data-stu-id="d225a-152"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><p><span data-ttu-id="d225a-153">Define o valor de índice de recurso inicial que o <a href="ctrpp.md">ctrpp</a> usa para gerar os identificadores de recurso.</span><span class="sxs-lookup"><span data-stu-id="d225a-153">Defines the starting resource index value that <a href="ctrpp.md">CTRPP</a> uses to generate the resource identifiers.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d225a-154">símbolo</span><span class="sxs-lookup"><span data-stu-id="d225a-154">symbol</span></span></td>
<td><span data-ttu-id="d225a-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>homem: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d225a-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="d225a-156">Um nome simbólico que identifica o provedor.</span><span class="sxs-lookup"><span data-stu-id="d225a-156">A symbolic name that identifies the provider.</span></span> <span data-ttu-id="d225a-157">A ferramenta <a href="ctrpp.md">ctrpp</a> cria uma variável de identificador que você pode usar ao chamar funções que exigem um identificador para o provedor (por exemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="d225a-157">The <a href="ctrpp.md">CTRPP</a> tool creates a HANDLE variable that you can use when calling functions that require a handle to the provider (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span></span> <span data-ttu-id="d225a-158">O nome simbólico é o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="d225a-158">The symbolic name is the name of the variable.</span></span></p>
<p><span data-ttu-id="d225a-159">Se você incluir o argumento <strong>-prefix</strong> ao chamar <a href="ctrpp.md">ctrpp</a>, a cadeia de caracteres de prefixo será adicionada ao início do nome simbólico.</span><span class="sxs-lookup"><span data-stu-id="d225a-159">If you include the <strong>-prefix</strong> argument when calling <a href="ctrpp.md">CTRPP</a>, the prefix string is added to the beginning of the symbolic name.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="d225a-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d225a-160">Requirements</span></span>



| <span data-ttu-id="d225a-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="d225a-161">Requirement</span></span> | <span data-ttu-id="d225a-162">Valor</span><span class="sxs-lookup"><span data-stu-id="d225a-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d225a-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d225a-163">Minimum supported client</span></span><br/> | <span data-ttu-id="d225a-164">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d225a-164">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d225a-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d225a-165">Minimum supported server</span></span><br/> | <span data-ttu-id="d225a-166">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d225a-166">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




