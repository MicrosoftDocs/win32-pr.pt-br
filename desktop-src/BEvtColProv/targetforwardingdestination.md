---
description: Os destinos conhecidos que contêm os dados coletados. Disponível somente se o coletor estiver em execução com o log de status habilitado.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Classe TargetForwardingDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456893"
---
# <a name="targetforwardingdestination-class"></a><span data-ttu-id="1eb8c-104">Classe TargetForwardingDestination</span><span class="sxs-lookup"><span data-stu-id="1eb8c-104">TargetForwardingDestination class</span></span>

<span data-ttu-id="1eb8c-105">Os destinos conhecidos que contêm os dados coletados.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-105">The known destinations containing the collected data.</span></span> <span data-ttu-id="1eb8c-106">Disponível somente se o coletor estiver em execução com o log de status habilitado.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-106">Available only if the collector is running with the status log enabled.</span></span>

<span data-ttu-id="1eb8c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb8c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1eb8c-108">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
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

## <a name="members"></a><span data-ttu-id="1eb8c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="1eb8c-109">Members</span></span>

<span data-ttu-id="1eb8c-110">A classe **TargetForwardingDestination** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1eb8c-110">The **TargetForwardingDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="1eb8c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1eb8c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1eb8c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1eb8c-112">Properties</span></span>

<span data-ttu-id="1eb8c-113">A classe **TargetForwardingDestination** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-113">The **TargetForwardingDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1eb8c-114">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-114">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-117">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-117">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-118">As informações de host: porta do ponto de extremidade no lado do coletor.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-118">The host:port information of the endpoint on the collector side.</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-119">**Computador**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-122">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-123">Nome do computador de destino, conforme determinado pelo coletor de acordo com sua configuração.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-123">Target computer name, as determined by the collector according to its configuration.</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-125">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-127">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-128">Carimbo de data/hora de quando a conexão foi estabelecida.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-128">Timestamp of when the connection was established.</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-129">**Destino**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-132">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-133">Destino dos dados.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-133">Destination of the data.</span></span> <span data-ttu-id="1eb8c-134">O significado depende do tipo de encaminhador.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-134">The meaning depends on the forwarder type.</span></span> <span data-ttu-id="1eb8c-135">Pode ser um nome de arquivo ou alguma outra identificação.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-135">May be a file name or some other identification.</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-136">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-136">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-139">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-139">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-140">Padrão usado para gerar o destino dos dados.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-140">Pattern used to generate the destination of the data.</span></span> <span data-ttu-id="1eb8c-141">O significado depende do tipo de encaminhador e da configuração.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-141">The meaning depends on the forwarder type and configuration.</span></span> <span data-ttu-id="1eb8c-142">Para um destino fixo, seria o mesmo que o próprio destino.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-142">For a fixed destination, would be the same as the destination itself.</span></span> <span data-ttu-id="1eb8c-143">Para o destino com rotação dos arquivos, conterá os caracteres padrão que serão substituídos pelo índice real no destino.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-143">For the destination with rotation of the files would contain the pattern characters that will be replaced with the actual index in the destination.</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-144">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-144">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-145">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-147">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-147">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-148">Carimbo de data/hora de quando a conexão foi descartada.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-148">Timestamp of when the connection was dropped.</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-149">**Erro**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-149">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-152">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-153">Mensagem de erro se um erro foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-153">Error message if an error was encountered.</span></span> <span data-ttu-id="1eb8c-154">Caso contrário, estará vazio.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-154">Otherwise will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-155">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-155">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-158">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-159">Tipo do encaminhador (como ' ETL ').</span><span class="sxs-lookup"><span data-stu-id="1eb8c-159">Type of the forwarder (such as 'etl').</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-160">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-160">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-163">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-163">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-164">As informações do ponto de extremidade do computador de destino, no formato legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-164">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="1eb8c-165">Essa propriedade é formatada como uma cadeia de caracteres de *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="1eb8c-165">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="1eb8c-166">Por exemplo, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="1eb8c-166">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-167">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-167">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-170">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-170">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-171">O SMBIOS GUID do computador de destino (se conhecido).</span><span class="sxs-lookup"><span data-stu-id="1eb8c-171">The target computer's SMBIOS GUID (if known).</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-172">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-172">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-175">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-175">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-176">O endereço MAC do computador de destino (se conhecido).</span><span class="sxs-lookup"><span data-stu-id="1eb8c-176">The target computer's MAC address (if known).</span></span>

</dd> <dt>

<span data-ttu-id="1eb8c-177">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-177">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb8c-178">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1eb8c-178">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1eb8c-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb8c-180">Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb8c-180">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb8c-181">Carimbo de data/hora de quando essa alteração de estado foi registrada.</span><span class="sxs-lookup"><span data-stu-id="1eb8c-181">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1eb8c-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1eb8c-182">Requirements</span></span>



| <span data-ttu-id="1eb8c-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eb8c-183">Requirement</span></span> | <span data-ttu-id="1eb8c-184">Valor</span><span class="sxs-lookup"><span data-stu-id="1eb8c-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb8c-185">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1eb8c-185">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb8c-186">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1eb8c-186">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="1eb8c-187">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1eb8c-187">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb8c-188">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1eb8c-188">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="1eb8c-189">Namespace</span><span class="sxs-lookup"><span data-stu-id="1eb8c-189">Namespace</span></span><br/>                | <span data-ttu-id="1eb8c-190">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="1eb8c-190">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="1eb8c-191">MOF</span><span class="sxs-lookup"><span data-stu-id="1eb8c-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eb8c-192"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1eb8c-192"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eb8c-193">DLL</span><span class="sxs-lookup"><span data-stu-id="1eb8c-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eb8c-194"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1eb8c-194"><dt>BEvtCol.exe</dt></span></span> </dl>               |



 

