---
title: Tipo complexo ImportChannelType
description: Identifica um canal que foi definido por outro provedor ou em um manifesto que contém uma seção de metadados.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Log de eventos do tipo complexo ImportChannelType
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085517"
---
# <a name="importchanneltype-complex-type"></a><span data-ttu-id="c9fd7-104">Tipo complexo ImportChannelType</span><span class="sxs-lookup"><span data-stu-id="c9fd7-104">ImportChannelType Complex Type</span></span>

<span data-ttu-id="c9fd7-105">Identifica um canal que foi definido por outro provedor ou em um manifesto que contém uma seção de metadados.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-105">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span>

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="c9fd7-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9fd7-106">Attributes</span></span>



| <span data-ttu-id="c9fd7-107">Nome</span><span class="sxs-lookup"><span data-stu-id="c9fd7-107">Name</span></span>   | <span data-ttu-id="c9fd7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9fd7-108">Type</span></span>                                                              | <span data-ttu-id="c9fd7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9fd7-109">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fd7-110">chid</span><span class="sxs-lookup"><span data-stu-id="c9fd7-110">chid</span></span>   | <span data-ttu-id="c9fd7-111">token</span><span class="sxs-lookup"><span data-stu-id="c9fd7-111">token</span></span>                                                             | <span data-ttu-id="c9fd7-112">Um identificador que identifica exclusivamente o canal na lista de canais que o provedor define ou importa.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-112">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="c9fd7-113">Use esse valor ao referenciar esse canal em uma definição de evento.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-113">Use this value when referencing this channel in an event definition.</span></span> <span data-ttu-id="c9fd7-114">Se você não especificar um identificador de canal, use o nome do canal para fazer referência a esse canal em uma definição de evento.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-114">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/>  |
| <span data-ttu-id="c9fd7-115">name</span><span class="sxs-lookup"><span data-stu-id="c9fd7-115">name</span></span>   | <span data-ttu-id="c9fd7-116">anyURI</span><span class="sxs-lookup"><span data-stu-id="c9fd7-116">anyURI</span></span>                                                            | <span data-ttu-id="c9fd7-117">O nome do canal a ser importado.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-117">The name of the channel to import.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c9fd7-118">símbolo</span><span class="sxs-lookup"><span data-stu-id="c9fd7-118">symbol</span></span> | [<span data-ttu-id="c9fd7-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="c9fd7-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="c9fd7-120">O símbolo a ser usado para referenciar o canal em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-120">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="c9fd7-121">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o canal no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="c9fd7-122">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c9fd7-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9fd7-123">Remarks</span></span>

<span data-ttu-id="c9fd7-124">O manifesto que definiu o canal importado deve ser instalado antes que seu provedor grave eventos; caso contrário, os eventos não podem ser gravados no canal (a operação de gravação é realizada com sucesso, os eventos simplesmente não são gravados no canal).</span><span class="sxs-lookup"><span data-stu-id="c9fd7-124">The manifest that defined the imported channel must be installed before your provider writes events; otherwise, the events cannot be written to the channel (the write operation succeeds, the events are simply not written to the channel).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9fd7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9fd7-125">Requirements</span></span>



| <span data-ttu-id="c9fd7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9fd7-126">Requirement</span></span> | <span data-ttu-id="c9fd7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c9fd7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9fd7-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9fd7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c9fd7-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9fd7-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9fd7-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9fd7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c9fd7-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9fd7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





