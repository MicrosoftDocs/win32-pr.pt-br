---
title: Tipo complexo de LevelType
description: Define um valor de severidade que determina o detalhamento dos eventos que estão sendo registrados.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- EventLog de tipo complexo de LevelType
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085190"
---
# <a name="leveltype-complex-type"></a><span data-ttu-id="0fbee-104">Tipo complexo de LevelType</span><span class="sxs-lookup"><span data-stu-id="0fbee-104">LevelType Complex Type</span></span>

<span data-ttu-id="0fbee-105">Define um valor de severidade que determina o detalhamento dos eventos que estão sendo registrados.</span><span class="sxs-lookup"><span data-stu-id="0fbee-105">Defines a severity value that determines the verbosity of the events being logged.</span></span>

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
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
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="0fbee-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="0fbee-106">Attributes</span></span>



| <span data-ttu-id="0fbee-107">Nome</span><span class="sxs-lookup"><span data-stu-id="0fbee-107">Name</span></span>    | <span data-ttu-id="0fbee-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fbee-108">Type</span></span>                                                              | <span data-ttu-id="0fbee-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0fbee-109">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbee-110">message</span><span class="sxs-lookup"><span data-stu-id="0fbee-110">message</span></span> | [<span data-ttu-id="0fbee-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="0fbee-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="0fbee-112">O nome de exibição localizado para o nível.</span><span class="sxs-lookup"><span data-stu-id="0fbee-112">The localized display name for the level.</span></span> <span data-ttu-id="0fbee-113">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="0fbee-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                    |
| <span data-ttu-id="0fbee-114">name</span><span class="sxs-lookup"><span data-stu-id="0fbee-114">name</span></span>    | <span data-ttu-id="0fbee-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="0fbee-115">**QName**</span></span>                                                         | <span data-ttu-id="0fbee-116">O nome a ser atribuído a esse nível.</span><span class="sxs-lookup"><span data-stu-id="0fbee-116">The name to assign to this level.</span></span> <span data-ttu-id="0fbee-117">Esse nome deve ser exclusivo dentro do escopo do provedor.</span><span class="sxs-lookup"><span data-stu-id="0fbee-117">This name must be unique within the scope of the provider.</span></span><br/>                                                                                                                                                                                                            |
| <span data-ttu-id="0fbee-118">símbolo</span><span class="sxs-lookup"><span data-stu-id="0fbee-118">symbol</span></span>  | [<span data-ttu-id="0fbee-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="0fbee-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="0fbee-120">O símbolo a ser usado para referenciar o nível em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0fbee-120">The symbol to use to reference the level in your application.</span></span> <span data-ttu-id="0fbee-121">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o nível no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="0fbee-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the level in the header file that the compiler generates.</span></span> <span data-ttu-id="0fbee-122">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="0fbee-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="0fbee-123">value</span><span class="sxs-lookup"><span data-stu-id="0fbee-123">value</span></span>   | [<span data-ttu-id="0fbee-124">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="0fbee-124">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="0fbee-125">O valor de nível.</span><span class="sxs-lookup"><span data-stu-id="0fbee-125">The level value.</span></span> <span data-ttu-id="0fbee-126">Você pode especificar valores no intervalo de 16 a 255.</span><span class="sxs-lookup"><span data-stu-id="0fbee-126">You can specify values in the range 16 to 255.</span></span> <span data-ttu-id="0fbee-127">Para valores de nível predefinidos, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="0fbee-127">For predefined level values, see Remarks.</span></span><br/>                                                                                                                                                                                               |



## <a name="remarks"></a><span data-ttu-id="0fbee-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fbee-128">Remarks</span></span>

<span data-ttu-id="0fbee-129">A seguir estão os valores de nível predefinidos que você pode usar.</span><span class="sxs-lookup"><span data-stu-id="0fbee-129">The following are the predefined level values that you can use.</span></span> <span data-ttu-id="0fbee-130">Esses valores são definidos no arquivo de Winmeta.xml que está incluído no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="0fbee-130">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="0fbee-131">Nome</span><span class="sxs-lookup"><span data-stu-id="0fbee-131">Name</span></span>              | <span data-ttu-id="0fbee-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0fbee-132">Value</span></span> | <span data-ttu-id="0fbee-133">Símbolo</span><span class="sxs-lookup"><span data-stu-id="0fbee-133">Symbol</span></span>                    | <span data-ttu-id="0fbee-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="0fbee-134">Description</span></span>                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="0fbee-135">win:Critical</span><span class="sxs-lookup"><span data-stu-id="0fbee-135">win:Critical</span></span>      | <span data-ttu-id="0fbee-136">1</span><span class="sxs-lookup"><span data-stu-id="0fbee-136">1</span></span>     | <span data-ttu-id="0fbee-137">WINEVENT \_ nível \_ crítico</span><span class="sxs-lookup"><span data-stu-id="0fbee-137">WINEVENT\_LEVEL\_CRITICAL</span></span> | <span data-ttu-id="0fbee-138">Identifica um evento de saída anormal ou de encerramento.</span><span class="sxs-lookup"><span data-stu-id="0fbee-138">Identifies an abnormal exit or termination event.</span></span><br/>            |
| <span data-ttu-id="0fbee-139">win:Error</span><span class="sxs-lookup"><span data-stu-id="0fbee-139">win:Error</span></span>         | <span data-ttu-id="0fbee-140">2</span><span class="sxs-lookup"><span data-stu-id="0fbee-140">2</span></span>     | <span data-ttu-id="0fbee-141">\_erro no nível de WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="0fbee-141">WINEVENT\_LEVEL\_ERROR</span></span>    | <span data-ttu-id="0fbee-142">Identifica um evento de erro grave.</span><span class="sxs-lookup"><span data-stu-id="0fbee-142">Identifies a severe error event.</span></span><br/>                             |
| <span data-ttu-id="0fbee-143">win:Warning</span><span class="sxs-lookup"><span data-stu-id="0fbee-143">win:Warning</span></span>       | <span data-ttu-id="0fbee-144">3</span><span class="sxs-lookup"><span data-stu-id="0fbee-144">3</span></span>     | <span data-ttu-id="0fbee-145">\_aviso de nível de WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="0fbee-145">WINEVENT\_LEVEL\_WARNING</span></span>  | <span data-ttu-id="0fbee-146">Identifica um evento de aviso, como uma falha de alocação.</span><span class="sxs-lookup"><span data-stu-id="0fbee-146">Identifies a warning event such as an allocation failure.</span></span><br/>    |
| <span data-ttu-id="0fbee-147">win:Informational</span><span class="sxs-lookup"><span data-stu-id="0fbee-147">win:Informational</span></span> | <span data-ttu-id="0fbee-148">4</span><span class="sxs-lookup"><span data-stu-id="0fbee-148">4</span></span>     | <span data-ttu-id="0fbee-149">\_informações de nível de WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="0fbee-149">WINEVENT\_LEVEL\_INFO</span></span>     | <span data-ttu-id="0fbee-150">Identifica um evento que não é de erro, como um evento de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="0fbee-150">Identifies a non-error event such as an entry or exit event.</span></span><br/> |
| <span data-ttu-id="0fbee-151">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="0fbee-151">win:Verbose</span></span>       | <span data-ttu-id="0fbee-152">5</span><span class="sxs-lookup"><span data-stu-id="0fbee-152">5</span></span>     | <span data-ttu-id="0fbee-153">WINEVENT \_ nível \_ detalhado</span><span class="sxs-lookup"><span data-stu-id="0fbee-153">WINEVENT\_LEVEL\_VERBOSE</span></span>  | <span data-ttu-id="0fbee-154">Identifica um evento de rastreamento detalhado.</span><span class="sxs-lookup"><span data-stu-id="0fbee-154">Identifies a detailed trace event.</span></span><br/>                           |



 

<span data-ttu-id="0fbee-155">Números mais altos significam que você também obtém níveis mais baixos.</span><span class="sxs-lookup"><span data-stu-id="0fbee-155">Higher numbers imply that you get lower levels as well.</span></span> <span data-ttu-id="0fbee-156">Por exemplo, se você especificar Win: Warning, receberá todos os eventos de aviso, erro e crítico.</span><span class="sxs-lookup"><span data-stu-id="0fbee-156">For example, if you specify win:Warning, you receive all warning, error, and critical events.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fbee-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fbee-157">Requirements</span></span>



| <span data-ttu-id="0fbee-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fbee-158">Requirement</span></span> | <span data-ttu-id="0fbee-159">Valor</span><span class="sxs-lookup"><span data-stu-id="0fbee-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0fbee-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fbee-160">Minimum supported client</span></span><br/> | <span data-ttu-id="0fbee-161">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fbee-161">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0fbee-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fbee-162">Minimum supported server</span></span><br/> | <span data-ttu-id="0fbee-163">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0fbee-163">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





