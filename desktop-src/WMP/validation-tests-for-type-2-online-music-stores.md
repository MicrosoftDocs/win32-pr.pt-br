---
title: Testes de validação para armazenamentos online do tipo 2 de integração
description: Este tópico descreve os testes que a Microsoft executará para validar sua loja online do tipo 2. A Microsoft requer que você execute esses testes antes de enviar uma versão Release Candidate. Seu repositório online deve passar com êxito esses testes para serem publicados.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Lojas online do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364051"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a><span data-ttu-id="eb3f7-106">Testes de validação para armazenamentos online do tipo 2 de integração</span><span class="sxs-lookup"><span data-stu-id="eb3f7-106">Validation Tests for On-boarding Type 2 Online Stores</span></span>

<span data-ttu-id="eb3f7-107">Este tópico descreve os testes que a Microsoft executará para validar sua loja online do tipo 2.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-107">This topic describes tests that Microsoft will perform to validate your Type 2 online store.</span></span> <span data-ttu-id="eb3f7-108">A Microsoft requer que você execute esses testes antes de enviar uma versão Release Candidate.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-108">Microsoft requires that you run these tests before you submit a release candidate.</span></span> <span data-ttu-id="eb3f7-109">Seu repositório online deve passar com êxito esses testes para serem publicados.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-109">Your online store must successfully pass these tests to be published.</span></span>

> [!Note]  
> <span data-ttu-id="eb3f7-110">Se seu repositório for do tipo 1 em vez de tipo 2, você poderá usar este tópico como uma diretriz para entender o escopo do teste de certificação que é coberto para armazenamentos do tipo 1.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-110">If your store is Type 1 rather than Type 2, you can use this topic as a guideline to understand the scope of the certification testing that is covered for Type 1 stores.</span></span> <span data-ttu-id="eb3f7-111">Para obter o conjunto completo de testes para repositórios do tipo 1, entre em contato com [suporte da Microsoft](https://support.microsoft.com/ph/7763#tab0).</span><span class="sxs-lookup"><span data-stu-id="eb3f7-111">For the complete set of tests for Type 1 stores, contact [Microsoft Support](https://support.microsoft.com/ph/7763#tab0).</span></span>

 

