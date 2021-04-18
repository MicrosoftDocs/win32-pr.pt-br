---
title: Estrutura de RAS_PORT_1 (Rassapi. h)
description: A \_ estrutura da porta 1 do RAS \_ contém informações sobre uma porta RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS da estrutura de RAS_PORT_1
- RAS de ponteiro de estrutura de PRAS_PORT_1
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752426"
---
# <a name="ras_port_1-structure"></a><span data-ttu-id="cc67d-105">Estrutura da porta do RAS \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="cc67d-105">RAS\_PORT\_1 structure</span></span>

<span data-ttu-id="cc67d-106">\[Não há suporte para esta versão da estrutura da **porta do RAS \_ \_ 1** no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc67d-106">\[This version of the **RAS\_PORT\_1** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="cc67d-107">Em vez disso, use a [**\_ porta \_ 1 do RAS**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) mais recente definida em mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="cc67d-107">Use the newer [**RAS\_PORT\_1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="cc67d-108">A estrutura da **\_ porta \_ 1 do RAS** contém informações sobre uma porta RAS.</span><span class="sxs-lookup"><span data-stu-id="cc67d-108">The **RAS\_PORT\_1** structure contains information about a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc67d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc67d-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a><span data-ttu-id="cc67d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="cc67d-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc67d-111">**rasport0**</span><span class="sxs-lookup"><span data-stu-id="cc67d-111">**rasport0**</span></span>
</dt> <dd>

<span data-ttu-id="cc67d-112">Especifica uma estrutura de [**\_ porta \_ 0 RAS**](ras-port-0-str.md) que contém informações sobre a porta, como o nome da porta, o nome do usuário remoto conectado à porta e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cc67d-112">Specifies a [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port, such as the name of the port, the name of the remote user connected to the port, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="cc67d-113">**LineCondition**</span><span class="sxs-lookup"><span data-stu-id="cc67d-113">**LineCondition**</span></span>
</dt> <dd>

<span data-ttu-id="cc67d-114">Especifica o estado da porta.</span><span class="sxs-lookup"><span data-stu-id="cc67d-114">Specifies the state of the port.</span></span> <span data-ttu-id="cc67d-115">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc67d-115">This member can be one of the following values.</span></span>



| <span data-ttu-id="cc67d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cc67d-116">Value</span></span>                                                                                                                                                                                            | <span data-ttu-id="cc67d-117">Significado</span><span class="sxs-lookup"><span data-stu-id="cc67d-117">Meaning</span></span>                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <span data-ttu-id="cc67d-118"><dt>**\_porta RAS \_ não \_ operacional**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-118"><dt>**RAS\_PORT\_NON\_OPERATIONAL**</dt></span></span> </dl> | <span data-ttu-id="cc67d-119">A porta não está operacional.</span><span class="sxs-lookup"><span data-stu-id="cc67d-119">The port is not operational.</span></span> <span data-ttu-id="cc67d-120">Verifique se há erros relatados pelo servidor no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="cc67d-120">Check the event log for errors reported by the server.</span></span><br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <span data-ttu-id="cc67d-121"><dt>**\_porta RAS \_ desconectada**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-121"><dt>**RAS\_PORT\_DISCONNECTED**</dt></span></span> </dl>           | <span data-ttu-id="cc67d-122">A porta está desconectada no momento.</span><span class="sxs-lookup"><span data-stu-id="cc67d-122">The port is currently disconnected.</span></span><br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <span data-ttu-id="cc67d-123"><dt>**\_retorno de \_ chamada da porta RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-123"><dt>**RAS\_PORT\_CALLING\_BACK**</dt></span></span> </dl>          | <span data-ttu-id="cc67d-124">O servidor RAS está chamando novamente o cliente RAS.</span><span class="sxs-lookup"><span data-stu-id="cc67d-124">The RAS server is calling back the RAS client.</span></span><br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <span data-ttu-id="cc67d-125"><dt>**\_escuta de porta RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-125"><dt>**RAS\_PORT\_LISTENING**</dt></span></span> </dl>                    | <span data-ttu-id="cc67d-126">A porta está aguardando um cliente chamar.</span><span class="sxs-lookup"><span data-stu-id="cc67d-126">The port is waiting for a client to call in.</span></span><br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <span data-ttu-id="cc67d-127"><dt>**\_autenticação de porta RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-127"><dt>**RAS\_PORT\_AUTHENTICATING**</dt></span></span> </dl>     | <span data-ttu-id="cc67d-128">O servidor está no processo de autenticação do cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="cc67d-128">The server is in the process of authenticating the remote client.</span></span><br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <span data-ttu-id="cc67d-129"><dt>**\_porta RAS \_ autenticada**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-129"><dt>**RAS\_PORT\_AUTHENTICATED**</dt></span></span> </dl>        | <span data-ttu-id="cc67d-130">O cliente remoto agora está autenticado.</span><span class="sxs-lookup"><span data-stu-id="cc67d-130">The remote client is now authenticated.</span></span><br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <span data-ttu-id="cc67d-131"><dt>**\_inicialização de porta RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-131"><dt>**RAS\_PORT\_INITIALIZING**</dt></span></span> </dl>           | <span data-ttu-id="cc67d-132">O dispositivo conectado à porta está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="cc67d-132">The device attached to the port is being initialized.</span></span> <span data-ttu-id="cc67d-133">O estado da porta será alterado para escuta da \_ porta RAS \_ quando a inicialização for concluída.</span><span class="sxs-lookup"><span data-stu-id="cc67d-133">The state of the port will change to RAS\_PORT\_LISTENING when the initialization has been completed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cc67d-134">**HardwareCondition**</span><span class="sxs-lookup"><span data-stu-id="cc67d-134">**HardwareCondition**</span></span>
</dt> <dd>

<span data-ttu-id="cc67d-135">Especifica um dos valores a seguir para indicar o estado do dispositivo conectado à porta.</span><span class="sxs-lookup"><span data-stu-id="cc67d-135">Specifies one of the following values to indicate the state of the device attached to the port.</span></span>



| <span data-ttu-id="cc67d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="cc67d-136">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="cc67d-137">Significado</span><span class="sxs-lookup"><span data-stu-id="cc67d-137">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <span data-ttu-id="cc67d-138"><dt>**\_modem \_ operacional do RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-138"><dt>**RAS\_MODEM\_OPERATIONAL**</dt></span></span> </dl>                 | <span data-ttu-id="cc67d-139">O modem anexado a esta porta está funcionando e está pronto para receber chamadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="cc67d-139">The modem attached to this port is operational and is ready to receive client calls.</span></span><br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <span data-ttu-id="cc67d-140"><dt>**\_falha de \_ hardware do modem RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-140"><dt>**RAS\_MODEM\_HARDWARE\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="cc67d-141">O modem anexado a essa porta tem um problema de hardware.</span><span class="sxs-lookup"><span data-stu-id="cc67d-141">The modem attached to this port has a hardware problem.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="cc67d-142">**LineSpeed**</span><span class="sxs-lookup"><span data-stu-id="cc67d-142">**LineSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="cc67d-143">Especifica a velocidade, em bits por segundo, com a qual o computador pode se comunicar com a porta.</span><span class="sxs-lookup"><span data-stu-id="cc67d-143">Specifies the speed, in bits per second, with which the computer can communicate with the port.</span></span>

</dd> <dt>

<span data-ttu-id="cc67d-144">**NumStatistics**</span><span class="sxs-lookup"><span data-stu-id="cc67d-144">**NumStatistics**</span></span>
</dt> <dd>

<span data-ttu-id="cc67d-145">Este membro não é usado.</span><span class="sxs-lookup"><span data-stu-id="cc67d-145">This member is not used.</span></span> <span data-ttu-id="cc67d-146">As funções de administração de RAS, como a função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) , usam a estrutura de [**Estatísticas de \_ porta \_ de Ras**](ras-port-statistics-str.md) para retornar estatísticas de porta.</span><span class="sxs-lookup"><span data-stu-id="cc67d-146">The RAS administration functions, such as the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function, use the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure to return port statistics.</span></span>

