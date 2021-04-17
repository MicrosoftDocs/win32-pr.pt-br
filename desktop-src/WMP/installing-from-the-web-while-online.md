---
title: Instalando a partir da Web enquanto estiver online
description: Instalando a partir da Web enquanto estiver online
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Armazenamentos online do Windows Media Player, instalando da Web enquanto estiver online
- lojas online, instalando da Web enquanto estiver online
- Digite 1 lojas online, instalando da Web enquanto estiver online
- Digite 2 lojas online, instalando da Web enquanto estiver online
- Lojas online do Windows Media Player, instalações online da Web
- lojas online, instalações online da Web
- Digite 1 lojas online, instalações online da Web
- Digite 2 lojas online, instalações online da Web
- Instalando lojas online da Web enquanto estiver online
- instalações online de lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770487"
---
# <a name="installing-from-the-web-while-online"></a><span data-ttu-id="76d03-113">Instalando a partir da Web enquanto estiver online</span><span class="sxs-lookup"><span data-stu-id="76d03-113">Installing from the Web While Online</span></span>

<span data-ttu-id="76d03-114">Os usuários podem instalar o Windows Media Player como um download da Web enquanto estiver conectado à Internet.</span><span class="sxs-lookup"><span data-stu-id="76d03-114">Users can install Windows Media Player as a Web download while connected to the Internet.</span></span> <span data-ttu-id="76d03-115">Nesse caso, a Microsoft pode configurar a loja online inicial que você especificar.</span><span class="sxs-lookup"><span data-stu-id="76d03-115">In this case, Microsoft can configure the initial online store that you specify.</span></span>

<span data-ttu-id="76d03-116">Para redistribuir o Windows Media Player dessa maneira, use a seguinte URL:</span><span class="sxs-lookup"><span data-stu-id="76d03-116">To redistribute Windows Media Player in this manner, use the following URL:</span></span>

<span data-ttu-id="76d03-117"> https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*versão*&userlocalize =*LocalId*&Service =*Key*</span><span class="sxs-lookup"><span data-stu-id="76d03-117">https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*</span></span>

<span data-ttu-id="76d03-118">Na URL anterior, defina *chave* como o nome da chave para sua loja online e defina *LocaleID* como o identificador da localidade onde sua loja fornece o serviço.</span><span class="sxs-lookup"><span data-stu-id="76d03-118">In the preceding URL, set *key* to the key name for your online store, and set *localeID* to the identifier of the locale where your store provides service.</span></span> <span data-ttu-id="76d03-119">Defina a *versão* como 2 para Windows Media Player 11 no Windows XP ou 1 para Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="76d03-119">Set *version* to 2 for Windows Media Player 11 on Windows XP or 1 for Windows Media Player 10.</span></span> <span data-ttu-id="76d03-120">A URL instala o Windows Media Player e define o repositório ativo inicial para aquele especificado por *chave*.</span><span class="sxs-lookup"><span data-stu-id="76d03-120">The URL installs Windows Media Player and sets the initial active store to the one specified by *key*.</span></span>

<span data-ttu-id="76d03-121">O exemplo a seguir mostra uma URL que instala o Windows Media Player 11 e define o Proseware como o repositório ativo inicial.</span><span class="sxs-lookup"><span data-stu-id="76d03-121">The following example shows a URL that installs Windows Media Player 11 and sets Proseware as the initial active store.</span></span> <span data-ttu-id="76d03-122">O valor de 409 para *LocaleID* indica que o Proseware fornece serviço no Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="76d03-122">The value of 409 for *localeID* indicates that Proseware provides service in the United States.</span></span>

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

<span data-ttu-id="76d03-123">Se o documento do serviceInfo para a loja online incluir um elemento de instalação, a instalação do Windows Media Player personalizará o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="76d03-123">If the ServiceInfo document for the online store includes an Install element, Windows Media Player setup will customize the setup process.</span></span> <span data-ttu-id="76d03-124">Usando os valores de atributo, a instalação exibe o contrato de licença de usuário final (EULA) e sua declaração de privacidade, além de recuperar e instalar o arquivo. cab no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="76d03-124">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="76d03-125">Por exemplo, você pode usar esse recurso para instalar a versão mais recente de um objeto COM que sua loja online requer.</span><span class="sxs-lookup"><span data-stu-id="76d03-125">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76d03-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76d03-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d03-127">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="76d03-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="76d03-128">**Elemento de instalação**</span><span class="sxs-lookup"><span data-stu-id="76d03-128">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="76d03-129">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="76d03-129">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="76d03-130">**Configurando a loja online inicial**</span><span class="sxs-lookup"><span data-stu-id="76d03-130">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




