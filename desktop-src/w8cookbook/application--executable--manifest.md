---
title: Manifesto do aplicativo (executável)
description: Manifesto do aplicativo (executável)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008493"
---
# <a name="app-executable-manifest"></a><span data-ttu-id="7f75e-103">Manifesto do aplicativo (executável)</span><span class="sxs-lookup"><span data-stu-id="7f75e-103">App (executable) manifest</span></span>

## <a name="platforms"></a><span data-ttu-id="7f75e-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="7f75e-104">Platforms</span></span>

<span data-ttu-id="7f75e-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="7f75e-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="7f75e-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f75e-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="7f75e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f75e-107">Description</span></span>

<span data-ttu-id="7f75e-108">A seção de compatibilidade do manifesto do aplicativo (executável) introduzido no Windows ajuda o sistema operacional a determinar as versões do Windows que um aplicativo foi projetado para direcionar.</span><span class="sxs-lookup"><span data-stu-id="7f75e-108">The compatibility section of the app (executable) manifest introduced in Windows helps the operating system determine the versions of Windows an app was designed to target.</span></span> <span data-ttu-id="7f75e-109">Além disso, o manifesto do aplicativo permite que o Windows forneça o comportamento que o aplicativo espera com base na versão do Windows de destino do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7f75e-109">Additionally, the app manifest enables Windows to provide the behavior that the app expects based on the version of Windows that the app targeted.</span></span>

<span data-ttu-id="7f75e-110">A seção de compatibilidade do manifesto permite que o Windows forneça um novo comportamento ao software recém-criado, mantendo a compatibilidade com o software existente.</span><span class="sxs-lookup"><span data-stu-id="7f75e-110">The compatibility section of the manifest allows Windows to provide new behavior to newly created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="7f75e-111">Esta seção ajuda o Windows a fornecer maior compatibilidade em versões futuras do Windows também.</span><span class="sxs-lookup"><span data-stu-id="7f75e-111">This section helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="7f75e-112">Por exemplo, um aplicativo que declara suporte somente para o Windows 8 na seção de compatibilidade continuará a receber o comportamento do Windows 8 em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f75e-112">For example, an app declaring support for only Windows 8 in the compatibility section will continue to receive Windows 8 behavior in future versions of Windows.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7f75e-113">Manifestação</span><span class="sxs-lookup"><span data-stu-id="7f75e-113">Manifestation</span></span>

<span data-ttu-id="7f75e-114">Aplicativos sem uma seção de compatibilidade em seu manifesto terão o comportamento do Windows Vista por padrão no Windows 7 e no Windows 8 e em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="7f75e-114">Apps without a compatibility section in their manifest will have Windows Vista behavior by default on Windows 7 and Windows 8 and future Windows versions.</span></span> <span data-ttu-id="7f75e-115">Lembre-se de que o Windows XP e o Windows Vista ignoram essa seção de manifesto e não têm nenhum impacto sobre elas.</span><span class="sxs-lookup"><span data-stu-id="7f75e-115">Be aware that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="7f75e-116">Esses componentes do Windows fornecem comportamento divergente com base na seção de compatibilidade:</span><span class="sxs-lookup"><span data-stu-id="7f75e-116">These Windows components provide divergent behavior based on the compatibility section:</span></span>

<span data-ttu-id="7f75e-117">**Pool de threads padrão RPC (chamada de procedimento remoto)**</span><span class="sxs-lookup"><span data-stu-id="7f75e-117">**Remote procedure call (RPC) default thread pool**</span></span>

