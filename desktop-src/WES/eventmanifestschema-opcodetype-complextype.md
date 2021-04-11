---
title: Tipo complexo de OpCodeType
description: Define uma operação dentro de um componente do aplicativo.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Código de log de tipo complexo OpCodeType
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086337"
---
# <a name="opcodetype-complex-type"></a><span data-ttu-id="67a5e-104">Tipo complexo de OpCodeType</span><span class="sxs-lookup"><span data-stu-id="67a5e-104">OpcodeType Complex Type</span></span>

<span data-ttu-id="67a5e-105">Define uma operação dentro de um componente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67a5e-105">Defines an operation within a component of the application.</span></span> <span data-ttu-id="67a5e-106">Usado em conjunto com uma tarefa para identificar a seção do aplicativo que está registrando o evento.</span><span class="sxs-lookup"><span data-stu-id="67a5e-106">Used in conjunction with a task to identify the section of the application that is logging the event.</span></span>

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="67a5e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="67a5e-107">Attributes</span></span>



| <span data-ttu-id="67a5e-108">Nome</span><span class="sxs-lookup"><span data-stu-id="67a5e-108">Name</span></span>     | <span data-ttu-id="67a5e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="67a5e-109">Type</span></span>                                                              | <span data-ttu-id="67a5e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="67a5e-110">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a5e-111">message</span><span class="sxs-lookup"><span data-stu-id="67a5e-111">message</span></span>  | [<span data-ttu-id="67a5e-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="67a5e-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="67a5e-113">O nome de exibição localizado para o opcode.</span><span class="sxs-lookup"><span data-stu-id="67a5e-113">The localized display name for the opcode.</span></span> <span data-ttu-id="67a5e-114">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="67a5e-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                     |
| <span data-ttu-id="67a5e-115">mofValue</span><span class="sxs-lookup"><span data-stu-id="67a5e-115">mofValue</span></span> | [<span data-ttu-id="67a5e-116">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="67a5e-116">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="67a5e-117">Reservado apenas para uso interno.</span><span class="sxs-lookup"><span data-stu-id="67a5e-117">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="67a5e-118">name</span><span class="sxs-lookup"><span data-stu-id="67a5e-118">name</span></span>     | <span data-ttu-id="67a5e-119">**QName**</span><span class="sxs-lookup"><span data-stu-id="67a5e-119">**QName**</span></span>                                                         | <span data-ttu-id="67a5e-120">O nome do opcode.</span><span class="sxs-lookup"><span data-stu-id="67a5e-120">The name of the opcode.</span></span> <span data-ttu-id="67a5e-121">Esse nome deve ser exclusivo dentro do escopo deste provedor.</span><span class="sxs-lookup"><span data-stu-id="67a5e-121">This name must be unique within the scope of this provider.</span></span> <br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="67a5e-122">símbolo</span><span class="sxs-lookup"><span data-stu-id="67a5e-122">symbol</span></span>   | [<span data-ttu-id="67a5e-123">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="67a5e-123">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="67a5e-124">O símbolo a ser usado para referenciar o opcode em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67a5e-124">The symbol to use to reference the opcode in your application.</span></span> <span data-ttu-id="67a5e-125">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o opcode no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="67a5e-125">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the opcode in the header file that the compiler generates.</span></span> <span data-ttu-id="67a5e-126">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="67a5e-126">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="67a5e-127">value</span><span class="sxs-lookup"><span data-stu-id="67a5e-127">value</span></span>    | [<span data-ttu-id="67a5e-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="67a5e-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="67a5e-129">O valor de opcode.</span><span class="sxs-lookup"><span data-stu-id="67a5e-129">The opcode value.</span></span> <span data-ttu-id="67a5e-130">Você pode especificar valores no intervalo de 10 a 239.</span><span class="sxs-lookup"><span data-stu-id="67a5e-130">You can specify values in the range 10 and 239.</span></span> <span data-ttu-id="67a5e-131">Para obter uma lista de valores de opcode predefinidos, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="67a5e-131">For a list of predefined opcode values, see Remarks.</span></span><br/>                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="67a5e-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="67a5e-132">Remarks</span></span>

<span data-ttu-id="67a5e-133">A seguir estão os valores de opcode predefinidos que você pode usar.</span><span class="sxs-lookup"><span data-stu-id="67a5e-133">The following are the predefined opcode values that you can use.</span></span> <span data-ttu-id="67a5e-134">Esses valores são definidos no arquivo de Winmeta.xml que está incluído no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="67a5e-134">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="67a5e-135">Nome</span><span class="sxs-lookup"><span data-stu-id="67a5e-135">Name</span></span>          | <span data-ttu-id="67a5e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="67a5e-136">Value</span></span> | <span data-ttu-id="67a5e-137">Símbolo</span><span class="sxs-lookup"><span data-stu-id="67a5e-137">Symbol</span></span>                      | <span data-ttu-id="67a5e-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="67a5e-138">Description</span></span>                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a5e-139">Win: info</span><span class="sxs-lookup"><span data-stu-id="67a5e-139">win:Info</span></span>      | <span data-ttu-id="67a5e-140">0</span><span class="sxs-lookup"><span data-stu-id="67a5e-140">0</span></span>     | <span data-ttu-id="67a5e-141">\_informações de opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-141">WINEVENT\_OPCODE\_INFO</span></span>      | <span data-ttu-id="67a5e-142">Um evento informativo.</span><span class="sxs-lookup"><span data-stu-id="67a5e-142">An informational event.</span></span>                                                                                |
| <span data-ttu-id="67a5e-143">Win: iniciar</span><span class="sxs-lookup"><span data-stu-id="67a5e-143">win:Start</span></span>     | <span data-ttu-id="67a5e-144">1</span><span class="sxs-lookup"><span data-stu-id="67a5e-144">1</span></span>     | <span data-ttu-id="67a5e-145">\_início do opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-145">WINEVENT\_OPCODE\_START</span></span>     | <span data-ttu-id="67a5e-146">Um evento que representa o início de uma atividade.</span><span class="sxs-lookup"><span data-stu-id="67a5e-146">An event that represents starting an activity.</span></span>                                                         |
| <span data-ttu-id="67a5e-147">Win: parar</span><span class="sxs-lookup"><span data-stu-id="67a5e-147">win:Stop</span></span>      | <span data-ttu-id="67a5e-148">2</span><span class="sxs-lookup"><span data-stu-id="67a5e-148">2</span></span>     | <span data-ttu-id="67a5e-149">\_parada de opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-149">WINEVENT\_OPCODE\_STOP</span></span>      | <span data-ttu-id="67a5e-150">Um evento que representa a interrupção de uma atividade.</span><span class="sxs-lookup"><span data-stu-id="67a5e-150">An event that represents stopping an activity.</span></span> <span data-ttu-id="67a5e-151">O evento corresponde ao último evento de início não emparelhado.</span><span class="sxs-lookup"><span data-stu-id="67a5e-151">The event corresponds to the last unpaired start event.</span></span> |
| <span data-ttu-id="67a5e-152">Win: \_ Iniciar DC</span><span class="sxs-lookup"><span data-stu-id="67a5e-152">win:DC\_Start</span></span> | <span data-ttu-id="67a5e-153">3</span><span class="sxs-lookup"><span data-stu-id="67a5e-153">3</span></span>     | <span data-ttu-id="67a5e-154">inicialização do WINEVENT \_ opcode \_ DC \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-154">WINEVENT\_OPCODE\_DC\_START</span></span> | <span data-ttu-id="67a5e-155">Um evento que representa a coleta de dados iniciando.</span><span class="sxs-lookup"><span data-stu-id="67a5e-155">An event that represents data collection starting.</span></span> <span data-ttu-id="67a5e-156">Esses são tipos de evento de encerramento.</span><span class="sxs-lookup"><span data-stu-id="67a5e-156">These are rundown event types.</span></span>                      |
| <span data-ttu-id="67a5e-157">Win: parada de DC \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-157">win:DC\_Stop</span></span>  | <span data-ttu-id="67a5e-158">4</span><span class="sxs-lookup"><span data-stu-id="67a5e-158">4</span></span>     | <span data-ttu-id="67a5e-159">WINEVENT \_ opcode \_ DC \_ Stop</span><span class="sxs-lookup"><span data-stu-id="67a5e-159">WINEVENT\_OPCODE\_DC\_STOP</span></span>  | <span data-ttu-id="67a5e-160">Um evento que representa a interrupção da coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="67a5e-160">An event that represents data collection stopping.</span></span> <span data-ttu-id="67a5e-161">Esses são tipos de evento de encerramento.</span><span class="sxs-lookup"><span data-stu-id="67a5e-161">These are rundown event types.</span></span>                      |
| <span data-ttu-id="67a5e-162">Win: extensão</span><span class="sxs-lookup"><span data-stu-id="67a5e-162">win:Extension</span></span> | <span data-ttu-id="67a5e-163">5</span><span class="sxs-lookup"><span data-stu-id="67a5e-163">5</span></span>     | <span data-ttu-id="67a5e-164">\_extensão de opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-164">WINEVENT\_OPCODE\_EXTENSION</span></span> | <span data-ttu-id="67a5e-165">Um evento de extensão.</span><span class="sxs-lookup"><span data-stu-id="67a5e-165">An extension event.</span></span>                                                                                    |
| <span data-ttu-id="67a5e-166">Win: responder</span><span class="sxs-lookup"><span data-stu-id="67a5e-166">win:Reply</span></span>     | <span data-ttu-id="67a5e-167">6</span><span class="sxs-lookup"><span data-stu-id="67a5e-167">6</span></span>     | <span data-ttu-id="67a5e-168">\_resposta de opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-168">WINEVENT\_OPCODE\_REPLY</span></span>     | <span data-ttu-id="67a5e-169">Um evento de resposta.</span><span class="sxs-lookup"><span data-stu-id="67a5e-169">A reply event.</span></span>                                                                                         |
| <span data-ttu-id="67a5e-170">Win: retomar</span><span class="sxs-lookup"><span data-stu-id="67a5e-170">win:Resume</span></span>    | <span data-ttu-id="67a5e-171">7</span><span class="sxs-lookup"><span data-stu-id="67a5e-171">7</span></span>     | <span data-ttu-id="67a5e-172">\_currículo de opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-172">WINEVENT\_OPCODE\_RESUME</span></span>    | <span data-ttu-id="67a5e-173">Um evento que representa uma atividade retomada após ser suspensa.</span><span class="sxs-lookup"><span data-stu-id="67a5e-173">An event that represents an activity resuming after being suspended.</span></span>                                   |
| <span data-ttu-id="67a5e-174">Win: suspender</span><span class="sxs-lookup"><span data-stu-id="67a5e-174">win:Suspend</span></span>   | <span data-ttu-id="67a5e-175">8</span><span class="sxs-lookup"><span data-stu-id="67a5e-175">8</span></span>     | <span data-ttu-id="67a5e-176">\_suspensão de opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-176">WINEVENT\_OPCODE\_SUSPEND</span></span>   | <span data-ttu-id="67a5e-177">Um evento que representa a atividade que está sendo suspensa pendente da conclusão de outra atividade.</span><span class="sxs-lookup"><span data-stu-id="67a5e-177">An event that represents the activity being suspended pending another activity's completion.</span></span>           |
| <span data-ttu-id="67a5e-178">Win: enviar</span><span class="sxs-lookup"><span data-stu-id="67a5e-178">win:Send</span></span>      | <span data-ttu-id="67a5e-179">9</span><span class="sxs-lookup"><span data-stu-id="67a5e-179">9</span></span>     | <span data-ttu-id="67a5e-180">\_envio de opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-180">WINEVENT\_OPCODE\_SEND</span></span>      | <span data-ttu-id="67a5e-181">Um evento que representa a atividade de transferência para outro componente.</span><span class="sxs-lookup"><span data-stu-id="67a5e-181">An event that represents transferring activity to another component.</span></span>                                   |
| <span data-ttu-id="67a5e-182">Win: receber</span><span class="sxs-lookup"><span data-stu-id="67a5e-182">win:Receive</span></span>   | <span data-ttu-id="67a5e-183">240</span><span class="sxs-lookup"><span data-stu-id="67a5e-183">240</span></span>   | <span data-ttu-id="67a5e-184">\_recebimento de opcode WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="67a5e-184">WINEVENT\_OPCODE\_RECEIVE</span></span>   | <span data-ttu-id="67a5e-185">Um evento que representa o recebimento de uma transferência de atividade de outro componente.</span><span class="sxs-lookup"><span data-stu-id="67a5e-185">An event that represents receiving an activity transfer from another component.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="67a5e-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67a5e-186">Requirements</span></span>



| <span data-ttu-id="67a5e-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="67a5e-187">Requirement</span></span> | <span data-ttu-id="67a5e-188">Valor</span><span class="sxs-lookup"><span data-stu-id="67a5e-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67a5e-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67a5e-189">Minimum supported client</span></span><br/> | <span data-ttu-id="67a5e-190">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67a5e-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="67a5e-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67a5e-191">Minimum supported server</span></span><br/> | <span data-ttu-id="67a5e-192">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67a5e-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





