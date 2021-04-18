---
title: Transferências de dados descarregadas
description: Transferências de dados descarregadas
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- descarregamento de cópia
- carregado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105788643"
---
# <a name="offloaded-data-transfers"></a><span data-ttu-id="4424f-106">Transferências de dados descarregadas</span><span class="sxs-lookup"><span data-stu-id="4424f-106">Offloaded data transfers</span></span>

## <a name="platforms"></a><span data-ttu-id="4424f-107">Plataformas</span><span class="sxs-lookup"><span data-stu-id="4424f-107">Platforms</span></span>

<span data-ttu-id="4424f-108">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="4424f-108">**Clients** – Windows 8</span></span>  
<span data-ttu-id="4424f-109">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4424f-109">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="4424f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4424f-110">Description</span></span>

<span data-ttu-id="4424f-111">Para avançar a movimentação de dados de armazenamento, a Microsoft desenvolveu uma nova tecnologia de transferência de dados – transferência de dados descarregada (ODX).</span><span class="sxs-lookup"><span data-stu-id="4424f-111">To advance the storage data movement, Microsoft has developed a new data transfer technology – offloaded data transfer (ODX).</span></span> <span data-ttu-id="4424f-112">Em vez de usar operações de gravação armazenadas em buffer e de leitura em buffer, o Windows ODX inicia a operação de cópia com uma leitura de descarregamento e recupera um token que representa os dados do dispositivo de armazenamento e, em seguida, usa um comando de gravação de descarregamento com o token para solicitar a movimentação de dados do disco de origem para o disco de destino.</span><span class="sxs-lookup"><span data-stu-id="4424f-112">Instead of using buffered read and buffered write operations, Windows ODX starts the copy operation with an offload read and retrieves a token representing the data from the storage device, then uses an offload write command with the token to request data movement from the source disk to the destination disk.</span></span> <span data-ttu-id="4424f-113">O Gerenciador de cópia dos dispositivos de armazenamento executa a movimentação de dados de acordo com o token.</span><span class="sxs-lookup"><span data-stu-id="4424f-113">The copy manager of the storage devices performs the data movement according to the token.</span></span> <span data-ttu-id="4424f-114">No Windows 8, o gerente de ti e o administrador de armazenamento podem usar o recurso ODX do Windows para interagir com o dispositivo de armazenamento para mover arquivos ou dados grandes por meio da rede de armazenamento de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="4424f-114">In the Windows 8, the IT manager and storage administrator are able to use the Windows ODX feature to interact with the storage device to move large files or data through the high-speed storage network.</span></span> <span data-ttu-id="4424f-115">O Windows ODX reduzirá significativamente o tráfego de rede do servidor cliente e o uso de tempo de CPU durante transferências de dados grandes, pois toda a movimentação de dados está na rede de armazenamento de back-end.</span><span class="sxs-lookup"><span data-stu-id="4424f-115">Windows ODX will significantly reduce client-server network traffic and CPU time usage during large data transfers because all the data movement is at the backend storage network.</span></span> <span data-ttu-id="4424f-116">O ODX pode ser usado na implantação de máquinas virtuais, na migração maciça de dados e no suporte a dispositivos de armazenamento em camadas e pode reduzir o custo da implantação de hardware físico por meio dos recursos de armazenamento de provisionamento dinâmico e ODX.</span><span class="sxs-lookup"><span data-stu-id="4424f-116">ODX can be used in virtual machine deployment, massive data migration, and tiered storage device support, and can lower the cost of physical hardware deployment through the ODX and thin provisioning storage features.</span></span>

> [!Note]  
> <span data-ttu-id="4424f-117">Este recurso só funcionará em dispositivos de armazenamento com a implementação de especificação SPC4 e SBC3.</span><span class="sxs-lookup"><span data-stu-id="4424f-117">This feature will only work on storage devices with SPC4 and SBC3 specification implementation.</span></span>

 

## <a name="functional-details"></a><span data-ttu-id="4424f-118">Detalhes funcionais</span><span class="sxs-lookup"><span data-stu-id="4424f-118">Functional details</span></span>

-   <span data-ttu-id="4424f-119">O recurso ODX do Windows é inserido no mecanismo de cópia do sistema operacional Windows; durante a enumeração de armazenamento, o Windows consultará o recurso ODX do dispositivo de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4424f-119">The Windows ODX feature is embedded in the copy engine of the Windows operating system; during storage enumeration, Windows will query the ODX capability of the storage device</span></span>
-   <span data-ttu-id="4424f-120">Copiar dispositivo de armazenamento de origem e copiar o dispositivo de armazenamento de destino deve ser gerenciado no mesmo Gerenciador de cópia para suporte de descarregamento de cópia</span><span class="sxs-lookup"><span data-stu-id="4424f-120">Copy source storage device and copy destination storage device should be managed under the same copy manager for copy offload support</span></span>
-   <span data-ttu-id="4424f-121">Se uma operação de descarregamento de cópia falhar, o Gerenciador de cópia do dispositivo de armazenamento deverá retornar os dados de detecção adicionais apropriados para o tratamento de erros dos aplicativos</span><span class="sxs-lookup"><span data-stu-id="4424f-121">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for the apps’ error handling</span></span>
-   <span data-ttu-id="4424f-122">O mecanismo de cópia do Windows voltará para a operação de cópia tradicional se a operação de descarregamento de cópia falhar</span><span class="sxs-lookup"><span data-stu-id="4424f-122">The Windows copy engine will fall back to the traditional copy operation if the copy offload operation fails</span></span>