-   <span data-ttu-id="7f75e-118">Windows 8 e Windows 7: para melhorar a escalabilidade e reduzir as contagens de threads, o RPC alternou para o pool de threads do NT (pool padrão).</span><span class="sxs-lookup"><span data-stu-id="7f75e-118">Windows 8 and Windows 7: To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="7f75e-119">Para o Windows Vista, o RPC usou um pool de threads privado:</span><span class="sxs-lookup"><span data-stu-id="7f75e-119">For Windows Vista, RPC used a private thread pool:</span></span>

    -   <span data-ttu-id="7f75e-120">Para binários compilados para o Windows 7 e versões posteriores do Windows, o pool padrão é usado.</span><span class="sxs-lookup"><span data-stu-id="7f75e-120">For binaries compiled for Windows 7 and later versions of Windows, the default pool is used.</span></span>
    -   <span data-ttu-id="7f75e-121">Se I \_ RpcMgmtEnableDedicatedThreadPool for chamado antes de qualquer API RPC ser chamada, o pool de threads privado será usado (comportamento do vista).</span><span class="sxs-lookup"><span data-stu-id="7f75e-121">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior).</span></span>
    -   <span data-ttu-id="7f75e-122">Se eu \_ RpcMgmtEnableDedicatedThreadPool for chamado depois de uma chamada RPC, o pool padrão será usado, I \_ RpcMgmtEnableDedicatedThreadPool retornará o erro 1764 e não haverá suporte para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="7f75e-122">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported.</span></span>

-   <span data-ttu-id="7f75e-123">Windows Vista (padrão): para binários compilados para o Windows Vista e versões anteriores do Windows, o pool privado é usado.</span><span class="sxs-lookup"><span data-stu-id="7f75e-123">Windows Vista (default): For binaries compiled for Windows Vista and earlier versions of Windows, the private pool is used.</span></span>

<span data-ttu-id="7f75e-124">**Bloqueio do DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="7f75e-124">**DirectDraw lock**</span></span>

-   <span data-ttu-id="7f75e-125">Windows 8 e Windows 7: os aplicativos manifestados para o Windows 7 e versões posteriores do sistema operacional não podem chamar a API de bloqueio em DDRAW para bloquear o buffer de vídeo da área de trabalho principal; Isso resultará em um erro e será retornado um ponteiro nulo para o primário.</span><span class="sxs-lookup"><span data-stu-id="7f75e-125">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of the operating system cannot call Lock API in DDRAW to lock the primary desktop video buffer; doing so will result in an error, and a NULL pointer for the primary is returned.</span></span> <span data-ttu-id="7f75e-126">Esse comportamento é imposto mesmo se Gerenciador de Janelas da Área de Trabalho composição não estiver ativada.</span><span class="sxs-lookup"><span data-stu-id="7f75e-126">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="7f75e-127">Aplicativos com compatibilidade declarada para o Windows 7 e posterior não devem bloquear o buffer de vídeo primário para renderização.</span><span class="sxs-lookup"><span data-stu-id="7f75e-127">Apps with compatibility declared for Windows 7 and later must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="7f75e-128">Windows Vista (padrão): os aplicativos podem adquirir um bloqueio no buffer de vídeo primário, pois os aplicativos herdados dependem desse comportamento; a execução do aplicativo é desativada Gerenciador de Janelas da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="7f75e-128">Windows Vista (default): Apps can acquire a lock on the primary video buffer, as legacy apps depend on this behavior; running the app turns off Desktop Window Manager.</span></span>

<span data-ttu-id="7f75e-129">**BitBlt (transferência de bloco de bits) do DirectDraw para primário sem janela de recorte**</span><span class="sxs-lookup"><span data-stu-id="7f75e-129">**DirectDraw bit-block transfer (bitblt) to primary without clipping window**</span></span>

