---
description: Recupera os dados de encaminhamento de um computador de destino.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: Classe TargetForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: aba0a40ccd5611cecfe7450e518620d4d41ec1e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500764"
---
# <a name="targetforwarding-class"></a><span data-ttu-id="8443f-103">Classe TargetForwarding</span><span class="sxs-lookup"><span data-stu-id="8443f-103">TargetForwarding class</span></span>

<span data-ttu-id="8443f-104">Recupera os dados de encaminhamento de um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="8443f-104">Retrieves forwarding data from a target computer.</span></span>

> [!Note]  
> <span data-ttu-id="8443f-105">Um computador de destino pode ter vários encaminhadores configurados.</span><span class="sxs-lookup"><span data-stu-id="8443f-105">A target computer may have multiple forwarders configured.</span></span>

 

<span data-ttu-id="8443f-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8443f-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8443f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8443f-107">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
};
```

## <a name="members"></a><span data-ttu-id="8443f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8443f-108">Members</span></span>

<span data-ttu-id="8443f-109">A classe **TargetForwarding** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8443f-109">The **TargetForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="8443f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8443f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8443f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8443f-111">Properties</span></span>

<span data-ttu-id="8443f-112">A classe **TargetForwarding** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8443f-112">The **TargetForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8443f-113">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="8443f-113">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-116">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-116">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-117">As informações do ponto de extremidade do servidor do coletor.</span><span class="sxs-lookup"><span data-stu-id="8443f-117">The endpoint information of the collector server.</span></span> <span data-ttu-id="8443f-118">Essa propriedade é formatada como uma cadeia de caracteres de *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="8443f-118">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="8443f-119">**Computador**</span><span class="sxs-lookup"><span data-stu-id="8443f-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-122">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-123">O nome do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="8443f-123">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="8443f-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="8443f-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-125">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8443f-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-127">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-128">O carimbo de data/hora que indica quando a conexão foi estabelecida para os dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="8443f-128">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="8443f-129">**Destino**</span><span class="sxs-lookup"><span data-stu-id="8443f-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-132">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-132">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-133">O destino dos dados de encaminhamento, como um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8443f-133">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="8443f-134">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="8443f-134">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-137">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-137">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-138">O formato usado para gerar o destino dos dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="8443f-138">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="8443f-139">**Erro**</span><span class="sxs-lookup"><span data-stu-id="8443f-139">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-142">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-143">Uma mensagem de erro que descreve um erro encontrado.</span><span class="sxs-lookup"><span data-stu-id="8443f-143">An error message that describes an encountered error.</span></span> <span data-ttu-id="8443f-144">Essa propriedade estará vazia se nenhum erro for encontrado.</span><span class="sxs-lookup"><span data-stu-id="8443f-144">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="8443f-145">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="8443f-145">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-148">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-148">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-149">O tipo de arquivo que contém os dados de encaminhamento, como ETL.</span><span class="sxs-lookup"><span data-stu-id="8443f-149">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="8443f-150">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="8443f-150">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-153">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-154">As informações do ponto de extremidade do computador de destino, no formato legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="8443f-154">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="8443f-155">Essa propriedade é formatada como uma cadeia de caracteres de *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="8443f-155">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="8443f-156">Por exemplo, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="8443f-156">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="8443f-157">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="8443f-157">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-160">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-160">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-161">O SMBIOS **GUID** do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="8443f-161">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="8443f-162">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="8443f-162">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8443f-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8443f-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8443f-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8443f-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8443f-165">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8443f-165">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8443f-166">O endereço MAC do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="8443f-166">The MAC address of the target computer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8443f-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8443f-167">Requirements</span></span>



| <span data-ttu-id="8443f-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="8443f-168">Requirement</span></span> | <span data-ttu-id="8443f-169">Valor</span><span class="sxs-lookup"><span data-stu-id="8443f-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8443f-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8443f-170">Minimum supported client</span></span><br/> | <span data-ttu-id="8443f-171">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8443f-171">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="8443f-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8443f-172">Minimum supported server</span></span><br/> | <span data-ttu-id="8443f-173">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8443f-173">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="8443f-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="8443f-174">Namespace</span></span><br/>                | <span data-ttu-id="8443f-175">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="8443f-175">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="8443f-176">MOF</span><span class="sxs-lookup"><span data-stu-id="8443f-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8443f-177"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8443f-177"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="8443f-178">DLL</span><span class="sxs-lookup"><span data-stu-id="8443f-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8443f-179"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8443f-179"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8443f-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="8443f-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8443f-181">Provedor WMI do coletor de eventos de inicialização</span><span class="sxs-lookup"><span data-stu-id="8443f-181">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