</dd> <dt>

<span data-ttu-id="cc67d-147">**NumMediaParms**</span><span class="sxs-lookup"><span data-stu-id="cc67d-147">**NumMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="cc67d-148">Especifica o número de parâmetros específicos de mídia para esta porta.</span><span class="sxs-lookup"><span data-stu-id="cc67d-148">Specifies the number of media-specific parameters for this port.</span></span> <span data-ttu-id="cc67d-149">Para mídia serial, normalmente é o número de valores que aparecem no arquivo de SERIAL.INI.</span><span class="sxs-lookup"><span data-stu-id="cc67d-149">For serial media this is typically the number of values that appear in the SERIAL.INI file.</span></span>

</dd> <dt>

<span data-ttu-id="cc67d-150">**SizeMediaParms**</span><span class="sxs-lookup"><span data-stu-id="cc67d-150">**SizeMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="cc67d-151">Especifica o tamanho, em bytes, do buffer necessário para todos os parâmetros específicos de mídia.</span><span class="sxs-lookup"><span data-stu-id="cc67d-151">Specifies the size, in bytes, of the buffer required for all media-specific parameters.</span></span> <span data-ttu-id="cc67d-152">A função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) retorna um buffer que contém uma matriz de estruturas de [**\_ parâmetros de Ras**](ras-parameters-str.md) com os parâmetros de mídia e os valores da porta.</span><span class="sxs-lookup"><span data-stu-id="cc67d-152">The [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function returns a buffer that contains an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures with the media parameters and values for the port.</span></span>

</dd> <dt>

<span data-ttu-id="cc67d-153">**ProjResult**</span><span class="sxs-lookup"><span data-stu-id="cc67d-153">**ProjResult**</span></span>
</dt> <dd>

<span data-ttu-id="cc67d-154">Uma estrutura de [**\_ \_ \_ resultados de projeção de Ras PPP**](ras-ppp-projection-result-str.md) que especifica as informações de projeção PPP para esta porta.</span><span class="sxs-lookup"><span data-stu-id="cc67d-154">A [**RAS\_PPP\_PROJECTION\_RESULT**](ras-ppp-projection-result-str.md) structure that specifies the PPP projection information for this port.</span></span> <span data-ttu-id="cc67d-155">Essa estrutura fornece informações para cada protocolo negociado quando um cliente RAS se conecta a um servidor.</span><span class="sxs-lookup"><span data-stu-id="cc67d-155">This structure provides information for each protocol that is negotiated when a RAS client connects to a server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc67d-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc67d-156">Requirements</span></span>



| <span data-ttu-id="cc67d-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc67d-157">Requirement</span></span> | <span data-ttu-id="cc67d-158">Valor</span><span class="sxs-lookup"><span data-stu-id="cc67d-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc67d-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc67d-159">Minimum supported client</span></span><br/> | <span data-ttu-id="cc67d-160">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc67d-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cc67d-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc67d-161">Minimum supported server</span></span><br/> | <span data-ttu-id="cc67d-162">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc67d-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cc67d-163">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cc67d-163">End of client support</span></span><br/>    | <span data-ttu-id="cc67d-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc67d-164">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="cc67d-165">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="cc67d-165">End of server support</span></span><br/>    | <span data-ttu-id="cc67d-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc67d-166">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="cc67d-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc67d-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc67d-168"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc67d-168"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc67d-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc67d-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc67d-170">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="cc67d-170">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="cc67d-171">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="cc67d-171">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="cc67d-172">**parâmetros de RAS \_**</span><span class="sxs-lookup"><span data-stu-id="cc67d-172">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="cc67d-173">**\_Porta RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="cc67d-173">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="cc67d-174">**\_Estatísticas de porta RAS \_**</span><span class="sxs-lookup"><span data-stu-id="cc67d-174">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="cc67d-175">**\_resultado da \_ projeção do RAS PPP \_**</span><span class="sxs-lookup"><span data-stu-id="cc67d-175">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="cc67d-176">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="cc67d-176">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="cc67d-177">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="cc67d-177">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="cc67d-178">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="cc67d-178">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