-   <span data-ttu-id="7f75e-130">Windows 8 e Windows 7: os aplicativos manifestados para o Windows 7 e versões posteriores do Windows são impedidos de executar um BitBlt para o buffer de vídeo da área de trabalho principal sem uma janela de recorte; Isso resulta em um erro e a área de BitBlt não será renderizada.</span><span class="sxs-lookup"><span data-stu-id="7f75e-130">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of Windows are prevented from performing a bitblt to the primary Desktop video buffer without a clipping window; doing so results in an error and the bitblt area will not be rendered.</span></span> <span data-ttu-id="7f75e-131">O Windows impõe esse comportamento mesmo se você não ativar Gerenciador de Janelas da Área de Trabalho composição.</span><span class="sxs-lookup"><span data-stu-id="7f75e-131">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="7f75e-132">Aplicativos com compatibilidade declarada para o Windows 7 e posterior devem executar um BitBlt em uma janela de recorte.</span><span class="sxs-lookup"><span data-stu-id="7f75e-132">Apps with compatibility declared for Windows 7 and later must perform a bitblt to a clipping window.</span></span>
-   <span data-ttu-id="7f75e-133">Windows Vista (padrão): os aplicativos devem ser capazes de executar um BitBlt para o primário sem uma janela de recorte, pois os aplicativos herdados dependem desse comportamento; a execução desse aplicativo desativa o Gerenciador de Janelas da Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="7f75e-133">Windows Vista (default): Apps must be able to perform a bitblt to the primary without a clipping window, as legacy apps depend on this behavior; running this app turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="7f75e-134">**API GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="7f75e-134">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="7f75e-135">Windows 8 e Windows 7: resolve uma condição de corrida em que um aplicativo multithread usando **GetOverlappedResult** pode retornar sem redefinir o evento na estrutura sobreposta, fazendo com que a próxima chamada para essa função seja retornada prematuramente.</span><span class="sxs-lookup"><span data-stu-id="7f75e-135">Windows 8 and Windows 7: Resolves a race condition where a multithreaded app using **GetOverlappedResult** can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="7f75e-136">Windows Vista (padrão): fornece o comportamento com a condição de corrida na qual os aplicativos podem ter uma dependência.</span><span class="sxs-lookup"><span data-stu-id="7f75e-136">Windows Vista (default): Provides the behavior with the race condition that apps might have a dependency on.</span></span> <span data-ttu-id="7f75e-137">Os aplicativos que devem evitar essa corrida antes do comportamento do Windows 7 devem aguardar no evento sobreposto e, quando sinalizado, chamar GetOverlappedResult com bWait = = FALSE.</span><span class="sxs-lookup"><span data-stu-id="7f75e-137">Apps that must avoid this race prior to the Windows 7 behavior should wait on the overlapped event and, when signaled, call GetOverlappedResult with bWait == FALSE.</span></span>

<span data-ttu-id="7f75e-138">**Status de temas do Shell no modo de alto contraste**</span><span class="sxs-lookup"><span data-stu-id="7f75e-138">**Shell themes status in high contrast mode**</span></span>

-   <span data-ttu-id="7f75e-139">Windows 8: retorna o status real de ti para quando estiver no modo de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="7f75e-139">Windows 8: Returns the real theming status for when in high contrast mode.</span></span>
-   <span data-ttu-id="7f75e-140">Windows 7: retorna-os como indisponíveis no modo de alto contraste porque o DWM ainda está ativado.</span><span class="sxs-lookup"><span data-stu-id="7f75e-140">Windows 7: Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>
-   <span data-ttu-id="7f75e-141">Windows Vista (padrão): retorna-os como indisponíveis no modo de alto contraste, pois o DWM ainda está ativado.</span><span class="sxs-lookup"><span data-stu-id="7f75e-141">Windows Vista (default): Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>

<span data-ttu-id="7f75e-142">**Método Shell iPersistFile:: Save**</span><span class="sxs-lookup"><span data-stu-id="7f75e-142">**Shell iPersistFile::Save method**</span></span>

-   <span data-ttu-id="7f75e-143">Windows 8: CShellLink:: Save agora determina se o manipulador IPersistFile é chamado com um argumento de caminho relativo e falha na chamada, se for.</span><span class="sxs-lookup"><span data-stu-id="7f75e-143">Windows 8: CShellLink::Save now determines if the IPersistFile handler is called with a relative path argument and fails the call if it is.</span></span>

    <span data-ttu-id="7f75e-144">A [documentação pública](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) que descreve esse comportamento indica que o argumento de caminho deve ser um caminho absoluto:</span><span class="sxs-lookup"><span data-stu-id="7f75e-144">The [public documentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) describing this behavior indicates that path argument has to be an absolute path:</span></span>

-   <span data-ttu-id="7f75e-145">Windows 7 e anterior (padrão): CShellLink:: Save não determina se o manipulador iPersistFile envia uma verificação de caminho relativa e permite que os aplicativos continuem trabalhando com caminhos absolutos ou relativos.</span><span class="sxs-lookup"><span data-stu-id="7f75e-145">Windows 7 and earlier (default): CShellLink::Save does not determine if the iPersistFile handler sends a relative path check and allows apps to continue working with absolute or relative paths.</span></span>

