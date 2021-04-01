---
title: Tipo complexo ChannelLoggingType
description: Define as propriedades do arquivo de log que faz o backup do canal, como sua capacidade e se ele é sequencial ou circular. | Tipo complexo ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Log de eventos do tipo complexo ChannelLoggingType
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104091931"
---
# <a name="channelloggingtype-complex-type"></a><span data-ttu-id="721c6-105">Tipo complexo ChannelLoggingType</span><span class="sxs-lookup"><span data-stu-id="721c6-105">ChannelLoggingType Complex Type</span></span>

<span data-ttu-id="721c6-106">Define as propriedades do arquivo de log que faz o backup do canal, como sua capacidade e se ele é sequencial ou circular.</span><span class="sxs-lookup"><span data-stu-id="721c6-106">Defines the properties of the log file that backs the channel, such as its capacity and whether it is sequential or circular.</span></span>

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="721c6-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="721c6-107">Child elements</span></span>



| <span data-ttu-id="721c6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="721c6-108">Element</span></span>                                                                         | <span data-ttu-id="721c6-109">Type</span><span class="sxs-lookup"><span data-stu-id="721c6-109">Type</span></span>                                                              | <span data-ttu-id="721c6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="721c6-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="721c6-111">**Backup automático**</span><span class="sxs-lookup"><span data-stu-id="721c6-111">**autoBackup**</span></span>](eventmanifestschema-autobackup-channelloggingtype-element.md) | <span data-ttu-id="721c6-112">booleano</span><span class="sxs-lookup"><span data-stu-id="721c6-112">boolean</span></span>                                                           | <span data-ttu-id="721c6-113">Determina se um novo arquivo de log deve ser criado quando o arquivo de log atual atinge seu tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="721c6-113">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span> <span data-ttu-id="721c6-114">Defina como **true** para solicitar que o serviço crie um novo arquivo quando o arquivo de log atingir seu tamanho máximo; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="721c6-114">Set to **true** to request that the service create a new file when the log file reaches its maximum size; otherwise, **false**.</span></span> <span data-ttu-id="721c6-115">Você pode definir o [**backup**](eventmanifestschema-autobackup-channelloggingtype-element.md) único como **true** somente se a [**retenção**](eventmanifestschema-retention-channelloggingtype-element.md) estiver definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="721c6-115">You can set [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) to **true** only if [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) is set to **true**.</span></span> <span data-ttu-id="721c6-116">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="721c6-116">The default is **false**.</span></span><br/> <span data-ttu-id="721c6-117">Não há nenhum limite para o número de arquivos de backup que o serviço pode criar (limitado apenas pelo espaço em disco disponível).</span><span class="sxs-lookup"><span data-stu-id="721c6-117">There is no limit to the number of backup files that the service can create (limited only by available disk space).</span></span> <span data-ttu-id="721c6-118">Os nomes dos arquivos de backup estão no formato Archive-*channelName* - *timestamp*. evtx e estão localizados na pasta% windir% \\ System32 \\ winevt \\ logs.</span><span class="sxs-lookup"><span data-stu-id="721c6-118">The backup file names are of the form Archive-*channelName*-*timestamp*.evtx and are located in %windir%\\System32\\winevt\\Logs folder.</span></span><br/> |
| [<span data-ttu-id="721c6-119">**maxSize**</span><span class="sxs-lookup"><span data-stu-id="721c6-119">**maxSize**</span></span>](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [<span data-ttu-id="721c6-120">**UInt64type**</span><span class="sxs-lookup"><span data-stu-id="721c6-120">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="721c6-121">O tamanho máximo, em bytes, do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="721c6-121">The maximum size, in bytes, of the log file.</span></span> <span data-ttu-id="721c6-122">O valor padrão (e mínimo) é 1 MB.</span><span class="sxs-lookup"><span data-stu-id="721c6-122">The default (and minimum) value is 1 MB.</span></span> <span data-ttu-id="721c6-123">Se o tamanho do log físico for menor que o tamanho máximo configurado e o espaço adicional for necessário no log para armazenar eventos, o serviço alocará outro bloco de espaço, mesmo se o tamanho físico resultante do log for maior do que o tamanho máximo configurado.</span><span class="sxs-lookup"><span data-stu-id="721c6-123">If the physical log size is less than the configured maximum size and additional space is required in the log to store events, the service will allocate another block of space even if the resulting physical size of the log will be larger than the configured maximum size.</span></span> <span data-ttu-id="721c6-124">O serviço aloca blocos de 1 MB para que o tamanho físico possa aumentar para até 1 MB maior do que o tamanho máximo configurado.</span><span class="sxs-lookup"><span data-stu-id="721c6-124">The service allocates blocks of 1 MB so the physical size could grow to up to 1 MB larger than the configured max size.</span></span> <br/>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="721c6-125">**políticas**</span><span class="sxs-lookup"><span data-stu-id="721c6-125">**retention**</span></span>](eventmanifestschema-retention-channelloggingtype-element.md)   | <span data-ttu-id="721c6-126">booleano</span><span class="sxs-lookup"><span data-stu-id="721c6-126">boolean</span></span>                                                           | <span data-ttu-id="721c6-127">Determina se o arquivo de log é um arquivo de log seqüencial ou circular.</span><span class="sxs-lookup"><span data-stu-id="721c6-127">Determines whether the log file is a sequential or circular log file.</span></span> <span data-ttu-id="721c6-128">Defina como **true** para um arquivo de log sequencial e **false** para um arquivo de log circular.</span><span class="sxs-lookup"><span data-stu-id="721c6-128">Set to **true** for a sequential log file and **false** for a circular log file.</span></span> <span data-ttu-id="721c6-129">O padrão é **false** para os tipos de canal de administração e operacionais e **verdadeiro** para os tipos de canal analítico e de depuração.</span><span class="sxs-lookup"><span data-stu-id="721c6-129">The default is **false** for Admin and Operational channel types and **true** for Analytic and Debug channel types.</span></span><br/> <span data-ttu-id="721c6-130">Para consultar um log circular, primeiro você deve desabilitar o canal.</span><span class="sxs-lookup"><span data-stu-id="721c6-130">To query a circular log, you must first disable the channel.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="721c6-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="721c6-131">Remarks</span></span>

<span data-ttu-id="721c6-132">Você pode especificar o atributo **MaxSize** para qualquer tipo de canal.</span><span class="sxs-lookup"><span data-stu-id="721c6-132">You can specify the **maxSize** attribute for any channel type.</span></span>

<span data-ttu-id="721c6-133">Você pode especificar o atributo de **backup** único somente para os tipos de canal de administrador e operacional.</span><span class="sxs-lookup"><span data-stu-id="721c6-133">You can specify the **autoBackup** attribute only for Admin and Operational channel types.</span></span>

<span data-ttu-id="721c6-134">Você pode definir o atributo de **retenção** como falso (log circular) para os tipos de canal de administrador e operacional.</span><span class="sxs-lookup"><span data-stu-id="721c6-134">You can set the **retention** attribute to false (circular logging) for Admin and Operational channel types.</span></span> <span data-ttu-id="721c6-135">Você pode definir o atributo de **retenção** como falso (log circular) para tipos de canal analíticos e de depuração, mas para exibir os eventos no Visualizador de eventos do Windows, você precisará primeiro desabilitar o canal.</span><span class="sxs-lookup"><span data-stu-id="721c6-135">You can set the **retention** attribute to false (circular logging) for Analytic and Debug channel types but to view the events in the Windows Event Viewer, you will need to first disable the channel.</span></span> <span data-ttu-id="721c6-136">Observe que, quando você habilita o canal novamente, os eventos são removidos do canal.</span><span class="sxs-lookup"><span data-stu-id="721c6-136">Note that when you enable the channel again, the events are removed from the channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="721c6-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="721c6-137">Requirements</span></span>



| <span data-ttu-id="721c6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="721c6-138">Requirement</span></span> | <span data-ttu-id="721c6-139">Valor</span><span class="sxs-lookup"><span data-stu-id="721c6-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="721c6-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="721c6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="721c6-141">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="721c6-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="721c6-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="721c6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="721c6-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="721c6-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





