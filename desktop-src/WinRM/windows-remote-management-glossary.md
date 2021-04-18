---
title: Glossário de Gerenciamento Remoto do Windows
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105789931"
---
# <a name="windows-remote-management-glossary"></a><span data-ttu-id="5348d-103">Glossário de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="5348d-103">Windows Remote Management Glossary</span></span>


<dl> <dt>

<span data-ttu-id="5348d-104">WSMan: itens \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5348d-104">\*\*\*\*wsman:Items\*\*\*\*</span></span>
</dt> <dd>

<span data-ttu-id="5348d-105">Um elemento de protocolo WS-Management retornado em uma enumeração que obtém as instâncias e a instância [*EPRS*](/windows).</span><span class="sxs-lookup"><span data-stu-id="5348d-105">A WS-Management protocol element returned in an enumeration that obtains both the instances and the instance [*EPRs*](/windows).</span></span> <span data-ttu-id="5348d-106">**WSMan: Items** é um contêiner que mantém uma instância e seu EPR.</span><span class="sxs-lookup"><span data-stu-id="5348d-106">**wsman:Items** is a container that holds an instance and its EPR.</span></span> <span data-ttu-id="5348d-107">Esse tipo de enumeração é iniciado quando o sinalizador **WSManFlagReturnObjectAndEPR** é definido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="5348d-107">This type of enumeration is initiated when the **WSManFlagReturnObjectAndEPR** flag is set in the request.</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="5348d-108">B</span><span class="sxs-lookup"><span data-stu-id="5348d-108">B</span></span>

<dl> <dt>

