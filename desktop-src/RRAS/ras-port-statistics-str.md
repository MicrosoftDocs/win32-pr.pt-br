---
title: Estrutura de RAS_PORT_STATISTICS (Rassapi. h)
description: A estrutura de estatísticas de porta de RAS \_ \_ relata as estatísticas que um servidor RAS coleta para uma porta conectada.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS da estrutura de RAS_PORT_STATISTICS
- RAS de ponteiro de estrutura de PRAS_PORT_STATISTICS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759603"
---
# <a name="ras_port_statistics-structure"></a><span data-ttu-id="277ae-105">Estrutura de estatísticas de \_ porta de Ras \_</span><span class="sxs-lookup"><span data-stu-id="277ae-105">RAS\_PORT\_STATISTICS structure</span></span>

<span data-ttu-id="277ae-106">\[A estrutura de **\_ \_ Estatísticas de porta de Ras** não tem suporte no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="277ae-106">\[The **RAS\_PORT\_STATISTICS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="277ae-107">A estrutura de **\_ \_ Estatísticas de porta de Ras** relata as estatísticas que um servidor RAS coleta para uma porta conectada.</span><span class="sxs-lookup"><span data-stu-id="277ae-107">The **RAS\_PORT\_STATISTICS** structure reports the statistics that a RAS server collects for a connected port.</span></span> <span data-ttu-id="277ae-108">O servidor RAS redefine os vários contadores de estatística cada vez que a porta é conectada.</span><span class="sxs-lookup"><span data-stu-id="277ae-108">The RAS server resets the various statistic counters each time the port is connected.</span></span> <span data-ttu-id="277ae-109">Chame a função [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para forçar o servidor RAS a redefinir os contadores de estatística.</span><span class="sxs-lookup"><span data-stu-id="277ae-109">Call the [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) function to force the RAS server to reset the statistic counters.</span></span>

<span data-ttu-id="277ae-110">Para uma porta que faz parte de uma conexão Multilink, essa estrutura fornece dois conjuntos de estatísticas.</span><span class="sxs-lookup"><span data-stu-id="277ae-110">For a port that is part of a multilink connection, this structure provides two sets of statistics.</span></span> <span data-ttu-id="277ae-111">O primeiro conjunto contém as estatísticas cumulativas para todas as portas na conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-111">The first set contains the cumulative statistics for all ports in the connection.</span></span> <span data-ttu-id="277ae-112">Essas estatísticas são as mesmas para todas as portas na conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-112">These statistics are the same for all ports in the connection.</span></span> <span data-ttu-id="277ae-113">O segundo conjunto contém as estatísticas apenas para essa porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-113">The second set contains the statistics for just this port.</span></span> <span data-ttu-id="277ae-114">Se a porta não fizer parte de uma conexão Multilink, os dois conjuntos de estatísticas terão as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="277ae-114">If the port is not part of a multilink connection, both sets of statistics have the same information.</span></span> <span data-ttu-id="277ae-115">Para determinar se uma porta faz parte de uma conexão de vínculos múltiplos, verifique a porta de \_ bits com múltiplas conexões no membro **flags** da estrutura [**da \_ porta \_ 0 do RAS**](ras-port-0-str.md) da porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-115">To determine whether a port is part of a multilink connection, check the PORT\_MULTILINKED bit in the **Flags** member of the port's [**RAS\_PORT\_0**](ras-port-0-str.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="277ae-116">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="277ae-116">Syntax</span></span>


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a><span data-ttu-id="277ae-117">Membros</span><span class="sxs-lookup"><span data-stu-id="277ae-117">Members</span></span>

<dl> <dt>

<span data-ttu-id="277ae-118">**dwBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="277ae-118">**dwBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-119">Especifica o número total de bytes transmitidos pela conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-119">Specifies the total number of bytes transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-120">**dwBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="277ae-120">**dwBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-121">Especifica o número total de bytes recebidos pela conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-121">Specifies the total number of bytes received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-122">**dwFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="277ae-122">**dwFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-123">Especifica o número total de quadros transmitidos pela conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-123">Specifies the total number of frames transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-124">**dwFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="277ae-124">**dwFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-125">Especifica o número total de quadros recebidos pela conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-125">Specifies the total number of frames received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-126">**dwCrcErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-126">**dwCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-127">Especifica o número total de erros de CRC na conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-127">Specifies the total number of CRC errors on the connection.</span></span> <span data-ttu-id="277ae-128">Os erros de CRC são causados pela falha de uma verificação de redundância cíclica.</span><span class="sxs-lookup"><span data-stu-id="277ae-128">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="277ae-129">Um erro de CRC indica que um ou mais caracteres no pacote de dados recebidos foram encontrados ilegíveis na chegada.</span><span class="sxs-lookup"><span data-stu-id="277ae-129">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-130">**dwTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-130">**dwTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-131">Especifica o número total de erros de tempo limite na conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-131">Specifies the total number of time-out errors on the connection.</span></span> <span data-ttu-id="277ae-132">Os erros de tempo limite ocorrem quando um caractere esperado não é recebido no tempo.</span><span class="sxs-lookup"><span data-stu-id="277ae-132">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="277ae-133">Quando isso ocorre, o software pressupõe que os dados foram perdidos e solicita que eles sejam reenviados.</span><span class="sxs-lookup"><span data-stu-id="277ae-133">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-134">**dwAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-134">**dwAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-135">Especifica o número total de erros de alinhamento na conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-135">Specifies the total number of alignment errors on the connection.</span></span> <span data-ttu-id="277ae-136">Os erros de alinhamento ocorrem quando um caractere recebido não é o esperado.</span><span class="sxs-lookup"><span data-stu-id="277ae-136">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="277ae-137">Isso geralmente acontece quando um caractere é perdido ou quando ocorre um erro de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="277ae-137">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-138">**dwHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-138">**dwHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-139">Especifica o número total de erros de saturação de hardware na conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-139">Specifies the total number of hardware overrun errors on the connection.</span></span> <span data-ttu-id="277ae-140">Esses erros indicam o número de vezes que o computador de envio transmitiu caracteres mais rápido do que o hardware do computador de recebimento pode processá-los.</span><span class="sxs-lookup"><span data-stu-id="277ae-140">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="277ae-141">Se esse problema persistir, reduza a taxa de conexão de BPS no cliente.</span><span class="sxs-lookup"><span data-stu-id="277ae-141">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-142">**dwFramingErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-142">**dwFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-143">Especifica o número total de erros de enquadramento na conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-143">Specifies the total number of framing errors on the connection.</span></span> <span data-ttu-id="277ae-144">Um erro de enquadramento ocorre quando um caractere assíncrono é recebido com um bit de início ou de parada inválido.</span><span class="sxs-lookup"><span data-stu-id="277ae-144">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-145">**dwBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-145">**dwBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-146">Especifica o número total de erros de saturação de buffer na conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-146">Specifies the total number of buffer overrun errors on the connection.</span></span> <span data-ttu-id="277ae-147">Um erro de saturação de buffer ocorre quando o computador de envio está transmitindo caracteres mais rápido do que o computador receptor pode acomodá-los.</span><span class="sxs-lookup"><span data-stu-id="277ae-147">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="277ae-148">Se esse problema persistir, reduza a taxa de conexão de BPS no cliente.</span><span class="sxs-lookup"><span data-stu-id="277ae-148">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-149">**dwBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="277ae-149">**dwBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-150">Especifica o número total de bytes transmitidos não compactados pela conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-150">Specifies the total number of bytes transmitted uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-151">**dwBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="277ae-151">**dwBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-152">Especifica o número total de bytes recebidos descompactados pela conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-152">Specifies the total number of bytes received uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-153">**dwBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="277ae-153">**dwBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-154">Especifica o número total de bytes transmitidos compactados pela conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-154">Specifies the total number of bytes transmitted compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-155">**dwBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="277ae-155">**dwBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-156">Especifica o número total de bytes recebidos compactados pela conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-156">Specifies the total number of bytes received compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-157">**dwPortBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="277ae-157">**dwPortBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-158">Especifica o número total de bytes transmitidos pela porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-158">Specifies the total number of bytes transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-159">**dwPortBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="277ae-159">**dwPortBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-160">Especifica o número total de bytes recebidos pela porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-160">Specifies the total number of bytes received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-161">**dwPortFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="277ae-161">**dwPortFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-162">Especifica o número total de quadros transmitidos pela porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-162">Specifies the total number of frames transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-163">**dwPortFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="277ae-163">**dwPortFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-164">Especifica o número total de quadros recebidos pela porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-164">Specifies the total number of frames received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-165">**dwPortCrcErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-165">**dwPortCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-166">Especifica o número total de erros de CRC na porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-166">Specifies the total number of CRC errors on the port.</span></span> <span data-ttu-id="277ae-167">Os erros de CRC são causados pela falha de uma verificação de redundância cíclica.</span><span class="sxs-lookup"><span data-stu-id="277ae-167">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="277ae-168">Um erro de CRC indica que um ou mais caracteres no pacote de dados recebidos foram encontrados ilegíveis na chegada.</span><span class="sxs-lookup"><span data-stu-id="277ae-168">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-169">**dwPortTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-169">**dwPortTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-170">Especifica o número total de erros de tempo limite na porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-170">Specifies the total number of time-out errors on the port.</span></span> <span data-ttu-id="277ae-171">Os erros de tempo limite ocorrem quando um caractere esperado não é recebido no tempo.</span><span class="sxs-lookup"><span data-stu-id="277ae-171">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="277ae-172">Quando isso ocorre, o software pressupõe que os dados foram perdidos e solicita que eles sejam reenviados.</span><span class="sxs-lookup"><span data-stu-id="277ae-172">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-173">**dwPortAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-173">**dwPortAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-174">Especifica o número total de erros de alinhamento na porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-174">Specifies the total number of alignment errors on the port.</span></span> <span data-ttu-id="277ae-175">Os erros de alinhamento ocorrem quando um caractere recebido não é o esperado.</span><span class="sxs-lookup"><span data-stu-id="277ae-175">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="277ae-176">Isso geralmente acontece quando um caractere é perdido ou quando ocorre um erro de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="277ae-176">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-177">**dwPortHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-177">**dwPortHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-178">Especifica o número total de erros de saturação de hardware na porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-178">Specifies the total number of hardware overrun errors on the port.</span></span> <span data-ttu-id="277ae-179">Esses erros indicam o número de vezes que o computador de envio transmitiu caracteres mais rápido do que o hardware do computador de recebimento pode processá-los.</span><span class="sxs-lookup"><span data-stu-id="277ae-179">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="277ae-180">Se esse problema persistir, reduza a taxa de conexão de BPS no cliente.</span><span class="sxs-lookup"><span data-stu-id="277ae-180">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-181">**dwPortFramingErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-181">**dwPortFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-182">Especifica o número total de erros de enquadramento na porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-182">Specifies the total number of framing errors on the port.</span></span> <span data-ttu-id="277ae-183">Um erro de enquadramento ocorre quando um caractere assíncrono é recebido com um bit de início ou de parada inválido.</span><span class="sxs-lookup"><span data-stu-id="277ae-183">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-184">**dwPortBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="277ae-184">**dwPortBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-185">Especifica o número total de erros de saturação de buffer na porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-185">Specifies the total number of buffer overrun errors on the port.</span></span> <span data-ttu-id="277ae-186">Um erro de saturação de buffer ocorre quando o computador de envio está transmitindo caracteres mais rápido do que o computador receptor pode acomodá-los.</span><span class="sxs-lookup"><span data-stu-id="277ae-186">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="277ae-187">Se esse problema persistir, reduza a taxa de conexão de BPS no cliente.</span><span class="sxs-lookup"><span data-stu-id="277ae-187">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-188">**dwPortBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="277ae-188">**dwPortBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-189">Especifica o número total de bytes transmitidos não compactados pela porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-189">Specifies the total number of bytes transmitted uncompressed by the port.</span></span> <span data-ttu-id="277ae-190">Se a porta fizer parte de uma conexão Multilink, esse membro não será válido.</span><span class="sxs-lookup"><span data-stu-id="277ae-190">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="277ae-191">Em vez disso, use as estatísticas de compactação para a conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-191">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-192">**dwPortBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="277ae-192">**dwPortBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-193">Especifica o número total de bytes recebidos descompactados pela porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-193">Specifies the total number of bytes received uncompressed by the port.</span></span> <span data-ttu-id="277ae-194">Se a porta fizer parte de uma conexão Multilink, esse membro não será válido.</span><span class="sxs-lookup"><span data-stu-id="277ae-194">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="277ae-195">Em vez disso, use as estatísticas de compactação para a conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-195">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-196">**dwPortBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="277ae-196">**dwPortBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-197">Especifica o número total de bytes transmitidos compactados pela porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-197">Specifies the total number of bytes transmitted compressed by the port.</span></span> <span data-ttu-id="277ae-198">Se a porta fizer parte de uma conexão Multilink, esse membro não será válido.</span><span class="sxs-lookup"><span data-stu-id="277ae-198">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="277ae-199">Em vez disso, use as estatísticas de compactação para a conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-199">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="277ae-200">**dwPortBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="277ae-200">**dwPortBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="277ae-201">Especifica o número total de bytes recebidos compactados pela porta.</span><span class="sxs-lookup"><span data-stu-id="277ae-201">Specifies the total number of bytes received compressed by the port.</span></span> <span data-ttu-id="277ae-202">Se a porta fizer parte de uma conexão Multilink, esse membro não será válido.</span><span class="sxs-lookup"><span data-stu-id="277ae-202">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="277ae-203">Em vez disso, use as estatísticas de compactação para a conexão.</span><span class="sxs-lookup"><span data-stu-id="277ae-203">Use the compression statistics for the connection instead.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="277ae-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="277ae-204">Requirements</span></span>



| <span data-ttu-id="277ae-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="277ae-205">Requirement</span></span> | <span data-ttu-id="277ae-206">Valor</span><span class="sxs-lookup"><span data-stu-id="277ae-206">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="277ae-207">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="277ae-207">Minimum supported client</span></span><br/> | <span data-ttu-id="277ae-208">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="277ae-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="277ae-209">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="277ae-209">Minimum supported server</span></span><br/> | <span data-ttu-id="277ae-210">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="277ae-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="277ae-211">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="277ae-211">End of client support</span></span><br/>    | <span data-ttu-id="277ae-212">Windows XP</span><span class="sxs-lookup"><span data-stu-id="277ae-212">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="277ae-213">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="277ae-213">End of server support</span></span><br/>    | <span data-ttu-id="277ae-214">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="277ae-214">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="277ae-215">parâmetro</span><span class="sxs-lookup"><span data-stu-id="277ae-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="277ae-216"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="277ae-216"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277ae-217">Confira também</span><span class="sxs-lookup"><span data-stu-id="277ae-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277ae-218">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="277ae-218">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="277ae-219">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="277ae-219">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="277ae-220">**\_Porta RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="277ae-220">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="277ae-221">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="277ae-221">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="277ae-222">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="277ae-222">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="277ae-223">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="277ae-223">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)
</dt> <dt>

[<span data-ttu-id="277ae-224">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="277ae-224">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