<span data-ttu-id="eb3f7-112">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-112">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eb3f7-113">Lista de verificação de teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-113">Test Checklist</span></span>](#test-checklist)
    -   [<span data-ttu-id="eb3f7-114">Preparação de aprovação de teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-114">Test Pass Preparation</span></span>](#test-pass-preparation)
-   [<span data-ttu-id="eb3f7-115">Ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-115">Test Environment</span></span>](#test-environment)
-   [<span data-ttu-id="eb3f7-116">Configuração</span><span class="sxs-lookup"><span data-stu-id="eb3f7-116">Configuration and Setup</span></span>](#configuration-and-setup)
    -   [<span data-ttu-id="eb3f7-117">Configurando um computador de teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-117">Setting Up a Test Machine</span></span>](#setting-up-a-test-machine)
    -   [<span data-ttu-id="eb3f7-118">Configurando um repositório</span><span class="sxs-lookup"><span data-stu-id="eb3f7-118">Setting Up a Store</span></span>](#setting-up-a-store)
    -   [<span data-ttu-id="eb3f7-119">Criando uma conta</span><span class="sxs-lookup"><span data-stu-id="eb3f7-119">Creating an Account</span></span>](#creating-an-account)
    -   [<span data-ttu-id="eb3f7-120">Configurando o cache de credenciais</span><span class="sxs-lookup"><span data-stu-id="eb3f7-120">Setting Up Credential Caching</span></span>](#setting-up-credential-caching)
-   [<span data-ttu-id="eb3f7-121">Aquisição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-121">Content Acquisition</span></span>](#content-acquisition)
    -   [<span data-ttu-id="eb3f7-122">Conteúdo de streaming</span><span class="sxs-lookup"><span data-stu-id="eb3f7-122">Streaming Content</span></span>](#streaming-content)
    -   [<span data-ttu-id="eb3f7-123">Obtendo conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-123">Obtaining Content</span></span>](#obtaining-content)
    -   [<span data-ttu-id="eb3f7-124">Gravando conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-124">Burning Content</span></span>](#burning-content)
    -   [<span data-ttu-id="eb3f7-125">Transferindo conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-125">Transferring Content</span></span>](#transferring-content)
-   [<span data-ttu-id="eb3f7-126">Armazenar recursos</span><span class="sxs-lookup"><span data-stu-id="eb3f7-126">Store Features</span></span>](#store-features)
    -   [<span data-ttu-id="eb3f7-127">Gerenciando uma conta</span><span class="sxs-lookup"><span data-stu-id="eb3f7-127">Managing an Account</span></span>](#managing-an-account)
    -   [<span data-ttu-id="eb3f7-128">Gerenciando o centro de informações</span><span class="sxs-lookup"><span data-stu-id="eb3f7-128">Managing the Info Center</span></span>](#managing-the-info-center)
-   [<span data-ttu-id="eb3f7-129">Interação de armazenamento</span><span class="sxs-lookup"><span data-stu-id="eb3f7-129">Store Interaction</span></span>](#store-interaction)
    -   [<span data-ttu-id="eb3f7-130">Gerando para o repositório ativo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-130">Yielding to the Active Store</span></span>](#yielding-to-the-active-store)
    -   [<span data-ttu-id="eb3f7-131">Impedir que o armazenamento testado assuma o armazenamento ativo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-131">Preventing the Tested Store From Taking Over the Active Store</span></span>](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [<span data-ttu-id="eb3f7-132">Acessando um repositório no modo de High-Contrast</span><span class="sxs-lookup"><span data-stu-id="eb3f7-132">Accessing a Store in High-Contrast Mode</span></span>](#accessing-a-store-in-high-contrast-mode)
    -   [<span data-ttu-id="eb3f7-133">Protegendo uma loja</span><span class="sxs-lookup"><span data-stu-id="eb3f7-133">Securing a Store</span></span>](#securing-a-store)

## <a name="test-checklist"></a><span data-ttu-id="eb3f7-134">Lista de verificação de teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-134">Test Checklist</span></span>

<span data-ttu-id="eb3f7-135">Use a lista de verificação na tabela a seguir para validar sua loja online do tipo 2 que você deseja colocar no painel.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-135">Use the checklist in the following table to validate your Type 2 online store that you wish to bring on board.</span></span>



<span data-ttu-id="eb3f7-136">Teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-136">Test</span></span>

<span data-ttu-id="eb3f7-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb3f7-137">Windows XP</span></span>

<span data-ttu-id="eb3f7-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb3f7-138">Windows Vista</span></span>

<span data-ttu-id="eb3f7-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb3f7-139">Windows 7</span></span>

<span data-ttu-id="eb3f7-140">Resultado (aprovado/reprovado/não aplicável)</span><span class="sxs-lookup"><span data-stu-id="eb3f7-140">Result (pass/fail/not applicable)</span></span>

<span data-ttu-id="eb3f7-141">32</span><span class="sxs-lookup"><span data-stu-id="eb3f7-141">32</span></span>

<span data-ttu-id="eb3f7-142">64</span><span class="sxs-lookup"><span data-stu-id="eb3f7-142">64</span></span>

<span data-ttu-id="eb3f7-143">32</span><span class="sxs-lookup"><span data-stu-id="eb3f7-143">32</span></span>

<span data-ttu-id="eb3f7-144">64</span><span class="sxs-lookup"><span data-stu-id="eb3f7-144">64</span></span>

<span data-ttu-id="eb3f7-145">32</span><span class="sxs-lookup"><span data-stu-id="eb3f7-145">32</span></span>

<span data-ttu-id="eb3f7-146">64</span><span class="sxs-lookup"><span data-stu-id="eb3f7-146">64</span></span>

1. <span data-ttu-id="eb3f7-147">Verifique se o software é instalado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-147">Verify that software installs.</span></span>

2. <span data-ttu-id="eb3f7-148">Verifique se o software é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-148">Verify that software uninstalls.</span></span>

3. <span data-ttu-id="eb3f7-149">Verifique se o software não é executado na bandeja.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-149">Verify that software does not run in the tray.</span></span>

4. <span data-ttu-id="eb3f7-150">Verifique se a guia loja Opera.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-150">Verify that the store tab operates.</span></span>

5. <span data-ttu-id="eb3f7-151">Verifique se o repositório tem uma opção para criar uma nova conta.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-151">Verify that the store has an option to create a new account.</span></span>

6. <span data-ttu-id="eb3f7-152">Verifique se a conta criada pode entrar.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-152">Verify that the created account can sign in.</span></span>

7. <span data-ttu-id="eb3f7-153">Verifique se o repositório tem uma opção para salvar as informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-153">Verify that the store has an option to save user information.</span></span>

8. <span data-ttu-id="eb3f7-154">Verifique se o cache de credenciais está presente e funcionando.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-154">Verify that credential caching is present and working.</span></span>

9. <span data-ttu-id="eb3f7-155">Verifique se as credenciais do usuário são solicitadas se elas não estiverem armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-155">Verify that the user is prompted for credentials if they are not cached.</span></span>

10. <span data-ttu-id="eb3f7-156">Verifique se todos os tipos de fluxo de conteúdo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-156">Verify that all available types of content stream.</span></span>

11. <span data-ttu-id="eb3f7-157">Verifique se o conteúdo é reproduzido no Microsoft Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-157">Verify that content plays in Microsoft Windows Media Player.</span></span>

12. <span data-ttu-id="eb3f7-158">Verifique se um preço calculado está correto.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-158">Verify that a calculated price is correct.</span></span>

13. <span data-ttu-id="eb3f7-159">Verifique se o conteúdo comprado foi baixado para a biblioteca.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-159">Verify that purchased content is downloaded to the library.</span></span>

14. <span data-ttu-id="eb3f7-160">Verifique se os metadados são baixados para a compra.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-160">Verify that metadata is downloaded for the purchase.</span></span>

15. <span data-ttu-id="eb3f7-161">Verifique se os direitos de uso de mídia estão corretos para a compra.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-161">Verify that media usage rights are correct for the purchase.</span></span>

16. <span data-ttu-id="eb3f7-162">Verifique se o conteúdo comprado pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-162">Verify that the purchased content can play.</span></span>

17. <span data-ttu-id="eb3f7-163">Verifique se clicar no botão **comprar** ou **comprar** alterna para o repositório.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-163">Verify that clicking the **Buy** or **Shop** button switches to the store.</span></span>

18. <span data-ttu-id="eb3f7-164">Verifique se o conteúdo comprado foi baixado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-164">Verify that purchased content downloaded.</span></span>

19. <span data-ttu-id="eb3f7-165">Verifique se o conteúdo comprado pode ser gravado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-165">Verify that purchased content can be burned.</span></span>

20. <span data-ttu-id="eb3f7-166">Verifique se a contagem de gravação foi decrementada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-166">Verify that the burn count is decremented.</span></span>

21. <span data-ttu-id="eb3f7-167">Verifique se o conteúdo pode ser transferido para outro computador.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-167">Verify that content can be transferred to another computer.</span></span>

22. <span data-ttu-id="eb3f7-168">Verifique se o conteúdo é transferido para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-168">Verify that content transfers to a device.</span></span>

23. <span data-ttu-id="eb3f7-169">Verifique se a contagem de sincronização foi decrementada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-169">Verify that the sync count is decremented.</span></span>

24. <span data-ttu-id="eb3f7-170">Verifique se o histórico de compras acompanha as compras anteriores.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-170">Verify that the purchase history tracks prior purchases.</span></span>

25. <span data-ttu-id="eb3f7-171">Verifique se uma compra anterior pode ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-171">Verify that a prior purchase can be restored.</span></span>

26. <span data-ttu-id="eb3f7-172">Verifique a funcionalidade de um repositório para gerenciar vários computadores.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-172">Verify a store's functionality to manage multiple computers.</span></span>

27. <span data-ttu-id="eb3f7-173">Verifique se o centro de informações está desativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-173">Verify that the Info Center is off by default.</span></span>

28. <span data-ttu-id="eb3f7-174">Verifique se o centro de informações tem informações de mídia na área de execução.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-174">Verify that the Info Center has media information in the now-playing area.</span></span>

29. <span data-ttu-id="eb3f7-175">Verifique se os links navegam para a loja.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-175">Verify that links navigate to the store.</span></span>

30. <span data-ttu-id="eb3f7-176">Verifique se o armazenamento testado resulta no repositório ativo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-176">Verify that the tested store yields to the active store.</span></span>

31. <span data-ttu-id="eb3f7-177">Verifique se o repositório testado não assume o armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-177">Verify that the tested store does not take over the current store.</span></span>

32. <span data-ttu-id="eb3f7-178">Verifique se o repositório está acessível no modo de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-178">Verify that the store is accessible in high-contrast mode.</span></span>

33. <span data-ttu-id="eb3f7-179">Verifique se o repositório é seguro.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-179">Verify that the store is secure.</span></span>



 

### <a name="test-pass-preparation"></a><span data-ttu-id="eb3f7-180">Preparação de aprovação de teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-180">Test Pass Preparation</span></span>

<span data-ttu-id="eb3f7-181">Antes de executar uma aprovação de teste, você deve garantir que a loja e as contas de teste estejam prontas para teste.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-181">Before you run a test pass, you should ensure that the store and the test accounts are ready for testing.</span></span> <span data-ttu-id="eb3f7-182">Você deve determinar as seguintes informações antes que a passagem seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-182">You should determine the following information before the pass starts.</span></span> <span data-ttu-id="eb3f7-183">Se você puder determinar as informações de alguns dias antes da aprovação do teste, a passagem será executada com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-183">If you can determine the information some days in advance of the test pass, the pass will run more efficiently.</span></span>

-   <span data-ttu-id="eb3f7-184">Determine as seguintes informações sobre as contas de teste que são fornecidas pela loja:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-184">Determine the following information about test accounts that are supplied by the store:</span></span>
    -   <span data-ttu-id="eb3f7-185">Contas e senhas funcionam para permitir que um usuário entre</span><span class="sxs-lookup"><span data-stu-id="eb3f7-185">Accounts and passwords work to allow a user to sign in</span></span>
    -   <span data-ttu-id="eb3f7-186">As contas são financiadas corretamente e adequadamente para cada tipo de modo de negócios que a loja oferece</span><span class="sxs-lookup"><span data-stu-id="eb3f7-186">Accounts are correctly and adequately funded for each type of business mode the store offers</span></span>
    -   <span data-ttu-id="eb3f7-187">As contas são válidas para que todas as localidades sejam testadas ou as contas existem para cada localidade se as contas não podem cruzar as localidades</span><span class="sxs-lookup"><span data-stu-id="eb3f7-187">Accounts are valid for all locales to be tested, or accounts exist for each locale if accounts cannot cross locales</span></span>
-   <span data-ttu-id="eb3f7-188">Determine quais localidades testar.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-188">Determine which locales to test.</span></span>
-   <span data-ttu-id="eb3f7-189">Determine quais idiomas testar.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-189">Determine which languages to test.</span></span>
-   <span data-ttu-id="eb3f7-190">Determine as seguintes informações sobre o ambiente de teste:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-190">Determine the following information about the test environment:</span></span>

    -   <span data-ttu-id="eb3f7-191">Lojas ao vivo que funcionam com o Windows XP, o Windows Vista e o Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb3f7-191">Live stores that work with Windows XP, Windows Vista, and Windows 7</span></span>
    -   <span data-ttu-id="eb3f7-192">A loja não dinâmica a ser testada</span><span class="sxs-lookup"><span data-stu-id="eb3f7-192">The non-live store to test</span></span>
    -   <span data-ttu-id="eb3f7-193">Verifique se a loja não dinâmica a ser testada está visível em todas as versões do sistema operacional e todas as versões da plataforma Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-193">Verify that the non-live store to test is visible in all versions of the operating system and all versions of the Windows Media Player platform.</span></span>

-   <span data-ttu-id="eb3f7-194">Determine as seguintes informações sobre a loja a ser testada:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-194">Determine the following information about the store to test:</span></span>

    -   <span data-ttu-id="eb3f7-195">Nome do repositório</span><span class="sxs-lookup"><span data-stu-id="eb3f7-195">Store name</span></span>
    -   <span data-ttu-id="eb3f7-196">Elemento gráfico e rótulo do logotipo da guia de armazenamento esperado</span><span class="sxs-lookup"><span data-stu-id="eb3f7-196">Expected store tab logo graphics and label</span></span>
    -   <span data-ttu-id="eb3f7-197">O armazenamento reside para todas as versões do sistema operacional?</span><span class="sxs-lookup"><span data-stu-id="eb3f7-197">Is the store live for all operating system versions?</span></span>
    -   <span data-ttu-id="eb3f7-198">Esta é uma nova versão do Store em teste?</span><span class="sxs-lookup"><span data-stu-id="eb3f7-198">Is this is a new version of the store under test?</span></span>
    -   <span data-ttu-id="eb3f7-199">O repositório está sendo testado em um armazenamento tipo 1 ou tipo 2?</span><span class="sxs-lookup"><span data-stu-id="eb3f7-199">Is the store under test a Type 1 or Type 2 store?</span></span>
    -   <span data-ttu-id="eb3f7-200">O tipo de loja foi alterado?</span><span class="sxs-lookup"><span data-stu-id="eb3f7-200">Has the store type changed?</span></span>

-   <span data-ttu-id="eb3f7-201">Determine em quais versões e plataformas do sistema operacional você planeja testar o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-201">Determine on which operating system versions and platforms you plan to test the store.</span></span>
-   <span data-ttu-id="eb3f7-202">Determine se o instalador e o plug-in funcionam em todas as versões de sistema operacional e plataformas a serem testadas.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-202">Determine that the installer and plug-in works on all operating system versions and platforms to be tested.</span></span>
-   <span data-ttu-id="eb3f7-203">Determine se um documento de navegação é necessário.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-203">Determine if a navigation document is required.</span></span>
-   <span data-ttu-id="eb3f7-204">Determine as seguintes informações sobre a mídia que a loja oferece:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-204">Determine the following information about the media that the store offers:</span></span>

    -   <span data-ttu-id="eb3f7-205">Formatos</span><span class="sxs-lookup"><span data-stu-id="eb3f7-205">Formats</span></span>
    -   <span data-ttu-id="eb3f7-206">Algum software proprietário é necessário?</span><span class="sxs-lookup"><span data-stu-id="eb3f7-206">Is any proprietary software required?</span></span>
    -   <span data-ttu-id="eb3f7-207">Você deve testar todos os tipos de mídia ou apenas um subconjunto de tipos de mídia?</span><span class="sxs-lookup"><span data-stu-id="eb3f7-207">Must you test all media types, or only a subset of media types?</span></span>

-   <span data-ttu-id="eb3f7-208">Determine as seguintes informações sobre os direitos de uso de mídia:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-208">Determine the following information about media usage rights:</span></span>

    -   <span data-ttu-id="eb3f7-209">A mídia de armazenamento tem proteção de conteúdo?</span><span class="sxs-lookup"><span data-stu-id="eb3f7-209">Does the store media have content protection?</span></span>
    -   <span data-ttu-id="eb3f7-210">Nesse caso, determine o tipo de proteção de conteúdo que a mídia tem.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-210">If so, determine the type of content protection that the media have.</span></span>
    -   <span data-ttu-id="eb3f7-211">Nesse caso, determine o comportamento protegido esperado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-211">If so, determine the expected protected behavior.</span></span>
    -   <span data-ttu-id="eb3f7-212">Os direitos de uso de mídia incluem compartilhamento de computador para computador?</span><span class="sxs-lookup"><span data-stu-id="eb3f7-212">Do the media usage rights include computer-to-computer sharing?</span></span>
    -   <span data-ttu-id="eb3f7-213">Os direitos de sincronização</span><span class="sxs-lookup"><span data-stu-id="eb3f7-213">The sync rights</span></span>
    -   <span data-ttu-id="eb3f7-214">Os direitos de gravação</span><span class="sxs-lookup"><span data-stu-id="eb3f7-214">The burn rights</span></span>
    -   <span data-ttu-id="eb3f7-215">Os direitos de reprodução</span><span class="sxs-lookup"><span data-stu-id="eb3f7-215">The play rights</span></span>
    -   <span data-ttu-id="eb3f7-216">As datas de expiração, se houver</span><span class="sxs-lookup"><span data-stu-id="eb3f7-216">The expiration dates, if any</span></span>

-   <span data-ttu-id="eb3f7-217">Determine se você tem mídia suficiente (um catálogo grande o suficiente) para fornecer um exemplo significativo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-217">Determine if you have sufficient media (a large enough catalog) to provide a meaningful sample.</span></span>
-   <span data-ttu-id="eb3f7-218">Determine qual é a passagem de estágio: RC 0, Compliance e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-218">Determine what the stage pass is: RC 0, compliance, and so on.</span></span>
-   <span data-ttu-id="eb3f7-219">Determine se a aprovação de teste é um tipo específico: regressão, fumaça e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-219">Determine if the test pass is a certain type: regression, smoke, and so on.</span></span>

## <a name="test-environment"></a><span data-ttu-id="eb3f7-220">Ambiente de Teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-220">Test Environment</span></span>

<span data-ttu-id="eb3f7-221">Você deve realizar testes nas seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-221">You must conduct testing on the following configurations:</span></span>

-   <span data-ttu-id="eb3f7-222">Microsoft Windows Media Player 11 no Windows XP com Service Pack 3 (SP3) 32 bits e sistemas operacionais de 64 bits</span><span class="sxs-lookup"><span data-stu-id="eb3f7-222">Microsoft Windows Media Player 11 on Windows XP with Service Pack 3 (SP3) 32-bit and 64-bit operating systems</span></span>
-   <span data-ttu-id="eb3f7-223">Sistemas operacionais Windows Media Player 11 no Windows Vista 32 bits e 64 bits (32 bits Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="eb3f7-223">Windows Media Player 11 on Windows Vista 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>
-   <span data-ttu-id="eb3f7-224">Sistemas operacionais Microsoft Windows Media Player 12 no Windows 7 32-bit e 64-bit (32-bit Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="eb3f7-224">Microsoft Windows Media Player 12 on Windows 7 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>

<span data-ttu-id="eb3f7-225">Embora seja necessário executar testes em todas as versões de sistema operacional e plataformas listadas, as versões de 32 bits do Windows Vista e do Windows 7 são as versões de sistema operacional de prioridade.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-225">Although you must perform testing on all the operating system versions and platforms listed, 32-bit versions of Windows Vista and Windows 7 are the priority targeted operating system versions.</span></span> <span data-ttu-id="eb3f7-226">Você deve testar a instalação de qualquer software em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-226">You must test the installation of any software on all platforms.</span></span>

<span data-ttu-id="eb3f7-227">Capturas de tela neste tópico usam um repositório fictício, Proseware, para demonstrar o uso da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-227">Screen shots in this topic use a fictitious store, Proseware, to demonstrate the usage of the user interface.</span></span>

## <a name="configuration-and-setup"></a><span data-ttu-id="eb3f7-228">Configuração e instalação</span><span class="sxs-lookup"><span data-stu-id="eb3f7-228">Configuration and Setup</span></span>

<span data-ttu-id="eb3f7-229">As seções a seguir descrevem como configurar e configurar o teste de validação para o on-board a tipo 2 loja online.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-229">The following sections describe how to configure and set up validation testing to on-board a Type 2 online store.</span></span>

### <a name="setting-up-a-test-machine"></a><span data-ttu-id="eb3f7-230">Configurando um computador de teste</span><span class="sxs-lookup"><span data-stu-id="eb3f7-230">Setting Up a Test Machine</span></span>

<span data-ttu-id="eb3f7-231">Execute as seguintes etapas para configurar um computador de teste:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-231">Perform the following steps to set up a test machine:</span></span>

1.  <span data-ttu-id="eb3f7-232">Aponte o computador de teste para os servidores de teste de conteúdo adicionando uma chave do Registro específica do repositório.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-232">Point the test computer to content test servers by adding a store-specific registry key.</span></span>
2.  <span data-ttu-id="eb3f7-233">Defina valores na caixa de diálogo **Opções regionais e de idioma** para as configurações adequadas de idioma e localidade.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-233">Set values in the **Regional and Language Options** dialog box to the proper language and locale settings.</span></span> <span data-ttu-id="eb3f7-234">Para definir o idioma, selecione a guia **formatos** e, em seguida, selecione o idioma na caixa de combinação **formato atual** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-234">To set the language, select the **Formats** tab and then select the language from the **Current format** combo box.</span></span> <span data-ttu-id="eb3f7-235">Para definir a região, selecione a guia **local** e, em seguida, selecione a região na caixa de combinação **local atual** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-235">To set the region, select the **Location** tab and then select the region from the **Current location** combo box.</span></span> <span data-ttu-id="eb3f7-236">Além disso, para lojas que exigem a instalação de um plug-in ou software personalizado específico para armazenamento, talvez seja necessário alterar a localidade do sistema para o idioma da localidade do repositório para facilitar a instalação.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-236">Additionally, for stores that require installation of a plug-in or store-specific custom software, you might need to change the system locale to the language of the store's locale to facilitate installation.</span></span> <span data-ttu-id="eb3f7-237">O instalador de software deve dar suporte a caracteres de byte único e duplo e deve ser executado em qualquer localidade.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-237">The software installer must support both single and double byte characters and must run on any locale.</span></span> <span data-ttu-id="eb3f7-238">Você deve testar na localidade nativa.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-238">You must test in the native locale.</span></span> <span data-ttu-id="eb3f7-239">Para definir a localidade nativa, abra a caixa de diálogo **região e idioma** , selecione a guia **administrativo** e clique no botão **alterar localidade do sistema** , conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-239">To set the native locale, open the **Region and Language** dialog box, select the **Administrative** tab, and then click the **Change system locale** button as shown in the following screen shot.</span></span> <span data-ttu-id="eb3f7-240">Clicar nesse botão exibe a caixa de diálogo **configurações de região e idioma** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-240">Clicking this button displays the **Region and Language Settings** dialog box.</span></span> <span data-ttu-id="eb3f7-241">A caixa de combinação de **localidade do sistema atual** nessa caixa de diálogo altera a localidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-241">The **Current system locale** combo box in that dialog box changes the system locale.</span></span>

    <span data-ttu-id="eb3f7-242">As capturas de tela a seguir mostram as guias nas quais você pode definir a região e o idioma:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-242">The following screen shots show the tabs on which you can set region and language:</span></span>

    ![captura de tela da caixa de diálogo opções regionais e de idiomas](images/reg-lang-opt.png)

    ![captura de tela mostrando como alterar a localidade do sistema atual](images/reg-lang-settings.png)

3.  <span data-ttu-id="eb3f7-245">Desative a exibição do centro de informações de um repositório Configurando o Windows Media Player para reproduzir uma visualização.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-245">Turn off the view of a store's Info Center by setting Windows Media Player to play a visualization.</span></span> <span data-ttu-id="eb3f7-246">A principal diferença entre as plataformas é que, no Windows Media Player 11, você começa clicando **agora em execução**, enquanto no Windows Media Player 12, você começa clicando com o botão direito do mouse na janela principal.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-246">The main difference between the platforms is that in Windows Media Player 11, you start by clicking **Now Playing**, whereas in Windows Media Player 12, you start by right-clicking the main window.</span></span>

    <span data-ttu-id="eb3f7-247">A captura de tela a seguir mostra a sequência de opções de menu que desempenha uma visualização no Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-247">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 11:</span></span>

    ![captura de tela mostrando como reproduzir uma visualização no Windows Media Player 11](images/wmp11-visual.png)

    <span data-ttu-id="eb3f7-249">A captura de tela a seguir mostra a sequência de opções de menu que desempenha uma visualização no Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-249">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 12:</span></span>

    ![captura de tela mostrando como reproduzir uma visualização no Windows Media Player 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a><span data-ttu-id="eb3f7-251">Configurando um repositório</span><span class="sxs-lookup"><span data-stu-id="eb3f7-251">Setting Up a Store</span></span>

<span data-ttu-id="eb3f7-252">Primeiro, execute as etapas a seguir para configurar um repositório e, em seguida, execute as etapas a seguir as etapas iniciais para verificar a configuração da loja:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-252">First perform the following steps to set up a store, and then perform the steps that follow the initial steps to verify the store setup:</span></span>

1.  <span data-ttu-id="eb3f7-253">Inicie o Windows Media Player e aguarde alguns segundos para adquirir o arquivo de AllServices.xml mais recente.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-253">Launch Windows Media Player and wait several seconds to acquire the latest AllServices.xml file.</span></span>
2.  <span data-ttu-id="eb3f7-254">Para o Windows XP e o Windows Vista, para selecionar uma loja online, primeiro clique na guia que divide entre o modo de exibição de guia de mídia e a exibição de lojas online.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-254">For Windows XP and Windows Vista, to select an online store, first click the tab that splits between the Media Guide view and the Online Stores view.</span></span> <span data-ttu-id="eb3f7-255">Em seguida, no menu, clique em **procurar todas as lojas online** e selecione o repositório clicando em seu ícone na lista de lojas.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-255">Then, from the menu click **Browse all Online Stores**, and select the store by clicking its icon in the list of stores.</span></span> <span data-ttu-id="eb3f7-256">Para o Windows 7, clique no botão no painel de navegação biblioteca que se divide entre o botão **Guia de mídia** e o botão **lojas online** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-256">For Windows 7, click the button in the library-navigation pane that splits between the **Media Guide** button and the **Online Stores** button.</span></span> <span data-ttu-id="eb3f7-257">Em seguida, no menu, clique em **procurar todas as lojas online** e selecione o repositório clicando em seu ícone na lista de lojas.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-257">Then, from the menu click **Browse all online stores**, and select the store by clicking its icon in the list of stores.</span></span>

    <span data-ttu-id="eb3f7-258">A captura de tela a seguir mostra como selecionar uma loja online no Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-258">The following screen shot shows how to select an online store in Windows Media Player 11:</span></span>

    ![captura de tela mostrando como selecionar uma loja online no Windows Media Player 11](images/wmp11-set-store.png)

    <span data-ttu-id="eb3f7-260">A captura de tela a seguir mostra como selecionar uma loja online no Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-260">The following screen shot shows how to select an Online Store in Windows Media Player 12:</span></span>

    ![captura de tela mostrando como selecionar uma loja online no Windows Media Player 12](images/wmp12-set-store.png)

3.  <span data-ttu-id="eb3f7-262">Siga as instruções da loja para instalar qualquer software adicional necessário para usar a loja.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-262">Follow instructions from the store to install any additional software that is needed to use the store.</span></span>

<span data-ttu-id="eb3f7-263">**Para verificar a configuração do repositório**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-263">**To verify store setup**</span></span>

1.  <span data-ttu-id="eb3f7-264">Verifique se o software é instalado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-264">Verify that the software installs.</span></span>

    <span data-ttu-id="eb3f7-265">Verifique se o plug-in OCX ou qualquer outro software da loja baixa e instala sem erros.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-265">Verify that the OCX plug-in or any other software from the store downloads and installs without error.</span></span>

2.  <span data-ttu-id="eb3f7-266">Verifique se o software é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-266">Verify that the software uninstalls.</span></span>

    <span data-ttu-id="eb3f7-267">Verifique se, no painel de controle, no item **programas e recursos** , o software que a loja instala aparece na lista **desinstalar ou alterar um programa** e verifique se você pode desinstalá-lo dessa lista sem erros.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-267">Verify that in Control Panel, in the **Programs and Features** item, the software that the store installs appears in the **Uninstall or change a program** list, and verify that you can uninstall it from this list without error.</span></span>

3.  <span data-ttu-id="eb3f7-268">Verifique se o software não é executado na bandeja do sistema.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-268">Verify that software does not run in the system tray.</span></span>

    <span data-ttu-id="eb3f7-269">Verifique se nenhum software da loja adiciona ícones à área de notificação do programa (na barra de tarefas à esquerda do relógio) antes do consentimento do cliente para baixar o software do repositório.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-269">Verify that none of the software from the store adds icons to the program notification area (on the Taskbar to the left of the clock) prior to customer consent to download store software.</span></span>

    <span data-ttu-id="eb3f7-270">A experiência básica de armazenamento não deve exigir a instalação de software adicional.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-270">The basic store experience should not require installation of additional software.</span></span> <span data-ttu-id="eb3f7-271">Uma experiência de mídia básica, como mídia de streaming, deve estar disponível.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-271">A basic media experience, such as streaming media, should be available.</span></span> <span data-ttu-id="eb3f7-272">Alguns armazenamentos instalam software adicional, como gerenciadores de download para uma experiência de mídia Premier; esses armazenamentos podem ter ícones na bandeja do sistema se os ícones representarem aplicativos separados do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-272">Some stores install additional software such as download managers for a premier media experience; these stores can have icons in the system tray if the icons represent applications that are separate from Windows Media Player.</span></span>

4.  <span data-ttu-id="eb3f7-273">Verifique se a guia loja Opera.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-273">Verify that the store tab operates.</span></span>

    <span data-ttu-id="eb3f7-274">Verifique se a guia loja é alterada para indicar o repositório selecionado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-274">Verify that the store tab changes to indicate the selected store.</span></span>

    <span data-ttu-id="eb3f7-275">Para o Windows XP e o Windows Vista com o Windows Media Player 11, verifique se o nome e o ícone da loja estão visíveis em relação ao plano de fundo do Windows Media Player 11 escuro.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-275">For Windows XP and Windows Vista with Windows Media Player 11, verify that the store name and icon are visible against the dark Windows Media Player 11 background.</span></span>

    <span data-ttu-id="eb3f7-276">Para o Windows 7 com Windows Media Player 12, verifique se o nome e o ícone da loja estão visíveis no painel de navegação biblioteca, no menu de contexto seletor de serviço.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-276">For Windows 7 with Windows Media Player 12, verify the store name and icon are visible in the library-navigation pane, in the service-selector context menu.</span></span>

    <span data-ttu-id="eb3f7-277">Verifique se o repositório está listado na parte superior da lista seletor de repositório no menu.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-277">Verify that the store is listed at the top of the store selector list in the menu.</span></span>

    > [!Note]  
    > <span data-ttu-id="eb3f7-278">Não haverá a opção **Adicionar serviço atual ao menu** se o repositório do tipo 2 for o repositório em destaque (padrão) para a região.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-278">There will be no **Add current service to menu** option if the Type 2 store is the featured (default) store for the region.</span></span>

     

    <span data-ttu-id="eb3f7-279">A captura de tela a seguir mostra o menu que aparece quando você clica na guia no canto superior direito do Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-279">The following screen shot shows the menu that appears when you click the tab at the top right corner of Windows Media Player 11:</span></span>

    ![captura de tela mostrando a guia armazenar no Windows Media Player 11](images/wmp11-verify-store.png)

    <span data-ttu-id="eb3f7-281">A captura de tela a seguir mostra o menu que aparece quando você clica no botão dividir no canto inferior esquerdo do Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-281">The following screen shot shows the menu that appears when you click the split button at the lower left corner of Windows Media Player 12:</span></span>

    ![captura de tela mostrando a guia armazenar no Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a><span data-ttu-id="eb3f7-283">Criando uma conta</span><span class="sxs-lookup"><span data-stu-id="eb3f7-283">Creating an Account</span></span>

<span data-ttu-id="eb3f7-284">**Para verificar a configuração da conta**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-284">**To verify account setup**</span></span>

1.  <span data-ttu-id="eb3f7-285">Verifique se o repositório tem uma opção para criar uma nova conta e siga as instruções da loja para criar uma nova conta.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-285">Verify that the store has an option to create a new account, and then follow the store instructions to create a new account.</span></span>

    <span data-ttu-id="eb3f7-286">A captura de tela a seguir destaca um botão **criar nova conta** , como pode aparecer no Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-286">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 11:</span></span>

    ![captura de tela mostrando como verificar a configuração da conta do Windows Media Player 11](images/wmp11-verify-account.png)

    <span data-ttu-id="eb3f7-288">A captura de tela a seguir destaca um botão **criar nova conta** , como pode aparecer no Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-288">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 12:</span></span>

    ![captura de tela mostrando como verificar a configuração da conta do Windows Media Player 12](images/wmp12-verify-account.png)

2.  <span data-ttu-id="eb3f7-290">Verifique se você pode entrar na conta que você criou.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-290">Verify that you can sign in to the account that you created.</span></span>

### <a name="setting-up-credential-caching"></a><span data-ttu-id="eb3f7-291">Configurando o cache de credenciais</span><span class="sxs-lookup"><span data-stu-id="eb3f7-291">Setting Up Credential Caching</span></span>

<span data-ttu-id="eb3f7-292">Primeiro, execute as seguintes etapas para configurar o cache de credenciais e execute as etapas a seguir as etapas iniciais para verificar a configuração de caching de credencial:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-292">First perform the following steps to set up credential caching, and then perform the steps that follow the initial steps to verify the credential-caching setup:</span></span>

1.  <span data-ttu-id="eb3f7-293">Na página de entrada, insira as credenciais e selecione a opção para salvar as informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-293">At the sign-in page, enter credentials and select the option to save user information.</span></span>
2.  <span data-ttu-id="eb3f7-294">Verifique se a página de entrada tem uma caixa de seleção que permite ao usuário armazenar em cache as credenciais.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-294">Verify that the sign-in page has a check box that allows the user to cache credentials.</span></span>
3.  <span data-ttu-id="eb3f7-295">O cache de credenciais opcional é um ponto de segurança importante.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-295">Optional credential caching is an important security point.</span></span> <span data-ttu-id="eb3f7-296">O cache automático de credenciais pode expor informações de identificação pessoal de usuários que entram em um computador compartilhado ou público.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-296">Automatic credential caching can expose personally identifiable information of users who sign into a shared or public computer.</span></span> <span data-ttu-id="eb3f7-297">Você deve proteger as informações do cliente oferecendo uma caixa de seleção que processa o cache opcional.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-297">You should protect customer information by offering a check box that renders the caching optional.</span></span>

<span data-ttu-id="eb3f7-298">**Para verificar o cache de credenciais**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-298">**To verify credential caching**</span></span>

1.  <span data-ttu-id="eb3f7-299">Verifique se o repositório tem uma caixa de seleção para uma opção **salvar minhas informações de usuário** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-299">Verify that the store has a check box for a **Save my user information** option.</span></span>

    1.  <span data-ttu-id="eb3f7-300">Feche o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-300">Close Windows Media Player.</span></span>
    2.  <span data-ttu-id="eb3f7-301">Reabra o Windows Media Player e tente baixar algum conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-301">Reopen Windows Media Player and attempt to download some content.</span></span>

2.  <span data-ttu-id="eb3f7-302">Verifique se o cache de credenciais está presente e funcionando.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-302">Verify that credential caching is present and working.</span></span>

    1.  <span data-ttu-id="eb3f7-303">Saia da loja.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-303">Sign out of the store.</span></span>
    2.  <span data-ttu-id="eb3f7-304">Feche o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-304">Close Windows Media Player.</span></span>
    3.  <span data-ttu-id="eb3f7-305">Reabra o Windows Media Player e tente baixar algum conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-305">Reopen Windows Media Player and attempt to download some content.</span></span>

3.  <span data-ttu-id="eb3f7-306">Verifique se as credenciais do usuário são solicitadas se elas não estiverem armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-306">Verify that the user is prompted for credentials if they are not cached.</span></span>

    <span data-ttu-id="eb3f7-307">Depois de sair e, em seguida, tentar usar a loja, as credenciais do cliente deverão ser solicitadas.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-307">After signing out and then trying to use the store, the customer should be prompted for credentials.</span></span>

## <a name="content-acquisition"></a><span data-ttu-id="eb3f7-308">Aquisição de conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-308">Content Acquisition</span></span>

<span data-ttu-id="eb3f7-309">Esta seção descreve as várias maneiras de adquirir conteúdo e como verificar se o conteúdo foi adquirido.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-309">This section describes the various ways to acquire content and how to verify that that content was acquired.</span></span>

### <a name="streaming-content"></a><span data-ttu-id="eb3f7-310">Conteúdo de streaming</span><span class="sxs-lookup"><span data-stu-id="eb3f7-310">Streaming Content</span></span>

<span data-ttu-id="eb3f7-311">Transmita todos os tipos de conteúdo disponíveis do repositório.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-311">Stream all available types of content from the store.</span></span> <span data-ttu-id="eb3f7-312">Por exemplo, transmita o conteúdo de rádio, vídeo, áudio e visualizações.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-312">For example, stream radio, video, audio, and previews content.</span></span>

<span data-ttu-id="eb3f7-313">**Para verificar o conteúdo de streaming**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-313">**To verify streaming content**</span></span>

1.  <span data-ttu-id="eb3f7-314">Verifique se todos os tipos de fluxo de conteúdo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-314">Verify that all available types of content stream.</span></span>

2.  <span data-ttu-id="eb3f7-315">Verifique se o conteúdo é reproduzido no Windows Media Player e não em outro jogador ou controle.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-315">Verify that content plays in Windows Media Player and not some other player or control.</span></span>

### <a name="obtaining-content"></a><span data-ttu-id="eb3f7-316">Obtendo conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-316">Obtaining Content</span></span>

<span data-ttu-id="eb3f7-317">Primeiro, execute as etapas a seguir para comprar conteúdo e, em seguida, execute as etapas a seguir as etapas iniciais para verificar a compra e verificar se o conteúdo foi baixado:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-317">First perform the following steps to purchase content, and then perform the steps that follow the initial steps to verify the purchase and verify that the content downloaded:</span></span>

1.  <span data-ttu-id="eb3f7-318">Inicie o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-318">Launch Windows Media Player.</span></span>
2.  <span data-ttu-id="eb3f7-319">Entre na conta de teste.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-319">Sign in to the test account.</span></span>
3.  <span data-ttu-id="eb3f7-320">Navegue até o conteúdo a ser comprado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-320">Navigate to the content to purchase.</span></span>
4.  <span data-ttu-id="eb3f7-321">Siga o procedimento específico do repositório para comprar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-321">Follow the store-specific procedure to purchase content.</span></span>

<span data-ttu-id="eb3f7-322">**Para verificar o conteúdo adquirido e baixado**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-322">**To verify purchased and downloaded content**</span></span>

1.  <span data-ttu-id="eb3f7-323">Verifique se o preço calculado está correto.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-323">Verify that the calculated price is correct.</span></span>

    <span data-ttu-id="eb3f7-324">Verifique se o preço está correto, especialmente ao comprar várias partes de conteúdo ao mesmo tempo e verifique se as informações de saldo da conta foram atualizadas corretamente após a compra.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-324">Verify that the price is correct, especially when purchasing multiple pieces of content at once, and verify that any account balance information is updated correctly after purchase.</span></span> <span data-ttu-id="eb3f7-325">Alguns conteúdos podem ser comprados como faixas únicas e apenas como álbuns.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-325">Some content can be purchased as single tracks and some as albums only.</span></span> <span data-ttu-id="eb3f7-326">Verifique se o preço do álbum não é maior do que a soma das faixas individuais.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-326">Verify that the album price is not larger than the sum of the individual tracks.</span></span>

2.  <span data-ttu-id="eb3f7-327">Verifique se o conteúdo adquirido é baixado para a biblioteca.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-327">Verify that the purchased content downloads to the library.</span></span>

    <span data-ttu-id="eb3f7-328">Quando o download for concluído, navegue até o conteúdo baixado na biblioteca do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-328">When the download completes, navigate to the downloaded content in the Windows Media Player library.</span></span> <span data-ttu-id="eb3f7-329">O conteúdo baixado está localizado na biblioteca do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-329">The downloaded content is located in the current user's library.</span></span>

    -   <span data-ttu-id="eb3f7-330">Para o Windows XP e o Windows Vista com o Windows Media Player 11, o conteúdo baixado aparece no painel de navegação **da biblioteca, em tabela dinâmica** e, em seguida, em **músicas**.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-330">For Windows XP and Windows Vista with Windows Media Player 11, downloaded content appears in the library navigation pane, under **Library** pivot, and then under **Songs**.</span></span>
    -   <span data-ttu-id="eb3f7-331">Para o Windows 7 com Windows Media Player 12, o conteúdo baixado para a biblioteca do Windows Media Player aparece no painel de navegação do Windows Media Player em **música**.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-331">For Windows 7 with Windows Media Player 12, content that is downloaded to the Windows Media Player library appears in the Windows Media Player navigation pane under **Music**.</span></span>

3.  <span data-ttu-id="eb3f7-332">Verifique se os metadados são baixados para a compra.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-332">Verify that metadata downloads for the purchase.</span></span>

    <span data-ttu-id="eb3f7-333">Verifique se as colunas a seguir aparecem na biblioteca do Windows Media Player (adicione-as se não):</span><span class="sxs-lookup"><span data-stu-id="eb3f7-333">Ensure that the following columns appear in the Windows Media Player library (add them if not):</span></span>

    -   <span data-ttu-id="eb3f7-334">Artista do álbum</span><span class="sxs-lookup"><span data-stu-id="eb3f7-334">Album Artist</span></span>
    -   <span data-ttu-id="eb3f7-335">Título</span><span class="sxs-lookup"><span data-stu-id="eb3f7-335">Title</span></span>
    -   <span data-ttu-id="eb3f7-336">Título do álbum</span><span class="sxs-lookup"><span data-stu-id="eb3f7-336">Album Title</span></span>
    -   <span data-ttu-id="eb3f7-337">Provedor de conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-337">Content Provider</span></span>
    -   <span data-ttu-id="eb3f7-338">Gênero</span><span class="sxs-lookup"><span data-stu-id="eb3f7-338">Genre</span></span>

    <span data-ttu-id="eb3f7-339">As colunas anteriores devem ser preenchidas.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-339">The preceding columns must be populated.</span></span> <span data-ttu-id="eb3f7-340">O conteúdo deve ter arte do álbum.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-340">Content should have album art.</span></span> <span data-ttu-id="eb3f7-341">No entanto, a arte do álbum não é necessária para passar no teste de validação.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-341">However, album art is not required to pass validation testing.</span></span>

4.  <span data-ttu-id="eb3f7-342">Verifique se os direitos de uso de mídia estão corretos para a compra.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-342">Verify that media usage rights are correct for the purchase.</span></span>

    <span data-ttu-id="eb3f7-343">Para cada trilha baixada, clique com o botão direito do mouse na faixa e selecione **Propriedades** e selecione a guia **direitos de uso de mídia** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-343">For each downloaded track, right-click the track and select **Properties**, and then select the **Media Usage Rights** tab.</span></span>

    <span data-ttu-id="eb3f7-344">O repositório pode optar por proteger seu conteúdo com direitos de uso de mídia ou optar por não proteger o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-344">The store can choose to protect its content with media usage rights, or can choose to not protect the content.</span></span> <span data-ttu-id="eb3f7-345">A guia **direitos de uso de mídia** reflete esse status listando as restrições ou informando que o conteúdo não está protegido.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-345">The **Media Usage Rights** tab reflects that status either by listing the restrictions, or by stating that the content is not protected.</span></span> <span data-ttu-id="eb3f7-346">O repositório deve comunicar seu plano mais atual para direitos de uso de mídia.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-346">The store must communicate its most current plan for media usage rights.</span></span> <span data-ttu-id="eb3f7-347">Você deve verificar os resultados reais em relação a esse comportamento esperado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-347">You must verify actual results against this expected behavior.</span></span>

    <span data-ttu-id="eb3f7-348">As licenças de direitos de mídia devem ser previamente entregues.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-348">Media rights licenses must be pre-delivered.</span></span> <span data-ttu-id="eb3f7-349">O cliente não deve ser solicitado a reproduzir o conteúdo ou passar por algum outro processo para obter a licença.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-349">The customer must not be required to play the content or go through some other process to get the license.</span></span> <span data-ttu-id="eb3f7-350">Você deve comparar os direitos de uso de mídia específicos para o que a loja se comunica com o cliente, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-350">You must compare the specific media usage rights to what the store has communicated to the customer as appropriate.</span></span> <span data-ttu-id="eb3f7-351">Os direitos devem ser transferíveis para pelo menos dois outros computadores.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-351">Rights must be transferable to at least two other computers.</span></span> <span data-ttu-id="eb3f7-352">Os clientes devem ser capazes de gravar e sincronizar suas mídias.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-352">Customers must be able to burn and synchronize their media.</span></span>

    <span data-ttu-id="eb3f7-353">A captura de tela a seguir mostra os direitos de uso de mídia de um arquivo protegido:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-353">The following screen shot shows the media usage rights of a protected file:</span></span>

    ![captura de tela mostrando os direitos de uso de mídia para um arquivo protegido](images/media-rights-protected.png)

    <span data-ttu-id="eb3f7-355">Se o conteúdo não estiver protegido, a guia **direitos de uso de mídia** indicará esse fato.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-355">If the content is not protected, the **Media Usage Rights** tab indicates this fact.</span></span>

    <span data-ttu-id="eb3f7-356">A captura de tela a seguir mostra os direitos de uso de mídia de um arquivo desprotegido:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-356">The following screen shot shows the media usage rights of an unprotected file:</span></span>

    ![captura de tela mostrando os direitos de uso de mídia para um arquivo desprotegido](images/media-rights-not-protected.png)

5.  <span data-ttu-id="eb3f7-358">Verifique se o conteúdo comprado é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-358">Verify that the purchased content plays.</span></span>

    <span data-ttu-id="eb3f7-359">Verifique se o conteúdo baixado é reproduzido no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-359">Verify that downloaded content plays in Windows Media Player.</span></span>

    <span data-ttu-id="eb3f7-360">Reproduzir qualquer conteúdo adquirido da loja e que resida na biblioteca local ou transmitir uma visualização.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-360">Play any content that was purchased from the store and that resides in the local library, or stream a preview.</span></span>

    <span data-ttu-id="eb3f7-361">Execute as seguintes etapas para comprar o conteúdo no Windows XP e no Windows Vista com o Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-361">Perform the following steps to purchase content in Windows XP and Windows Vista with Windows Media Player 11:</span></span>

    1.  <span data-ttu-id="eb3f7-362">Clique na guia **executando agora** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-362">Click the **Now Playing** tab.</span></span>
    2.  <span data-ttu-id="eb3f7-363">No painel lista, posicione o ponteiro do mouse para focalizar a arte do álbum para mostrar o link **comprar** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-363">In the list pane, position the mouse pointer to hover over album art in order to show the **Buy** link.</span></span>
    3.  <span data-ttu-id="eb3f7-364">Clique em **comprar**.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-364">Click **Buy**.</span></span>

    <span data-ttu-id="eb3f7-365">A captura de tela a seguir mostra o local do link **comprar** no Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-365">The following screen shot shows the location of the **Buy** link in Windows Media Player 11:</span></span>

    ![captura de tela mostrando como comprar conteúdo no Windows Media Player 11](images/wmp11-verify-buy-play.png)

    <span data-ttu-id="eb3f7-367">Execute as seguintes etapas para comprar o conteúdo no Windows 7 com o Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-367">Perform the following steps to purchase content in Windows 7 with Windows Media Player 12:</span></span>

    1.  <span data-ttu-id="eb3f7-368">Em modo de biblioteca, clique na guia **reproduzir** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-368">In library mode, click the **Play** tab.</span></span>
    2.  <span data-ttu-id="eb3f7-369">Na lista de reprodução, na arte do álbum, clique em **comprar**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-369">In the playlist, under the album art, click **Shop**</span></span>

    <span data-ttu-id="eb3f7-370">A captura de tela a seguir mostra como comprar conteúdo no Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-370">The following screen shot shows how to buy content in Windows Media Player 12:</span></span>

    ![captura de tela mostrando como comprar conteúdo no Windows Media Player 12](images/wmp12-verify-buy-play.png)

6.  <span data-ttu-id="eb3f7-372">Verifique se clicar em **comprar** ou **comprar** alterna para o repositório.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-372">Verify that clicking **Buy** or **Shop** switches to the store.</span></span>

    <span data-ttu-id="eb3f7-373">O Windows Media Player deve alternar para o repositório na exibição de biblioteca e carregar a experiência de compra da loja.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-373">The Windows Media Player should switch to the store in library view and load the purchasing experience of the store.</span></span>

    <span data-ttu-id="eb3f7-374">Em seguida, você deve continuar a comprar a faixa.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-374">You must then continue to purchase the track.</span></span>

7.  <span data-ttu-id="eb3f7-375">Verifique se, depois de clicar em **comprar** ou **comprar**, o conteúdo é baixado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-375">Verify that after clicking **Buy** or **Shop**, the content downloads.</span></span>

    <span data-ttu-id="eb3f7-376">Verifique se os direitos de uso de mídia são apropriados para o conteúdo comprado e seus metadados e verifique se o roteiro é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-376">Verify that the media usage rights are appropriate for the purchased content and its metadata, and verify that the track plays.</span></span> <span data-ttu-id="eb3f7-377">Em geral, esse método de compra deve ter os mesmos resultados que outros métodos.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-377">In general, this method of purchase should have the same results as other methods.</span></span>

### <a name="burning-content"></a><span data-ttu-id="eb3f7-378">Gravando conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-378">Burning Content</span></span>

<span data-ttu-id="eb3f7-379">Primeiro, execute as seguintes etapas para gravar o conteúdo adquirido (copiar conteúdo adquirido em um CD ou DVD gravável) e, em seguida, execute as etapas que seguem as etapas iniciais para verificar se o conteúdo grava:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-379">First perform the following steps to burn purchased content (copy purchased content to a writeable CD or DVD), and then perform the steps that follow the initial steps to verify that the content burns:</span></span>

> [!Note]  
> <span data-ttu-id="eb3f7-380">Antes de gravar uma faixa adquirida, anote sua contagem de gravação para que você possa verificar se a contagem diminui depois de gravar a faixa.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-380">Before you burn a purchased track, note its burn count so you can later verify whether the count decrements after you burn the track.</span></span>

 

1.  <span data-ttu-id="eb3f7-381">Clique na guia **gravar**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-381">Click the **Burn** tab</span></span>
2.  <span data-ttu-id="eb3f7-382">Arraste as faixas adquiridas para a **lista de gravação**.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-382">Drag purchased tracks to the **Burn List**.</span></span>
3.  <span data-ttu-id="eb3f7-383">Clique no botão **Iniciar gravação** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-383">Click the **Start Burn** button.</span></span>

<span data-ttu-id="eb3f7-384">A captura de tela a seguir mostra a **lista de gravação** no lado direito da tela e o botão **Iniciar gravação** abaixo da **lista de gravação** no Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-384">The following screen shot shows the **Burn List** on the right side of the screen and the **Start Burn** button below the **Burn List** in Windows Media Player 11:</span></span>

![captura de tela mostrando como gravar conteúdo no Windows Media Player 11](images/wmp11-verify-burn.png)

<span data-ttu-id="eb3f7-386">A captura de tela a seguir mostra como a lista de gravação aparece no Windows Media Player 12 depois que você arrasta uma faixa para a lista de gravação e mostra o botão **Iniciar gravação** na parte superior da guia **gravar** :</span><span class="sxs-lookup"><span data-stu-id="eb3f7-386">The following screen shot shows how the burn list appears in Windows Media Player 12 after you drag a track to the burn list, and it shows the **Start Burn** button at the top of the **Burn** tab:</span></span>

![captura de tela mostrando como gravar conteúdo no Windows Media Player 12](images/wmp12-verify-burn.png)

<span data-ttu-id="eb3f7-388">**Para verificar se o conteúdo comprado pode ser gravado**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-388">**To verify that purchased content can be burned**</span></span>

1.  <span data-ttu-id="eb3f7-389">Verifique se o conteúdo comprado é gravado reproduzindo o CD ou DVD após a gravação ser concluída.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-389">Verify that the purchased content burns by playing the CD or DVD after burning completes.</span></span>

2.  <span data-ttu-id="eb3f7-390">Verifique se a contagem de gravação foi decrementada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-390">Verify that the burn count is decremented.</span></span>

    <span data-ttu-id="eb3f7-391">Navegue até a biblioteca e abra os direitos de uso de mídia para um roteiro comprado que foi gravado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-391">Navigate to the library and open the media usage rights for a purchased track that was burned.</span></span>

    <span data-ttu-id="eb3f7-392">Se o número de vezes que um controle pode ser gravado for limitado, verifique se esse número diminui depois que a faixa é gravada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-392">If the number of times a track can be burned is limited, verify that this number decreases after the track is burned.</span></span>

### <a name="transferring-content"></a><span data-ttu-id="eb3f7-393">Transferindo conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-393">Transferring Content</span></span>

<span data-ttu-id="eb3f7-394">Transferir conteúdo para outro computador.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-394">Transfer content to another computer.</span></span>

<span data-ttu-id="eb3f7-395">**Para verificar se o conteúdo comprado pode ser transferido para outro computador**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-395">**To verify that purchased content can be transferred to another computer**</span></span>

-   <span data-ttu-id="eb3f7-396">Se o repositório permitir a transferência de conteúdo para outro computador, transfira o conteúdo para pelo menos dois computadores.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-396">If the store allows transferring content to another computer, transfer the content to at least two computers.</span></span>

<span data-ttu-id="eb3f7-397">Primeiro execute as seguintes etapas para sincronizar um dispositivo e transferir o conteúdo adquirido para esse dispositivo e, em seguida, execute as etapas a seguir as etapas iniciais para verificar se o conteúdo foi transferido:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-397">First perform the following steps to sync to a device and transfer purchased content to that device, and then perform the steps that follow the initial steps to verify that the content is transferred:</span></span>

> [!Note]  
> <span data-ttu-id="eb3f7-398">Antes de transferir uma faixa adquirida, anote sua contagem de sincronização para que você possa verificar se a contagem diminui depois de transferir a faixa.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-398">Before you transfer a purchased track, note its sync count so you can later verify whether the count decrements after you transfer the track.</span></span>

 

1.  <span data-ttu-id="eb3f7-399">Conecte um dispositivo com um relógio seguro.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-399">Connect a device with a secure clock.</span></span> <span data-ttu-id="eb3f7-400">Os exemplos incluem dispositivos que usam o DRM do Windows Media para dispositivos portáteis, como um Media Center portátil como o iRiver H10, o Zen criativo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-400">Examples include devices that use Windows Media DRM for Portable Devices, such as a Portable Media Center like the iRiver H10, the Creative Zen, and so on.</span></span>
2.  <span data-ttu-id="eb3f7-401">No Windows Media Player, clique na guia **sincronizar** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-401">In Windows Media Player, click the **Sync** tab.</span></span>
3.  <span data-ttu-id="eb3f7-402">Arraste conteúdo da biblioteca para a área de **lista de sincronização** na guia **sincronizar** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-402">Drag content from the library to the **Sync list** area on the **Sync** tab.</span></span>
4.  <span data-ttu-id="eb3f7-403">Clique no botão **Iniciar sincronização** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-403">Click the **Start Sync** button.</span></span>

<span data-ttu-id="eb3f7-404">A captura de tela a seguir mostra o Track 1 na área de **lista de sincronização** e mostra o botão **Iniciar sincronização** no Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-404">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 11:</span></span>

![captura de tela mostrando como transferir conteúdo no Windows Media Player 11](images/wmp11-verify-transfer.png)

<span data-ttu-id="eb3f7-406">A captura de tela a seguir mostra o Track 1 na área de **lista de sincronização** e mostra o botão **Iniciar sincronização** no Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-406">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 12:</span></span>

![captura de tela mostrando como transferir conteúdo no Windows Media Player 12](images/wmp12-verify-transfer.png)

<span data-ttu-id="eb3f7-408">**Para verificar se o conteúdo comprado pode ser transferido para outro dispositivo**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-408">**To verify that purchased content can be transferred to another device**</span></span>

1.  <span data-ttu-id="eb3f7-409">Verifique se o conteúdo comprado é transferido para o dispositivo executando o conteúdo no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-409">Verify that the purchased content is transferred to the device by playing the content on the device.</span></span> <span data-ttu-id="eb3f7-410">O conteúdo transferido também deve ter metadados apropriados.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-410">The transferred content must also have appropriate metadata.</span></span>

2.  <span data-ttu-id="eb3f7-411">Verifique se a contagem de sincronização foi decrementada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-411">Verify that the sync count is decremented.</span></span>

    <span data-ttu-id="eb3f7-412">Navegue até a biblioteca e abra os direitos de uso de mídia para uma faixa transferida.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-412">Navigate to the library and open the media usage rights for a transferred track.</span></span>

    <span data-ttu-id="eb3f7-413">Se o número de vezes que uma faixa pode sincronizar é limitado, verifique se esse número diminui quando a faixa é transferida.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-413">If the number of times a track can sync is limited, verify that this number decreases when the track is transferred.</span></span>

## <a name="store-features"></a><span data-ttu-id="eb3f7-414">Armazenar recursos</span><span class="sxs-lookup"><span data-stu-id="eb3f7-414">Store Features</span></span>

<span data-ttu-id="eb3f7-415">As seções a seguir descrevem como testar vários recursos de uma loja online integrada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-415">The following sections describe how to test various features of an on-boarded online store.</span></span>

### <a name="managing-an-account"></a><span data-ttu-id="eb3f7-416">Gerenciando uma conta</span><span class="sxs-lookup"><span data-stu-id="eb3f7-416">Managing an Account</span></span>

<span data-ttu-id="eb3f7-417">Entre com uma conta que tenha feito algumas compras e abra o histórico de compra.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-417">Sign in with an account that has made some purchases and open the purchase history.</span></span>

<span data-ttu-id="eb3f7-418">**Para verificar o histórico de compra**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-418">**To verify purchase history**</span></span>

-   <span data-ttu-id="eb3f7-419">Verifique se o histórico de compras acompanha as compras anteriores.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-419">Verify that the purchase history tracks prior purchases.</span></span>

<span data-ttu-id="eb3f7-420">Se o tipo de conta ou armazenamento der suporte a esse recurso, tente restaurar uma compra excluída.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-420">If the store or account type supports this feature, attempt to restore a deleted purchase.</span></span>

<span data-ttu-id="eb3f7-421">**Para verificar se as compras anteriores podem ser readquiridas**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-421">**To verify that prior purchases can be reacquired**</span></span>

-   <span data-ttu-id="eb3f7-422">Verifique se uma compra anterior pode ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-422">Verify that a prior purchase can be restored.</span></span>

<span data-ttu-id="eb3f7-423">Se o armazenamento oferecer suporte ao uso de vários computadores com a conta, verifique todas as funcionalidades fornecidas por esse recurso.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-423">If the store supports using multiple computers with the account, verify any functionality that this feature provides.</span></span>

<span data-ttu-id="eb3f7-424">**Para verificar o gerenciamento de vários computadores com uma única conta**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-424">**To verify multiple computer management with a single account**</span></span>

-   <span data-ttu-id="eb3f7-425">Verifique a funcionalidade do repositório para gerenciar vários computadores.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-425">Verify the store's functionality to manage multiple computers.</span></span>

### <a name="managing-a-store-specific-account"></a><span data-ttu-id="eb3f7-426">Gerenciando uma conta de Store-Specific</span><span class="sxs-lookup"><span data-stu-id="eb3f7-426">Managing a Store-Specific Account</span></span>

<span data-ttu-id="eb3f7-427">O repositório pode não ter tipos de conta, restrições ou conteúdo típicos.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-427">The store might not have typical account types, restrictions, or content.</span></span> <span data-ttu-id="eb3f7-428">Por exemplo, uma loja que aluga o vídeo de streaming precisaria de alguma interface do usuário para exibir locações ativas e essa interface do usuário precisaria ser testada.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-428">For example, a store that rents streaming video would need some user interface to display active rentals and that user interface would need to be tested.</span></span>

> [!Note]  
> <span data-ttu-id="eb3f7-429">Embora a Microsoft não possa certificar a funcionalidade de conta específica da loja, para garantir uma boa experiência do cliente, você deve testar essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-429">Although Microsoft cannot certify store-specific account functionality, to ensure a good customer experience, you should test that functionality.</span></span>

 

### <a name="managing-the-info-center"></a><span data-ttu-id="eb3f7-430">Gerenciando o centro de informações</span><span class="sxs-lookup"><span data-stu-id="eb3f7-430">Managing the Info Center</span></span>

<span data-ttu-id="eb3f7-431">Primeiro, execute as seguintes etapas para se preparar para testar o estado padrão e, em seguida, execute a próxima etapa que segue as etapas iniciais para verificar se o centro de informações está desativado por padrão:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-431">First perform the following steps to prepare for testing the default state, and then perform the next step that follows the initial steps to verify that the Info Center is off by default:</span></span>

1.  <span data-ttu-id="eb3f7-432">Reproduzir algum conteúdo da loja.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-432">Play some content from the store.</span></span>
2.  <span data-ttu-id="eb3f7-433">Alterne para o modo de agora em execução.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-433">Switch to Now Playing mode.</span></span> <span data-ttu-id="eb3f7-434">No Windows XP ou no Windows Vista com Windows Media Player 11, clique na guia **executando agora** . No Windows 7 com Windows Media Player 12, clique no botão **alternar para agora** no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-434">In Windows XP or Windows Vista with Windows Media Player 11, click the **Now Playing** tab. In Windows 7 with Windows Media Player 12, click the **Switch to Now Playing** button at the lower right corner.</span></span>

<span data-ttu-id="eb3f7-435">**Para verificar se o centro de informações está desativado por padrão**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-435">**To verify that the Info Center is off by default**</span></span>

-   <span data-ttu-id="eb3f7-436">Verifique se o centro de informações está desativado por padrão.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-436">Verify that the Info Center is off by default.</span></span>

<span data-ttu-id="eb3f7-437">Se a loja oferece uma exibição do centro de informações, jogue algum conteúdo da loja e, enquanto o conteúdo está em execução, alterne para o modo de execução e ative o centro de informações.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-437">If the store offers an Info Center view, play some content from the store, and while the content is playing, switch to Now Playing mode and turn Info Center on.</span></span>

<span data-ttu-id="eb3f7-438">No Windows XP ou Windows Vista com Windows Media Player 11, clique com o botão direito do mouse na janela agora em execução e, no menu de contexto, selecione **exibição do centro de informações**.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-438">In Windows XP or Windows Vista with Windows Media Player 11, right-click the now-playing window, and then from the context menu select **Info Center View**.</span></span>

<span data-ttu-id="eb3f7-439">A captura de tela a seguir mostra o menu de contexto no Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-439">The following screen shot shows the context menu in Windows Media Player 11:</span></span>

![captura de tela mostrando como acessar o centro de informações de um repositório no Windows Media Player 11](images/wmp11-info-center.png)

<span data-ttu-id="eb3f7-441">No Windows 7 com Windows Media Player 12, clique com o botão direito do mouse na janela agora em execução, no menu de contexto, selecione **visualizações** e clique em **exibição do centro de informações**.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-441">In Windows 7 with Windows Media Player 12, right-click the now-playing window, on the context menu select **Visualizations**, and then click **Info Center View**.</span></span>

<span data-ttu-id="eb3f7-442">A captura de tela a seguir mostra o menu de contexto no Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-442">The following screen shot shows the context menu in Windows Media Player 12:</span></span>

![captura de tela mostrando como acessar o centro de informações de um repositório no Windows Media Player 12](images/wmp12-info-center.png)

<span data-ttu-id="eb3f7-444">**Para verificar se o centro de informações está funcional**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-444">**To verify that the Info Center is functional**</span></span>

-   <span data-ttu-id="eb3f7-445">Verifique se o centro de informações mostra informações de mídia na área de execução.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-445">Verify that the Info Center shows media information in the now-playing area.</span></span> <span data-ttu-id="eb3f7-446">A captura de tela a seguir mostra um exemplo dessas informações de mídia:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-446">The following screen shot shows an example of such media information:</span></span>

    ![captura de tela mostrando a funcionalidade do centro de informações de um repositório](images/media-information.png)

<span data-ttu-id="eb3f7-448">Se quaisquer links de compra ou outros links aparecerem na página, clique nos links.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-448">If any buy links or other links appear on the page, click the links.</span></span>

<span data-ttu-id="eb3f7-449">**Para verificar os links na exibição do centro de informações**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-449">**To verify links in the Info Center view**</span></span>

-   <span data-ttu-id="eb3f7-450">Verifique se os links mostram o repositório.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-450">Verify that the links show the store.</span></span>

    <span data-ttu-id="eb3f7-451">O Windows Media Player deve mudar para o repositório em sua biblioteca.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-451">The Windows Media Player should switch to the store in its library.</span></span>

## <a name="store-interaction"></a><span data-ttu-id="eb3f7-452">Interação de armazenamento</span><span class="sxs-lookup"><span data-stu-id="eb3f7-452">Store Interaction</span></span>

<span data-ttu-id="eb3f7-453">As seções a seguir descrevem como testar a interação entre as outras lojas e a loja que você está testando.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-453">The following sections describe how to test interaction between the other stores and the store that you are testing.</span></span>

### <a name="yielding-to-the-active-store"></a><span data-ttu-id="eb3f7-454">Gerando para o repositório ativo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-454">Yielding to the Active Store</span></span>

<span data-ttu-id="eb3f7-455">Alternar para um repositório diferente do armazenamento que está sendo testado.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-455">Switch to a store other than the store being tested.</span></span>

<span data-ttu-id="eb3f7-456">**Para verificar a concessão para o repositório ativo**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-456">**To verify yielding to the active store**</span></span>

-   <span data-ttu-id="eb3f7-457">Verifique se o armazenamento testado resulta no repositório ativo.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-457">Verify that the tested store yields to the active store.</span></span>

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a><span data-ttu-id="eb3f7-458">Impedir que o armazenamento testado assuma o armazenamento ativo</span><span class="sxs-lookup"><span data-stu-id="eb3f7-458">Preventing the Tested Store From Taking Over the Active Store</span></span>

-   <span data-ttu-id="eb3f7-459">Com outra loja selecionada, feche o Windows Media Player e reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-459">With another store selected, close Windows Media Player and restart the computer.</span></span>
-   <span data-ttu-id="eb3f7-460">Inicie o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-460">Launch Windows Media Player.</span></span>

<span data-ttu-id="eb3f7-461">**Para verificar se o armazenamento testado não assume**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-461">**To verify that the tested store does not take over**</span></span>

-   <span data-ttu-id="eb3f7-462">Verifique se o repositório ativo mais recentemente aparece e se o repositório testado não aparece.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-462">Verify that the most recently active store appears and that the tested store does not appear.</span></span>

### <a name="accessing-a-store-in-high-contrast-mode"></a><span data-ttu-id="eb3f7-463">Acessando um repositório no modo de High-Contrast</span><span class="sxs-lookup"><span data-stu-id="eb3f7-463">Accessing a Store in High-Contrast Mode</span></span>

<span data-ttu-id="eb3f7-464">Primeiro, habilite o modo de alto contraste pressionando SHIFT esquerda + ALT esquerda + PRINT SCREEN e, em seguida, execute as seguintes etapas para verificar a acessibilidade de alto contraste:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-464">First enable high-contrast mode by pressing LEFT SHIFT+LEFT ALT+PRINT SCREEN, and then perform the following steps to verify high-contrast accessibility:</span></span>

<span data-ttu-id="eb3f7-465">**Para verificar se o repositório está acessível no modo de alto contraste**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-465">**To verify that the store is accessible in high-contrast mode**</span></span>

1.  <span data-ttu-id="eb3f7-466">Verifique se a interface do usuário de logon está intacta e funcional.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-466">Verify that the log-in user interface is intact and functional.</span></span>
2.  <span data-ttu-id="eb3f7-467">Verifique se todas as janelas e caixas de diálogo aparecem corretamente.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-467">Verify that all windows and dialog boxes appear correctly.</span></span>
3.  <span data-ttu-id="eb3f7-468">Mídia de compra.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-468">Purchase media.</span></span> <span data-ttu-id="eb3f7-469">Verifique se os botões de compra e download, os gerentes de download, as informações de preço e assim por diante estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-469">Verify that purchase and download buttons, download managers, price information, and so on is visible.</span></span>
4.  <span data-ttu-id="eb3f7-470">Verifique se você pode transmitir, gravar e sincronizar.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-470">Verify that you can stream, burn, and synchronize.</span></span>
5.  <span data-ttu-id="eb3f7-471">Procure por texto recortado e elementos da interface do usuário, texto que não seja legível e outros defeitos visíveis.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-471">Look for clipped text and user-interface elements, text that is not legible, and other visible defects.</span></span>

### <a name="securing-a-store"></a><span data-ttu-id="eb3f7-472">Protegendo uma loja</span><span class="sxs-lookup"><span data-stu-id="eb3f7-472">Securing a Store</span></span>

<span data-ttu-id="eb3f7-473">Execute as seguintes etapas para verificar a segurança da conta:</span><span class="sxs-lookup"><span data-stu-id="eb3f7-473">Perform the following steps to verify account security:</span></span>

<span data-ttu-id="eb3f7-474">**Para verificar a segurança da conta**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-474">**To verify account security**</span></span>

1.  <span data-ttu-id="eb3f7-475">Insira informações de conta malformadas na página de logon e na caixa de diálogo e verifique se a loja a rejeita.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-475">Enter malformed account information into the log-in page and dialog box and verify that the store rejects it.</span></span>
2.  <span data-ttu-id="eb3f7-476">Entre, exiba a página da conta e saia.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-476">Sign in, view the account page, and sign out.</span></span>
3.  <span data-ttu-id="eb3f7-477">Clique no botão voltar no Windows Media Player e verifique se você não vê as informações da conta de usuário anterior.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-477">Click the back button in Windows Media Player, and verify that you do not see the previous user account information.</span></span>

 

 




