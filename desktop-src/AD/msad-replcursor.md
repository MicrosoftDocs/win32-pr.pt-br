---
title: Classe MSAD_ReplCursor
description: Fornece informações de estado de replicação de entrada sobre todas as réplicas de um determinado contexto de nomenclatura (NC).
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- Classe de MSAD_ReplCursor Active Directory
- Active Directory de MSAD_ReplCursor classe, descrita
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455189"
---
# <a name="msad_replcursor-class"></a><span data-ttu-id="8271b-105">\_Classe MSAD ReplCursor</span><span class="sxs-lookup"><span data-stu-id="8271b-105">MSAD\_ReplCursor class</span></span>

<span data-ttu-id="8271b-106">Fornece informações de estado de replicação de entrada sobre todas as réplicas de um determinado contexto de nomenclatura (NC).</span><span class="sxs-lookup"><span data-stu-id="8271b-106">Provides inbound replication state information about all replicas of a given naming context (NC).</span></span>

## <a name="syntax"></a><span data-ttu-id="8271b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8271b-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a><span data-ttu-id="8271b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8271b-108">Members</span></span>

<span data-ttu-id="8271b-109">A classe **MSAD \_ ReplCursor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8271b-109">The **MSAD\_ReplCursor** class has these types of members:</span></span>

-   [<span data-ttu-id="8271b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8271b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8271b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8271b-111">Properties</span></span>

<span data-ttu-id="8271b-112">A classe **MSAD \_ ReplCursor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8271b-112">The **MSAD\_ReplCursor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8271b-113">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="8271b-113">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8271b-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8271b-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8271b-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8271b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8271b-116">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8271b-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8271b-117">Obtém o caminho X. 500 para o NC (contexto de nomenclatura) que contém este cursor.</span><span class="sxs-lookup"><span data-stu-id="8271b-117">Gets the X.500 path for the naming context (NC) that holds this cursor.</span></span>

</dd> <dt>

<span data-ttu-id="8271b-118">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="8271b-118">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8271b-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8271b-119">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8271b-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8271b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8271b-121">Obtém o caminho X. 500 para o Directory System Agent (DSA) que representa o controlador de domínio de origem (DC).</span><span class="sxs-lookup"><span data-stu-id="8271b-121">Gets the X.500 path for the directory system agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="8271b-122">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="8271b-122">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8271b-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8271b-123">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="8271b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8271b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8271b-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8271b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8271b-126">Obtém o identificador de invocação do servidor de origem ao qual o **USNAttributeFilter** corresponde.</span><span class="sxs-lookup"><span data-stu-id="8271b-126">Gets the invocation identifier of the originating server to which the **USNAttributeFilter** corresponds.</span></span>

</dd> <dt>

<span data-ttu-id="8271b-127">**TimeOfLastSuccessfulSync**</span><span class="sxs-lookup"><span data-stu-id="8271b-127">**TimeOfLastSuccessfulSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8271b-128">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8271b-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8271b-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8271b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8271b-130">Obtém o carimbo de data/hora da última sincronização de replicação com êxito com o DSA de origem.</span><span class="sxs-lookup"><span data-stu-id="8271b-130">Gets the timestamp of the last successful replication sync with the source DSA.</span></span> <span data-ttu-id="8271b-131">Indica a hora em que esse controlador de domínio viu últimas alterações feitas no DSA de origem para este NC.</span><span class="sxs-lookup"><span data-stu-id="8271b-131">Indicates the time when this DC last saw changes made on the source DSA for this NC.</span></span>

</dd> <dt>

<span data-ttu-id="8271b-132">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="8271b-132">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8271b-133">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8271b-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8271b-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8271b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8271b-135">Obtém o número máximo de sequência de atualização para o qual o servidor de destino pode indicar que gravou todas as alterações originadas pelo servidor determinado em números de sequência de atualização menores ou iguais a esse número de sequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="8271b-135">Gets the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number.</span></span> <span data-ttu-id="8271b-136">Essa propriedade é usada para filtrar alterações que o servidor de destino já aplicou nos servidores de origem de replicação.</span><span class="sxs-lookup"><span data-stu-id="8271b-136">This property is used to filter changes that the destination server has already applied at replication source servers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8271b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8271b-137">Requirements</span></span>



| <span data-ttu-id="8271b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8271b-138">Requirement</span></span> | <span data-ttu-id="8271b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="8271b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8271b-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8271b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8271b-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8271b-141">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8271b-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8271b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8271b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8271b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8271b-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="8271b-144">Namespace</span></span><br/>                | <span data-ttu-id="8271b-145">\\MicrosoftActiveDirectory raiz</span><span class="sxs-lookup"><span data-stu-id="8271b-145">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="8271b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="8271b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8271b-147"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8271b-147"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="8271b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8271b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8271b-149"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8271b-149"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8271b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="8271b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8271b-151">**\_cursor repl \_ DS**</span><span class="sxs-lookup"><span data-stu-id="8271b-151">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