<span data-ttu-id="7f75e-146">**PCA (Assistente de compatibilidade do programa)**</span><span class="sxs-lookup"><span data-stu-id="7f75e-146">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="7f75e-147">Windows 8: os aplicativos com a seção de compatibilidade não obtêm a mitigação do PCA.</span><span class="sxs-lookup"><span data-stu-id="7f75e-147">Windows 8: Apps with the compatibility section do not get the PCA mitigation.</span></span>
-   <span data-ttu-id="7f75e-148">Windows 7: os aplicativos com a seção de compatibilidade são acompanhados para possíveis problemas de compatibilidade com as alterações do Windows 8 (descritas neste documento).</span><span class="sxs-lookup"><span data-stu-id="7f75e-148">Windows 7: Apps with the compatibility section are tracked for potential compatibility issues for Windows 8 changes (described in this document).</span></span>
-   <span data-ttu-id="7f75e-149">Windows Vista (padrão): aplicativos que não são instalados corretamente ou falham durante o tempo de execução em algumas circunstâncias específicas obtêm a mitigação do PCA.</span><span class="sxs-lookup"><span data-stu-id="7f75e-149">Windows Vista (default): Apps that fail to install properly or crash during runtime under some specific circumstances get the PCA mitigation.</span></span> <span data-ttu-id="7f75e-150">Para obter mais informações, consulte a seção recursos.</span><span class="sxs-lookup"><span data-stu-id="7f75e-150">For more info, see the Resources section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="7f75e-151">Aproveitando os recursos do recurso</span><span class="sxs-lookup"><span data-stu-id="7f75e-151">Leveraging feature capabilities</span></span>

<span data-ttu-id="7f75e-152">Atualize o manifesto do aplicativo com as informações de compatibilidade mais recentes para o suporte do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7f75e-152">Update the app manifest with the latest compatibility info for operating system support.</span></span> <span data-ttu-id="7f75e-153">Esta seção descreve as adições ao manifesto:</span><span class="sxs-lookup"><span data-stu-id="7f75e-153">This section describes the additions to the manifest:</span></span>

