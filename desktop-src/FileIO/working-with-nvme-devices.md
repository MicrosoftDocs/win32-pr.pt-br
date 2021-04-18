---
description: Saiba como trabalhar com dispositivos NVMe de alta velocidade de seu aplicativo do Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Trabalhando com unidades NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766911"
---
# <a name="working-with-nvme-drives"></a><span data-ttu-id="6a513-103">Trabalhando com unidades NVMe</span><span class="sxs-lookup"><span data-stu-id="6a513-103">Working with NVMe drives</span></span>

<span data-ttu-id="6a513-104">**Aplica-se a:**</span><span class="sxs-lookup"><span data-stu-id="6a513-104">**Applies to:**</span></span>

-   <span data-ttu-id="6a513-105">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6a513-105">Windows 10</span></span>
-   <span data-ttu-id="6a513-106">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6a513-106">Windows Server 2016</span></span>

<span data-ttu-id="6a513-107">Saiba como trabalhar com dispositivos NVMe de alta velocidade de seu aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a513-107">Learn how to work with high-speed NVMe devices from your Windows application.</span></span> <span data-ttu-id="6a513-108">O acesso ao dispositivo é habilitado via **StorNVMe.sys**, o driver na caixa introduzido primeiro no Windows Server 2012 R2 e no Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="6a513-108">Device access is enabled via **StorNVMe.sys**, the in-box driver first introduced in Windows Server 2012 R2 and Windows 8.1.</span></span> <span data-ttu-id="6a513-109">Ele também está disponível para dispositivos Windows 7 por meio de um Hot Fix do KB.</span><span class="sxs-lookup"><span data-stu-id="6a513-109">It's also available to Windows 7 devices through a KB hot fix.</span></span> <span data-ttu-id="6a513-110">No Windows 10, vários novos recursos foram introduzidos, incluindo um mecanismo de passagem para comandos do NVMe específicos do fornecedor e atualizações para os IOCTLs existentes.</span><span class="sxs-lookup"><span data-stu-id="6a513-110">In Windows 10, several new features were introduced, including a pass-through mechanism for vendor-specific NVMe commands and updates to existing IOCTLs.</span></span>

<span data-ttu-id="6a513-111">Este tópico fornece uma visão geral das APIs de uso geral que você pode usar para acessar as unidades do NVMe no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6a513-111">This topic provides an overview of general-use APIs that you can use to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="6a513-112">Ele também descreve:</span><span class="sxs-lookup"><span data-stu-id="6a513-112">It also describes:</span></span>

