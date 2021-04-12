---
description: A comunicação com um dispositivo de rede usando a interface WMI SNMP requer a configuração dos serviços de dispositivo, SNMP e WMI. As informações neste tópico explicam como configurar o ambiente SNMP WMI.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configurando o ambiente SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297494"
---
# <a name="setting-up-the-wmi-snmp-environment"></a><span data-ttu-id="6dcc4-104">Configurando o ambiente SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="6dcc4-104">Setting up the WMI SNMP Environment</span></span>

<span data-ttu-id="6dcc4-105">A comunicação com um dispositivo de rede usando a interface WMI SNMP requer a configuração dos serviços de dispositivo, SNMP e WMI.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-105">Communicating with a network device using the WMI SNMP interface requires the configuration of the device, SNMP, and WMI services.</span></span> <span data-ttu-id="6dcc4-106">As informações neste tópico explicam como configurar o ambiente SNMP WMI.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-106">The information in this topic explains how to set up the WMI SNMP environment.</span></span>

<span data-ttu-id="6dcc4-107">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="6dcc4-107">The following sections are discussed in this topic:</span></span>

## <a name="installing-the-snmp-provider"></a><span data-ttu-id="6dcc4-108">Instalando o provedor SNMP</span><span class="sxs-lookup"><span data-stu-id="6dcc4-108">Installing the SNMP Provider</span></span>

<span data-ttu-id="6dcc4-109">O serviço SNMP não está habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-109">The SNMP service is not enabled by default.</span></span> <span data-ttu-id="6dcc4-110">Você pode habilitar o serviço SNMP e o provedor WMI SNMP por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-110">You can enable the SNMP service and the WMI SNMP Provider through the Control Panel.</span></span> <span data-ttu-id="6dcc4-111">Lembre-se de que o serviço SNMP deve estar habilitado e em execução para que o provedor WMI SNMP funcione.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-111">Be aware that the SNMP service must be enabled and running for the WMI SNMP provider to work.</span></span>

<span data-ttu-id="6dcc4-112">A partir do Windows Vista, use o procedimento a seguir para instalar o provedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-112">Starting with Windows Vista, use the following procedure to install the SNMP provider.</span></span>

<span data-ttu-id="6dcc4-113">**Para instalar o provedor SNMP**</span><span class="sxs-lookup"><span data-stu-id="6dcc4-113">**To install the SNMP Provider**</span></span>

1.  <span data-ttu-id="6dcc4-114">No **painel de controle**, selecione **programas**.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-114">From the **Control Panel**, select **Programs**.</span></span>
2.  <span data-ttu-id="6dcc4-115">Em **programas e recursos**, selecione **Ativar ou desativar recursos do Windows**.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-115">Under **Programs and Features**, select **Turn Windows features on or off**.</span></span>
3.  <span data-ttu-id="6dcc4-116">Na lista recursos do Windows, role para baixo até o **recurso SNMP** e expanda a lista para que você possa ver o **provedor SNMP WMI**.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-116">In the Windows features list, scroll down to **SNMP feature** and expand the list so that you can see **WMI SNMP Provider**.</span></span>
4.  <span data-ttu-id="6dcc4-117">Marque a caixa de seleção para o **provedor WMI SNMP**.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-117">Select the check box for **WMI SNMP Provider**.</span></span> <span data-ttu-id="6dcc4-118">A caixa de seleção do **recurso SNMP** é selecionada automaticamente porque o provedor requer SNMP.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-118">The check box for **SNMP feature** is selected automatically because the provider requires SNMP.</span></span>
5.  <span data-ttu-id="6dcc4-119">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-119">Click **OK**.</span></span>
6.  <span data-ttu-id="6dcc4-120">Em um prompt de comando ou no menu **Iniciar** , execute Services. msc e verifique se o serviço SNMP foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-120">From a command prompt or the **Start** menu, run Services.msc and ensure that the SNMP service is started.</span></span>

## <a name="creating-an-snmp-namespace"></a><span data-ttu-id="6dcc4-121">Criando um namespace SNMP</span><span class="sxs-lookup"><span data-stu-id="6dcc4-121">Creating an SNMP Namespace</span></span>

<span data-ttu-id="6dcc4-122">Um namespace SNMP define uma exibição de um dispositivo de rede.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-122">An SNMP namespace defines a view of a network device.</span></span>

> [!Note]  
> <span data-ttu-id="6dcc4-123">Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="6dcc4-123">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="6dcc4-124">O procedimento a seguir descreve como criar um [*namespace*](gloss-n.md)SNMP WMI.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-124">The following procedure describes how to create an SNMP WMI [*namespace*](gloss-n.md).</span></span>