## <a name="using-odx"></a><span data-ttu-id="4424f-123">Usando ODX</span><span class="sxs-lookup"><span data-stu-id="4424f-123">Using ODX</span></span>

-   <span data-ttu-id="4424f-124">O aplicativo de transferência de dados deve garantir que o LUN de origem de cópia e o LUN de destino de cópia sejam ODX capazes antes de chamar as rotinas de API ODX</span><span class="sxs-lookup"><span data-stu-id="4424f-124">The data transfer app must ensure both copy source LUN and copy destination LUN are ODX capable before calling the ODX API routines</span></span>
-   <span data-ttu-id="4424f-125">No Windows Explorer, os usuários podem usar "arrastar" ou "copiar e colar" para executar o descarregamento de cópia</span><span class="sxs-lookup"><span data-stu-id="4424f-125">In Windows explorer, users could use “drag” or “copy and paste” to perform copy offload</span></span>
-   <span data-ttu-id="4424f-126">Quando o LUN de origem e o LUN de destino são montados com o sistema de arquivos, o aplicativo deve chamar somente a gravação de descarregamento de FSCTL \_ \_ e leitura de \_ descarregamento de fsctl \_ para executar a transferência de dados do LUN de origem para o LUN de destino</span><span class="sxs-lookup"><span data-stu-id="4424f-126">When the source LUN and destination LUN are mounted with the file system, the app must only call FSCTL\_Offload\_Read and FSCTL\_Offload\_Write to perform data transfer from the source LUN to the destination LUN</span></span>
-   <span data-ttu-id="4424f-127">Se uma operação de descarregamento de cópia falhar, o Gerenciador de cópia do dispositivo de armazenamento deverá retornar os dados de detecção adicionais apropriados para o tratamento de erros dos aplicativos</span><span class="sxs-lookup"><span data-stu-id="4424f-127">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for apps’ error handling</span></span>
-   <span data-ttu-id="4424f-128">Quando o LUN de origem ou o LUN de destino não é montado com o sistema de arquivos e bloqueado, o aplicativo deve chamar o \_ armazenamento \_ de IOCTL gerenciar \_ \_ \_ atributos de conjunto de dados com a \_ ação DeviceDsmAction OffloadRead ou DeviceDsmAction \_ OffloadWrite para executar o descarregamento de cópia</span><span class="sxs-lookup"><span data-stu-id="4424f-128">When the source LUN or destination LUN is not mounted with the file system and locked, the app must call IOCTL\_STORAGE\_MANAGE\_DATA\_SET\_ATTRIBUTES with DeviceDsmAction\_OffloadRead or DeviceDsmAction\_OffloadWrite action to perform copy offload</span></span>
-   <span data-ttu-id="4424f-129">Os aplicativos de gerenciamento de armazenamento podem usar \_ \_ a API de passagem SCSI para executar transferências de dados descarregadas quando os LUNs de origem e de destino não são montados com nenhum sistema de arquivos e bloqueados</span><span class="sxs-lookup"><span data-stu-id="4424f-129">Storage management apps may use SCSI\_PASS\_THROUGH API to perform offloaded data transfers when both source and destination LUNs are not mounted with any file system and locked</span></span>

## <a name="tests"></a><span data-ttu-id="4424f-130">Testes</span><span class="sxs-lookup"><span data-stu-id="4424f-130">Tests</span></span>

-   <span data-ttu-id="4424f-131">Para garantir uma experiência de usuário robusta, verifique a certificação ODX do Windows da matriz de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4424f-131">To ensure a robust user experience, verify the Windows ODX certification of the storage array</span></span>
-   <span data-ttu-id="4424f-132">O dispositivo de armazenamento deve estar em conformidade com os requisitos de certificação de transferência de dados descarregados do Windows (usado para ser logotipo) para dar suporte ao recurso ODX</span><span class="sxs-lookup"><span data-stu-id="4424f-132">The storage device must comply with Windows Offloaded Data Transfers certification (used to be Logo) requirements to support ODX feature</span></span>
-   <span data-ttu-id="4424f-133">Usar o kit de certificação de hardware de transferência de dados descarregados do Windows para verificar o suporte do recurso ODX dos dispositivos de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4424f-133">Use the Windows Offloaded Data Transfers Hardware Certification Kit to verify the ODX feature support of the storage devices</span></span>

## <a name="resources"></a><span data-ttu-id="4424f-134">Recursos</span><span class="sxs-lookup"><span data-stu-id="4424f-134">Resources</span></span>

-   <span data-ttu-id="4424f-135">Especificação T10 XCOPY Lite (11-059r8)</span><span class="sxs-lookup"><span data-stu-id="4424f-135">T10 XCOPY Lite Spec (11-059r8)</span></span>
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [<span data-ttu-id="4424f-136">Serviços de painel de hardware</span><span class="sxs-lookup"><span data-stu-id="4424f-136">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)
-   [<span data-ttu-id="4424f-137">\_Estrutura de passagem SCSI \_</span><span class="sxs-lookup"><span data-stu-id="4424f-137">SCSI\_PASS\_THROUGH Structure</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 