<span data-ttu-id="7f75e-154">**Namespace:** Compatibility. v1 (xmlns = "urn: schemas-microsoft-com: Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="7f75e-154">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

<span data-ttu-id="7f75e-155">**Nome da seção:** Compatibilidade (nova seção)</span><span class="sxs-lookup"><span data-stu-id="7f75e-155">**Section name:** Compatibility (new section)</span></span>

<span data-ttu-id="7f75e-156">**SupportedOS:** GUID do sistema operacional com suporte-os GUIDs que mapeiam para os sistemas operacionais com suporte são:</span><span class="sxs-lookup"><span data-stu-id="7f75e-156">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

-   <span data-ttu-id="7f75e-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="7f75e-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span>

    <span data-ttu-id="7f75e-158">para o **Windows Vista**: esse é o valor padrão para o contexto Switchback</span><span class="sxs-lookup"><span data-stu-id="7f75e-158">for **Windows Vista**: This is the default value for the switchback context</span></span>

-   <span data-ttu-id="7f75e-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="7f75e-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span>

    <span data-ttu-id="7f75e-160">para o **Windows 7**: os aplicativos que definem esse valor no manifesto do aplicativo obtêm o comportamento do Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f75e-160">for **Windows 7**: Apps that set this value in the app manifest get the Windows 7 behavior</span></span>

-   <span data-ttu-id="7f75e-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="7f75e-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span>

    <span data-ttu-id="7f75e-162">para o **Windows 8**: os aplicativos que definem esse valor no manifesto do aplicativo obtêm o comportamento do Windows 8</span><span class="sxs-lookup"><span data-stu-id="7f75e-162">for **Windows 8**: Apps that set this value in the application manifest get the Windows 8 behavior</span></span>

<span data-ttu-id="7f75e-163">A Microsoft irá gerar e lançar GUIDs para versões futuras do Windows, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7f75e-163">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

<span data-ttu-id="7f75e-164">Um exemplo de XML de um manifesto atualizado:</span><span class="sxs-lookup"><span data-stu-id="7f75e-164">An XML example of an updated manifest:</span></span>

> [!Note]  
> <span data-ttu-id="7f75e-165">O atributo e os nomes de marca no manifesto do aplicativo diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7f75e-165">The attribute and tag names in the app manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



<span data-ttu-id="7f75e-166">Os GUIDs para todos os sistemas operacionais no exemplo anterior fornecem suporte de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="7f75e-166">The GUIDs for all the operating systems in the previous example provide down-level support.</span></span> <span data-ttu-id="7f75e-167">Os aplicativos que dão suporte a várias plataformas não precisam de manifestos separados para cada plataforma.</span><span class="sxs-lookup"><span data-stu-id="7f75e-167">Apps that support multiple platforms do not need separate manifests for each platform.</span></span>

## <a name="tests"></a><span data-ttu-id="7f75e-168">Testes</span><span class="sxs-lookup"><span data-stu-id="7f75e-168">Tests</span></span>

<span data-ttu-id="7f75e-169">Um aplicativo pode especificar várias IDs de sistema operacional com suporte.</span><span class="sxs-lookup"><span data-stu-id="7f75e-169">An app can specify multiple supported operating system IDs.</span></span> <span data-ttu-id="7f75e-170">Você deve adicionar uma ID do sistema operacional com suporte se tiver testado ou estiver no processo de teste, o aplicativo nesse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7f75e-170">You should add a supported operating system ID if you have tested, or are in the process of testing, the app on that operating system.</span></span> <span data-ttu-id="7f75e-171">O Windows Vista e versões anteriores do sistema operacional não preste atenção a essas entradas.</span><span class="sxs-lookup"><span data-stu-id="7f75e-171">Windows Vista and prior operating system versions do not pay attention to these entries.</span></span> <span data-ttu-id="7f75e-172">A partir do Windows 7, o Windows escolherá o GUID de versão mais alto no manifesto até a versão do Windows em execução e dará ao aplicativo o suporte nesse nível.</span><span class="sxs-lookup"><span data-stu-id="7f75e-172">Starting with Windows 7, Windows will choose the highest version GUID in the manifest up to the running Windows version, and give the app support at that level.</span></span> <span data-ttu-id="7f75e-173">Para verificar se o aplicativo funciona com a nova seção de compatibilidade de manifesto de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="7f75e-173">To verify that the app works with the new app manifest compatibility section:</span></span>

1.  <span data-ttu-id="7f75e-174">Teste o aplicativo com a nova seção de compatibilidade e SupportedOS ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} para garantir que o aplicativo funcione corretamente usando o comportamento mais recente do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f75e-174">Test the app with the new compatibility section and SupportedOS ID = { 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} to ensure that the app works properly using the latest Windows 8 behavior.</span></span>
2.  <span data-ttu-id="7f75e-175">Teste o aplicativo com a nova seção de compatibilidade e SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para garantir que o aplicativo funcione corretamente usando o comportamento do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7f75e-175">Test the app with the new compatibility section and SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} to ensure that the app works properly using the Windows 7 behavior.</span></span>
3.  <span data-ttu-id="7f75e-176">Teste o aplicativo com a nova seção de compatibilidade e SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} para garantir que o aplicativo funcione corretamente usando o comportamento do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7f75e-176">Test the app with the new compatibility section and SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} to ensure that the app works properly using the Windows Vista behavior.</span></span>

## <a name="resources"></a><span data-ttu-id="7f75e-177">Recursos</span><span class="sxs-lookup"><span data-stu-id="7f75e-177">Resources</span></span>

-   [<span data-ttu-id="7f75e-178">Função QueryActCtxW</span><span class="sxs-lookup"><span data-stu-id="7f75e-178">QueryActCtxW Function</span></span>](../sbscs/application-manifests.md)
-   <span data-ttu-id="7f75e-179">[Manifesto do UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7f75e-179">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="7f75e-180">Manifestos de aplicativo para aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="7f75e-180">Application Manifests for Windows Applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="7f75e-181">Gerenciador de Janelas da Área de Trabalho (DWM)</span><span class="sxs-lookup"><span data-stu-id="7f75e-181">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="7f75e-182">Atualização de incompatibilidade de contexto</span><span class="sxs-lookup"><span data-stu-id="7f75e-182">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)
-   <span data-ttu-id="7f75e-183">[Assistente de compatibilidade de programa](/previous-versions/bb756937(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7f75e-183">[Program Compatibility Assistant](/previous-versions/bb756937(v=msdn.10))</span></span>

 

 