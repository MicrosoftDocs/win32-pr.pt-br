---
title: Tipo complexo ChannelPublishingType
description: Define as propriedades de log para a sessão que o canal usa. | Tipo complexo ChannelPublishingType
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- Log de eventos do tipo complexo ChannelPublishingType
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105800197"
---
# <a name="channelpublishingtype-complex-type"></a><span data-ttu-id="2f5b6-105">Tipo complexo ChannelPublishingType</span><span class="sxs-lookup"><span data-stu-id="2f5b6-105">ChannelPublishingType Complex Type</span></span>

<span data-ttu-id="2f5b6-106">Define as propriedades de log para a sessão que o canal usa.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-106">Defines the logging properties for the session that the channel uses.</span></span>

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
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

## <a name="child-elements"></a><span data-ttu-id="2f5b6-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2f5b6-107">Child elements</span></span>



| <span data-ttu-id="2f5b6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2f5b6-108">Element</span></span>                                                                              | <span data-ttu-id="2f5b6-109">Type</span><span class="sxs-lookup"><span data-stu-id="2f5b6-109">Type</span></span>                                                              | <span data-ttu-id="2f5b6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f5b6-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f5b6-111">**bufferSize**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-111">**bufferSize**</span></span>](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [<span data-ttu-id="2f5b6-112">**UInt32type**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-112">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="2f5b6-113">A quantidade de memória, em quilobytes, a ser alocada para cada buffer.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-113">The amount of memory, in kilobytes, to allocate for each buffer.</span></span> <span data-ttu-id="2f5b6-114">Se você espera uma taxa de eventos relativamente baixa, o tamanho do buffer deve ser definido como o tamanho da página de memória.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-114">If you expect a relatively low event rate, the buffer size should be set to the memory page size.</span></span> <span data-ttu-id="2f5b6-115">Se espera-se que a taxa de eventos seja relativamente alta, você deve especificar um tamanho de buffer maior e aumentar o número máximo de buffers.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-115">If the event rate is expected to be relatively high, you should specify a larger buffer size and increase the maximum number of buffers.</span></span><br/> <span data-ttu-id="2f5b6-116">O tamanho do buffer afeta a taxa na qual os buffers são preenchidos e devem ser liberados.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-116">The buffer size affects the rate at which buffers fill and must be flushed.</span></span> <span data-ttu-id="2f5b6-117">Embora um pequeno tamanho de buffer exija menos memória, ele aumenta a taxa em que os buffers devem ser liberados.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-117">Although a small buffer size requires less memory, it increases the rate at which buffers must be flushed.</span></span><br/> <span data-ttu-id="2f5b6-118">O tamanho de buffer padrão para os canais analíticos e de depuração é 4 KB e para administração e operacional é 64 KB.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-118">The default buffer size for Analytic and Debug channels is 4 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="2f5b6-119">**clocktype**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-119">**clockType**</span></span>](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | <span data-ttu-id="2f5b6-120">A resolução de relógio a ser usada ao registrar em log o carimbo de data/hora para cada evento.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-120">The clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="2f5b6-121">Você pode especificar SystemTime ou QPC.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-121">You can specify SystemTime or QPC.</span></span> <span data-ttu-id="2f5b6-122">O SystemTime fornece um carimbo de data/hora de baixa resolução (10 milissegundos), mas é comparativamente menos dispendioso para ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-122">SystemTime provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve.</span></span> <span data-ttu-id="2f5b6-123">O padrão é SystemTime.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-123">The default is SystemTime.</span></span> <br/> <span data-ttu-id="2f5b6-124">O contador de desempenho de consulta (QPC) fornece um carimbo de data/hora de alta resolução (100 nanossegundos), mas é comparativamente mais caro de recuperar.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-124">Query performance counter (QPC) provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve.</span></span> <span data-ttu-id="2f5b6-125">Você deve QPC se tiver taxas de eventos altas ou se o consumidor mesclar eventos de buffers diferentes.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-125">You should QPC if you have high event rates or if the consumer merges events from different buffers.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="2f5b6-126">**controlGuid**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-126">**controlGuid**</span></span>](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [<span data-ttu-id="2f5b6-127">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-127">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="2f5b6-128">Identifica o GUID de sessão para uma sessão de ETW que contém eventos de WPP.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-128">Identifies the session GUID for an ETW session that contains WPP events.</span></span> <span data-ttu-id="2f5b6-129">Essa configuração só é permitida para canais do tipo Debug.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-129">This setting is only allowed for channels of type Debug.</span></span> <span data-ttu-id="2f5b6-130">Esses canais não podem ser totalmente habilitados com palavras-chave definidas como zero (0x0000000000000000).</span><span class="sxs-lookup"><span data-stu-id="2f5b6-130">These channels cannot be fully enabled with keywords set to zero (0x0000000000000000).</span></span> <span data-ttu-id="2f5b6-131">Eles devem ser habilitados com palavras-chave definidas como 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-131">They must be enabled with keywords set to 0xffffffffffffffff.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="2f5b6-132">**fileMax**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-132">**fileMax**</span></span>                                                                          | [<span data-ttu-id="2f5b6-133">**UInt32type**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-133">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="2f5b6-134">O número máximo de vezes que você deseja que o serviço crie um novo arquivo de log quando o canal está habilitado (inclui quando o computador é reiniciado).</span><span class="sxs-lookup"><span data-stu-id="2f5b6-134">The maximum number of times that you want the service to create a new log file when the channel is enabled (includes when the computer is restarted).</span></span> <span data-ttu-id="2f5b6-135">Se o valor for 0 ou 1, o serviço substituirá o arquivo de log cada vez que o canal for habilitado e os eventos anteriores serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-135">If the value is 0 or 1, the service will overwrite the log file each time the channel is enabled and the previous events will be lost.</span></span> <span data-ttu-id="2f5b6-136">Se o valor for maior que 1, o serviço criará um novo arquivo de log cada vez que o canal estiver habilitado para preservar os eventos.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-136">If the value is greater than 1, the service will create a new log file each time the channel is enabled in order to preserve the events.</span></span> <span data-ttu-id="2f5b6-137">O padrão é 1 e o máximo que você pode especificar é 16.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-137">The default is 1 and the maximum that you can specify is 16.</span></span><br/> <span data-ttu-id="2f5b6-138">O serviço acrescenta um número decimal de três dígitos entre 0 e fileMax 1 a cada nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-138">The service appends a three digit decimal number between 0 and fileMax 1 to each file name.</span></span> <span data-ttu-id="2f5b6-139">Por exemplo, *filename*. etl.xxx, em que xxx é o número decimal de três dígitos.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-139">For example, *filename*.etl.xxx, where xxx is the three digit decimal number.</span></span> <span data-ttu-id="2f5b6-140">Os arquivos estão localizados em% windir% \\ System32 \\ winevt \\ logs.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-140">The files are located in %windir%\\System32\\winevt\\Logs.</span></span><br/> |
| [<span data-ttu-id="2f5b6-141">**palavras-chave**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-141">**keywords**</span></span>](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [<span data-ttu-id="2f5b6-142">**UInt64type**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-142">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="2f5b6-143">Um bitmask que determina a categoria de eventos que são gravados no canal.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-143">A bitmask that determines the category of events that are written to the channel.</span></span> <span data-ttu-id="2f5b6-144">Se o valor do atributo **Keywords** for 0, todos os eventos que o provedor gravar serão gravados no canal; caso contrário, somente os eventos que definiram uma palavra-chave que está incluída no bitmask das **palavras-chave** serão gravados no canal.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-144">If the value of **keywords** attribute is 0, all events that the provider writes are written to the channel; otherwise only events that have defined a keyword that is included in the **keywords** bitmask are written to the channel.</span></span> <span data-ttu-id="2f5b6-145">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-145">The default is 0.</span></span><br/> <span data-ttu-id="2f5b6-146">Os canais de depuração que têm o atributo controlGuid definido devem definir o atributo **Keywords** como 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-146">Debug channels that have the controlGuid attribute set must set the **keywords** attribute to 0xFFFFFFFFFFFFFFFF.</span></span><br/> <span data-ttu-id="2f5b6-147">A sessão passa o valor de palavras-chave para o provedor quando ele habilita o provedor.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-147">The session passes the keywords value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="2f5b6-148">**MOLAP**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-148">**latency**</span></span>](eventmanifestschema-latency-channelpublishingtype-element.md)         | [<span data-ttu-id="2f5b6-149">**UInt32type**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-149">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="2f5b6-150">O tempo de espera antes de liberar os buffers, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-150">The time to wait before flushing the buffers, in milliseconds.</span></span> <span data-ttu-id="2f5b6-151">Se zero, o ETW libera os buffers assim que eles ficam cheios.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-151">If zero, ETW flushes the buffers as soon as they become full.</span></span> <span data-ttu-id="2f5b6-152">Se for diferente de zero, o ETW liberará todos os buffers que contêm eventos com base no valor, mesmo se o buffer não estiver cheio.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-152">If nonzero, ETW flushes all buffers that contain events based on the value even if the buffer is not full.</span></span> <span data-ttu-id="2f5b6-153">Normalmente, você deseja liberar buffers somente quando eles se tornam cheios.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-153">Typically, you want to flush buffers only when they become full.</span></span> <span data-ttu-id="2f5b6-154">Forçar os buffers a serem liberados pode aumentar o tamanho do arquivo de log com espaço de buffer não preenchido.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-154">Forcing the buffers to flush can increase the file size of the log file with unfilled buffer space.</span></span> <span data-ttu-id="2f5b6-155">O valor padrão é 1 segundo para logs de administração e operacionais e 5 segundos para logs analíticos e de depuração.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-155">The default value is 1 second for Admin and Operational logs and 5 seconds for Analytic and Debug logs.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="2f5b6-156">**nível**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-156">**level**</span></span>](eventmanifestschema-level-channelpublishingtype-element.md)             | [<span data-ttu-id="2f5b6-157">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-157">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="2f5b6-158">O nível de severidade dos eventos a serem gravados no canal.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-158">The severity level of the events to write to the channel.</span></span> <span data-ttu-id="2f5b6-159">O serviço grava eventos no canal que têm um valor de nível menor ou igual ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-159">The service writes events to the channel that have a level value that is less than or equal to the specified value.</span></span> <span data-ttu-id="2f5b6-160">O padrão é 0, o que significa registrar eventos com qualquer valor de nível.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-160">The default is 0, which means to log events with any level value.</span></span><br/> <span data-ttu-id="2f5b6-161">A sessão passa o valor de nível para o provedor quando ele habilita o provedor.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-161">The session passes the level value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="2f5b6-162">**maxBuffers**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-162">**maxBuffers**</span></span>](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="2f5b6-163">**UInt32type**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-163">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="2f5b6-164">O número máximo de buffers a serem alocados para a sessão.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-164">The maximum number of buffers to allocate for the session.</span></span> <span data-ttu-id="2f5b6-165">Normalmente, esse valor é o número mínimo de buffers, mais vinte.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-165">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="2f5b6-166">Esse valor deve ser maior ou igual ao valor especificado para minBuffers.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-166">This value must be greater than or equal to the value specified for minBuffers.</span></span><br/> <span data-ttu-id="2f5b6-167">O número máximo padrão de buffers para canais analíticos e de depuração é 10 KB e para administração e operacional ele é de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-167">The default maximum number of buffers for Analytic and Debug channels is 10 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="2f5b6-168">**minBuffers**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-168">**minBuffers**</span></span>](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="2f5b6-169">**UInt32type**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-169">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="2f5b6-170">O número mínimo de buffers a serem alocados para a sessão.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-170">The minimum number of buffers to allocate for the session.</span></span> <span data-ttu-id="2f5b6-171">O padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-171">The default is zero.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="2f5b6-172">**sidType**</span><span class="sxs-lookup"><span data-stu-id="2f5b6-172">**sidType**</span></span>](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | <span data-ttu-id="2f5b6-173">Determina se um SID (identificador de segurança) do principal deve ser incluído em cada evento gravado no canal.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-173">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span> <span data-ttu-id="2f5b6-174">Para incluir o SID com o evento, defina esse atributo como "Publishing".</span><span class="sxs-lookup"><span data-stu-id="2f5b6-174">To include the SID with the event, set this attribute to "Publishing".</span></span> <span data-ttu-id="2f5b6-175">O SID é definido com base na identidade do thread no momento em que o evento é gravado.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-175">The SID is set based on the thread identity at the time the event is written.</span></span> <span data-ttu-id="2f5b6-176">Se você não quiser incluir o SID com o evento, defina esse atributo como "nenhum".</span><span class="sxs-lookup"><span data-stu-id="2f5b6-176">If you do not want to include the SID with the event, set this attribute to "None".</span></span> <span data-ttu-id="2f5b6-177">O padrão é "publicação".</span><span class="sxs-lookup"><span data-stu-id="2f5b6-177">The default is "Publishing".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="2f5b6-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f5b6-178">Remarks</span></span>

<span data-ttu-id="2f5b6-179">Você pode especificar essas informações de publicação para tipos de canal analíticos e de depuração ou para qualquer canal que especifica o isolamento personalizado.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-179">You can specify this publishing information for Analytic and Debug channel types or for any channel that specifies Custom isolation.</span></span>

<span data-ttu-id="2f5b6-180">Embora você possa especificar o nível e as palavras-chave, considere que esses serão os únicos eventos que você receberá do provedor para esse canal.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-180">Although you can specify level and keywords, you should consider that these will be the only events that you will receive from the provider for that channel.</span></span>

<span data-ttu-id="2f5b6-181">Quando um buffer está cheio, o ETW libera o buffer para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-181">When a buffer is full, ETW flushes the buffer to the log file.</span></span> <span data-ttu-id="2f5b6-182">Se os buffers forem preenchidos mais rapidamente do que podem ser liberados, novos buffers serão alocados e adicionados ao pool de buffers da sessão, até o número máximo especificado.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-182">If the buffers are filled faster than they can be flushed, new buffers are allocated and added to the session's buffer pool, up to the maximum number specified.</span></span> <span data-ttu-id="2f5b6-183">Além desse limite, a sessão descarta eventos de entrada até que um buffer fique disponível.</span><span class="sxs-lookup"><span data-stu-id="2f5b6-183">Beyond this limit, the session discards incoming events until a buffer becomes available.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f5b6-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f5b6-184">Requirements</span></span>



| <span data-ttu-id="2f5b6-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f5b6-185">Requirement</span></span> | <span data-ttu-id="2f5b6-186">Valor</span><span class="sxs-lookup"><span data-stu-id="2f5b6-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f5b6-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f5b6-187">Minimum supported client</span></span><br/> | <span data-ttu-id="2f5b6-188">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f5b6-188">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2f5b6-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f5b6-189">Minimum supported server</span></span><br/> | <span data-ttu-id="2f5b6-190">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f5b6-190">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





