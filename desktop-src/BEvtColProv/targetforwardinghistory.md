---
description: O histórico recente de alterações nos dados de encaminhamento de um computador de destino.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Classe TargetForwardingHistory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089682"
---
# <a name="targetforwardinghistory-class"></a><span data-ttu-id="b7f22-103">Classe TargetForwardingHistory</span><span class="sxs-lookup"><span data-stu-id="b7f22-103">TargetForwardingHistory class</span></span>

<span data-ttu-id="b7f22-104">O histórico recente de alterações nos dados de encaminhamento de um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="b7f22-104">The recent history of changes to the forwarding data for a target computer.</span></span>

<span data-ttu-id="b7f22-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b7f22-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f22-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7f22-106">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
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
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a><span data-ttu-id="b7f22-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b7f22-107">Members</span></span>

<span data-ttu-id="b7f22-108">A classe **TargetForwardingHistory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b7f22-108">The **TargetForwardingHistory** class has these types of members:</span></span>

-   [<span data-ttu-id="b7f22-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b7f22-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7f22-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b7f22-110">Properties</span></span>

<span data-ttu-id="b7f22-111">A classe **TargetForwardingHistory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b7f22-111">The **TargetForwardingHistory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7f22-112">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="b7f22-112">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-115">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-115">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-116">As informações do ponto de extremidade do servidor do coletor.</span><span class="sxs-lookup"><span data-stu-id="b7f22-116">The endpoint information of the collector server.</span></span> <span data-ttu-id="b7f22-117">Essa propriedade é formatada como uma cadeia de caracteres de *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="b7f22-117">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-118">**Computador**</span><span class="sxs-lookup"><span data-stu-id="b7f22-118">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-121">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-121">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-122">O nome do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="b7f22-122">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-123">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="b7f22-123">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-124">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7f22-124">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-126">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-126">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-127">O carimbo de data/hora que indica quando a conexão foi estabelecida para os dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="b7f22-127">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-128">**Destino**</span><span class="sxs-lookup"><span data-stu-id="b7f22-128">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-131">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-131">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-132">O destino dos dados de encaminhamento, como um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b7f22-132">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-133">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="b7f22-133">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-136">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-136">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-137">O formato usado para gerar o destino dos dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="b7f22-137">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-138">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="b7f22-138">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-139">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7f22-139">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-141">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-141">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-142">O carimbo de data/hora que indica quando a conexão foi desconectada.</span><span class="sxs-lookup"><span data-stu-id="b7f22-142">The timestamp that indicates when the connection was disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-143">**Erro**</span><span class="sxs-lookup"><span data-stu-id="b7f22-143">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-146">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-146">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-147">Uma mensagem de erro que descreve um erro encontrado.</span><span class="sxs-lookup"><span data-stu-id="b7f22-147">An error message that describes an encountered error.</span></span> <span data-ttu-id="b7f22-148">Essa propriedade estará vazia se nenhum erro for encontrado.</span><span class="sxs-lookup"><span data-stu-id="b7f22-148">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-149">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="b7f22-149">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-152">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-153">O tipo de arquivo que contém os dados de encaminhamento, como ETL.</span><span class="sxs-lookup"><span data-stu-id="b7f22-153">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-154">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="b7f22-154">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-157">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-158">As informações do ponto de extremidade do computador de destino, no formato legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="b7f22-158">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="b7f22-159">Essa propriedade é formatada como uma cadeia de caracteres de *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="b7f22-159">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="b7f22-160">Por exemplo, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="b7f22-160">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-161">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="b7f22-161">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-164">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-165">O SMBIOS **GUID** do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="b7f22-165">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-166">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="b7f22-166">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7f22-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-169">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-169">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-170">O endereço MAC do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="b7f22-170">The MAC address of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="b7f22-171">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="b7f22-171">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f22-172">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7f22-172">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7f22-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f22-174">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f22-174">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f22-175">Carimbo de data/hora de quando essa alteração de estado foi registrada.</span><span class="sxs-lookup"><span data-stu-id="b7f22-175">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7f22-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7f22-176">Requirements</span></span>



| <span data-ttu-id="b7f22-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f22-177">Requirement</span></span> | <span data-ttu-id="b7f22-178">Valor</span><span class="sxs-lookup"><span data-stu-id="b7f22-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f22-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7f22-179">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f22-180">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b7f22-180">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="b7f22-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7f22-181">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f22-182">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b7f22-182">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="b7f22-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7f22-183">Namespace</span></span><br/>                | <span data-ttu-id="b7f22-184">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="b7f22-184">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="b7f22-185">MOF</span><span class="sxs-lookup"><span data-stu-id="b7f22-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7f22-186"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7f22-186"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7f22-187">DLL</span><span class="sxs-lookup"><span data-stu-id="b7f22-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f22-188"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7f22-188"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b7f22-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7f22-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f22-190">Provedor WMI do coletor de eventos de inicialização</span><span class="sxs-lookup"><span data-stu-id="b7f22-190">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