-   <span data-ttu-id="6a513-113">Como enviar um comando do NVMe específico do fornecedor com [passagem](#pass-through-mechanism)</span><span class="sxs-lookup"><span data-stu-id="6a513-113">How to send a vendor-specific NVMe command with [pass-through](#pass-through-mechanism)</span></span>
-   <span data-ttu-id="6a513-114">Como [enviar um comando de identificação, obter recursos ou obter páginas de log](#protocol-specific-queries) para a unidade NVMe</span><span class="sxs-lookup"><span data-stu-id="6a513-114">How to [send an Identify, Get Features, or Get Log Pages command](#protocol-specific-queries) to the NVMe drive</span></span>
-   <span data-ttu-id="6a513-115">Como [obter informações de temperatura](#temperature-queries) de uma unidade NVMe</span><span class="sxs-lookup"><span data-stu-id="6a513-115">How to [obtain temperature information](#temperature-queries) from an NVMe drive</span></span>
-   <span data-ttu-id="6a513-116">Como executar comandos de alteração de comportamento, como a [configuração de limites de temperatura](#behavior-changing-commands)</span><span class="sxs-lookup"><span data-stu-id="6a513-116">How to perform behavior changing commands, such as [setting temperature thresholds](#behavior-changing-commands)</span></span>

## <a name="apis-for-working-with-nvme-drives"></a><span data-ttu-id="6a513-117">APIs para trabalhar com unidades NVMe</span><span class="sxs-lookup"><span data-stu-id="6a513-117">APIs for working with NVMe drives</span></span>

<span data-ttu-id="6a513-118">Você pode usar as seguintes APIs de uso geral para acessar as unidades do NVMe no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6a513-118">You can use the following general-use APIs to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="6a513-119">Essas APIs podem ser encontradas em **winioctl. h** para aplicativos de modo de usuário e **ntddstor. h** para drivers de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="6a513-119">These APIs can be found in **winioctl.h** for user mode applications, and **ntddstor.h** for kernel mode drivers.</span></span> <span data-ttu-id="6a513-120">Para obter mais informações sobre arquivos de cabeçalho, consulte [arquivos de cabeçalho](#header-files).</span><span class="sxs-lookup"><span data-stu-id="6a513-120">For more information about header files, see [Header files](#header-files).</span></span>

-   <span data-ttu-id="6a513-121">[**IOCTL \_ \_ \_ Comando de protocolo de armazenamento**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use este IOCTL com a estrutura de **\_ \_ comando do protocolo de armazenamento** para emitir comandos do NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-121">[**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use this IOCTL with the **STORAGE\_PROTOCOL\_COMMAND** structure to issue NVMe commands.</span></span> <span data-ttu-id="6a513-122">Esse IOCTL habilita a passagem de NVMe e dá suporte ao log de efeitos de comando no NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-122">This IOCTL enables NVMe pass-through and supports the Command Effects log in NVMe.</span></span> <span data-ttu-id="6a513-123">Você pode usá-lo com comandos específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6a513-123">You can use it with vendor-specific commands.</span></span> <span data-ttu-id="6a513-124">Para obter mais informações, consulte [mecanismo de passagem](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="6a513-124">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

-   <span data-ttu-id="6a513-125">[**Armazenamento \_ do \_Comando de protocolo**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : essa estrutura de buffer de entrada inclui um campo **ReturnStatus** que pode ser usado para relatar os valores de status a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a513-125">[**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : This input-buffer structure includes a **ReturnStatus** field that can be used report the following status values.</span></span>
    -   <span data-ttu-id="6a513-126">**STATUS do protocolo de armazenamento \_ \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="6a513-126">**STORAGE\_PROTOCOL\_STATUS\_PENDING**</span></span>
    -   <span data-ttu-id="6a513-127">**\_êxito do \_ status do protocolo de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="6a513-127">**STORAGE\_PROTOCOL\_STATUS\_SUCCESS**</span></span>
    -   <span data-ttu-id="6a513-128">**\_erro de \_ status do protocolo de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="6a513-128">**STORAGE\_PROTOCOL\_STATUS\_ERROR**</span></span>
    -   <span data-ttu-id="6a513-129">**\_ \_ \_ solicitação inválida de status do protocolo de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="6a513-129">**STORAGE\_PROTOCOL\_STATUS\_INVALID\_REQUEST**</span></span>
    -   <span data-ttu-id="6a513-130">**STATUS do protocolo de armazenamento \_ \_ \_ sem \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="6a513-130">**STORAGE\_PROTOCOL\_STATUS\_NO\_DEVICE**</span></span>
    -   <span data-ttu-id="6a513-131">**STATUS de protocolo de armazenamento \_ \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="6a513-131">**STORAGE\_PROTOCOL\_STATUS\_BUSY**</span></span>
    -   <span data-ttu-id="6a513-132">**\_saturação de \_ dados de status do protocolo de armazenamento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a513-132">**STORAGE\_PROTOCOL\_STATUS\_DATA\_OVERRUN**</span></span>
    -   <span data-ttu-id="6a513-133">**\_ \_ \_ recursos insuficientes do status do protocolo de armazenamento \_**</span><span class="sxs-lookup"><span data-stu-id="6a513-133">**STORAGE\_PROTOCOL\_STATUS\_INSUFFICIENT\_RESOURCES**</span></span>
    -   <span data-ttu-id="6a513-134">**STATUS do protocolo de armazenamento \_ \_ \_ não \_ suportado**</span><span class="sxs-lookup"><span data-stu-id="6a513-134">**STORAGE\_PROTOCOL\_STATUS\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="6a513-135">[**IOCTL \_ \_ \_ Propriedade de consulta de armazenamento**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use este IOCTL com a estrutura de **\_ \_ consulta de propriedade de armazenamento** para recuperar informações do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a513-135">[**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use this IOCTL with the **STORAGE\_PROPERTY\_QUERY** structure to retrieve device information.</span></span> <span data-ttu-id="6a513-136">Para obter mais informações, consulte [consultas específicas de protocolo](#protocol-specific-queries) e [consultas de temperatura](#temperature-queries).</span><span class="sxs-lookup"><span data-stu-id="6a513-136">For more info, see [Protocol-specific queries](#protocol-specific-queries) and [Temperature queries](#temperature-queries).</span></span>

-   <span data-ttu-id="6a513-137">[**Armazenamento \_ do \_Consulta de propriedade**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : essa estrutura inclui os campos **PropertyId** e **AdditionalParameters** para especificar os dados a serem consultados.</span><span class="sxs-lookup"><span data-stu-id="6a513-137">[**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : This structure includes the **PropertyId** and **AdditionalParameters** fields to specify the data to be queried.</span></span> <span data-ttu-id="6a513-138">Na **PropertyId** arquivada, use a enumeração de **\_ \_ ID de propriedade de armazenamento** para especificar o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6a513-138">In the **PropertyId** filed, use the **STORAGE\_PROPERTY\_ID** enumeration to specify the type of data.</span></span> <span data-ttu-id="6a513-139">Use o campo **AdditionalParameters** para especificar mais detalhes, dependendo do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6a513-139">Use the **AdditionalParameters** field to specify more details, depending on the type of data.</span></span> <span data-ttu-id="6a513-140">Para dados específicos de protocolo, use a estrutura de **\_ \_ \_ dados específica do protocolo de armazenamento** no campo **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="6a513-140">For protocol-specific data, use the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure in the **AdditionalParameters** field.</span></span> <span data-ttu-id="6a513-141">Para dados de temperatura, use a estrutura **\_ \_ informações de temperatura de armazenamento** no campo **AdditionalParameters** .</span><span class="sxs-lookup"><span data-stu-id="6a513-141">For temperature data, use the **STORAGE\_TEMPERATURE\_INFO** structure in the **AdditionalParameters** field.</span></span>
-   <span data-ttu-id="6a513-142">[**Armazenamento \_ do \_ID da propriedade**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : essa enumeração inclui novos valores que permitem que a **\_ \_ \_ propriedade de consulta de armazenamento do IOCTL** recupere informações específicas de protocolo e de temperatura.</span><span class="sxs-lookup"><span data-stu-id="6a513-142">[**STORAGE\_PROPERTY\_ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : This enumeration includes new values that allow **IOCTL\_STORAGE\_QUERY\_PROPERTY** to retrieve protocol-specific and temperature information.</span></span>

    -   <span data-ttu-id="6a513-143">**StorageAdapterProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="6a513-143">**StorageAdapterProtocolSpecificProperty**</span></span>
    -   <span data-ttu-id="6a513-144">**StorageDeviceProtocolSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="6a513-144">**StorageDeviceProtocolSpecificProperty**</span></span>

    <span data-ttu-id="6a513-145">Use uma dessas IDs de propriedade específicas de protocolo em combinação com **\_ \_ \_ dados específicos do protocolo de armazenamento** para recuperar dados específicos do protocolo na estrutura do [**\_ \_ \_ descritor de dados do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="6a513-145">Use one of these protocol-specific property IDs in combination with **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** to retrieve protocol-specific data in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) structure.</span></span>

    -   <span data-ttu-id="6a513-146">**StorageAdapterTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="6a513-146">**StorageAdapterTemperatureProperty**</span></span>
    -   <span data-ttu-id="6a513-147">**StorageDeviceTemperatureProperty**</span><span class="sxs-lookup"><span data-stu-id="6a513-147">**StorageDeviceTemperatureProperty**</span></span>

    <span data-ttu-id="6a513-148">Use uma dessas IDs de propriedade de temperatura para recuperar dados de temperatura na estrutura do [**\_ \_ \_ descritor de dados de temperatura de armazenamento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="6a513-148">Use one of these temperature property IDs to retrieve temperature data in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) structure.</span></span>

-   <span data-ttu-id="6a513-149">[**Armazenamento \_ do \_ \_ Dados específicos do protocolo**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : recupere dados específicos do NVMe quando essa estrutura é usada para o campo **AdditionalParameters** da **\_ \_ consulta de propriedade de armazenamento** e um valor de enumeração de [**\_ \_ \_ \_ tipo de dados de protocolo de armazenamento NVMe**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) é especificado.</span><span class="sxs-lookup"><span data-stu-id="6a513-149">[**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Retrieve NVMe-specific data when this structure is used for the **AdditionalParameters** field of **STORAGE\_PROPERTY\_QUERY** and a [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) enum value is specified.</span></span> <span data-ttu-id="6a513-150">Use um dos seguintes valores **de \_ \_ tipo de \_ dados \_ NVME do protocolo de armazenamento** no campo **DataType** da estrutura de **\_ \_ \_ dados específica do protocolo de armazenamento** :</span><span class="sxs-lookup"><span data-stu-id="6a513-150">Use one of the following **STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE** values in the **DataType** field of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure:</span></span>

    -   <span data-ttu-id="6a513-151">Use **NVMeDataTypeIdentify** para obter dados do controlador de identificação ou identificar dados de namespace.</span><span class="sxs-lookup"><span data-stu-id="6a513-151">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="6a513-152">Use **NVMeDataTypeLogPage** para obter páginas de log (incluindo dados inteligentes/de integridade).</span><span class="sxs-lookup"><span data-stu-id="6a513-152">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="6a513-153">Use **NVMeDataTypeFeature** para obter recursos da unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-153">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

-   <span data-ttu-id="6a513-154">[**Armazenamento \_ do \_Informações de temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : essa estrutura é usada para manter dados de temperatura específicos.</span><span class="sxs-lookup"><span data-stu-id="6a513-154">[**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : This structure is used to hold specific temperature data.</span></span> <span data-ttu-id="6a513-155">Ele é usado no **\_ \_ \_ descritor de dados TEMERATURE de armazenamento** para retornar os resultados de uma consulta de temperatura.</span><span class="sxs-lookup"><span data-stu-id="6a513-155">It's used in the **STORAGE\_TEMERATURE\_DATA\_DESCRIPTOR** to return the results of a temperature query.</span></span>

-   <span data-ttu-id="6a513-156">[**IOCTL \_ \_Limite de \_ temperatura \_ do conjunto de armazenamento**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use este IOCTL com a estrutura de **\_ \_ limite de temperatura de armazenamento** para definir limites de temperatura.</span><span class="sxs-lookup"><span data-stu-id="6a513-156">[**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use this IOCTL with the **STORAGE\_TEMPERATURE\_THRESHOLD** structure to set temperature thresholds.</span></span> <span data-ttu-id="6a513-157">Para obter mais informações, consulte [comportamento alterando comandos](#behavior-changing-commands).</span><span class="sxs-lookup"><span data-stu-id="6a513-157">For more info, see [Behavior changing commands](#behavior-changing-commands).</span></span>

-   <span data-ttu-id="6a513-158">[**Armazenamento \_ do \_Limite de temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : essa estrutura é usada como um buffer de entrada para especificar o limite de temperatura.</span><span class="sxs-lookup"><span data-stu-id="6a513-158">[**STORAGE\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : This structure is used as an input buffer to specify the temperature threshold.</span></span> <span data-ttu-id="6a513-159">O campo de **limite** excedente (booliano) especifica se o campo de **limite** é acima do valor limite ou não (caso contrário, é o valor de limite).</span><span class="sxs-lookup"><span data-stu-id="6a513-159">The **OverThreshold** field (boolean) specifies if the **Threshold** field is the over threshold value or not (otherwise, it's the under threshold value).</span></span>

## <a name="pass-through-mechanism"></a><span data-ttu-id="6a513-160">Mecanismo de passagem</span><span class="sxs-lookup"><span data-stu-id="6a513-160">Pass-through mechanism</span></span>

<span data-ttu-id="6a513-161">Os comandos que não são definidos na especificação NVMe são os mais difíceis para o sistema operacional host lidar – o host não tem informações sobre os efeitos que os comandos podem ter no dispositivo de destino, a infraestrutura exposta (namespaces/tamanhos de bloco) e seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="6a513-161">Commands which are not defined in the NVMe specification are the most difficult for the host OS to handle – the host has no insight into the effects that the commands may have on the target device, the exposed infrastructure (namespaces/block sizes), and its behavior.</span></span>

<span data-ttu-id="6a513-162">Para executar melhor esses comandos específicos do dispositivo por meio da pilha de armazenamento do Windows, um novo mecanismo de passagem permite que comandos específicos do fornecedor sejam canalizados.</span><span class="sxs-lookup"><span data-stu-id="6a513-162">To better carry such device specific commands through the Windows storage stack, a new pass-through mechanism allows vendor-specific commands to be piped through.</span></span> <span data-ttu-id="6a513-163">Esse pipe de passagem também ajudará no desenvolvimento de ferramentas de gerenciamento e teste.</span><span class="sxs-lookup"><span data-stu-id="6a513-163">This pass-through pipe will also aid in development of management and testing tools.</span></span> <span data-ttu-id="6a513-164">No entanto, esse mecanismo de passagem requer o uso do log de efeitos de comando.</span><span class="sxs-lookup"><span data-stu-id="6a513-164">However, this pass-through mechanism requires use of the Command Effects Log.</span></span> <span data-ttu-id="6a513-165">Além disso, StoreNVMe.sys exige que todos os comandos, não apenas os comandos de passagem, sejam descritos no log de efeitos de comando.</span><span class="sxs-lookup"><span data-stu-id="6a513-165">Moreover, StoreNVMe.sys requires all commands, not just pass-through commands, to be described in the Command Effects Log.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a513-166">StorNVMe.sys e Storport.sys bloquearão qualquer comando para um dispositivo se ele não estiver descrito no log de efeitos de comando.</span><span class="sxs-lookup"><span data-stu-id="6a513-166">StorNVMe.sys and Storport.sys will block any command to a device if it is not described in the Command Effects Log.</span></span>

 

### <a name="supporting-the-command-effects-log"></a><span data-ttu-id="6a513-167">Suporte ao log de efeitos de comando</span><span class="sxs-lookup"><span data-stu-id="6a513-167">Supporting the Command Effects Log</span></span>

<span data-ttu-id="6a513-168">O log de efeitos de comando (conforme descrito em comandos com suporte e efeitos, a seção 5.10.1.5 da [especificação do NVMe 1,2](https://nvmexpress.org/specifications)) permite a descrição dos efeitos de comandos específicos do fornecedor em conjunto com comandos definidos pela especificação.</span><span class="sxs-lookup"><span data-stu-id="6a513-168">The Command Effects Log (as described in Commands Supported and Effects, section 5.10.1.5 of [NVMe Specification 1.2](https://nvmexpress.org/specifications)) allows the description of the effects of vendor-specific commands together with specification-defined commands.</span></span> <span data-ttu-id="6a513-169">Isso facilita a validação de suporte de comandos, bem como a otimização do comportamento do comando, e, portanto, deve ser implementado para todo o conjunto de comandos que o dispositivo suporta.</span><span class="sxs-lookup"><span data-stu-id="6a513-169">This facilitates both command support validation as well as command behavior optimization, and therefore should be implemented for the entire set of commands that the device supports.</span></span> <span data-ttu-id="6a513-170">As condições a seguir descrevem o resultado de como o comando é enviado com base em sua entrada de log de efeitos de comando.</span><span class="sxs-lookup"><span data-stu-id="6a513-170">The following conditions describe the result on how the command is sent based on its Command Effects Log entry.</span></span>

<span data-ttu-id="6a513-171">Para qualquer comando específico descrito no log de efeitos de comando...</span><span class="sxs-lookup"><span data-stu-id="6a513-171">For any specific command described in the Command Effects Log...</span></span>

<span data-ttu-id="6a513-172">**Embora**:</span><span class="sxs-lookup"><span data-stu-id="6a513-172">**While**:</span></span>

-   <span data-ttu-id="6a513-173">O comando com suporte (CSUPP) está definido como ' 1 ', indicando que o comando tem suporte do controlador (bit 01)</span><span class="sxs-lookup"><span data-stu-id="6a513-173">Command Supported (CSUPP) is set to ‘1’ signifying that the command is supported by the controller (Bit 01)</span></span>

    > [!Note]  
    > <span data-ttu-id="6a513-174">Quando CSUPP é definido como ' 0 ' (indicando que não há suporte para o comando), o comando será bloqueado</span><span class="sxs-lookup"><span data-stu-id="6a513-174">When CSUPP is set to ‘0’ (signifying that the command is not supported) the command will be blocked</span></span>

     

<span data-ttu-id="6a513-175">**E se** qualquer um dos seguintes for definido:</span><span class="sxs-lookup"><span data-stu-id="6a513-175">**And if** any of the following is set:</span></span>

-   <span data-ttu-id="6a513-176">A alteração de capacidade do controlador (CCC) está definida como ' 1 ', indicando que o comando pode alterar os recursos do controlador (bit 04)</span><span class="sxs-lookup"><span data-stu-id="6a513-176">Controller Capability Change (CCC) is set to ‘1’ signifying that the command may change controller capabilities (Bit 04)</span></span>

-   <span data-ttu-id="6a513-177">A NIC (alteração de inventário) de namespace está definida como ' 1 ', indicando que o comando pode alterar o número ou recursos para vários namespaces (bit 03)</span><span class="sxs-lookup"><span data-stu-id="6a513-177">Namespace Inventory Change (NIC) is set to ‘1’ signifying that the command may change the number, or capabilities for multiple namespaces (Bit 03)</span></span>

-   <span data-ttu-id="6a513-178">A NCC (alteração de capacidade de namespace) está definida como ' 1 ', indicando que o comando pode alterar os recursos de um único namespace (bit 02)</span><span class="sxs-lookup"><span data-stu-id="6a513-178">Namespace Capability Change (NCC) is set to ‘1’ signifying that the command may change the capabilities of a single namespace (Bit 02)</span></span>

-   <span data-ttu-id="6a513-179">A CSE (envio e execução de comando) é definida como 001B ou 010b, significando que o comando pode ser enviado quando não há nenhum outro comando pendente para o mesmo ou qualquer namespace, e esse outro comando não deve ser enviado para o mesmo ou para qualquer namespace até que esse comando seja concluído (bits 18:16)</span><span class="sxs-lookup"><span data-stu-id="6a513-179">Command Submission and Execution (CSE) is set to 001b or 010b, signifying that the command may be submitted when there is no other outstanding command to the same or any namespace, and that another command should not be submitted to the same or any namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="6a513-180">**Em seguida,** o comando será enviado como o único comando pendente para o adaptador.</span><span class="sxs-lookup"><span data-stu-id="6a513-180">**Then** the command will be sent as the only command outstanding to the adapter.</span></span>

<span data-ttu-id="6a513-181">**Caso contrário, se**:</span><span class="sxs-lookup"><span data-stu-id="6a513-181">**Else if**:</span></span>

-   <span data-ttu-id="6a513-182">A CSE (envio e execução de comando) é definida como 001B, indicando que o comando pode ser enviado quando não há nenhum outro comando pendente para o mesmo namespace e que outro comando não deve ser enviado ao mesmo namespace até que esse comando seja concluído (bits 18:16)</span><span class="sxs-lookup"><span data-stu-id="6a513-182">Command Submission and Execution (CSE) is set to 001b, signifying that the command may be submitted when there is no other outstanding command to the same namespace, and that another command should not be submitted to the same namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="6a513-183">**Em seguida,** o comando será enviado como o único comando pendente para o objeto de número de unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="6a513-183">**Then** the command will be sent as the only command outstanding to the Logical Unit Number object (LUN).</span></span>

<span data-ttu-id="6a513-184">**Caso contrário**, o comando é enviado com outros comandos pendentes sem inibição.</span><span class="sxs-lookup"><span data-stu-id="6a513-184">**Otherwise**, the command is sent with other commands outstanding without inhibition.</span></span> <span data-ttu-id="6a513-185">Por exemplo, se um comando específico do fornecedor for enviado para o dispositivo para recuperar informações estatísticas que não são definidas pela especificação, não deverá haver nenhum risco para alterar o comportamento do dispositivo ou a capacidade de executar comandos de e/s.</span><span class="sxs-lookup"><span data-stu-id="6a513-185">For example, if a vendor-specific command is sent to the device to retrieve statistical information that is not spec-defined, there should be no risk to changing the device’s behavior or capability to execute I/O commands.</span></span> <span data-ttu-id="6a513-186">Essas solicitações podem ser atendidas em paralelo à e/s e nenhum Pause-retomar será necessário.</span><span class="sxs-lookup"><span data-stu-id="6a513-186">Such requests could be serviced in parallel to I/O and no pause-resume would be necessary.</span></span>

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a><span data-ttu-id="6a513-187">Usando o \_ \_ comando de protocolo de armazenamento do IOCTL \_ para enviar comandos</span><span class="sxs-lookup"><span data-stu-id="6a513-187">Using IOCTL\_STORAGE\_PROTOCOL\_COMMAND to send commands</span></span>

<span data-ttu-id="6a513-188">A passagem pode ser realizada usando o [**comando de \_ \_ protocolo de \_ armazenamento do IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduzido no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6a513-188">Pass-through can be conducted using the [**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduced in Windows 10.</span></span> <span data-ttu-id="6a513-189">Esse IOCTL foi projetado para ter um comportamento semelhante como os IOCTLs de passagem SCSI e ATA existentes, para enviar um comando incorporado ao dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6a513-189">This IOCTL was designed to have a similar behavior as the existing SCSI and ATA pass-through IOCTLs, to send an embedded command to the target device.</span></span> <span data-ttu-id="6a513-190">Por meio desse IOCTL, a passagem pode ser enviada para um dispositivo de armazenamento, incluindo uma unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-190">Via this IOCTL, pass-through can be sent to a storage device, including an NVMe drive.</span></span>

<span data-ttu-id="6a513-191">Por exemplo, no NVMe, o IOCTL permitirá o envio dos seguintes códigos de comando.</span><span class="sxs-lookup"><span data-stu-id="6a513-191">For example, in NVMe, the IOCTL will allow the sending down of the following command codes.</span></span>

-   <span data-ttu-id="6a513-192">Comandos de administrador específicos do fornecedor (C0h – FFh)</span><span class="sxs-lookup"><span data-stu-id="6a513-192">Vendor Specific Admin Commands (C0h – FFh)</span></span>
-   <span data-ttu-id="6a513-193">Comandos de NVMe específicos do fornecedor (80h – FFh)</span><span class="sxs-lookup"><span data-stu-id="6a513-193">Vendor Specific NVMe Commands (80h – FFh)</span></span>

<span data-ttu-id="6a513-194">Assim como acontece com todos os outros IOCTLs, use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar o IOCTL de passagem para baixo.</span><span class="sxs-lookup"><span data-stu-id="6a513-194">As with all other IOCTLs, Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to send the pass-through IOCTL down.</span></span> <span data-ttu-id="6a513-195">O IOCTL é populado usando a estrutura de buffer de entrada do [**\_ \_ comando do protocolo de armazenamento**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) encontrada em **ntddstor. h**.</span><span class="sxs-lookup"><span data-stu-id="6a513-195">The IOCTL is populated using the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) input-buffer structure found in **ntddstor.h**.</span></span> <span data-ttu-id="6a513-196">Preencha o campo de **comando** com o comando específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6a513-196">Populate the **Command** field with the vendor-specific command.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



<span data-ttu-id="6a513-197">O comando específico do fornecedor desejado para ser enviado deve ser preenchido no campo realçado acima.</span><span class="sxs-lookup"><span data-stu-id="6a513-197">The vendor specific command desired to be sent should be populated in the highlighted field above.</span></span> <span data-ttu-id="6a513-198">Observe novamente que o log de efeitos de comando deve ser implementado para comandos de passagem.</span><span class="sxs-lookup"><span data-stu-id="6a513-198">Note again that the Command Effects Log must be implemented for pass-through commands.</span></span> <span data-ttu-id="6a513-199">Em particular, esses comandos precisam ser relatados como com suporte no log de efeitos de comando (consulte a seção anterior para obter mais informações).</span><span class="sxs-lookup"><span data-stu-id="6a513-199">In particular, these commands need to be reported as supported in the Command Effects Log (see previous section for more information).</span></span> <span data-ttu-id="6a513-200">Observe também que os campos da PRP são específicos do driver, portanto, os aplicativos que enviam comandos podem deixá-los como 0.</span><span class="sxs-lookup"><span data-stu-id="6a513-200">Also note that PRP fields are driver specific thus applications sending commands can leave them as 0.</span></span>

<span data-ttu-id="6a513-201">Por fim, esse IOCTL de passagem destina-se ao envio de comandos específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6a513-201">Finally, this pass-through IOCTL is intended for sending vendor-specific commands.</span></span> <span data-ttu-id="6a513-202">Para enviar outros comandos do NVMe ou não específicos do fornecedor, como identificar, esse IOCTL de passagem não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="6a513-202">To send other admin or non-vendor specific NVMe commands such as Identify, this pass-through IOCTL should not be used.</span></span> <span data-ttu-id="6a513-203">Por exemplo, **a \_ \_ \_ propriedade de consulta de armazenamento de IOCTL** deve ser usada para identificar ou obter páginas de log.</span><span class="sxs-lookup"><span data-stu-id="6a513-203">For example, **IOCTL\_STORAGE\_QUERY\_PROPERTY** should be used for Identify or Get Log Pages.</span></span> <span data-ttu-id="6a513-204">Para obter mais informações, consulte a próxima seção, [consultas específicas de protocolo](/windows).</span><span class="sxs-lookup"><span data-stu-id="6a513-204">For more info, see the next section, [Protocol-specific queries](/windows).</span></span>

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a><span data-ttu-id="6a513-205">Não atualizar o firmware por meio do mecanismo de passagem</span><span class="sxs-lookup"><span data-stu-id="6a513-205">Don't update firmware through the pass-through mechanism</span></span>

<span data-ttu-id="6a513-206">Os comandos de download e ativação de firmware não devem ser enviados usando passagem.</span><span class="sxs-lookup"><span data-stu-id="6a513-206">Firmware download and activation commands should not be sent using pass-through.</span></span> <span data-ttu-id="6a513-207">**IOCTL \_ O \_ \_ comando de protocolo de armazenamento** só deve ser usado para comandos específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6a513-207">**IOCTL\_STORAGE\_PROTOCOL\_COMMAND** should only be used for vendor-specific commands.</span></span>

<span data-ttu-id="6a513-208">Em vez disso, use os seguintes IOCTLs de armazenamento geral (introduzidos no Windows 10) para evitar aplicativos diretamente usando a \_ versão de miniporta SCSI do firmware IOCTL.</span><span class="sxs-lookup"><span data-stu-id="6a513-208">Instead, use the following general storage IOCTLs (introduced in Windows 10) to avoid applications directly using the SCSI\_miniport version of the Firmware IOCTL.</span></span> <span data-ttu-id="6a513-209">Os drivers de armazenamento irão converter o IOCTL em um comando SCSI ou na \_ versão de miniporta SCSI do IOCTL para a miniporta.</span><span class="sxs-lookup"><span data-stu-id="6a513-209">Storage drivers will translate the IOCTL to either a SCSI command or the SCSI\_miniport version of the IOCTL to the miniport.</span></span>

<span data-ttu-id="6a513-210">Esses IOCTLs são recomendados para o desenvolvimento de ferramentas de atualização de firmware no Windows 10 e no Windows Server 2016:</span><span class="sxs-lookup"><span data-stu-id="6a513-210">These IOCTLs are recommended for developing firmware upgrade tools in Windows 10 and Windows Server 2016:</span></span>

-   [<span data-ttu-id="6a513-211">**\_informações de \_ obtenção do firmware de armazenamento do IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a513-211">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [<span data-ttu-id="6a513-212">**\_download do \_ firmware de armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="6a513-212">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [<span data-ttu-id="6a513-213">**\_ativação do \_ firmware de armazenamento do IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="6a513-213">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

<span data-ttu-id="6a513-214">Para obter informações de armazenamento e atualizar o firmware, o Windows também dá suporte a cmdlets do PowerShell para fazer isso rapidamente:</span><span class="sxs-lookup"><span data-stu-id="6a513-214">For getting storage information and updating firmware, Windows also supports PowerShell cmdlets for doing this quickly:</span></span>

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> <span data-ttu-id="6a513-215">Para atualizar o firmware no NVMe no Windows 8.1, use \_ o \_ firmware de miniporta SCSI do IOCTL \_ .</span><span class="sxs-lookup"><span data-stu-id="6a513-215">To update firmware on NVMe in Windows 8.1, use IOCTL\_SCSI\_MINIPORT\_FIRMWARE.</span></span> <span data-ttu-id="6a513-216">Este IOCTL não foi reportado para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a513-216">This IOCTL was not backported to Windows 7.</span></span> <span data-ttu-id="6a513-217">Para obter mais informações, consulte [atualizando o firmware para um dispositivo NVMe no Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span><span class="sxs-lookup"><span data-stu-id="6a513-217">For more information, see [Upgrading Firmware for an NVMe Device in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span></span>

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a><span data-ttu-id="6a513-218">Retornando erros por meio do mecanismo de passagem</span><span class="sxs-lookup"><span data-stu-id="6a513-218">Returning errors through the pass-through mechanism</span></span>

<span data-ttu-id="6a513-219">Semelhante aos IOCTLs de passagem SCSI e ATA, quando um comando/solicitação é enviado para a miniporta ou dispositivo, o IOCTL retorna se ele foi bem-sucedido ou não.</span><span class="sxs-lookup"><span data-stu-id="6a513-219">Similar to SCSI and ATA pass-through IOCTLs, when a command/request is sent to the miniport or device, the IOCTL returns if it was successful or not.</span></span> <span data-ttu-id="6a513-220">Na estrutura [**de \_ \_ comando do protocolo de armazenamento**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , o IOCTL retorna o status por meio do campo **ReturnStatus** .</span><span class="sxs-lookup"><span data-stu-id="6a513-220">In the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) structure, the IOCTL returns the status through the **ReturnStatus** field.</span></span>

### <a name="example-sending-a-vendor-specific-command"></a><span data-ttu-id="6a513-221">Exemplo: enviando um comando específico do fornecedor</span><span class="sxs-lookup"><span data-stu-id="6a513-221">Example: sending a vendor-specific command</span></span>

<span data-ttu-id="6a513-222">Neste exemplo, um comando arbitrário específico do fornecedor (0xFF) é enviado por passagem para uma unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-222">In this example, an arbitrary vendor-specific command (0xFF) is sent via pass-through to an NVMe drive.</span></span> <span data-ttu-id="6a513-223">O código a seguir aloca um buffer, Inicializa uma consulta e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="6a513-223">The following code allocates a buffer, initializes a query, and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



<span data-ttu-id="6a513-224">Neste exemplo, esperamos que `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` o comando tenha sido bem-sucedido para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a513-224">In this example, we expect `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` if the command succeeded to the device.</span></span>

## <a name="protocol-specific-queries"></a><span data-ttu-id="6a513-225">Consultas específicas de protocolo</span><span class="sxs-lookup"><span data-stu-id="6a513-225">Protocol-specific queries</span></span>

<span data-ttu-id="6a513-226">Windows 8.1 introduziu a propriedade de consulta de armazenamento de IOCTL para recuperação de dados. [**\_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property)</span><span class="sxs-lookup"><span data-stu-id="6a513-226">Windows 8.1 introduced [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) for data retrieval.</span></span> <span data-ttu-id="6a513-227">No Windows 10, o IOCTL foi aprimorado para dar suporte a recursos de NVMe comumente solicitados, como **obter páginas de log**, **obter recursos** e **identificar**.</span><span class="sxs-lookup"><span data-stu-id="6a513-227">In Windows 10, the IOCTL was enhanced to support commonly requested NVMe features such as **Get Log Pages**, **Get Features**, and **Identify**.</span></span> <span data-ttu-id="6a513-228">Isso permite a recuperação de informações específicas de NVMe para fins de monitoramento e inventário.</span><span class="sxs-lookup"><span data-stu-id="6a513-228">This allows for the retrieval of NVMe specific information for monitoring and inventory purposes.</span></span>

<span data-ttu-id="6a513-229">O buffer de entrada para o IOCTL [**, \_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (do Windows 10) é mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="6a513-229">The input buffer for the IOCTL, [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



<span data-ttu-id="6a513-230">Ao usar [**a \_ \_ \_ propriedade de consulta de armazenamento do IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para recuperar informações específicas do protocolo NVMe no [**\_ \_ \_ descritor de dados do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure a estrutura de [**\_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6a513-230">When using [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) to retrieve NVMe protocol-specific information in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="6a513-231">Aloque um buffer que possa conter uma [**consulta de \_ propriedade \_ de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) e uma estrutura de [**\_ \_ \_ dados específica de protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) .</span><span class="sxs-lookup"><span data-stu-id="6a513-231">Allocate a buffer that can contains both a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) and a [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure.</span></span>

-   <span data-ttu-id="6a513-232">Defina o campo **PropertyId** como **StorageAdapterProtocolSpecificProperty** ou **StorageDeviceProtocolSpecificProperty** para uma solicitação de controlador ou dispositivo/namespace, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6a513-232">Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="6a513-233">Defina o campo **QueryType** como **PropertyStandardQuery**.</span><span class="sxs-lookup"><span data-stu-id="6a513-233">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

-   <span data-ttu-id="6a513-234">Preencha a estrutura de [**\_ \_ \_ dados específica do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) com os valores desejados.</span><span class="sxs-lookup"><span data-stu-id="6a513-234">Fill the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure with the desired values.</span></span> <span data-ttu-id="6a513-235">O início dos **\_ \_ \_ dados específicos do protocolo de armazenamento** é o campo **adicionalparameters** da [**\_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span><span class="sxs-lookup"><span data-stu-id="6a513-235">The start of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** is the **AdditionalParameters** field of [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span></span>

<span data-ttu-id="6a513-236">A estrutura de [**\_ \_ \_ dados específica do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (do Windows 10) é mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="6a513-236">The [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



<span data-ttu-id="6a513-237">Para especificar um tipo de informações específicas do protocolo NVMe, configure a estrutura de [**\_ \_ \_ dados específica do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6a513-237">To specify a type of NVMe protocol-specific information, configure the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure as follows:</span></span>

-   <span data-ttu-id="6a513-238">Defina o campo **ProtocolType** como **ProtocolTypeNVMe**.</span><span class="sxs-lookup"><span data-stu-id="6a513-238">Set the **ProtocolType** field to **ProtocolTypeNVMe**.</span></span>

-   <span data-ttu-id="6a513-239">Defina o campo **DataType** como um valor de enumeração definido [**pelo \_ \_ tipo de \_ dados \_ NVME do protocolo de armazenamento**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span><span class="sxs-lookup"><span data-stu-id="6a513-239">Set the **DataType** field to an enumeration value defined by [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span></span>

    -   <span data-ttu-id="6a513-240">Use **NVMeDataTypeIdentify** para obter dados do controlador de identificação ou identificar dados de namespace.</span><span class="sxs-lookup"><span data-stu-id="6a513-240">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="6a513-241">Use **NVMeDataTypeLogPage** para obter páginas de log (incluindo dados inteligentes/de integridade).</span><span class="sxs-lookup"><span data-stu-id="6a513-241">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="6a513-242">Use **NVMeDataTypeFeature** para obter recursos da unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-242">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

<span data-ttu-id="6a513-243">Quando **ProtocolTypeNVMe** é usado como o **ProtocolType**, as consultas para informações específicas de protocolo podem ser recuperadas em paralelo com outras e/s na unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-243">When **ProtocolTypeNVMe** is used as the **ProtocolType**, queries for protocol-specific information can be retrieved in parallel with other I/O on the NVMe drive.</span></span>

<span data-ttu-id="6a513-244">Os exemplos a seguir demonstram consultas específicas do protocolo NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-244">The following examples demonstrate NVMe protocol-specific queries.</span></span>

### <a name="example-nvme-identify-query"></a><span data-ttu-id="6a513-245">Exemplo: NVMe identificar consulta</span><span class="sxs-lookup"><span data-stu-id="6a513-245">Example: NVMe Identify query</span></span>

<span data-ttu-id="6a513-246">Neste exemplo, a solicitação **identificar** é enviada para uma unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-246">In this example, the **Identify** request is sent to an NVMe drive.</span></span> <span data-ttu-id="6a513-247">O código a seguir inicializa a estrutura de dados de consulta e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="6a513-247">The following code initializes the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



<span data-ttu-id="6a513-248">Observe que o chamador precisa alocar um único buffer contendo \_ a consulta de propriedade de armazenamento \_ e o tamanho dos \_ dados específicos do protocolo de armazenamento \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6a513-248">Note that the caller needs to allocate a single buffer containing STORAGE\_PROPERTY\_QUERY and the size of STORAGE\_PROTOCOL\_SPECIFIC\_DATA.</span></span> <span data-ttu-id="6a513-249">Neste exemplo, ele está usando o mesmo buffer para entrada e saída da consulta de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6a513-249">In this example, it’s using the same buffer for input and output from the property query.</span></span> <span data-ttu-id="6a513-250">É por isso que o buffer que foi alocado tem um tamanho de " \_ deslocamento de campo \_ ( \_ consulta de propriedade de armazenamento, adicionalparameters) + sizeof ( \_ dados específicos de protocolo de armazenamento \_ \_ ) + \_ tamanho máximo de log de NVME \_ \_ ".</span><span class="sxs-lookup"><span data-stu-id="6a513-250">That’s why the buffer that was allocated has a size of “FIELD\_OFFSET(STORAGE\_PROPERTY\_QUERY, AdditionalParameters) + sizeof(STORAGE\_PROTOCOL\_SPECIFIC\_DATA) + NVME\_MAX\_LOG\_SIZE”.</span></span> <span data-ttu-id="6a513-251">Embora buffers separados pudessem ser alocados para entrada e saída, é recomendável usar um único buffer para consultar informações relacionadas ao NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-251">Although separate buffers could be allocated for both input and output, we recommend using a single buffer to query NVMe related-information.</span></span>

### <a name="example-nvme-get-log-pages-query"></a><span data-ttu-id="6a513-252">Exemplo: NVMe obter consulta de páginas de log</span><span class="sxs-lookup"><span data-stu-id="6a513-252">Example: NVMe Get Log Pages query</span></span>

<span data-ttu-id="6a513-253">Neste exemplo, com base no anterior, a solicitação _ *obter páginas do log*\* é enviada para uma unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-253">In this example, based off of the previous one, the _ *Get Log Pages*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="6a513-254">O código a seguir prepara a estrutura de dados de consulta e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="6a513-254">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a><span data-ttu-id="6a513-255">Exemplo: consulta de obter recursos do NVMe</span><span class="sxs-lookup"><span data-stu-id="6a513-255">Example: NVMe Get Features query</span></span>

<span data-ttu-id="6a513-256">Neste exemplo, com base no anterior, a solicitação _ *Get Features*\* é enviada para uma unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-256">In this example, based off of the previous one, the _ *Get Features*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="6a513-257">O código a seguir prepara a estrutura de dados de consulta e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="6a513-257">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a><span data-ttu-id="6a513-258">Conjunto específico de protocolo</span><span class="sxs-lookup"><span data-stu-id="6a513-258">Protocol-specific set</span></span>

<span data-ttu-id="6a513-259">No Windows 10 19H1, o IOCTL_STORAGE_SET_PROPERTY foi aprimorado para oferecer suporte a recursos do NVMe set.</span><span class="sxs-lookup"><span data-stu-id="6a513-259">From Windows 10 19H1, the IOCTL_STORAGE_SET_PROPERTY was enhanced to support NVMe Set Features.</span></span>

<span data-ttu-id="6a513-260">O buffer de entrada para o IOCTL_STORAGE_SET_PROPERTY é mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="6a513-260">The input buffer for the IOCTL_STORAGE_SET_PROPERTY is shown here:</span></span>

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

<span data-ttu-id="6a513-261">Ao usar IOCTL_STORAGE_SET_PROPERTY para definir o recurso NVMe, configure a estrutura de STORAGE_PROPERTY_SET da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6a513-261">When using IOCTL_STORAGE_SET_PROPERTY to set NVMe feature, configure the STORAGE_PROPERTY_SET structure as follows:</span></span>

-   <span data-ttu-id="6a513-262">Alocar um buffer que pode conter um STORAGE_PROPERTY_SET e uma estrutura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT;</span><span class="sxs-lookup"><span data-stu-id="6a513-262">Allocate a buffer that can contains both a STORAGE_PROPERTY_SET and a STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure;</span></span>
-   <span data-ttu-id="6a513-263">Defina o campo PropertyId como StorageAdapterProtocolSpecificProperty ou StorageDeviceProtocolSpecificProperty para uma solicitação de controlador ou dispositivo/namespace, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6a513-263">Set the PropertyID field to StorageAdapterProtocolSpecificProperty or StorageDeviceProtocolSpecificProperty for a controller or device/namespace request, respectively.</span></span>
-   <span data-ttu-id="6a513-264">Preencha a estrutura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT com os valores desejados.</span><span class="sxs-lookup"><span data-stu-id="6a513-264">Fill the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure with the desired values.</span></span> <span data-ttu-id="6a513-265">O início da STORAGE_PROTOCOL_SPECIFIC_DATA_EXT é o campoparameters adicional de STORAGE_PROPERTY_SET.</span><span class="sxs-lookup"><span data-stu-id="6a513-265">The start of the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT is the AdditionalParameters field of STORAGE_PROPERTY_SET.</span></span>

<span data-ttu-id="6a513-266">A estrutura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT é mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="6a513-266">The STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure is shown here.</span></span>

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

<span data-ttu-id="6a513-267">Para especificar um tipo de recurso NVMe a ser definido, configure a estrutura STORAGE_PROTOCOL_SPECIFIC_DATA_EXT da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6a513-267">To specify a type of NVMe feature to set, configure the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure as follows:</span></span>
-   <span data-ttu-id="6a513-268">Defina o campo ProtocolType como ProtocolTypeNvme;</span><span class="sxs-lookup"><span data-stu-id="6a513-268">Set the ProtocolType field to ProtocolTypeNvme;</span></span>
-   <span data-ttu-id="6a513-269">Defina o campo DataType para o valor de enumeração NVMeDataTypeFeature definido por STORAGE_PROTOCOL_NVME_DATA_TYPE;</span><span class="sxs-lookup"><span data-stu-id="6a513-269">Set the DataType field to the enumeration value NVMeDataTypeFeature defined by STORAGE_PROTOCOL_NVME_DATA_TYPE;</span></span>

<span data-ttu-id="6a513-270">Os exemplos a seguir demonstram o conjunto de recursos do NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-270">The following examples demonstrate NVMe feature set.</span></span>

### <a name="example-nvme-set-features"></a><span data-ttu-id="6a513-271">Exemplo: NVMe Set Features</span><span class="sxs-lookup"><span data-stu-id="6a513-271">Example: NVMe Set Features</span></span>

<span data-ttu-id="6a513-272">Neste exemplo, a solicitação definir recursos é enviada para uma unidade NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-272">In this example, the Set Features request is sent to an NVMe drive.</span></span> <span data-ttu-id="6a513-273">O código a seguir prepara a estrutura de dados definida e, em seguida, envia o comando para o dispositivo por meio de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="6a513-273">The following code prepares the set data structure and then sends the command down to the device via DeviceIoControl.</span></span>

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a><span data-ttu-id="6a513-274">Consultas de temperatura</span><span class="sxs-lookup"><span data-stu-id="6a513-274">Temperature queries</span></span>

<span data-ttu-id="6a513-275">No Windows 10, [**a \_ \_ \_ propriedade de consulta de armazenamento do IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) também pode ser usada para consultar dados de temperatura de dispositivos NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-275">In Windows 10, [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) can also be used to query temperature data from NVMe devices.</span></span>

<span data-ttu-id="6a513-276">Para recuperar informações de temperatura de uma unidade NVMe no [**\_ \_ \_ descritor de dados de temperatura de armazenamento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure a estrutura de [**\_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6a513-276">To retrieve temperature information from an NVMe drive in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="6a513-277">Aloque um buffer que possa conter uma estrutura de [**\_ \_ consulta de propriedade de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .</span><span class="sxs-lookup"><span data-stu-id="6a513-277">Allocate a buffer that can contains a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure.</span></span>

-   <span data-ttu-id="6a513-278">Defina o campo **PropertyId** como **StorageAdapterTemperatureProperty** ou **StorageDeviceTemperatureProperty** para uma solicitação de controlador ou dispositivo/namespace, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6a513-278">Set the **PropertyID** field to **StorageAdapterTemperatureProperty** or **StorageDeviceTemperatureProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="6a513-279">Defina o campo **QueryType** como **PropertyStandardQuery**.</span><span class="sxs-lookup"><span data-stu-id="6a513-279">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

<span data-ttu-id="6a513-280">A estrutura de [**\_ \_ informações de temperatura de armazenamento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (do Windows 10) é mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="6a513-280">The [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a><span data-ttu-id="6a513-281">Comandos de alteração de comportamento</span><span class="sxs-lookup"><span data-stu-id="6a513-281">Behavior changing commands</span></span>

<span data-ttu-id="6a513-282">Comandos que manipulam atributos de dispositivo ou potencialmente impactam o comportamento do dispositivo são mais difíceis de lidar com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6a513-282">Commands that manipulate device attributes or potentially impact device behavior are more difficult for the operating system to deal with.</span></span> <span data-ttu-id="6a513-283">Se os atributos do dispositivo forem alterados em tempo de execução enquanto a e/s estiver sendo processada, poderão ocorrer problemas de integridade de dados ou de sincronização se não forem manipulados corretamente.</span><span class="sxs-lookup"><span data-stu-id="6a513-283">If device attributes change at run-time while I/O is being processed, synchronization or data integrity issues can arise if not properly handled.</span></span>

<span data-ttu-id="6a513-284">O comando NVMe **set-Features** é um bom exemplo de um comando de alteração de comportamento.</span><span class="sxs-lookup"><span data-stu-id="6a513-284">The NVMe **Set-Features** command is a good example of a behavior changing command.</span></span> <span data-ttu-id="6a513-285">Ele permite a alteração do mecanismo de arbitragem e a configuração de limites de temperatura.</span><span class="sxs-lookup"><span data-stu-id="6a513-285">It allows for the changing of the arbitration mechanism and the setting of temperature thresholds.</span></span> <span data-ttu-id="6a513-286">Para garantir que os dados em trânsito não estejam em risco quando os comandos set que afetam o comportamento forem enviados, o Windows pausará todas as e/s no dispositivo NVMe, as filas de drenagem e os buffers de liberação.</span><span class="sxs-lookup"><span data-stu-id="6a513-286">To ensure that in-flight data is not at risk when behavior-affecting set commands are sent down, Windows will pause all I/O to the NVMe device, drain queues, and flush buffers.</span></span> <span data-ttu-id="6a513-287">Depois que o comando Set for executado com êxito, a e/s será retomada (se possível).</span><span class="sxs-lookup"><span data-stu-id="6a513-287">Once the set command has executed successfully, I/O is resumed (if possible).</span></span> <span data-ttu-id="6a513-288">Se a e/s não puder ser retomada, uma redefinição de dispositivo poderá ser necessária.</span><span class="sxs-lookup"><span data-stu-id="6a513-288">If I/O cannot be resumed, a device reset may be required.</span></span>

### <a name="setting-temperature-thresholds"></a><span data-ttu-id="6a513-289">Definindo limites de temperatura</span><span class="sxs-lookup"><span data-stu-id="6a513-289">Setting temperature thresholds</span></span>

<span data-ttu-id="6a513-290">O Windows 10 introduziu o limite de temperatura do conjunto de armazenamento do IOCTL, um IOCTL para obter e definir limites de temperatura. [**\_ \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold)</span><span class="sxs-lookup"><span data-stu-id="6a513-290">Windows 10 introduced [**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), an IOCTL for getting and setting temperature thresholds.</span></span> <span data-ttu-id="6a513-291">Você também pode usá-lo para obter a temperatura atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a513-291">You can also use it to get the current temperature of the device.</span></span> <span data-ttu-id="6a513-292">O buffer de entrada/saída para este IOCTL é a estrutura de [**\_ \_ informações de temperatura de armazenamento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) , da seção de código anterior.</span><span class="sxs-lookup"><span data-stu-id="6a513-292">The input/output buffer for this IOCTL is the [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure, from the previous code section.</span></span>

### <a name="example-setting-over-threshold-temperature"></a><span data-ttu-id="6a513-293">Exemplo: definindo a temperatura excedente do limite</span><span class="sxs-lookup"><span data-stu-id="6a513-293">Example: Setting over-threshold temperature</span></span>

<span data-ttu-id="6a513-294">Neste exemplo, a temperatura excedente do limite de uma unidade de NVMe está definida.</span><span class="sxs-lookup"><span data-stu-id="6a513-294">In this example, an NVMe drive's over-threshold temperature is set.</span></span> <span data-ttu-id="6a513-295">O código a seguir prepara o comando e, em seguida, o envia para o dispositivo por meio de DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="6a513-295">The following code prepares the command and then sends it down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a><span data-ttu-id="6a513-296">Configurando recursos específicos do fornecedor</span><span class="sxs-lookup"><span data-stu-id="6a513-296">Setting vendor-specific features</span></span>

<span data-ttu-id="6a513-297">Sem o log de efeitos de comando, o driver não tem conhecimento das ramificações do comando.</span><span class="sxs-lookup"><span data-stu-id="6a513-297">Without the Command Effects Log, the driver has no knowledge of the ramifications of the command.</span></span> <span data-ttu-id="6a513-298">É por isso que o log de efeitos de comando é necessário.</span><span class="sxs-lookup"><span data-stu-id="6a513-298">This is why the Command Effects Log is required.</span></span> <span data-ttu-id="6a513-299">Ele ajuda o sistema operacional a determinar se um comando tem um impacto alto e se ele pode ser enviado em paralelo com outros comandos para a unidade.</span><span class="sxs-lookup"><span data-stu-id="6a513-299">It helps the operating system determine if a command is high impact and if it can be sent in parallel with other commands to the drive.</span></span>

<span data-ttu-id="6a513-300">O log de efeitos de comando ainda não é granular o suficiente para abranger os comandos **set-Features** específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6a513-300">The Command Effects Log is not yet granular enough to encompass vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="6a513-301">Por esse motivo, ainda não é possível enviar comandos **set-Features** específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6a513-301">For this reason, it is not yet possible to send vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="6a513-302">No entanto, é possível usar o mecanismo de passagem, discutido anteriormente, para enviar comandos específicos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6a513-302">However, it is possible to use the pass-through mechanism, discussed earlier, to send vendor-specific commands.</span></span> <span data-ttu-id="6a513-303">Para obter mais informações, consulte [mecanismo de passagem](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="6a513-303">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

## <a name="header-files"></a><span data-ttu-id="6a513-304">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6a513-304">Header files</span></span>

<span data-ttu-id="6a513-305">Os arquivos a seguir são relevantes para o desenvolvimento do NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-305">The following files are relevant to NVMe development.</span></span> <span data-ttu-id="6a513-306">Esses arquivos estão incluídos no [SDK (Software Development Kit) do Microsoft Windows](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="6a513-306">These files are included with the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).</span></span>



| <span data-ttu-id="6a513-307">Arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6a513-307">Header file</span></span>    | <span data-ttu-id="6a513-308">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a513-308">Description</span></span>                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a513-309">**ntddstor. h**</span><span class="sxs-lookup"><span data-stu-id="6a513-309">**ntddstor.h**</span></span> | <span data-ttu-id="6a513-310">Define constantes e tipos para acessar os drivers de classe de armazenamento do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="6a513-310">Defines constants and types for accessing the storage class drivers from kernel mode.</span></span>   |
| <span data-ttu-id="6a513-311">**nvme. h**</span><span class="sxs-lookup"><span data-stu-id="6a513-311">**nvme.h**</span></span>     | <span data-ttu-id="6a513-312">Para outras estruturas de dados relacionadas ao NVMe.</span><span class="sxs-lookup"><span data-stu-id="6a513-312">For other NVMe-related data-structures.</span></span>                                                 |
| <span data-ttu-id="6a513-313">**winioctl. h**</span><span class="sxs-lookup"><span data-stu-id="6a513-313">**winioctl.h**</span></span> | <span data-ttu-id="6a513-314">Para definições gerais de IOCTL do Win32, incluindo APIs de armazenamento para aplicativos de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="6a513-314">For overall Win32 IOCTL definitions, including storage APIs for user mode applications.</span></span> |



 

 

 
