---
title: Atributos de identificação de usuário
description: A identidade do usuário que solicita autenticação é fornecida para as DLLs de extensão do NPS em vários atributos diferentes.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Atributos, identificação de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779388"
---
# <a name="user-identification-attributes"></a><span data-ttu-id="1b6ad-104">Atributos de identificação de usuário</span><span class="sxs-lookup"><span data-stu-id="1b6ad-104">User Identification Attributes</span></span>

> [!Note]  
> <span data-ttu-id="1b6ad-105">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1b6ad-106">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1b6ad-107">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1b6ad-108">A identidade do usuário que solicita autenticação é fornecida para as DLLs de extensão do NPS em vários atributos diferentes.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-108">The identity of the user requesting authentication is supplied to the NPS Extension DLLs in a number of different attributes.</span></span>

-   <span data-ttu-id="1b6ad-109">**ratUserName**</span><span class="sxs-lookup"><span data-stu-id="1b6ad-109">**ratUserName**</span></span>
-   <span data-ttu-id="1b6ad-110">**ratStrippedUserName**</span><span class="sxs-lookup"><span data-stu-id="1b6ad-110">**ratStrippedUserName**</span></span>
-   <span data-ttu-id="1b6ad-111">**ratFQUserName**</span><span class="sxs-lookup"><span data-stu-id="1b6ad-111">**ratFQUserName**</span></span>

<span data-ttu-id="1b6ad-112">Cada atributo fornece a identidade do usuário em um formato diferente.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-112">Each attribute provides the user identity in a different format.</span></span> <span data-ttu-id="1b6ad-113">Em geral, os desenvolvedores devem usar o **ratStrippedUserName**.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-113">In general, developers should use **ratStrippedUserName**.</span></span> <span data-ttu-id="1b6ad-114">Os usos dos atributos **ratUserName** e **ratFQUserName** são mais especializados.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-114">The uses of the **ratUserName** and **ratFQUserName** attributes are more specialized.</span></span>

> [!Note]  
> <span data-ttu-id="1b6ad-115">O atributo User-Password, **ratUserPassword**, já foi descriptografado quando é enviado para a DLL de extensão e pode ser usado nesse formulário.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-115">The User-Password attribute, **ratUserPassword**, has already been decrypted when it is sent to the extension DLL and is usable in that form.</span></span>

 

## <a name="ratusername"></a><span data-ttu-id="1b6ad-116">ratUserName</span><span class="sxs-lookup"><span data-stu-id="1b6ad-116">ratUserName</span></span>

<span data-ttu-id="1b6ad-117">O atributo **ratUserName** contém o nome que foi realmente enviado "pela transmissão".</span><span class="sxs-lookup"><span data-stu-id="1b6ad-117">The **ratUserName** attribute contains the name that was actually sent "over the wire."</span></span> <span data-ttu-id="1b6ad-118">O NPS não, de nenhuma forma, processou ou validou o conteúdo deste atributo.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-118">NPS has not, in any way, processed or validated the contents of this attribute.</span></span> <span data-ttu-id="1b6ad-119">Esse atributo pode não estar disponível porque o usuário pode ter sido identificado por meio de um meio, como a ID do chamador.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-119">This attribute may not be available at all because the user may have been identified through a means such as caller ID.</span></span>

<span data-ttu-id="1b6ad-120">Ao usar [**RadiusExtensionProcess/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), se esse atributo estiver disponível, ele estará disponível somente no ponto de plug-in DLL da extensão de autenticação.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-120">When using [**RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), if this attribute is available, it is available only at the Authentication Extension DLL plug-in point.</span></span> <span data-ttu-id="1b6ad-121">O atributo **ratUserName** não está disponível no ponto de plug-in DLL da extensão de autorização porque, em DLLs de extensão de autorização, as funções **RadiusExtensionProcess/ex** veem apenas os atributos de "saída".</span><span class="sxs-lookup"><span data-stu-id="1b6ad-121">The **ratUserName** attribute is not available at the Authorization Extension DLL plug-in point because in Authorization Extension DLLs the **RadiusExtensionProcess/Ex** functions see only the "outbound" attributes.</span></span>

<span data-ttu-id="1b6ad-122">Ao usar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), se esse atributo estiver disponível, ele estará disponível no ponto de plug-in DLL de extensão de autenticação e no ponto de plug-in DLL de extensão de autorização.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-122">When using [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), if this attribute is available, it is available at both the Authentication Extension DLL plug-in point and the Authorization Extension DLL plug-in point.</span></span>

## <a name="ratstrippedusername"></a><span data-ttu-id="1b6ad-123">ratStrippedUserName</span><span class="sxs-lookup"><span data-stu-id="1b6ad-123">ratStrippedUserName</span></span>

