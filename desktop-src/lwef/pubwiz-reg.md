---
title: Registrando um serviço
description: Para adicionar seu serviço à lista de provedores no assistente de publicação na Web ou no assistente de ordenação de impressão online, você deve adicionar a chave apropriada e seus valores ao registro do Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registrar, serviços
- Assistente de publicação na Web, registrando
- Assistente de ordenação de impressão online, registrando
- registrar, assistente de publicação na Web
- registrar, assistente de ordenação de impressão online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104172895"
---
# <a name="registering-a-service"></a><span data-ttu-id="4116c-108">Registrando um serviço</span><span class="sxs-lookup"><span data-stu-id="4116c-108">Registering a Service</span></span>

<span data-ttu-id="4116c-109">Para adicionar seu serviço à lista de provedores no assistente de publicação na Web ou no assistente de ordenação de impressão online, você deve adicionar a chave apropriada e seus valores ao registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="4116c-109">To add your service to the list of providers in either the Web Publishing Wizard or the Online Print Ordering Wizard, you must add the appropriate key and its values to the Windows registry.</span></span>

## <a name="required-keys-and-values"></a><span data-ttu-id="4116c-110">Chaves e valores necessários</span><span class="sxs-lookup"><span data-stu-id="4116c-110">Required Keys and Values</span></span>

<span data-ttu-id="4116c-111">Para adicionar seu serviço à lista de provedores para o assistente de publicação na Web, adicione uma chave, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="4116c-111">To add your service to the list of providers for the Web Publishing Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="4116c-112">Para adicionar seu serviço à lista de provedores para o assistente de ordenação de impressão online, adicione uma chave, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="4116c-112">To add your service to the list of providers for the Online Print Ordering Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="4116c-113">Cada um dos valores é uma cadeia de caracteres do tipo REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="4116c-113">Each of the values is a string of type REG\_SZ.</span></span> <span data-ttu-id="4116c-114">Forneça seus dados, conforme explicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4116c-114">Provide its data as explained in the following table.</span></span> 

| <span data-ttu-id="4116c-115">Nome do valor</span><span class="sxs-lookup"><span data-stu-id="4116c-115">Value Name</span></span>     | <span data-ttu-id="4116c-116">Explicação</span><span class="sxs-lookup"><span data-stu-id="4116c-116">Explanation</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4116c-117">IconPath</span><span class="sxs-lookup"><span data-stu-id="4116c-117">IconPath</span></span>       | <span data-ttu-id="4116c-118">O caminho completo para o arquivo de ícone, incluindo o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4116c-118">The full path to the icon file, including the file name.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="4116c-119">DisplayName</span><span class="sxs-lookup"><span data-stu-id="4116c-119">DisplayName</span></span>    | <span data-ttu-id="4116c-120">O nome exibido para o serviço na lista de provedores do assistente.</span><span class="sxs-lookup"><span data-stu-id="4116c-120">The name displayed for your service in the wizard's providers list.</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4116c-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="4116c-121">Description</span></span>    | <span data-ttu-id="4116c-122">Uma breve descrição do seu serviço.</span><span class="sxs-lookup"><span data-stu-id="4116c-122">A short description for your service.</span></span> <span data-ttu-id="4116c-123">Essa descrição também é exibida na lista de provedores do assistente diretamente abaixo do nome do seu serviço.</span><span class="sxs-lookup"><span data-stu-id="4116c-123">This description also displays in the wizard's providers list directly below the name of your service.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="4116c-124">HREF</span><span class="sxs-lookup"><span data-stu-id="4116c-124">HREF</span></span>           | <span data-ttu-id="4116c-125">A URL da primeira página do serviço.</span><span class="sxs-lookup"><span data-stu-id="4116c-125">The URL of the first page of your service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4116c-126">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="4116c-126">SupportedTypes</span></span> | <span data-ttu-id="4116c-127">Os tipos de arquivo com suporte no seu serviço.</span><span class="sxs-lookup"><span data-stu-id="4116c-127">The file types supported by your service.</span></span> <span data-ttu-id="4116c-128">Por exemplo, *\* . jpg*.</span><span class="sxs-lookup"><span data-stu-id="4116c-128">For instance, *\*.jpg*.</span></span> <span data-ttu-id="4116c-129">Ao especificar apenas determinados tipos de arquivo, seu serviço só aparece quando esses tipos de arquivo foram selecionados.</span><span class="sxs-lookup"><span data-stu-id="4116c-129">By specifying only certain file types, your service only appears when those file types have been selected.</span></span> <span data-ttu-id="4116c-130">Se mais de um tipo de arquivo tiver sido selecionado, seu serviço será exibido se qualquer um desses tipos de arquivo tiver suporte do seu serviço.</span><span class="sxs-lookup"><span data-stu-id="4116c-130">If more than one file type has been selected, your service appears if any of those file types are supported by your service.</span></span> <span data-ttu-id="4116c-131">Se você quiser especificar vários tipos de arquivo, separe-os na lista com pontos-e-vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4116c-131">If you want to specify multiple file types, separate them in the list with semicolons.</span></span> <span data-ttu-id="4116c-132">Por exemplo, *\* . jpg; \* . BMP*.</span><span class="sxs-lookup"><span data-stu-id="4116c-132">For example, *\*.jpg; \*.bmp*.</span></span> |



 

<span data-ttu-id="4116c-133">Veja a seguir um exemplo completo de um serviço de processamento de fotos intitulado "myfornecedor".</span><span class="sxs-lookup"><span data-stu-id="4116c-133">The following is a complete example for a photo processing service entitled "MyProvider."</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

<span data-ttu-id="4116c-134">Quando a URL do serviço é chamada, dois valores são adicionados ao final da URL – LCID e LangID.</span><span class="sxs-lookup"><span data-stu-id="4116c-134">When the URL of your service is called, two values are added to the end of the URL—lcid and langid.</span></span> <span data-ttu-id="4116c-135">Por exemplo, a cadeia de caracteres de URL para o exemplo acima pode ser https: \/ /www.MyProvider.com/Intro.htm? lcid = 1033&LangID = 1033.</span><span class="sxs-lookup"><span data-stu-id="4116c-135">For example, the URL string for the example above might be https:\//www.MyProvider.com/Intro.htm?lcid=1033&langid=1033.</span></span> <span data-ttu-id="4116c-136">Essas variáveis são usadas para informações de idioma e localização.</span><span class="sxs-lookup"><span data-stu-id="4116c-136">These variables are used for language and localization information.</span></span>

-   <span data-ttu-id="4116c-137">**LCID** é usado para informar o servidor do país/região do cliente e as configurações de idioma.</span><span class="sxs-lookup"><span data-stu-id="4116c-137">**lcid** is used to inform the server of the client's country/region and language settings.</span></span> <span data-ttu-id="4116c-138">Ele não é usado para determinar o idioma da interface do usuário do cliente, mas é usado para determinar o formato adequado para moeda, data e hora e outros dados específicos da região.</span><span class="sxs-lookup"><span data-stu-id="4116c-138">It is not used to determine the language of the client's UI, but is used to determine the proper format for currency, date and time, and other region-specific data.</span></span>
-   <span data-ttu-id="4116c-139">o **LangID** é usado para informar o servidor da configuração de idioma padrão do cliente para que ele possa usar o idioma apropriado na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4116c-139">**langid** is used to inform the server of the client's default language setting so that it can use the proper language in the UI.</span></span>

 

 