<span data-ttu-id="5348d-109">**Baseboard Management Controller (BMC)**</span><span class="sxs-lookup"><span data-stu-id="5348d-109">**baseboard management controller (BMC)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-110">Um microcontrolador conectado localmente a um servidor.</span><span class="sxs-lookup"><span data-stu-id="5348d-110">A microcontroller attached locally to a server.</span></span> <span data-ttu-id="5348d-111">BMCs têm sensores que monitoram o estado físico do servidor e uma conexão de rede separada que pode se comunicar pela rede, mesmo que o servidor esteja offline.</span><span class="sxs-lookup"><span data-stu-id="5348d-111">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="5348d-112">Você tem acesso aos dados do BMC por meio do provedor WMI da [*IPMI (interface de gerenciamento de plataforma inteligente)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5348d-112">You have access to BMC data through the [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-113">**Autenticação básica**</span><span class="sxs-lookup"><span data-stu-id="5348d-113">**Basic authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-114">O nome de usuário e a senha enviados na troca de autenticação.</span><span class="sxs-lookup"><span data-stu-id="5348d-114">The user name and password sent in the authentication exchange.</span></span> <span data-ttu-id="5348d-115">A autenticação básica pode ser configurada para usar o transporte HTTP ou HTTPS em um domínio ou grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5348d-115">Basic authentication can be configured to use either HTTP or HTTPS transport in a domain or workgroup.</span></span> <span data-ttu-id="5348d-116">Esse método é o método menos seguro de autenticação.</span><span class="sxs-lookup"><span data-stu-id="5348d-116">This method is the least secure method of authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-117">**BMC**</span><span class="sxs-lookup"><span data-stu-id="5348d-117">**BMC**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-118">Consulte [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-118">See [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="5348d-119">C</span><span class="sxs-lookup"><span data-stu-id="5348d-119">C</span></span>

<dl> <dt>

<span data-ttu-id="5348d-120">**CIM**</span><span class="sxs-lookup"><span data-stu-id="5348d-120">**CIM**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-121">Consulte [*modelo CIM (CIM)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-121">See [*Common Information Model (CIM)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-122">**cliente**</span><span class="sxs-lookup"><span data-stu-id="5348d-122">**client**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-123">O aplicativo cliente que usa o protocolo WS-Management para acessar o serviço de gerenciamento no computador local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="5348d-123">The client application using the WS-Management protocol to access the management service on either the local or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-124">**CIM (Modelo de Informação Comum)**</span><span class="sxs-lookup"><span data-stu-id="5348d-124">**Common Information Model (CIM)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-125">O modelo [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md) que descreve como representar objetos de rede e computador do mundo real.</span><span class="sxs-lookup"><span data-stu-id="5348d-125">The [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md) model that describes how to represent real-world computer and network objects.</span></span> <span data-ttu-id="5348d-126">O CIM usa um paradigma orientado a objeto, em que os objetos gerenciados são modelados usando os conceitos de classes e instâncias.</span><span class="sxs-lookup"><span data-stu-id="5348d-126">CIM uses an object-oriented paradigm, where managed objects are modeled using the concepts of classes and instances.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="5348d-127">D</span><span class="sxs-lookup"><span data-stu-id="5348d-127">D</span></span>

<dl> <dt>

<span data-ttu-id="5348d-128">**Autenticação Digest**</span><span class="sxs-lookup"><span data-stu-id="5348d-128">**Digest authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-129">Um Exchange em que o servidor recebe uma solicitação de um cliente e envia dados sobre o cliente para um servidor de autenticação, normalmente um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="5348d-129">An exchange wherein the server receives a request from a client and sends data about the client to an authenticating server, typically a domain controller.</span></span> <span data-ttu-id="5348d-130">Se o cliente for autenticado, o servidor receberá uma chave de sessão de resumo usada para autenticar solicitações subsequentes do cliente.</span><span class="sxs-lookup"><span data-stu-id="5348d-130">If the client is authenticated, then the server receives a Digest session key used to authenticate subsequent requests from the client.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-131">**DMTF (Distributed Management Task Force)**</span><span class="sxs-lookup"><span data-stu-id="5348d-131">**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-132">A organização do setor que desenvolve os padrões de gerenciamento e a tecnologia de integração para ambientes corporativos e de Internet.</span><span class="sxs-lookup"><span data-stu-id="5348d-132">The industry organization developing management standards and integration technology for enterprise and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-133">**DMTF**</span><span class="sxs-lookup"><span data-stu-id="5348d-133">**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-134">Consulte [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-134">See [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="5348d-135">E</span><span class="sxs-lookup"><span data-stu-id="5348d-135">E</span></span>

<dl> <dt>

<span data-ttu-id="5348d-136">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="5348d-136">**endpoint**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-137">Um recurso que pode ser resolvido por uma [*referência de ponto de extremidade (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-137">A resource that can be addressed by an [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-138">**referência de ponto de extremidade (EPR)**</span><span class="sxs-lookup"><span data-stu-id="5348d-138">**endpoint reference (EPR)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-139">Uma combinação de WS-Addressing e WS-Management elementos de endereçamento que descrevem em conjunto um endereço para um recurso no cabeçalho SOAP da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5348d-139">A combination of WS-Addressing and WS-Management addressing elements that together describe an address for a resource in the message SOAP header.</span></span> <span data-ttu-id="5348d-140">Este é um termo de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="5348d-140">This is a web service term.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-141">**enumeração**</span><span class="sxs-lookup"><span data-stu-id="5348d-141">**enumeration**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-142">Um conjunto, ou coleção, de instâncias de [*recurso*](windows-remote-management-glossary.md) ou a ação de solicitar um conjunto desse tipo.</span><span class="sxs-lookup"><span data-stu-id="5348d-142">A set, or collection, of [*resource*](windows-remote-management-glossary.md) instances or the action of requesting such a set.</span></span> <span data-ttu-id="5348d-143">No protocolo WS-Management, o [*WS-Enumeration*](windows-remote-management-glossary.md) é usado para obter a coleção.</span><span class="sxs-lookup"><span data-stu-id="5348d-143">In WS-Management protocol, [*WS-Enumeration*](windows-remote-management-glossary.md) is used to obtain the collection.</span></span> <span data-ttu-id="5348d-144">Na implementação de script do serviço WinRM de enumeração, [**Session. enumerar**](session-enumerate.md) e o objeto [**Enumerator**](enumerator.md) são usados.</span><span class="sxs-lookup"><span data-stu-id="5348d-144">In the WinRM service scripting implementation of enumeration, [**Session.Enumerate**](session-enumerate.md) and the [**Enumerator**](enumerator.md) object are used.</span></span> <span data-ttu-id="5348d-145">O método e a interface C++ correspondentes são [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) e [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="5348d-145">The corresponding C++ method and interface are [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) and [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-146">**EPR**</span><span class="sxs-lookup"><span data-stu-id="5348d-146">**EPR**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-147">Consulte [*referência de ponto de extremidade (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-147">See [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-148">**Serviço de coleta de eventos**</span><span class="sxs-lookup"><span data-stu-id="5348d-148">**Event Collection Service**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-149">O componente do sistema operacional que recebe eventos do BMC e outros componentes ou aplicativos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5348d-149">The operating system component that receives events from the BMC and other operating system components or applications.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-150">**encaminhamento de eventos**</span><span class="sxs-lookup"><span data-stu-id="5348d-150">**event forwarding**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-151">Uma notificação de eventos que ocorrem em computadores remotos pode ser enviada para aplicativos de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5348d-151">A notification of events that occur on remote computers can be sent to subscribing applications.</span></span> <span data-ttu-id="5348d-152">O encaminhamento de eventos não é um recurso do WinRM, mas do [log de eventos do Windows](/windows/desktop/WES/windows-event-log).</span><span class="sxs-lookup"><span data-stu-id="5348d-152">Event forwarding is not a feature of WinRM, but of the [Windows Event Log](/windows/desktop/WES/windows-event-log).</span></span> <span data-ttu-id="5348d-153">O encaminhamento de eventos se torna disponível pela primeira vez no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5348d-153">Event forwarding becomes available for the first time in Windows Vista.</span></span> <span data-ttu-id="5348d-154">Os aplicativos de gerenciamento, como o Microsoft Operations Manager (MOM), usam o encaminhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="5348d-154">The Management applications, such as Microsoft Operations Manager (MOM) use event forwarding.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="5348d-155">F</span><span class="sxs-lookup"><span data-stu-id="5348d-155">F</span></span>

<dl> <dt>

<span data-ttu-id="5348d-156">**filter**</span><span class="sxs-lookup"><span data-stu-id="5348d-156">**filter**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-157">Um mecanismo de consulta para especificar um conjunto limitado de instâncias na solicitação de um [*recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-157">A query mechanism for specifying a limited set of instances in the request for a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-158">Você pode especificar um parâmetro de *filtro* em chamadas para [**Session. enumerar**](session-enumerate.md) ou [**IWSManSession:: enumerar**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="5348d-158">You can specify a *filter* parameter on calls to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-159">**dialeto do filtro**</span><span class="sxs-lookup"><span data-stu-id="5348d-159">**filter dialect**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-160">Uma cadeia de caracteres XML que identifica o dialeto XML usado para especificar um [*filtro*](windows-remote-management-glossary.md) em uma chamada para [**Session. enumerar**](session-enumerate.md) ou [**IWSManSession:: enumerar**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="5348d-160">An XML string that identifies the XML dialect used to specify a [*filter*](windows-remote-management-glossary.md) in a call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span> <span data-ttu-id="5348d-161">O serviço WinRM oferece suporte a [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como um dialeto de filtro ao receber solicitações.</span><span class="sxs-lookup"><span data-stu-id="5348d-161">The WinRM service supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as a filter dialect when receiving requests.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-162">**fragmento**</span><span class="sxs-lookup"><span data-stu-id="5348d-162">**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-163">Uma cadeia de caracteres XML que identifica parte de uma instância de um recurso em vez de todo o recurso.</span><span class="sxs-lookup"><span data-stu-id="5348d-163">An XML string that identifies part of an instance of a resource rather than the entire resource.</span></span> <span data-ttu-id="5348d-164">Suporte a fragmento encontrado no objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5348d-164">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-165">**dialeto de fragmento**</span><span class="sxs-lookup"><span data-stu-id="5348d-165">**fragment dialect**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-166">Uma cadeia de caracteres XML que identifica o dialeto XML usado para especificar um [*fragmento*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-166">An XML string that identifies the XML dialect used to specify a [*fragment*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-167">Suporte a fragmento encontrado no objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5348d-167">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="5348d-168">O serviço WinRM oferece suporte a [*XPath*](windows-remote-management-glossary.md) para dialeto de fragmento ao receber solicitações.</span><span class="sxs-lookup"><span data-stu-id="5348d-168">The WinRM service supports [*XPath*](windows-remote-management-glossary.md) for fragment dialect when receiving requests.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="5348d-169">I</span><span class="sxs-lookup"><span data-stu-id="5348d-169">I</span></span>

<dl> <dt>

<span data-ttu-id="5348d-170">**em banda**</span><span class="sxs-lookup"><span data-stu-id="5348d-170">**in-band**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-171">O aplicativo cliente obtém dados do BMC por meio do [*ouvinte*](windows-remote-management-glossary.md) do WinRM no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5348d-171">The client application obtains BMC data through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-172">**IPMI (interface de gerenciamento de plataforma inteligente)**</span><span class="sxs-lookup"><span data-stu-id="5348d-172">**Intelligent Platform Management Interface (IPMI)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-173">Um padrão do setor de ti para a arquitetura do [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-173">An IT industry standard for the architecture of [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-174">Os recursos de gerenciamento de hardware do Windows fornecem um [*driver IPMI*](windows-remote-management-glossary.md) e um [*provedor WMI IPMI*](windows-remote-management-glossary.md) que permite que scripts de gerenciamento, ferramentas de linha de comando e aplicativos obtenham dados do BMC.</span><span class="sxs-lookup"><span data-stu-id="5348d-174">The Windows hardware management features supply an [*IPMI driver*](windows-remote-management-glossary.md) and a WMI [*IPMI provider*](windows-remote-management-glossary.md) that allow management scripts, command-line tools, and applications to obtain BMC data.</span></span> <span data-ttu-id="5348d-175">O provedor IPMI tem [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.</span><span class="sxs-lookup"><span data-stu-id="5348d-175">The IPMI provider has WMI [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-176">**IPMI**</span><span class="sxs-lookup"><span data-stu-id="5348d-176">**IPMI**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-177">Consulte [*IPMI (interface de gerenciamento de plataforma inteligente)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-177">See [*Intelligent Platform Management Interface (IMPI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-178">**Driver IPMI**</span><span class="sxs-lookup"><span data-stu-id="5348d-178">**IPMI driver**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-179">O driver de kernel que habilita o acesso a dispositivos [*BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) dos componentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5348d-179">The kernel driver that enables access to [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) devices from the operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-180">**Provedor IPMI**</span><span class="sxs-lookup"><span data-stu-id="5348d-180">**IPMI provider**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-181">Um provedor WMI padrão que define classes que modelam o [*IPMI*](windows-remote-management-glossary.md) e seus dados.</span><span class="sxs-lookup"><span data-stu-id="5348d-181">A standard WMI provider that defines classes modeling the [*IPMI*](windows-remote-management-glossary.md) and its data.</span></span> <span data-ttu-id="5348d-182">O [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) é uma DLL com que obtém dados do BMC.</span><span class="sxs-lookup"><span data-stu-id="5348d-182">The [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) is a COM DLL that obtains data from the BMC.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="5348d-183">K</span><span class="sxs-lookup"><span data-stu-id="5348d-183">K</span></span>

<dl> <dt>

<span data-ttu-id="5348d-184">**KCS**</span><span class="sxs-lookup"><span data-stu-id="5348d-184">**KCS**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-185">Consulte [*estilo do controlador de teclado (KCS)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-185">See [*Keyboard Controller Style (KCS)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-186">**Autenticação Kerberos**</span><span class="sxs-lookup"><span data-stu-id="5348d-186">**Kerberos authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-187">Um método de autenticação mútua entre o cliente e o servidor que usa chaves criptografadas.</span><span class="sxs-lookup"><span data-stu-id="5348d-187">A method of mutual authentication between the client and server that uses encrypted keys.</span></span> <span data-ttu-id="5348d-188">Para computadores em execução em um sistema operacional baseado no Windows, a conta do cliente deve ser uma conta de domínio no mesmo domínio que o servidor.</span><span class="sxs-lookup"><span data-stu-id="5348d-188">For computers running on a Windows-based operating system, the client account must be a domain account in the same domain as the server.</span></span> <span data-ttu-id="5348d-189">Quando um cliente usa credenciais padrão, o Kerberos é o método de autenticação se a cadeia de conexão não for uma das seguintes: localhost, 127.0.0.1 ou \[ :: 1 \] .</span><span class="sxs-lookup"><span data-stu-id="5348d-189">When a client uses default credentials, Kerberos is the authentication method if the connection string is not one of the following: localhost, 127.0.0.1, or \[::1\].</span></span>

</dd> <dt>

<span data-ttu-id="5348d-190">**Estilo do controlador de teclado (KCS)**</span><span class="sxs-lookup"><span data-stu-id="5348d-190">**Keyboard Controller Style (KCS)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-191">O protocolo usado pelo [*driver IPMI*](windows-remote-management-glossary.md) para se comunicar com o [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-191">The protocol used by the [*IPMI driver*](windows-remote-management-glossary.md) to communicate with the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="5348d-192">L</span><span class="sxs-lookup"><span data-stu-id="5348d-192">L</span></span>

<dl> <dt>

<span data-ttu-id="5348d-193">**listener**</span><span class="sxs-lookup"><span data-stu-id="5348d-193">**listener**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-194">Um serviço de gerenciamento que implementa WS-Management protocolo para enviar e receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="5348d-194">A management service that implements WS-Management protocol to send and receive messages.</span></span> <span data-ttu-id="5348d-195">O WinRM é um serviço de escuta.</span><span class="sxs-lookup"><span data-stu-id="5348d-195">WinRM is a listener service.</span></span> <span data-ttu-id="5348d-196">Um ouvinte é definido por um transporte (HTTP ou HTTPS) e um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="5348d-196">A listener is defined by a transport (HTTP or HTTPS) and an IPv4 or IPv6 address.</span></span> <span data-ttu-id="5348d-197">Você pode criar mais de uma instância de ouvinte do WinRM em um único computador fornecendo a eles um número de porta ou endereço TCP/IP diferente.</span><span class="sxs-lookup"><span data-stu-id="5348d-197">You can create more than one WinRM listener instance on a single computer by giving them a different TCP/IP address or port number.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="5348d-198">M</span><span class="sxs-lookup"><span data-stu-id="5348d-198">M</span></span>

<dl> <dt>

<span data-ttu-id="5348d-199">**message**</span><span class="sxs-lookup"><span data-stu-id="5348d-199">**message**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-200">Um pacote de informações transmitidas entre computadores ou redes separadas construídas com o protocolo [*SOAP*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5348d-200">A package of information transmitted between computers or separate networks constructed with the [*SOAP*](windows-remote-management-glossary.md) protocol.</span></span> <span data-ttu-id="5348d-201">O pacote tem um cabeçalho, que descreve o destino e o transporte da mensagem e um corpo que contém o conteúdo a ser usado quando a mensagem chega.</span><span class="sxs-lookup"><span data-stu-id="5348d-201">The package has a header, that describes the message target and transport, and a body that contains the content to be used when the message arrives.</span></span> <span data-ttu-id="5348d-202">Uma mensagem é uma combinação de elementos de especificações como [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)e [*WS-Management*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-202">A message is a combination of elements from specifications such as [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="5348d-203">N</span><span class="sxs-lookup"><span data-stu-id="5348d-203">N</span></span>

<dl> <dt>

<span data-ttu-id="5348d-204">**namespace**</span><span class="sxs-lookup"><span data-stu-id="5348d-204">**namespace**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-205">Um namespace do [*WMI*](windows-remote-management-glossary.md) , que é um agrupamento lógico de classes e instâncias do WMI para controlar o escopo e o acesso.</span><span class="sxs-lookup"><span data-stu-id="5348d-205">A [*WMI*](windows-remote-management-glossary.md) namespace, which is a logical grouping of WMI classes and instances to control scope and access.</span></span> <span data-ttu-id="5348d-206">A fonte de dados de gerenciamento mais frequente para sistemas que executam o Windows é o \\ namespace raiz cimv2, que contém classes como o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="5348d-206">The most frequent source of management data for systems running Windows is the root\\cimv2 namespace, which contains classes such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="5348d-207">Os namespaces aparecem no URI de recurso para classes WMI, por exemplo https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .</span><span class="sxs-lookup"><span data-stu-id="5348d-207">Namespaces appear in the resource URI for WMI classes, for example https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-208">**Negociar autenticação**</span><span class="sxs-lookup"><span data-stu-id="5348d-208">**Negotiate authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-209">Um tipo de autenticação negociado e de logon único que é a implementação do Windows do [*mecanismo de negociação de GSSAPI simples e protegido (SPNEGO)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-209">A negotiated, single sign on type of authentication that is the Windows implementation of [*Simple and Protected GSSAPI Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-210">A negociação SPNEGO determina se a autenticação é manipulada por Kerberos ou NTLM.</span><span class="sxs-lookup"><span data-stu-id="5348d-210">SPNEGO negotiation determines whether authentication is handled by Kerberos or NTLM.</span></span> <span data-ttu-id="5348d-211">Kerberos é o mecanismo preferencial.</span><span class="sxs-lookup"><span data-stu-id="5348d-211">Kerberos is the preferred mechanism.</span></span> <span data-ttu-id="5348d-212">A autenticação de negociação em sistemas baseados no Windows também é chamada de autenticação integrada do Windows.</span><span class="sxs-lookup"><span data-stu-id="5348d-212">Negotiate authentication on Windows-based systems is also called Windows Integrated Authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-213">**sensor numérico**</span><span class="sxs-lookup"><span data-stu-id="5348d-213">**numeric sensor**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-214">Um tipo numérico de sensor em um [*Controlador BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md), por exemplo, temperatura ou voltagem.</span><span class="sxs-lookup"><span data-stu-id="5348d-214">A numeric type of sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md), for example temperature or voltage.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="5348d-215">O</span><span class="sxs-lookup"><span data-stu-id="5348d-215">O</span></span>

<dl> <dt>

<span data-ttu-id="5348d-216">**opção**</span><span class="sxs-lookup"><span data-stu-id="5348d-216">**option**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-217">Os dados adicionais exigidos pelo provedor de recursos para processar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="5348d-217">The additional data required by the resource provider to process a request.</span></span> <span data-ttu-id="5348d-218">Por exemplo, alguns provedores WMI exigem dados adicionais fornecidos como objetos [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) .</span><span class="sxs-lookup"><span data-stu-id="5348d-218">For example, some WMI providers require additional data supplied as [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) objects.</span></span> <span data-ttu-id="5348d-219">O suporte à opção é encontrado no objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5348d-219">Option support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-220">**fora de banda**</span><span class="sxs-lookup"><span data-stu-id="5348d-220">**out-of-band**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-221">O aplicativo cliente obtém dados diretamente do [*BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) de outro computador, em vez do [*ouvinte*](windows-remote-management-glossary.md) do WinRM no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5348d-221">The client application obtains data directly from the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) of another computer, rather than through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="5348d-222">P</span><span class="sxs-lookup"><span data-stu-id="5348d-222">P</span></span>

<dl> <dt>

<span data-ttu-id="5348d-223">**recebimento**</span><span class="sxs-lookup"><span data-stu-id="5348d-223">**pull**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-224">Uma mensagem de pull de [*WS-Enumeration*](windows-remote-management-glossary.md) é enviada para continuar uma enumeração iniciada por uma chamada inicial para WS-Enumeration: Enumerate.</span><span class="sxs-lookup"><span data-stu-id="5348d-224">A [*WS-Enumeration*](windows-remote-management-glossary.md) pull message is sent to continue an enumeration started by an initial call to WS-Enumeration:Enumerate.</span></span> <span data-ttu-id="5348d-225">A operação pull no serviço WinRM é executada por [**enumerador. ReadItem**](enumerator-readitem.md) ou [**IWSManEnumerator:: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span><span class="sxs-lookup"><span data-stu-id="5348d-225">The pull operation in the WinRM service is performed by [**Enumerator.ReadItem**](enumerator-readitem.md) or [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="5348d-226">R</span><span class="sxs-lookup"><span data-stu-id="5348d-226">R</span></span>

<dl> <dt>

<span data-ttu-id="5348d-227">**Kit**</span><span class="sxs-lookup"><span data-stu-id="5348d-227">**resource**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-228">Um [*ponto de extremidade*](windows-remote-management-glossary.md) que representa um tipo distinto de operação de gerenciamento ou valor.</span><span class="sxs-lookup"><span data-stu-id="5348d-228">An [*endpoint*](windows-remote-management-glossary.md) that represents a distinct type of management operation or value.</span></span> <span data-ttu-id="5348d-229">Um serviço expõe um ou mais recursos e alguns recursos podem ter mais de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5348d-229">A service exposes one or more resources and some resources can have more than one instance.</span></span> <span data-ttu-id="5348d-230">Um recurso de gerenciamento é semelhante a uma classe WMI ou a uma tabela de banco de dados, e uma instância é semelhante a uma instância da classe ou uma linha na tabela.</span><span class="sxs-lookup"><span data-stu-id="5348d-230">A management resource is similar to a WMI class or a database table, and an instance is similar to an instance of the class or a row in the table.</span></span> <span data-ttu-id="5348d-231">Por exemplo, a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) representa um recurso.</span><span class="sxs-lookup"><span data-stu-id="5348d-231">For example, the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class represents a resource.</span></span> <span data-ttu-id="5348d-232">`Win32_LogicalDisk="C:\"` é uma instância específica do recurso.</span><span class="sxs-lookup"><span data-stu-id="5348d-232">`Win32_LogicalDisk="C:\"` is a specific instance of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-233">**URI de recurso**</span><span class="sxs-lookup"><span data-stu-id="5348d-233">**resource URI**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-234">O [*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md) usado para identificar um tipo específico de recurso, como discos ou processos, em um sistema.</span><span class="sxs-lookup"><span data-stu-id="5348d-234">The [*uniform resource identifier (URI)*](windows-remote-management-glossary.md) used to identify a specific type of resource, such as disks or processes, on a system.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="5348d-235">S</span><span class="sxs-lookup"><span data-stu-id="5348d-235">S</span></span>

<dl> <dt>

<span data-ttu-id="5348d-236">**REPOSITÓRIO**</span><span class="sxs-lookup"><span data-stu-id="5348d-236">**SEL**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-237">Consulte [*log de eventos do sistema (SEL)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-237">See [*System Event Log (SEL)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-238">**Adaptador SEL**</span><span class="sxs-lookup"><span data-stu-id="5348d-238">**SEL adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-239">O adaptador que envia dados do [*Controlador BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) para o [*coletor de eventos*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-239">The adapter that sends [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) data to the [*Event Collector*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-240">**seletor**</span><span class="sxs-lookup"><span data-stu-id="5348d-240">**selector**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-241">Um par de nome e valor que representa uma instância específica de um [*recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-241">A name and value pair that represents a particular instance of a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-242">Esse é essencialmente um filtro ou "chave" que identifica a instância desejada do recurso.</span><span class="sxs-lookup"><span data-stu-id="5348d-242">This is essentially a filter or "key" that identifies the desired instance of the resource.</span></span> <span data-ttu-id="5348d-243">O suporte ao seletor é encontrado no objeto [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5348d-243">Selector support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-244">**sensores**</span><span class="sxs-lookup"><span data-stu-id="5348d-244">**sensor**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-245">Um dispositivo de medição em um [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-245">A measurement device in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-246">**serviço**</span><span class="sxs-lookup"><span data-stu-id="5348d-246">**service**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-247">Um aplicativo que fornece serviços de gerenciamento para clientes por meio do protocolo WS-Management e outros [*Serviços Web*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-247">An application that provides management services to clients through the WS-Management protocol and other [*web services*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-248">Um serviço é geralmente o mesmo que o [*ouvinte*](windows-remote-management-glossary.md) em uma rede.</span><span class="sxs-lookup"><span data-stu-id="5348d-248">A service is usually the same as the [*listener*](windows-remote-management-glossary.md) on a network.</span></span> <span data-ttu-id="5348d-249">O serviço tem um endereço de transporte físico.</span><span class="sxs-lookup"><span data-stu-id="5348d-249">The service has a physical transport address.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-250">**sessão**</span><span class="sxs-lookup"><span data-stu-id="5348d-250">**session**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-251">Uma conexão entre um [*cliente*](windows-remote-management-glossary.md) gerenciamento remoto do Windows e o [*ouvinte*](windows-remote-management-glossary.md)ou serviço do WinRM local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="5348d-251">A connection between a Windows Remote Management [*client*](windows-remote-management-glossary.md) and the local or remote WinRM [*listener*](windows-remote-management-glossary.md), or service.</span></span> <span data-ttu-id="5348d-252">Essa conexão é semelhante à conexão entre um script de cliente WMI e o WMI em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="5348d-252">This connection is similar to the connection between a WMI client script and WMI on a remote server.</span></span> <span data-ttu-id="5348d-253">As operações de sessão, como a enumeração de um recurso (enumerar), a obtenção de uma instância de um recurso (Get) ou a execução de um método de recurso (Invoke) são métodos do objeto de **sessão** .</span><span class="sxs-lookup"><span data-stu-id="5348d-253">The session operations, such as enumerating a resource (Enumerate), getting an instance of a resource (Get), or running a resource method (Invoke) are methods of the **Session** object.</span></span> <span data-ttu-id="5348d-254">Um objeto de **sessão** é criado por [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-254">A **Session** object is created by [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-255">**Mecanismo de negociação GSS-API simples e protegido (SPNEGO)**</span><span class="sxs-lookup"><span data-stu-id="5348d-255">**Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-256">Um mecanismo de autenticação usado pelo cliente ou servidor que recebe solicitações de dados por meio do WinRM em um contexto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5348d-256">An authentication mechanism used by the client or server receiving requests for data through the WinRM in an Active Directory context.</span></span> <span data-ttu-id="5348d-257">O SPNEGO é baseado em um protocolo RFC (solicitação de comentários) produzido pela IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="5348d-257">SPNEGO is based on an Request For Comments (RFC) protocol produced by the Internet Engineering Task Force (IETF).</span></span> <span data-ttu-id="5348d-258">O SPNEGO também é conhecido como [*autenticação integrada do Windows*](windows-remote-management-glossary.md), o termo usado na gerenciamento remoto do Windows tópicos da ajuda.</span><span class="sxs-lookup"><span data-stu-id="5348d-258">SPNEGO is also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md), the term used in the Windows Remote Management help topics.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-259">**SOAP (Protocolo Simples de Acesso a Objetos)**</span><span class="sxs-lookup"><span data-stu-id="5348d-259">**Simple Object Access Protocol (SOAP)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-260">Um protocolo baseado em XML usado pelos serviços Web.</span><span class="sxs-lookup"><span data-stu-id="5348d-260">An XML-based protocol used by web services.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-261">**SOAP**</span><span class="sxs-lookup"><span data-stu-id="5348d-261">**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-262">Consulte [*protocolo SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-262">See [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-263">**SPNEGO**</span><span class="sxs-lookup"><span data-stu-id="5348d-263">**SPNEGO**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-264">Consulte [*mecanismo de negociação GSS-API simples e protegido (SPNEGO)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-264">See [*Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-265">**Registro de eventos do sistema (SEL)**</span><span class="sxs-lookup"><span data-stu-id="5348d-265">**System Event Log (SEL)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-266">O banco de dados de eventos no hardware do [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5348d-266">The database of events in the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) hardware.</span></span> <span data-ttu-id="5348d-267">O [*adaptador SEL*](windows-remote-management-glossary.md) transmite esses eventos para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5348d-267">The [*SEL adapter*](windows-remote-management-glossary.md) conveys these events to the operating system.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="5348d-268">U</span><span class="sxs-lookup"><span data-stu-id="5348d-268">U</span></span>

<dl> <dt>

<span data-ttu-id="5348d-269">**URI (Uniform Resource Identifier)**</span><span class="sxs-lookup"><span data-stu-id="5348d-269">**uniform resource identifier (URI)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-270">Uma cadeia de caracteres que identifica um recurso na empresa, como um computador, um processo, uma unidade de disco ou um sensor de temperatura em um [*Controlador BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-270">A string that identifies a resource in the enterprise, such as a computer, a process, a disk drive, or a temperature sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-271">O URI é o mecanismo de endereçamento do serviço Web definido na IETF (Internet Engineering Task Force) Uniform Resource Identifier (URI): sintaxe genérica \[ RFC3986 \] .</span><span class="sxs-lookup"><span data-stu-id="5348d-271">The URI is the web service addressing mechanism defined in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): Generic Syntax \[RFC3986\].</span></span>

</dd> <dt>

<span data-ttu-id="5348d-272">**URI**</span><span class="sxs-lookup"><span data-stu-id="5348d-272">**URI**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-273">Consulte [*Uniform Resource Identifier (URI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-273">See [*uniform resource identifier (URI)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="5348d-274">W</span><span class="sxs-lookup"><span data-stu-id="5348d-274">W</span></span>

<dl> <dt>

<span data-ttu-id="5348d-275">**serviço Web**</span><span class="sxs-lookup"><span data-stu-id="5348d-275">**web service**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-276">Um aplicativo de software usado para interação entre computadores na Internet ou em uma rede.</span><span class="sxs-lookup"><span data-stu-id="5348d-276">A software application used for interaction between computers across the Internet or a network.</span></span> <span data-ttu-id="5348d-277">Os serviços Web são descritos pelo [*WSDL (Web Service Description Language)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-277">Web services are described by the [*Web Service Description Language (WSDL)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-278">A descrição específica do serviço Web informa outros serviços como interagir com o serviço Web usando mensagens SOAP.</span><span class="sxs-lookup"><span data-stu-id="5348d-278">The specific description of the web service tells other services how to interact with the web service by using SOAP messages.</span></span> <span data-ttu-id="5348d-279">As mensagens são transmitidas entre computadores por um transporte, geralmente HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5348d-279">The messages are conveyed between computers by a transport, typically HTTP or HTTPS.</span></span> <span data-ttu-id="5348d-280">O [*WS-Addressing*](windows-remote-management-glossary.md), o [*WS-Eventing*](windows-remote-management-glossary.md)e o [*WS-Management*](windows-remote-management-glossary.md) são exemplos de protocolos usados por aplicativos de serviço Web para se comunicar entre si.</span><span class="sxs-lookup"><span data-stu-id="5348d-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md) are examples of protocols used by web service applications to communicate with each other.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-281">**WSDL (Web Service Description Language)**</span><span class="sxs-lookup"><span data-stu-id="5348d-281">**Web Service Description Language (WSDL)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-282">Uma linguagem baseada em XML usada para definir como interagir com um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="5348d-282">An XML-based language used to define how to interact with a web service.</span></span> <span data-ttu-id="5348d-283">Normalmente, o WSDL descreve quais mensagens SOAP o serviço Web requer para retornar dados ou executar operações.</span><span class="sxs-lookup"><span data-stu-id="5348d-283">Typically, the WSDL describes what SOAP messages the web service requires to return data or carry out operations.</span></span> <span data-ttu-id="5348d-284">O WSDL permite que uma implementação de um sistema operacional se comunique com o serviço Web implementado em outro sistema operacional, desde que os requisitos do WSDL sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="5348d-284">The WSDL allows an implementation from one operating system to communicate with the web service implemented on another operating system, as long as the requirements of the WSDL are met.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-285">**Autenticação Integrada do Windows**</span><span class="sxs-lookup"><span data-stu-id="5348d-285">**Windows Integrated Authentication**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-286">Consulte [*negociar autenticação*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-286">See [*Negotiate authentication*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-287">**WMI (Instrumentação de Gerenciamento do Windows)**</span><span class="sxs-lookup"><span data-stu-id="5348d-287">**Windows Management Instrumentation (WMI)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-288">A implementação da Microsoft do padrão Web-Based Enterprise Management (WBEM) publicado pela [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-288">The Microsoft implementation of the Web-Based Enterprise Management (WBEM) standard published by the [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5348d-289">O WMI permite que você gerencie computadores locais e remotos e os modelos de computador e rede usando uma extensão do padrão de [*modelo CIM (CIM)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="5348d-289">WMI allows you to manage local and remote computers and models computer and network objects using an extension of the [*Common Information Model (CIM)*](windows-remote-management-glossary.md) standard.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-290">**Gerenciamento Remoto do Windows (WinRM)**</span><span class="sxs-lookup"><span data-stu-id="5348d-290">**Windows Remote Management (WinRM)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-291">A implementação da Microsoft de um serviço Web de gerenciamento com base no protocolo [*WS-Management*](windows-remote-management-glossary.md) padrão público.</span><span class="sxs-lookup"><span data-stu-id="5348d-291">The Microsoft implementation of a management web service based on the public standard [*WS-Management*](windows-remote-management-glossary.md) protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-292">**Shell remoto do Windows (WinRS)**</span><span class="sxs-lookup"><span data-stu-id="5348d-292">**Windows Remote Shell (WinRS)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-293">Uma ferramenta de shell que se baseia em [*gerenciamento remoto do Windows*](windows-remote-management-glossary.md) executar comandos remotos, especialmente para servidores sem periféricos.</span><span class="sxs-lookup"><span data-stu-id="5348d-293">A shell tool that relies on [*Windows Remote Management*](windows-remote-management-glossary.md) to execute remote commands, especially for headless servers.</span></span> <span data-ttu-id="5348d-294">A ferramenta de linha de comando é winrs.</span><span class="sxs-lookup"><span data-stu-id="5348d-294">The command-line tool is Winrs.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-295">**WMI**</span><span class="sxs-lookup"><span data-stu-id="5348d-295">**WMI**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-296">Consulte [*Instrumentação de gerenciamento do Windows (WMI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-296">See [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="5348d-297">**Plug-in WMI**</span><span class="sxs-lookup"><span data-stu-id="5348d-297">**WMI plug-in**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-298">O plug-in do WinRM que disponibiliza dados do WMI para clientes WinRM.</span><span class="sxs-lookup"><span data-stu-id="5348d-298">The WinRM plug-in that makes WMI data available to WinRM clients.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-299">**WS-Addressing (WSA)**</span><span class="sxs-lookup"><span data-stu-id="5348d-299">**WS-Addressing (wsa)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-300">Um protocolo padrão público, que é baseado em SOAP, que cria um sistema de endereçamento usado nos cabeçalhos de mensagens enviadas pela Internet.</span><span class="sxs-lookup"><span data-stu-id="5348d-300">A public standard protocol, which is SOAP-based, that creates an addressing system used in the headers of messages sent across the Internet.</span></span> <span data-ttu-id="5348d-301">O padrão define como os recursos podem ser localizados em redes e firewalls.</span><span class="sxs-lookup"><span data-stu-id="5348d-301">The standard defines how resources can be located across networks and firewalls.</span></span> <span data-ttu-id="5348d-302">WS-Addressing é um dos protocolos de serviço Web que compõem o protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="5348d-302">WS-Addressing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-303">**WS-Enumeration (wsen)**</span><span class="sxs-lookup"><span data-stu-id="5348d-303">**WS-Enumeration (wsen)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-304">Um protocolo padrão público, que é baseado em SOAP, para enumerar uma sequência de elementos XML que pode representar coleções de dados, logs ou outras estruturas de informações lineares.</span><span class="sxs-lookup"><span data-stu-id="5348d-304">A public standard protocol, which is SOAP-based, for enumerating a sequence of XML elements that may represent data collections, logs, or other linear information structures.</span></span> <span data-ttu-id="5348d-305">WS-Enumeration é um dos protocolos de serviço Web que compõem o protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="5348d-305">WS-Enumeration is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-306">**WS-Eventing (WSE)**</span><span class="sxs-lookup"><span data-stu-id="5348d-306">**WS-Eventing (wse)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-307">Um protocolo padrão público, que é baseado em SOAP, que permite que um serviço Web (o assinante) assine e aceite mensagens de notificação de eventos de outro serviço Web (a origem do evento).</span><span class="sxs-lookup"><span data-stu-id="5348d-307">A public standard protocol, which is SOAP-based, that allows one web service (the subscriber) to subscribe to and accept event notification messages from another web service (the event source).</span></span> <span data-ttu-id="5348d-308">WS-Eventing é um dos protocolos de serviço Web que compõem o protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="5348d-308">WS-Eventing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-309">**WS-Management**</span><span class="sxs-lookup"><span data-stu-id="5348d-309">**WS-Management**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-310">Um protocolo padrão público, que é baseado em SOAP, para compartilhar dados de gerenciamento entre todos os sistemas operacionais, computadores e dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5348d-310">A public standard protocol, which is SOAP-based, for sharing management data among all operating systems, computers, and devices.</span></span> <span data-ttu-id="5348d-311">Todas as [*mensagens*](windows-remote-management-glossary.md) enviadas pelo cliente ou pelos componentes do servidor WinRM usam esse protocolo.</span><span class="sxs-lookup"><span data-stu-id="5348d-311">All [*messages*](windows-remote-management-glossary.md) sent by the WinRM client or server components use this protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5348d-312">**WS-Transfer (wxf)**</span><span class="sxs-lookup"><span data-stu-id="5348d-312">**WS-Transfer (wxf)**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-313">Um protocolo padrão público, que é baseado em SOAP, para acessar representações XML de recursos baseados em serviços da Web por meio de um conjunto simples de verbos, como Get, put, Invoke ou Delete.</span><span class="sxs-lookup"><span data-stu-id="5348d-313">A public standard protocol, which is SOAP-based, for accessing XML representations of web service-based resources through a simple set of verbs such as Get, Put, Invoke, or Delete.</span></span> <span data-ttu-id="5348d-314">WS-Transfer define as operações para enviar e receber a representação de um recurso específico e operações para criar ou excluir um recurso e sua representação correspondente.</span><span class="sxs-lookup"><span data-stu-id="5348d-314">WS-Transfer defines operations for sending and receiving the representation of a particular resource and operations for creating or deleting a resource and its corresponding representation.</span></span>

</dd> </dl>

## <a name="x"></a><span data-ttu-id="5348d-315">X</span><span class="sxs-lookup"><span data-stu-id="5348d-315">X</span></span>

<dl> <dt>

<span data-ttu-id="5348d-316">**XPath**</span><span class="sxs-lookup"><span data-stu-id="5348d-316">**XPath**</span></span>
</dt> <dd>

<span data-ttu-id="5348d-317">Uma notação de caminho para endereçar partes de um documento XML, semelhante a uma URL.</span><span class="sxs-lookup"><span data-stu-id="5348d-317">A path notation for addressing parts of an XML document, similar to a URL.</span></span> <span data-ttu-id="5348d-318">Uma expressão XPath é uma sequência de frases a serem obtidas do local atual no documento XML para outro nó ou conjunto de nós.</span><span class="sxs-lookup"><span data-stu-id="5348d-318">An XPath expression is a sequence of phrases to get from the current location in the XML document to another node or set of nodes.</span></span> <span data-ttu-id="5348d-319">As frases são separadas por caracteres de barra ("/").</span><span class="sxs-lookup"><span data-stu-id="5348d-319">The phrases are separated by forward-slash ("/") characters.</span></span> <span data-ttu-id="5348d-320">O serviço WinRM dá suporte a [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) para [*dialeto de fragmento*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5348d-320">The WinRM service supports [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) for [*fragment dialect*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

 

 