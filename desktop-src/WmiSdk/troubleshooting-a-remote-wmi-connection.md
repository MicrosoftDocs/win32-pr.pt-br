---
description: As seções a seguir descrevem os problemas comuns que os desenvolvedores podem ter com a criação de uma conexão WMI remota.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Solucionando problemas de conexão WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761209"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a><span data-ttu-id="355d7-103">Solucionando problemas de conexão WMI remota</span><span class="sxs-lookup"><span data-stu-id="355d7-103">Troubleshooting a Remote WMI Connection</span></span>

<span data-ttu-id="355d7-104">As seções a seguir descrevem os problemas comuns que os desenvolvedores podem ter com a criação de uma conexão WMI remota.</span><span class="sxs-lookup"><span data-stu-id="355d7-104">The following sections describe common issues developers may have with creating a remote WMI connection.</span></span>

<span data-ttu-id="355d7-105">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="355d7-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="355d7-106">Acesso ao DCOM negado</span><span class="sxs-lookup"><span data-stu-id="355d7-106">DCOM Access Denied</span></span>](#dcom-access-denied)
-   [<span data-ttu-id="355d7-107">Falha ao conectar</span><span class="sxs-lookup"><span data-stu-id="355d7-107">Failure to Connect</span></span>](#failure-to-connect)
-   [<span data-ttu-id="355d7-108">A conexão WMI atingiu o tempo limite</span><span class="sxs-lookup"><span data-stu-id="355d7-108">WMI Connection Timed Out</span></span>](#wmi-connection-timed-out)
-   [<span data-ttu-id="355d7-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="355d7-109">Related topics</span></span>](#related-topics)

## <a name="dcom-access-denied"></a><span data-ttu-id="355d7-110">Acesso ao DCOM negado</span><span class="sxs-lookup"><span data-stu-id="355d7-110">DCOM Access Denied</span></span>

<dl> <dt>

<span data-ttu-id="355d7-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomas</span><span class="sxs-lookup"><span data-stu-id="355d7-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="355d7-112">a conexão falhou com o erro "DCOM Access Denied", juntamente com o valor decimal-2147024891 ou hex value0x80070005.</span><span class="sxs-lookup"><span data-stu-id="355d7-112">your connection failed with the error "DCOM Access Denied", along with the decimal value -2147024891 or hex value0x80070005.</span></span>

</dd> <dt>

<span data-ttu-id="355d7-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Lo</span><span class="sxs-lookup"><span data-stu-id="355d7-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="355d7-114">O DCOM pode não estar configurado para permitir uma conexão WMI.</span><span class="sxs-lookup"><span data-stu-id="355d7-114">DCOM may not be configured to allow a WMI connection.</span></span>

</dd> <dt>

<span data-ttu-id="355d7-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolução</span><span class="sxs-lookup"><span data-stu-id="355d7-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="355d7-116">Você pode definir as configurações do DCOM para o WMI usando o utilitário de configuração do DCOM (**DCOMCnfg.exe**) encontrado em **Ferramentas administrativas** no **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="355d7-116">You can configure DCOM settings for WMI using the DCOM Config utility (**DCOMCnfg.exe**) found in **Administrative Tools** in **Control Panel**.</span></span> <span data-ttu-id="355d7-117">Esse utilitário expõe as configurações que permitem que determinados usuários se conectem ao computador remotamente por meio do DCOM.</span><span class="sxs-lookup"><span data-stu-id="355d7-117">This utility exposes the settings that enable certain users to connect to the computer remotely through DCOM.</span></span> <span data-ttu-id="355d7-118">Os membros do grupo Administradores têm permissão para se conectar remotamente ao computador por padrão.</span><span class="sxs-lookup"><span data-stu-id="355d7-118">Members of the Administrators group are allowed to remotely connect to the computer by default.</span></span> <span data-ttu-id="355d7-119">Com esse utilitário, você pode definir a segurança para iniciar, acessar e configurar o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="355d7-119">With this utility you can set the security to start, access, and configure the WMI service.</span></span>

<span data-ttu-id="355d7-120">Para obter mais informações, consulte [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="355d7-120">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

</dd> </dl>

## <a name="failure-to-connect"></a><span data-ttu-id="355d7-121">Falha ao conectar</span><span class="sxs-lookup"><span data-stu-id="355d7-121">Failure to Connect</span></span>

<dl> <dt>

<span data-ttu-id="355d7-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomas</span><span class="sxs-lookup"><span data-stu-id="355d7-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="355d7-123">Você não pode se conectar ao WMI em um sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="355d7-123">You cannot connect to WMI on a remote system.</span></span>

</dd> <dt>

<span data-ttu-id="355d7-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Lo</span><span class="sxs-lookup"><span data-stu-id="355d7-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="355d7-125">Você pode estar tentando se conectar a um sistema que não dá suporte a WMI.</span><span class="sxs-lookup"><span data-stu-id="355d7-125">You may be trying to connect to a system that does not support WMI.</span></span> <span data-ttu-id="355d7-126">Não há suporte para as seguintes conexões entre as versões do sistema operacional:</span><span class="sxs-lookup"><span data-stu-id="355d7-126">The following connections between operating system versions are not supported:</span></span>

-   <span data-ttu-id="355d7-127">Não é possível se conectar a um computador que esteja executando uma edição inicial, básica ou Home.</span><span class="sxs-lookup"><span data-stu-id="355d7-127">You cannot connect to a computer that is running a Starter, Basic, or Home edition.</span></span>

<span data-ttu-id="355d7-128">Como alternativa, você pode estar tentando se conectar a um namespace que requer uma conexão criptografada, uma que exija um nível de autenticação de `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** ou a privacidade do PCT do nível de autenticação **RPC \_ \_ \_ \_ \_ C**.</span><span class="sxs-lookup"><span data-stu-id="355d7-128">Alternately, you may be trying to connect to a namespace which requires an encrypted connection, one that requires an authentication level of `pktPrivacy`, **WbemAuthenticationLevelPktPrivacy**, or **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

</dd> <dt>

<span data-ttu-id="355d7-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolução</span><span class="sxs-lookup"><span data-stu-id="355d7-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="355d7-130">Para obter mais informações, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md), [protegendo clientes e provedores do C++](securing-c---clients-and-providers.md)ou [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="355d7-130">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

</dd> </dl>

## <a name="wmi-connection-timed-out"></a><span data-ttu-id="355d7-131">A conexão WMI atingiu o tempo limite</span><span class="sxs-lookup"><span data-stu-id="355d7-131">WMI Connection Timed Out</span></span>

<dl> <dt>

<span data-ttu-id="355d7-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomas</span><span class="sxs-lookup"><span data-stu-id="355d7-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="355d7-133">Sua conexão WMI atinge o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="355d7-133">Your WMI connection times out.</span></span>

</dd> <dt>

<span data-ttu-id="355d7-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Lo</span><span class="sxs-lookup"><span data-stu-id="355d7-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="355d7-135">Devido a problemas de atraso na rede, o computador simplesmente não pode responder no tempo.</span><span class="sxs-lookup"><span data-stu-id="355d7-135">Due to network lag issues, the computer is simply not able to respond in time.</span></span>

</dd> <dt>

<span data-ttu-id="355d7-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolução</span><span class="sxs-lookup"><span data-stu-id="355d7-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="355d7-137">Ao se conectar ao WMI por meio de uma chamada para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) ou [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), você pode definir o sinalizador **wbemConnectFlagUseMaxWait** (Scripting) ou o **\_ sinalizador WBEM \_ Connect \_ use \_ Max \_ Wait** no valor C++ para 128 (0x80) para impor um tempo limite de dois (2) minutos na chamada.</span><span class="sxs-lookup"><span data-stu-id="355d7-137">When connecting to WMI through a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) or [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), you can set the **wbemConnectFlagUseMaxWait** flag (scripting) or the **WBEM\_FLAG\_CONNECT\_USE\_MAX\_WAIT** in C++ value to 128 (0x80) to impose a two (2) minute time-out on the call.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="355d7-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="355d7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="355d7-139">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="355d7-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