<span data-ttu-id="6dcc4-125">**Para criar um namespace SNMP**</span><span class="sxs-lookup"><span data-stu-id="6dcc4-125">**To create an SNMP namespace**</span></span>

1.  <span data-ttu-id="6dcc4-126">Crie uma instância da classe de sistema de [**\_ \_ namespace**](--namespace.md) Compilando um arquivo [*formato MOF*](gloss-m.md) . mof ou usando a [API com para o WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6dcc4-126">Create an instance of the [**\_\_Namespace**](--namespace.md) system class either by compiling a [*Managed Object Format*](gloss-m.md) .mof file or by using the [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="6dcc4-127">Para obter mais informações, consulte [Criando hierarquias no WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6dcc4-127">For more information, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

2.  <span data-ttu-id="6dcc4-128">Associe os [*qualificadores*](gloss-q.md) do provedor SNMP à definição do namespace.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-128">Associate SNMP provider [*qualifiers*](gloss-q.md) with the namespace definition.</span></span>

    <span data-ttu-id="6dcc4-129">Os qualificadores do provedor SNMP contêm informações de contexto específicas de implementação e propriedades de transporte que definem como o provedor SNMP acessa um dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-129">The SNMP provider qualifiers contain implementation-specific context information and transport properties that define how the SNMP provider accesses an SNMP device.</span></span> <span data-ttu-id="6dcc4-130">Para obter mais informações, consulte [**qualificadores específicos para o provedor SNMP**](qualifiers-specific-to-the-snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6dcc4-130">For more information, see [**Qualifiers Specific to the SNMP Provider**](qualifiers-specific-to-the-snmp-provider.md).</span></span>

3.  <span data-ttu-id="6dcc4-131">Use a ferramenta de linha de comando [Mofcomp](mofcomp.md) para carregar o código MOF no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-131">Use the [mofcomp](mofcomp.md) command line tool to load the MOF code into the WMI repository.</span></span>

    <span data-ttu-id="6dcc4-132">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="6dcc4-132">For more information, see [Compiling MOF files](compiling-mof-files.md).</span></span>

<span data-ttu-id="6dcc4-133">O exemplo de código MOF a seguir define o \\ namespace SNMP com um subconjunto dos qualificadores que podem ser associados a um namespace SNMP.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-133">The following MOF code example defines the \\snmp namespace with a subset of the qualifiers that can be associated with an SNMP namespace.</span></span>

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a><span data-ttu-id="6dcc4-134">Inserindo dados de MIB SNMP no WMI</span><span class="sxs-lookup"><span data-stu-id="6dcc4-134">Inserting SNMP MIB Data into WMI</span></span>

<span data-ttu-id="6dcc4-135">Como um provedor, o provedor SNMP atua como uma ponte entre os dados SNMP e as classes WMI.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-135">As a provider, the SNMP provider acts as a bridge between SNMP data and WMI classes.</span></span> <span data-ttu-id="6dcc4-136">Portanto, você deve ter classes no WMI que representem diferentes aspectos de um dispositivo habilitado para SNMP.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-136">Therefore, you must have classes in WMI that represent different aspects of an SNMP-enabled device.</span></span> <span data-ttu-id="6dcc4-137">Para fazer isso, você deve usar o compilador do módulo de informações do SNMP ([smi2smir](smi2smir.md)) para compilar informações de gerenciamento SNMP do formato SNMP nas definições de esquema de CIM equivalentes.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-137">To do so, you must use the SNMP information module compiler ([smi2smir](smi2smir.md)) to compile SNMP management information from the SNMP format into the equivalent CIM schema definitions.</span></span> <span data-ttu-id="6dcc4-138">Você pode direcionar a saída do compilador de informações para um banco de dados de esquema SNMP chamado de "SMIR (repositório de informações do módulo SNMP)" ou vários tipos diferentes de arquivos MOF.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-138">You can then direct the output of the information compiler into an SNMP schema database called the "SNMP Module Information Repository (SMIR)" or to several different kinds of MOF files.</span></span>

<span data-ttu-id="6dcc4-139">O compilador é executado no modo de linha de comando, usando um arquivo MIB como entrada.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-139">The compiler runs in the command-line mode, using one MIB file as input.</span></span> <span data-ttu-id="6dcc4-140">O comando a seguir carrega o arquivo MIB especificado no SMIR.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-140">The following command loads the specified MIB file into the SMIR.</span></span>

<span data-ttu-id="6dcc4-141">\**smi2smir/a\*\*\*<MIB file>*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-141">**smi2smir /a** *<MIB file>*</span></span>

## <a name="setting-up-snmp-communities"></a><span data-ttu-id="6dcc4-142">Configurando comunidades SNMP</span><span class="sxs-lookup"><span data-stu-id="6dcc4-142">Setting Up SNMP Communities</span></span>

<span data-ttu-id="6dcc4-143">Como medida de segurança, a Comunidade "pública" SNMP não é criada por padrão.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-143">As a security measure, the SNMP "public" community is not created by default.</span></span> <span data-ttu-id="6dcc4-144">Você pode criar a Comunidade conforme descrito em [configurações do registro de comunidades](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="6dcc4-144">You can create the community as described in [Communities Registry Settings](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span></span> <span data-ttu-id="6dcc4-145">Se você não tiver nenhuma comunidade, crie a Comunidade "pública" para acessar o provedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-145">If you do not have any community, then create the "public" community to access the SNMP provider.</span></span>

## <a name="generating-mof-files-from-mib-files"></a><span data-ttu-id="6dcc4-146">Gerando arquivos MOF a partir de arquivos MIB</span><span class="sxs-lookup"><span data-stu-id="6dcc4-146">Generating MOF Files from MIB Files</span></span>

<span data-ttu-id="6dcc4-147">Os comandos a seguir são um exemplo de como gerar arquivos MOF a partir dos arquivos MIB instalados quando o provedor SNMP é instalado.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-147">The following commands are an example of how to generate MOF files from the MIB files that are installed when the SNMP provider is installed.</span></span>

<span data-ttu-id="6dcc4-148">**CD** *% windir% \\ System32 \\ WBEM \\ SNMP*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-148">**cd** *%windir%\\system32\\wbem\\SNMP*</span></span>

<span data-ttu-id="6dcc4-149">**Smi2smir/g** *.. \\ .. \\ hostmib. MIB* **>** *hostmib. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-149">**Smi2smir /g** *..\\..\\hostmib.mib* **>** *hostmib.mof*</span></span>

<span data-ttu-id="6dcc4-150">**Smi2smir/g** *.. \\ .. \\ ipforwd. MIB* **>** *ipforwd. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-150">**Smi2smir /g** *..\\..\\ipforwd.mib* **>** *ipforwd.mof*</span></span>

<span data-ttu-id="6dcc4-151">**Smi2smir/g** *.. \\ .. \\ nipx. MIB* **>** *nipx. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-151">**Smi2smir /g** *..\\..\\nipx.mib* **>** *nipx.mof*</span></span>

<span data-ttu-id="6dcc4-152">**Smi2smir/g** *.. \\ .. \\ MIB \_ II.* MIB MIB **>** *\_ II. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-152">**Smi2smir /g** *..\\..\\mib\_ii.mib* **>** *mib\_ii.mof*</span></span>

<span data-ttu-id="6dcc4-153">**Smi2smir/g** *.. \\ .. \\ lmmib2. MIB* **>** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-153">**Smi2smir /g** *..\\..\\lmmib2.mib* **>** *lmmib2.mof*</span></span>

<span data-ttu-id="6dcc4-154">**Smi2smir/g** *.. \\ .. \\ mcastmib. MIB* **>** *mcastmib. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-154">**Smi2smir /g** *..\\..\\mcastmib.mib* **>** *mcastmib.mof*</span></span>

<span data-ttu-id="6dcc4-155">**Smi2smir/g** *.. \\ .. \\ rfc2571. MIB* **>** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-155">**Smi2smir /g** *..\\..\\rfc2571.mib* **>** *rfc2571.mof*</span></span>

<span data-ttu-id="6dcc4-156">**Smi2smir/g** *.. \\ .. \\ wfospf. MIB* **>** *wfospf. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-156">**Smi2smir /g** *..\\..\\wfospf.mib* **>** *wfospf.mof*</span></span>

<span data-ttu-id="6dcc4-157">**Smi2smir/g** *.. \\ .. \\ DHCP. MIB \\ . \\ .. MSFT. MIB* **>** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-157">**Smi2smir /g** *..\\..\\dhcp.mib..\\..\\msft.mib* **>** *dhcp.mof*</span></span>

<span data-ttu-id="6dcc4-158">**Smi2smir/g** *.. \\ .. \\ WINS \\ . MIB.. \\ . MSFT. MIB* **>** *vence. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-158">**Smi2smir /g** *..\\..\\wins.mib..\\..\\msft.mib* **>** *wins.mof*</span></span>

<span data-ttu-id="6dcc4-159">**Smi2smir/g** *.. \\ .. \\ mipx. MIB. \\ \\ .. MSFT. MIB* **>** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-159">**Smi2smir /g** *..\\..\\mipx.mib..\\..\\msft.mib* **>** *mipx.mof*</span></span>

<span data-ttu-id="6dcc4-160">**Smi2smir/g** *.. \\ .. \\ mripsap. MIB. \\ \\ .. MSFT. MIB* **>** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-160">**Smi2smir /g** *..\\..\\mripsap.mib..\\..\\msft.mib* **>** *mripsap.mof*</span></span>

<span data-ttu-id="6dcc4-161">**Smi2smir/g** *.. \\ .. \\ msipbtp. MIB. \\ \\ .. MSFT. MIB* **>** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-161">**Smi2smir /g** *..\\..\\msipbtp.mib..\\..\\msft.mib* **>** *msipbtp.mof*</span></span>

<span data-ttu-id="6dcc4-162">**Smi2smir/g** *.. \\ .. \\ msiprip2. MIB. \\ \\ .. MSFT. MIB* **>** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-162">**Smi2smir /g** *..\\..\\msiprip2.mib..\\..\\msft.mib* **>** *msiprip2.mof*</span></span>

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a><span data-ttu-id="6dcc4-163">Adicionando arquivos MOF SNMP ao repositório WMI</span><span class="sxs-lookup"><span data-stu-id="6dcc4-163">Adding SNMP MOF Files to the WMI Repository</span></span>

<span data-ttu-id="6dcc4-164">Os comandos a seguir são um exemplo de como adicionar os arquivos MOF que são gerados a partir dos arquivos MIB para o repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-164">The following commands are an example of how to add the MOF files that are generated from the MIB files to the WMI repository.</span></span> <span data-ttu-id="6dcc4-165">Se você quiser adicionar os arquivos MOF à lista de arquivos a serem restaurados automaticamente em uma recuperação de [*repositório WMI*](gloss-w.md) , adicione o sinalizador **-AutoRecuperação** ao final de cada comando.</span><span class="sxs-lookup"><span data-stu-id="6dcc4-165">If you want to add the MOF files to the list of files to be automatically restored in a [*WMI repository*](gloss-w.md) recovery, add the **-AUTORECOVER** flag to the end of each command.</span></span> <span data-ttu-id="6dcc4-166">Para obter mais informações sobre a ferramenta de linha de comando WMI Mofcomp.exe, consulte [**Mofcomp**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="6dcc4-166">For more information about the WMI Mofcomp.exe command-line tool, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="6dcc4-167">**Mofcomp** *hostmib. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-167">**mofcomp** *hostmib.mof*</span></span>

<span data-ttu-id="6dcc4-168">**Mofcomp** *ipforwd. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-168">**mofcomp** *ipforwd.mof*</span></span>

<span data-ttu-id="6dcc4-169">**Mofcomp** *nipx. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-169">**mofcomp** *nipx.mof*</span></span>

<span data-ttu-id="6dcc4-170">**Mofcomp** *MIB \_ II. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-170">**mofcomp** *mib\_ii.mof*</span></span>

<span data-ttu-id="6dcc4-171">**Mofcomp** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-171">**mofcomp** *lmmib2.mof*</span></span>

<span data-ttu-id="6dcc4-172">**Mofcomp** *mcastmib. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-172">**mofcomp** *mcastmib.mof*</span></span>

<span data-ttu-id="6dcc4-173">**Mofcomp** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-173">**mofcomp** *rfc2571.mof*</span></span>

<span data-ttu-id="6dcc4-174">**Mofcomp** *wfospf. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-174">**mofcomp** *wfospf.mof*</span></span>

<span data-ttu-id="6dcc4-175">**Mofcomp** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-175">**mofcomp** *dhcp.mof*</span></span>

<span data-ttu-id="6dcc4-176">**Mofcomp** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-176">**mofcomp** *mipx.mof*</span></span>

<span data-ttu-id="6dcc4-177">**Mofcomp** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-177">**mofcomp** *mripsap.mof*</span></span>

<span data-ttu-id="6dcc4-178">**Mofcomp** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-178">**mofcomp** *msipbtp.mof*</span></span>

<span data-ttu-id="6dcc4-179">**Mofcomp** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="6dcc4-179">**mofcomp** *msiprip2.mof*</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dcc4-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6dcc4-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dcc4-181">Acessando dispositivos SNMP</span><span class="sxs-lookup"><span data-stu-id="6dcc4-181">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 
