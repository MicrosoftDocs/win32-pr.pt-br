---
title: Acesso à biblioteca
description: Acesso à biblioteca
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, acesso
- biblioteca, acessando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292158"
---
# <a name="library-access"></a><span data-ttu-id="a0687-112">Acesso à biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0687-112">Library Access</span></span>

<span data-ttu-id="a0687-113">As propriedades e métodos do modelo de objeto do Windows Media Player que acessam a biblioteca exigem acesso somente leitura ou de leitura/gravação ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a0687-113">Properties and methods of the Windows Media Player object model that access the library require either read-only or read/write access to the database.</span></span> <span data-ttu-id="a0687-114">A biblioteca contém informações que alguns usuários desejam manter particulares e que devem ser acessados ou alterados somente com seu consentimento.</span><span class="sxs-lookup"><span data-stu-id="a0687-114">The library contains information that some users want to keep private and that should be accessed or altered only with their consent.</span></span>

<span data-ttu-id="a0687-115">Para o Windows Media Player 9 Series ou posterior, você pode determinar programaticamente o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="a0687-115">For Windows Media Player 9 Series or later, you can programmatically determine access level.</span></span> <span data-ttu-id="a0687-116">Para determinar o nível atual de acesso concedido ao seu código, recupere as *configurações*. Propriedade **mediaAccessRights** .</span><span class="sxs-lookup"><span data-stu-id="a0687-116">To determine the current level of access granted to your code, retrieve the *Settings*.**mediaAccessRights** property.</span></span> <span data-ttu-id="a0687-117">Essa propriedade retorna "None", "Read" ou "Full" (leitura/gravação).</span><span class="sxs-lookup"><span data-stu-id="a0687-117">That property returns "none", "read", or "full" (read/write).</span></span> <span data-ttu-id="a0687-118">Para solicitar direitos de acesso específicos, chame as *configurações*. método **requestMediaAccessRights** , passando um parâmetro que especifica o nível que você está solicitando.</span><span class="sxs-lookup"><span data-stu-id="a0687-118">To request specific access rights, call the *Settings*.**requestMediaAccessRights** method, passing a parameter that specifies the level you are requesting.</span></span> <span data-ttu-id="a0687-119">O método exibe uma mensagem para o usuário explicando o nível de acesso solicitado e retorna um valor **booliano** que indica se o acesso foi concedido.</span><span class="sxs-lookup"><span data-stu-id="a0687-119">The method displays a message to the user explaining the requested level of access, and returns a **Boolean** value indicating whether the access was granted.</span></span>

<span data-ttu-id="a0687-120">Determinados direitos de acesso são concedidos automaticamente dependendo de onde seu código está sendo executado em relação ao computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0687-120">Certain access rights are granted automatically depending on where your code is running relative to the user's computer.</span></span>

-   <span data-ttu-id="a0687-121">Se a página da Web ou o programa estiver localizado no computador do usuário, os direitos de acesso completo serão concedidos por padrão.</span><span class="sxs-lookup"><span data-stu-id="a0687-121">If your webpage or program is located on the user's computer, full access rights are granted by default.</span></span>
-   <span data-ttu-id="a0687-122">Páginas da Web têm acesso de leitura ao *Player*. **currentMedia**, *Player*. **currentPlaylist** e *mídia*. **sourceURL** quando a página da Web está localizada em uma zona de segurança do Internet Explorer que é igual ou menos restrita do que a zona de segurança do item de mídia ou da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a0687-122">Web pages have read access to *Player*.**currentMedia**, *Player*.**currentPlaylist**, and *Media*.**sourceURL** when the webpage is located in an Internet Explorer security zone that is the same as or less restricted than the security zone of the media item or playlist.</span></span>

    <span data-ttu-id="a0687-123">Variando do menos restrito ao mais restrito, as zonas de segurança são a zona **confiável** (incluindo o computador local do usuário), a zona **da intranet local** , a zona da **Internet** e a zona **restrita** .</span><span class="sxs-lookup"><span data-stu-id="a0687-123">Ranging from least restricted to most restricted, the security zones are the **Trusted** zone (including the user's local computer), the **Local intranet** zone, the **Internet** zone, and the **Restricted** zone.</span></span>

    <span data-ttu-id="a0687-124">Por exemplo, uma página da Web na zona **da intranet local** tem direitos de acesso completo ao *Player*. **currentMedia** quando o item de mídia correspondente está na intranet local ou na Internet, mas os direitos de acesso devem ser solicitados para itens de mídia localizados no computador local de um usuário ou em um site na zona **confiável** .</span><span class="sxs-lookup"><span data-stu-id="a0687-124">For example, a webpage in the **Local intranet** zone has full access rights to *Player*.**currentMedia** when the corresponding media item is on the local intranet or the Internet, but access rights must be requested for media items located on a user's local computer or on a website in the **Trusted** zone.</span></span>

<span data-ttu-id="a0687-125">Você deve testar seu aplicativo baseado na Web ou no Windows em todas as zonas de segurança que ele pode encontrar.</span><span class="sxs-lookup"><span data-stu-id="a0687-125">You should test your Web-based or Windows-based application in all of the security zones it may encounter.</span></span> <span data-ttu-id="a0687-126">O aplicativo deve ser criado para lidar com a negação de uma solicitação de acesso corretamente.</span><span class="sxs-lookup"><span data-stu-id="a0687-126">The application should be designed to handle denial of an access request correctly.</span></span>

<span data-ttu-id="a0687-127">As versões do modelo de objeto do Windows Media Player anteriores ao Windows Media Player 9 Series não incluem **mediaAccessRights** ou **requestMediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="a0687-127">Windows Media Player object model versions prior to Windows Media Player 9 Series do not include **mediaAccessRights** or **requestMediaAccessRights**.</span></span> <span data-ttu-id="a0687-128">Essas versões anteriores do Windows Media Player permitem que o usuário defina níveis de acesso usando a caixa de diálogo **Opções** .</span><span class="sxs-lookup"><span data-stu-id="a0687-128">These earlier versions of Windows Media Player enable the user to set access levels using the **Options** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0687-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0687-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0687-130">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="a0687-130">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="a0687-131">**Trabalhando com a biblioteca**</span><span class="sxs-lookup"><span data-stu-id="a0687-131">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




