---
title: Estrutura de RAS_PORT_0 (Rassapi. h)
description: A \_ estrutura da porta 0 do RAS \_ contém informações que descrevem uma porta RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS da estrutura de RAS_PORT_0
- RAS de ponteiro de estrutura de PRAS_PORT_0
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499409"
---
# <a name="ras_port_0-structure"></a><span data-ttu-id="a4a54-105">Estrutura da porta do RAS \_ \_ 0</span><span class="sxs-lookup"><span data-stu-id="a4a54-105">RAS\_PORT\_0 structure</span></span>

<span data-ttu-id="a4a54-106">\[Não há suporte para esta versão da estrutura de **\_ porta \_ 0 do RAS** a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a4a54-106">\[This version of the **RAS\_PORT\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="a4a54-107">Em vez disso, use a [**porta do RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) mais recente definida em mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="a4a54-107">Use the newer [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="a4a54-108">A estrutura da **\_ porta \_ 0 do RAS** contém informações que descrevem uma porta RAS.</span><span class="sxs-lookup"><span data-stu-id="a4a54-108">The **RAS\_PORT\_0** structure contains information that describes a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a54-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4a54-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a><span data-ttu-id="a4a54-110">Membros</span><span class="sxs-lookup"><span data-stu-id="a4a54-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="a4a54-111">**wszPortName**</span><span class="sxs-lookup"><span data-stu-id="a4a54-111">**wszPortName**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-112">Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta, como "COM1".</span><span class="sxs-lookup"><span data-stu-id="a4a54-112">A null-terminated Unicode string that specifies the name of the port, such as "COM1".</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-113">**wszDeviceType**</span><span class="sxs-lookup"><span data-stu-id="a4a54-113">**wszDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-114">Uma cadeia de caracteres Unicode terminada em nulo que especifica o tipo do dispositivo no qual a conexão foi feita, como modem ou ISDN.</span><span class="sxs-lookup"><span data-stu-id="a4a54-114">A null-terminated Unicode string that specifies the type of the device on which the connection was made, such as Modem or ISDN.</span></span> <span data-ttu-id="a4a54-115">A lista de tipos de dispositivos que podem ser especificados nesse membro inclui todos os tipos de dispositivos instalados no servidor, incluindo dispositivos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a4a54-115">The list of device types that might be specified in this member includes all the device types installed on the server, including third-party devices.</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-116">**wszDeviceName**</span><span class="sxs-lookup"><span data-stu-id="a4a54-116">**wszDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-117">Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do dispositivo no qual a conexão foi feita, como "Hayes 9600" ou "PCIMACISDN1".</span><span class="sxs-lookup"><span data-stu-id="a4a54-117">A null-terminated Unicode string that specifies the name of the device on which the connection was made, such as "Hayes 9600" or "PCIMACISDN1".</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-118">**wszMediaName**</span><span class="sxs-lookup"><span data-stu-id="a4a54-118">**wszMediaName**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-119">Especifica uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da mídia usada para a conexão, como *rasser* ou *RASTAPI*.</span><span class="sxs-lookup"><span data-stu-id="a4a54-119">Specifies a null-terminated Unicode string that specifies the name of the media used for the connection, such as *rasser* or *rastapi*.</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-120">**reservado**</span><span class="sxs-lookup"><span data-stu-id="a4a54-120">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a4a54-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-122">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="a4a54-122">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-123">Especifica um conjunto de sinalizadores de bits que especificam a natureza da conexão feita nessa porta.</span><span class="sxs-lookup"><span data-stu-id="a4a54-123">Specifies a set of bit flags that specify the nature of the connection made on this port.</span></span> <span data-ttu-id="a4a54-124">Esse membro pode ser uma combinação dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4a54-124">This member can be a combination of the following flags.</span></span>



| <span data-ttu-id="a4a54-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a4a54-125">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="a4a54-126">Significado</span><span class="sxs-lookup"><span data-stu-id="a4a54-126">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <span data-ttu-id="a4a54-127"><dt>**GATEWAY \_ ativo**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a54-127"><dt>**GATEWAY\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="a4a54-128">Se esse sinalizador for definido, o gateway NetBIOS estará ativo no servidor.</span><span class="sxs-lookup"><span data-stu-id="a4a54-128">If this flag is set, the NetBIOS gateway is active on the server.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <span data-ttu-id="a4a54-129"><dt>**MESSENGER \_ presente**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a54-129"><dt>**MESSENGER\_PRESENT**</dt></span></span> </dl>    | <span data-ttu-id="a4a54-130">Se esse sinalizador for definido, o serviço de mensageiro será executado no cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="a4a54-130">If this flag is set, the messenger service is running on the remote client.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <span data-ttu-id="a4a54-131"><dt>**PORTA \_ MULTIlink**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a54-131"><dt>**PORT\_MULTILINKED**</dt></span></span> </dl>       | <span data-ttu-id="a4a54-132">Se esse sinalizador for definido, a porta será vinculada com outras portas.</span><span class="sxs-lookup"><span data-stu-id="a4a54-132">If this flag is set, the port is multilinked with other ports.</span></span> <span data-ttu-id="a4a54-133">Use essas informações para exibir o status da conexão como uma porta com conexões múltiplas.</span><span class="sxs-lookup"><span data-stu-id="a4a54-133">Use this information to display the connection status as a multilinked port.</span></span> <br/> <span data-ttu-id="a4a54-134">Para uma porta com múltiplas conexões, a estrutura de [**\_ \_ Estatísticas de porta de Ras**](ras-port-statistics-str.md) contém dois conjuntos de estatísticas: um para a porta sozinha e outro para as portas combinadas na conexão de vínculos múltiplos.</span><span class="sxs-lookup"><span data-stu-id="a4a54-134">For a multilinked port, the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure contains two sets of statistics: one for the port alone, and another for the combined ports in the multilink connection.</span></span><br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <span data-ttu-id="a4a54-135"><dt>**\_cliente PPP**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a54-135"><dt>**PPP\_CLIENT**</dt></span></span> </dl>                         | <span data-ttu-id="a4a54-136">Se esse sinalizador estiver definido, o cliente remoto conectado usando o PPP.</span><span class="sxs-lookup"><span data-stu-id="a4a54-136">If this flag is set, the remote client connected using PPP.</span></span> <span data-ttu-id="a4a54-137">Se esse sinalizador não for definido, o cliente remoto será conectado usando o protocolo AMB.</span><span class="sxs-lookup"><span data-stu-id="a4a54-137">If this flag is not set, the remote client connected using the AMB protocol.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <span data-ttu-id="a4a54-138"><dt>**\_escuta remota**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a54-138"><dt>**REMOTE\_LISTEN**</dt></span></span> </dl>                | <span data-ttu-id="a4a54-139">Se esse sinalizador for definido, o parâmetro RemoteListen do gateway NetBIOS será definido como 1 no servidor.</span><span class="sxs-lookup"><span data-stu-id="a4a54-139">If this flag is set, the RemoteListen parameter of the NetBIOS gateway is set to 1 on the server.</span></span><br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <span data-ttu-id="a4a54-140"><dt>**USUÁRIO \_ autenticado**</dt></span><span class="sxs-lookup"><span data-stu-id="a4a54-140"><dt>**USER\_AUTHENTICATED**</dt></span></span> </dl> | <span data-ttu-id="a4a54-141">Se esse sinalizador for definido, um cliente remoto será conectado ao servidor e o usuário foi autenticado.</span><span class="sxs-lookup"><span data-stu-id="a4a54-141">If this flag is set, a remote client is connected to the server and the user has been authenticated.</span></span> <span data-ttu-id="a4a54-142">Marque esse sinalizador para garantir que um cliente esteja realmente conectado a uma porta.</span><span class="sxs-lookup"><span data-stu-id="a4a54-142">Check this flag to ensure that a client is actually connected to a port.</span></span><br/>                                                                                                                                                                                                   |



 

<span data-ttu-id="a4a54-143">Se o MESSENGER \_ presente, o gateway \_ ativo e os \_ sinalizadores de escuta remota estiverem definidos, use o serviço mensageiro para enviar uma mensagem administrativa ao cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="a4a54-143">If the MESSENGER\_PRESENT, GATEWAY\_ACTIVE, and REMOTE\_LISTEN flags are set, use the messenger service to send an administrative message to the remote client.</span></span> <span data-ttu-id="a4a54-144">Se \_ o Messenger presente e a \_ escuta remota estiverem definidos, mas o gateway \_ ativo não estiver, envie mensagens para o cliente somente do servidor RAS ao qual o cliente está conectado.</span><span class="sxs-lookup"><span data-stu-id="a4a54-144">If MESSENGER\_PRESENT and REMOTE\_LISTEN are set, but GATEWAY\_ACTIVE is not, send messages to the client only from the RAS server to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-145">**wszUserName**</span><span class="sxs-lookup"><span data-stu-id="a4a54-145">**wszUserName**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-146">Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do usuário remoto conectado a esta porta.</span><span class="sxs-lookup"><span data-stu-id="a4a54-146">A null-terminated Unicode string that specifies the name of the remote user connected to this port.</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-147">**wszComputer**</span><span class="sxs-lookup"><span data-stu-id="a4a54-147">**wszComputer**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-148">Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do computador cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="a4a54-148">A null-terminated Unicode string that specifies the name of the remote client computer.</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-149">**dwStartSessionTime**</span><span class="sxs-lookup"><span data-stu-id="a4a54-149">**dwStartSessionTime**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-150">Especifica o tempo, em segundos, de 1º de janeiro de 1970, que o cliente conectou ao servidor RAS nesta porta.</span><span class="sxs-lookup"><span data-stu-id="a4a54-150">Specifies the time, in seconds from January 1, 1970, that the client connected to the RAS server on this port.</span></span> <span data-ttu-id="a4a54-151">Use as funções de hora padrão para formatar esse valor para exibição.</span><span class="sxs-lookup"><span data-stu-id="a4a54-151">Use the standard time functions to format this value for display.</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-152">**wszLogonDomain**</span><span class="sxs-lookup"><span data-stu-id="a4a54-152">**wszLogonDomain**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-153">Especifica uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do domínio no qual o usuário remoto foi autenticado.</span><span class="sxs-lookup"><span data-stu-id="a4a54-153">Specifies a null-terminated Unicode string that specifies the name of the domain on which the remote user was authenticated.</span></span> <span data-ttu-id="a4a54-154">Essa cadeia de caracteres é apenas o nome de domínio, sem o \\ \\ prefixo "".</span><span class="sxs-lookup"><span data-stu-id="a4a54-154">This string is the domain name only, with no "\\\\" prefix.</span></span>

</dd> <dt>

<span data-ttu-id="a4a54-155">**fAdvancedServer**</span><span class="sxs-lookup"><span data-stu-id="a4a54-155">**fAdvancedServer**</span></span>
</dt> <dd>

<span data-ttu-id="a4a54-156">Especifica um sinalizador que será diferente de zero se o servidor RAS associado a essa porta for um servidor avançado, como o Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="a4a54-156">Specifies a flag that is nonzero if the RAS server associated with this port is an advanced server such as Windows 2000 Advanced Server.</span></span> <span data-ttu-id="a4a54-157">Use essas informações para determinar o nome do servidor que tem o banco de dados da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="a4a54-157">Use this information to determine the name of the server that has the user account database.</span></span> <span data-ttu-id="a4a54-158">Se o servidor RAS for um servidor avançado, obtenha o nome do servidor de conta de usuário concatenando o prefixo " \\ \\ " para o nome retornado no membro **wszLogonDomain** .</span><span class="sxs-lookup"><span data-stu-id="a4a54-158">If the RAS server is an advanced server, get the name of the user account server by concatenating the prefix "\\\\" to the name returned in the **wszLogonDomain** member.</span></span> <span data-ttu-id="a4a54-159">Isso ocorre porque, para um servidor avançado, o nome de domínio de logon local é o mesmo que o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a4a54-159">This is because for an advanced server the local logon domain name is the same as the server name.</span></span> <span data-ttu-id="a4a54-160">Se o servidor RAS for uma estação de trabalho, use a função [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obter o nome do servidor de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="a4a54-160">If the RAS server is a workstation, use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get the name of the user account server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4a54-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4a54-161">Requirements</span></span>



| <span data-ttu-id="a4a54-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a54-162">Requirement</span></span> | <span data-ttu-id="a4a54-163">Valor</span><span class="sxs-lookup"><span data-stu-id="a4a54-163">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a54-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4a54-164">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a54-165">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4a54-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a4a54-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4a54-166">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a54-167">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4a54-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a4a54-168">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a4a54-168">End of client support</span></span><br/>    | <span data-ttu-id="a4a54-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4a54-169">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="a4a54-170">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a4a54-170">End of server support</span></span><br/>    | <span data-ttu-id="a4a54-171">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a4a54-171">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="a4a54-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4a54-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4a54-173"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4a54-173"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4a54-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4a54-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a54-175">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="a4a54-175">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a4a54-176">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="a4a54-176">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="a4a54-177">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a4a54-177">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="a4a54-178">**\_Estatísticas de porta RAS \_**</span><span class="sxs-lookup"><span data-stu-id="a4a54-178">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="a4a54-179">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="a4a54-179">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="a4a54-180">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="a4a54-180">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> </dl>

 

 





