---
description: Essa classe é a classe de tipo de evento para eventos de rede. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: Classe SystemConfig_Network
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967408"
---
# <a name="systemconfig_network-class"></a><span data-ttu-id="9d2d2-104">\_Classe de rede SystemConfig</span><span class="sxs-lookup"><span data-stu-id="9d2d2-104">SystemConfig\_Network class</span></span>

<span data-ttu-id="9d2d2-105">Essa classe é a classe de tipo de evento para eventos de rede.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-105">This class is the event type class for network events.</span></span>

<span data-ttu-id="9d2d2-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d2d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d2d2-107">Syntax</span></span>

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a><span data-ttu-id="9d2d2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9d2d2-108">Members</span></span>

<span data-ttu-id="9d2d2-109">A classe de **\_ rede SystemConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9d2d2-109">The **SystemConfig\_Network** class has these types of members:</span></span>

-   [<span data-ttu-id="9d2d2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d2d2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d2d2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d2d2-111">Properties</span></span>

<span data-ttu-id="9d2d2-112">A classe de **\_ rede SystemConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-112">The **SystemConfig\_Network** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d2d2-113">**MaxHashTableSize**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-113">**MaxHashTableSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d2d2-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d2d2-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d2d2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d2d2-116">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="9d2d2-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9d2d2-117">O tamanho da tabela de hash na qual os blocos de controle TCP (TCBs) são armazenados.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-117">The size of the hash table in which TCP control blocks (TCBs) are stored.</span></span> <span data-ttu-id="9d2d2-118">O TCP armazena blocos de controle em uma tabela de hash para que possa encontrá-los muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-118">TCP stores control blocks in a hash table so it can find them very quickly.</span></span>

</dd> <dt>

<span data-ttu-id="9d2d2-119">**MaxUserPort**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-119">**MaxUserPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d2d2-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d2d2-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d2d2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d2d2-122">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="9d2d2-122">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="9d2d2-123">O número de porta mais alto que TCP pode atribuir quando um aplicativo solicita uma porta de usuário disponível do sistema.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-123">The highest port number TCP can assign when an application requests an available user port from the system.</span></span> <span data-ttu-id="9d2d2-124">Normalmente, as portas efêmeras (usadas brevemente) são alocadas aos números de porta 1024 a 5000.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-124">Typically, ephemeral ports (those used briefly) are allocated to port numbers 1024 through 5000.</span></span>

<span data-ttu-id="9d2d2-125">O valor para o número de porta de usuário mais alto que o TCP pode atribuir é controlado por uma configuração de registro.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-125">The value for the highest user port number TCP can assign is controlled by a registry setting.</span></span> <span data-ttu-id="9d2d2-126">Para obter mais informações, consulte [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="9d2d2-126">For more information, see [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span></span>

</dd> <dt>

<span data-ttu-id="9d2d2-127">**TcbTablePartitions**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-127">**TcbTablePartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d2d2-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d2d2-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d2d2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d2d2-130">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="9d2d2-130">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9d2d2-131">O número de partições na tabela de blocos de controle de transporte.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-131">The number of partitions in the Transport Control Block table.</span></span> <span data-ttu-id="9d2d2-132">O particionamento da tabela de blocos de controle de transporte minimiza a contenção de acesso à tabela.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-132">Partitioning the Transport Control Block table minimizes contention for table access.</span></span> <span data-ttu-id="9d2d2-133">Isso é especialmente útil em sistemas multiprocessadores.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-133">This is especially useful on multiprocessor systems.</span></span>

</dd> <dt>

<span data-ttu-id="9d2d2-134">**TcpTimedWaitDelay**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-134">**TcpTimedWaitDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d2d2-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d2d2-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d2d2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d2d2-137">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="9d2d2-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="9d2d2-138">O tempo que deve decorrer antes que o TCP possa liberar uma conexão fechada e reutilizar seus recursos.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-138">The time that must elapse before TCP can release a closed connection and reuse its resources.</span></span> <span data-ttu-id="9d2d2-139">Esse intervalo entre o fechamento e o lançamento é conhecido como estado de espera de tempo \_ ou estado 2MSL.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-139">This interval between closure and release is known as the TIME\_WAIT state or 2MSL state.</span></span> <span data-ttu-id="9d2d2-140">Durante esse tempo, a conexão pode ser reaberta com muito menos custo para o cliente e o servidor do que estabelecer uma nova conexão.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-140">During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.</span></span>

<span data-ttu-id="9d2d2-141">A RFC 793 publicada pela IETF requer que o TCP mantenha uma conexão fechada para um intervalo pelo menos igual a duas vezes o tempo de vida máximo do segmento (2MSL) da rede.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-141">RFC 793 published by the IETF requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (2MSL) of the network.</span></span> <span data-ttu-id="9d2d2-142">Quando uma conexão é liberada, seu par de soquetes e o TCB (bloco de controle TCP) podem ser usados para dar suporte a outra conexão.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-142">When a connection is released, its socket pair and TCP control block (TCB) can be used to support another connection.</span></span> <span data-ttu-id="9d2d2-143">Por padrão, o MSL é definido como 120 segundos, e o valor dessa entrada é igual a dois MSLs ou 4 minutos.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-143">By default, the MSL is defined to be 120 seconds, and the value of this entry is equal to two MSLs, or 4 minutes.</span></span> <span data-ttu-id="9d2d2-144">Para obter mais informações, consulte [RFC 793](https://tools.ietf.org/html/rfc973).</span><span class="sxs-lookup"><span data-stu-id="9d2d2-144">For more information, see [RFC 793](https://tools.ietf.org/html/rfc973).</span></span>

<span data-ttu-id="9d2d2-145">Reduzir o valor dessa entrada usando uma configuração de registro permite que o TCP libere conexões fechadas mais rápido, fornecendo mais recursos para novas conexões.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-145">Reducing the value of this entry using a registry setting allows TCP to release closed connections faster, providing more resources for new connections.</span></span> <span data-ttu-id="9d2d2-146">No entanto, se o valor for muito baixo, o TCP poderá liberar recursos de conexão antes que a conexão seja concluída, exigindo que o servidor use recursos adicionais para restabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-146">However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to reestablish the connection.</span></span>

<span data-ttu-id="9d2d2-147">Normalmente, o TCP não libera conexões fechadas até que o valor dessa entrada expire.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-147">Normally, TCP does not release closed connections until the value of this entry expires.</span></span> <span data-ttu-id="9d2d2-148">No entanto, o TCP pode liberar conexões antes que esse valor expire se estiver ficando sem blocos de controle TCP (TCBs).</span><span class="sxs-lookup"><span data-stu-id="9d2d2-148">However, TCP can release connections before this value expires if it is running out of TCP control blocks (TCBs).</span></span> <span data-ttu-id="9d2d2-149">O número de TCBs que o sistema cria é controlado por uma configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="9d2d2-149">The number of TCBs the system creates is controlled by a registry setting.</span></span> <span data-ttu-id="9d2d2-150">Para obter mais informações, consulte [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="9d2d2-150">For more information, see [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d2d2-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d2d2-151">Requirements</span></span>



| <span data-ttu-id="9d2d2-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d2d2-152">Requirement</span></span> | <span data-ttu-id="9d2d2-153">Valor</span><span class="sxs-lookup"><span data-stu-id="9d2d2-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d2d2-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d2d2-154">Minimum supported client</span></span><br/> | <span data-ttu-id="9d2d2-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d2d2-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9d2d2-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d2d2-156">Minimum supported server</span></span><br/> | <span data-ttu-id="9d2d2-157">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d2d2-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d2d2-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d2d2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d2d2-159">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="9d2d2-159">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 