<span data-ttu-id="1b6ad-124">O **ratStrippedUserName** é a identidade do usuário após "remoção de realm".</span><span class="sxs-lookup"><span data-stu-id="1b6ad-124">The **ratStrippedUserName** is the user's identity after "realm stripping."</span></span> <span data-ttu-id="1b6ad-125">Para obter mais informações sobre a remoção de realm, consulte o tópico [nomes de territórios](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) em http: \\ \\ technet2.Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-125">For more information on realm stripping, see the [Realm names](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) topic on http:\\\\technet2.microsoft.com.</span></span>

<span data-ttu-id="1b6ad-126">Esse atributo pode estar presente no ponto de plug-in de DLL de extensão de autenticação, no ponto de plug-in de DLL de extensão de autorização ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-126">This attribute may be present at the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="1b6ad-127">É garantido que esse atributo tenha o formato:</span><span class="sxs-lookup"><span data-stu-id="1b6ad-127">This attribute is guaranteed to have the format:</span></span>

<span data-ttu-id="1b6ad-128">\*Nome de usuário do domínio \*\*\*\\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1b6ad-128">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="1b6ad-129">Em que *domínio* é o nome de domínio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-129">Where *Domain* is the NetBIOS domain name.</span></span>

## <a name="ratfqusername"></a><span data-ttu-id="1b6ad-130">ratFQUserName</span><span class="sxs-lookup"><span data-stu-id="1b6ad-130">ratFQUserName</span></span>

<span data-ttu-id="1b6ad-131">O atributo **ratFQUserName** é o nome de usuário "totalmente qualificado".</span><span class="sxs-lookup"><span data-stu-id="1b6ad-131">The **ratFQUserName** attribute is the "fully qualified" user name.</span></span>

<span data-ttu-id="1b6ad-132">Esse atributo pode estar presente no ponto de plug-in de DLL de extensão de autenticação, no ponto de plug-in de DLL de extensão de autorização ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-132">This attribute may be present in the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="1b6ad-133">No entanto, o formato do atributo pode ser diferente entre os dois pontos de plug-in.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-133">However, the format of the attribute may differ between the two plug-in points.</span></span> <span data-ttu-id="1b6ad-134">No ponto de plug-in de DLL da extensão de autenticação, esse atributo sempre estará no formato:</span><span class="sxs-lookup"><span data-stu-id="1b6ad-134">At the Authentication Extension DLL plug-in point, this attribute will always be of the form:</span></span>

<span data-ttu-id="1b6ad-135">\*Nome de usuário do domínio \*\*\*\\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1b6ad-135">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="1b6ad-136">O formato do atributo **ratFQUserName** no ponto de plug-in de dll da extensão de autorização depende se o usuário é um usuário Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-136">The format of the **ratFQUserName** attribute at the Authorization Extension DLL plug-in point depends on whether the user is an Active Directory user.</span></span>

-   <span data-ttu-id="1b6ad-137">Se o usuário for um usuário local, **ratFQUserName** terá o mesmo formato para o ponto de plug-in DLL da extensão de autenticação:</span><span class="sxs-lookup"><span data-stu-id="1b6ad-137">If the user is a local user **ratFQUserName** has the same format as for the Authentication Extension DLL plug-in point:</span></span>

    <span data-ttu-id="1b6ad-138">\*Nome de usuário do domínio \*\*\*\\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1b6ad-138">*Domain ***\\*** UserName*</span></span>

    <span data-ttu-id="1b6ad-139">.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-139">.</span></span>

-   <span data-ttu-id="1b6ad-140">Se o usuário for um usuário Active Directory, **ratFQUserName** poderá conter o nome do usuário no formato "canônico".</span><span class="sxs-lookup"><span data-stu-id="1b6ad-140">If the user is an Active Directory user, **ratFQUserName** may contain the user's name in "canonical" format.</span></span> <span data-ttu-id="1b6ad-141">O formato canônico é o formato usado pelo Active Directory para identificar o usuário.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-141">Canonical format is the format used by the Active Directory to identify the user.</span></span> <span data-ttu-id="1b6ad-142">É o caminho da raiz da árvore de Active Directory e inclui a UO (unidade organizacional) do usuário.</span><span class="sxs-lookup"><span data-stu-id="1b6ad-142">It is the path from the root of the Active Directory tree, and includes the user's Organizational Unit (OU).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b6ad-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b6ad-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b6ad-144">Configurando as DLLs de extensão</span><span class="sxs-lookup"><span data-stu-id="1b6ad-144">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[<span data-ttu-id="1b6ad-145">Invocando as DLLs de extensão</span><span class="sxs-lookup"><span data-stu-id="1b6ad-145">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 