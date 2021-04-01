---
description: Este tópico descreve como seu aplicativo pode especificar qual URL a ferramenta de recorte do Tablet PC deve obter ao capturar seu aplicativo.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Suporte a ferramentas de recorte no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829377"
---
# <a name="snipping-tool-support-in-windows-vista"></a><span data-ttu-id="9f3e9-103">Suporte a ferramentas de recorte no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f3e9-103">Snipping Tool Support in Windows Vista</span></span>

<span data-ttu-id="9f3e9-104">Este tópico descreve como seu aplicativo pode especificar qual URL a ferramenta de recorte do Tablet PC deve obter ao capturar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-104">This topic describes how your application can specify what URL the Tablet PC Snipping Tool should obtain when capturing your application.</span></span>

## <a name="specifying-the-url-via-registry-key"></a><span data-ttu-id="9f3e9-105">Especificando a URL por meio da chave do registro</span><span class="sxs-lookup"><span data-stu-id="9f3e9-105">Specifying the URL via Registry Key</span></span>

<span data-ttu-id="9f3e9-106">A ferramenta de recorte permite que os usuários capturem um recorte (captura de tela) de qualquer objeto na tela e, em seguida, anotem, salvem ou compartilhem a imagem.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-106">Snipping Tool allows users to capture a snip (screen shot) of any object on the screen and then annotate, save, or share the image.</span></span> <span data-ttu-id="9f3e9-107">Quando os dados são salvos em formato HTML, ou quando são enviados a um cliente de email que dá suporte a HTML embutido, a ferramenta de recorte pode adicionar uma URL ao recorte se o aplicativo fornecer informações sobre como obter a URL.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-107">When the data is saved in HTML format, or when it is sent to an email client that supports inline HTML, Snipping Tool can add a URL to the snip if the application provides information on how to obtain the URL.</span></span>

<span data-ttu-id="9f3e9-108">A ferramenta de recorte Obtém a URL por meio de objetos de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-108">Snipping Tool obtains the URL via accessibility objects.</span></span> <span data-ttu-id="9f3e9-109">Os aplicativos devem especificar as informações necessárias nas seguintes chaves do registro:</span><span class="sxs-lookup"><span data-stu-id="9f3e9-109">Applications should specify the necessary information under the following registry keys:</span></span>

<span data-ttu-id="9f3e9-110">HKLM \\ software \\ Microsoft \\ Windows \\ Tablet \\ \\ reLinkFingerprintstion Tool,</span><span class="sxs-lookup"><span data-stu-id="9f3e9-110">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints,</span></span>

<span data-ttu-id="9f3e9-111">E deve criar uma subchave cujo nome seja o mesmo da classe de janela da qual o link deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-111">And should create a subkey whose name is the same as the window class from which the link should be obtained.</span></span> <span data-ttu-id="9f3e9-112">O nome da classe da janela deve ser a janela mais alta do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-112">The window class name should be the topmost window of the application.</span></span>

<span data-ttu-id="9f3e9-113">HKLM \\ software \\ Microsoft \\ Windows \\ Tablet \\ \\ LinkFingerprints Tool\\<Window Class Name></span><span class="sxs-lookup"><span data-stu-id="9f3e9-113">HKLM\\Software\\Microsoft\\Windows\\TabletPC\\Snipping Tool\\LinkFingerprints\\<Window Class Name></span></span>

### <a name="window-class-key-details"></a><span data-ttu-id="9f3e9-114">Detalhes da chave da classe Window</span><span class="sxs-lookup"><span data-stu-id="9f3e9-114">Window Class Key Details</span></span>

<span data-ttu-id="9f3e9-115">Na chave de classe da janela, os valores apropriados devem ser definidos para indicar que a ferramenta de recorte deve detectar o objeto de acessibilidade correto.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-115">Under the window class key, the appropriate values should be set in order to indicate Snipping Tool should detect the correct accessibility object.</span></span>



| <span data-ttu-id="9f3e9-116">VALOR</span><span class="sxs-lookup"><span data-stu-id="9f3e9-116">VALUE</span></span>                        | <span data-ttu-id="9f3e9-117">TYPE</span><span class="sxs-lookup"><span data-stu-id="9f3e9-117">TYPE</span></span>                  | <span data-ttu-id="9f3e9-118">MASCARA</span><span class="sxs-lookup"><span data-stu-id="9f3e9-118">MASK</span></span>            | <span data-ttu-id="9f3e9-119">INFORMAÇÕES ARMAZENADAS</span><span class="sxs-lookup"><span data-stu-id="9f3e9-119">INFORMATION STORED</span></span>                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| <span data-ttu-id="9f3e9-120">Mask</span><span class="sxs-lookup"><span data-stu-id="9f3e9-120">Mask</span></span><br/>              | <span data-ttu-id="9f3e9-121">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="9f3e9-121">REG\_DWORD</span></span><br/> |                 | <span data-ttu-id="9f3e9-122">Indica quais dos campos a seguir verificar</span><span class="sxs-lookup"><span data-stu-id="9f3e9-122">Indicates which of the following fields to check</span></span><br/> |
| <span data-ttu-id="9f3e9-123">Nome</span><span class="sxs-lookup"><span data-stu-id="9f3e9-123">Name</span></span><br/>              | <span data-ttu-id="9f3e9-124">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="9f3e9-124">REG\_SZ</span></span><br/>    | <span data-ttu-id="9f3e9-125">0x02</span><span class="sxs-lookup"><span data-stu-id="9f3e9-125">0x02</span></span><br/> | <span data-ttu-id="9f3e9-126">Nome de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9f3e9-126">Accessibility name</span></span><br/>                               |
| <span data-ttu-id="9f3e9-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f3e9-127">Description</span></span><br/>       | <span data-ttu-id="9f3e9-128">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="9f3e9-128">REG\_SZ</span></span><br/>    | <span data-ttu-id="9f3e9-129">0x04</span><span class="sxs-lookup"><span data-stu-id="9f3e9-129">0x04</span></span><br/> | <span data-ttu-id="9f3e9-130">Descrição da acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9f3e9-130">Accessibility description</span></span><br/>                        |
| <span data-ttu-id="9f3e9-131">Função</span><span class="sxs-lookup"><span data-stu-id="9f3e9-131">Role</span></span><br/>              | <span data-ttu-id="9f3e9-132">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="9f3e9-132">REG\_DWORD</span></span><br/> | <span data-ttu-id="9f3e9-133">0x08</span><span class="sxs-lookup"><span data-stu-id="9f3e9-133">0x08</span></span><br/> | <span data-ttu-id="9f3e9-134">Função de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9f3e9-134">Accessibility role</span></span><br/>                               |
| <span data-ttu-id="9f3e9-135">ParentName</span><span class="sxs-lookup"><span data-stu-id="9f3e9-135">ParentName</span></span><br/>        | <span data-ttu-id="9f3e9-136">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="9f3e9-136">REG\_SZ</span></span><br/>    | <span data-ttu-id="9f3e9-137">0x10</span><span class="sxs-lookup"><span data-stu-id="9f3e9-137">0x10</span></span><br/> | <span data-ttu-id="9f3e9-138">Nome de acessibilidade do pai</span><span class="sxs-lookup"><span data-stu-id="9f3e9-138">Accessibility name of parent</span></span><br/>                     |
| <span data-ttu-id="9f3e9-139">Paivalue</span><span class="sxs-lookup"><span data-stu-id="9f3e9-139">ParentValue</span></span><br/>       | <span data-ttu-id="9f3e9-140">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="9f3e9-140">REG\_SZ</span></span><br/>    | <span data-ttu-id="9f3e9-141">0x20</span><span class="sxs-lookup"><span data-stu-id="9f3e9-141">0x20</span></span><br/> | <span data-ttu-id="9f3e9-142">Valor de acessibilidade do pai</span><span class="sxs-lookup"><span data-stu-id="9f3e9-142">Accessibility value of parent</span></span><br/>                    |
| <span data-ttu-id="9f3e9-143">ParentRole</span><span class="sxs-lookup"><span data-stu-id="9f3e9-143">ParentRole</span></span><br/>        | <span data-ttu-id="9f3e9-144">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="9f3e9-144">REG\_DWORD</span></span><br/> | <span data-ttu-id="9f3e9-145">0x40</span><span class="sxs-lookup"><span data-stu-id="9f3e9-145">0x40</span></span><br/> | <span data-ttu-id="9f3e9-146">Função de acessibilidade do pai</span><span class="sxs-lookup"><span data-stu-id="9f3e9-146">Accessibility role of parent</span></span><br/>                     |
| <span data-ttu-id="9f3e9-147">ParentDescription</span><span class="sxs-lookup"><span data-stu-id="9f3e9-147">ParentDescription</span></span><br/> | <span data-ttu-id="9f3e9-148">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="9f3e9-148">REG\_SZ</span></span><br/>    | <span data-ttu-id="9f3e9-149">0x80</span><span class="sxs-lookup"><span data-stu-id="9f3e9-149">0x80</span></span><br/> | <span data-ttu-id="9f3e9-150">Descrição de acessibilidade do pai</span><span class="sxs-lookup"><span data-stu-id="9f3e9-150">Accessibility description of parent</span></span><br/>              |



 

<span data-ttu-id="9f3e9-151">Além disso, se o valor de bit de máscara 0x1 for definido, a URL deverá ser extraída do nome de acessibilidade; caso contrário, a URL deve ser retirada do valor de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-151">Additionally, if the mask bit value 0x1 is set, then the URL should be taken from the accessibility name; otherwise, the URL should be taken from the accessibility value.</span></span>

<span data-ttu-id="9f3e9-152">Se o aplicativo usar cadeias de caracteres localizadas para os valores de REG \_ sz acima, a cadeia de caracteres deverá ser fornecida como uma cadeia indireta usando o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="9f3e9-152">If the application uses localized strings for the REG\_SZ values above, the string should be provided as an indirect string by using the following format:</span></span>

<span data-ttu-id="9f3e9-153">@filename, recurso</span><span class="sxs-lookup"><span data-stu-id="9f3e9-153">@filename,resource</span></span>

<span data-ttu-id="9f3e9-154">A cadeia de caracteres é extraída do arquivo chamado, usando o valor do recurso como um localizador.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-154">The string is extracted from the file named, using the resource value as a locator.</span></span> <span data-ttu-id="9f3e9-155">Se o valor do recurso for zero ou maior, o número se tornará o índice da cadeia de caracteres no arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-155">If the resource value is zero or greater, the number becomes the index of the string in the binary file.</span></span> <span data-ttu-id="9f3e9-156">Se o número for negativo, ele se tornará um identificador de recurso (ID).</span><span class="sxs-lookup"><span data-stu-id="9f3e9-156">If the number is negative, it becomes a resource identifier (ID).</span></span>

> [!Note]  
> <span data-ttu-id="9f3e9-157">As constantes de função podem ser encontradas em OleAcc. h na SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-157">Role constants can be found in oleacc.h in the Windows SDK.</span></span> <span data-ttu-id="9f3e9-158">Os valores de registro descritos são específicos do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-158">The registry values described are specific to Windows Vista.</span></span>

 

 

 




