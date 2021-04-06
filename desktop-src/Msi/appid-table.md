---
description: A tabela AppId ou a tabela de registro especifica que o instalador configura e registra servidores DCOM para executar uma das ações a seguir durante uma instalação.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Tabela AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828075"
---
# <a name="appid-table"></a><span data-ttu-id="8ab8a-103">Tabela AppId</span><span class="sxs-lookup"><span data-stu-id="8ab8a-103">AppId Table</span></span>

<span data-ttu-id="8ab8a-104">A tabela AppId ou a [tabela de registro](registry-table.md) especifica que o instalador configura e registra servidores DCOM para executar uma das ações a seguir durante uma instalação.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-104">The AppId table or the [Registry table](registry-table.md) specifies that the installer configure and register DCOM servers to do one of the following during an installation.</span></span>

-   <span data-ttu-id="8ab8a-105">Execute o servidor DCOM com uma identidade diferente do usuário que está ativando o servidor.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-105">Run the DCOM server under a different identity than the user activating the server.</span></span> <span data-ttu-id="8ab8a-106">Por exemplo, para configurar um servidor DCOM para sempre executar como um usuário interativo ou como um usuário predefinido.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-106">For example, to configure a DCOM server to always run as an interactive user or as a predefined user.</span></span>
-   <span data-ttu-id="8ab8a-107">Execute o servidor DCOM como um serviço.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-107">Run the DCOM server as a service.</span></span>
-   <span data-ttu-id="8ab8a-108">Configure o acesso de segurança padrão para o servidor DCOM.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-108">Configure the default security access for the DCOM server.</span></span>
-   <span data-ttu-id="8ab8a-109">Registre o servidor DCOM de modo que ele seja ativado em um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-109">Register the DCOM server such that it is activated on a different computer.</span></span>

<span data-ttu-id="8ab8a-110">Essa tabela é processada na instalação do componente associado ao servidor DCOM na \_ coluna componente da [tabela classe](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ab8a-110">This table is processed at the installation of the component associated with the DCOM server in the \_Component column of the [Class table](class-table.md).</span></span> <span data-ttu-id="8ab8a-111">Uma AppId não é anunciada.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-111">An AppId is not advertised.</span></span>

<span data-ttu-id="8ab8a-112">A tabela AppId tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-112">The AppId table has the following columns.</span></span>



| <span data-ttu-id="8ab8a-113">Coluna</span><span class="sxs-lookup"><span data-stu-id="8ab8a-113">Column</span></span>               | <span data-ttu-id="8ab8a-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ab8a-114">Type</span></span>                       | <span data-ttu-id="8ab8a-115">Chave</span><span class="sxs-lookup"><span data-stu-id="8ab8a-115">Key</span></span> | <span data-ttu-id="8ab8a-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="8ab8a-116">Nullable</span></span> |
|----------------------|----------------------------|-----|----------|
| <span data-ttu-id="8ab8a-117">AppId</span><span class="sxs-lookup"><span data-stu-id="8ab8a-117">AppId</span></span>                | [<span data-ttu-id="8ab8a-118">GUID</span><span class="sxs-lookup"><span data-stu-id="8ab8a-118">GUID</span></span>](guid.md)           | <span data-ttu-id="8ab8a-119">S</span><span class="sxs-lookup"><span data-stu-id="8ab8a-119">Y</span></span>   | <span data-ttu-id="8ab8a-120">N</span><span class="sxs-lookup"><span data-stu-id="8ab8a-120">N</span></span>        |
| <span data-ttu-id="8ab8a-121">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="8ab8a-121">RemoteServerName</span></span>     | [<span data-ttu-id="8ab8a-122">Binário</span><span class="sxs-lookup"><span data-stu-id="8ab8a-122">Formatted</span></span>](formatted.md) | <span data-ttu-id="8ab8a-123">N</span><span class="sxs-lookup"><span data-stu-id="8ab8a-123">N</span></span>   | <span data-ttu-id="8ab8a-124">S</span><span class="sxs-lookup"><span data-stu-id="8ab8a-124">Y</span></span>        |
| <span data-ttu-id="8ab8a-125">LocalService</span><span class="sxs-lookup"><span data-stu-id="8ab8a-125">LocalService</span></span>         | [<span data-ttu-id="8ab8a-126">Text</span><span class="sxs-lookup"><span data-stu-id="8ab8a-126">Text</span></span>](text.md)           | <span data-ttu-id="8ab8a-127">N</span><span class="sxs-lookup"><span data-stu-id="8ab8a-127">N</span></span>   | <span data-ttu-id="8ab8a-128">S</span><span class="sxs-lookup"><span data-stu-id="8ab8a-128">Y</span></span>        |
| <span data-ttu-id="8ab8a-129">Serviceparameters</span><span class="sxs-lookup"><span data-stu-id="8ab8a-129">ServiceParameters</span></span>    | [<span data-ttu-id="8ab8a-130">Text</span><span class="sxs-lookup"><span data-stu-id="8ab8a-130">Text</span></span>](text.md)           | <span data-ttu-id="8ab8a-131">N</span><span class="sxs-lookup"><span data-stu-id="8ab8a-131">N</span></span>   | <span data-ttu-id="8ab8a-132">S</span><span class="sxs-lookup"><span data-stu-id="8ab8a-132">Y</span></span>        |
| <span data-ttu-id="8ab8a-133">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="8ab8a-133">DllSurrogate</span></span>         | [<span data-ttu-id="8ab8a-134">Text</span><span class="sxs-lookup"><span data-stu-id="8ab8a-134">Text</span></span>](text.md)           | <span data-ttu-id="8ab8a-135">N</span><span class="sxs-lookup"><span data-stu-id="8ab8a-135">N</span></span>   | <span data-ttu-id="8ab8a-136">S</span><span class="sxs-lookup"><span data-stu-id="8ab8a-136">Y</span></span>        |
| <span data-ttu-id="8ab8a-137">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="8ab8a-137">ActivateAtStorage</span></span>    | [<span data-ttu-id="8ab8a-138">Inteiro</span><span class="sxs-lookup"><span data-stu-id="8ab8a-138">Integer</span></span>](integer.md)     | <span data-ttu-id="8ab8a-139">N</span><span class="sxs-lookup"><span data-stu-id="8ab8a-139">N</span></span>   | <span data-ttu-id="8ab8a-140">S</span><span class="sxs-lookup"><span data-stu-id="8ab8a-140">Y</span></span>        |
| <span data-ttu-id="8ab8a-141">RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="8ab8a-141">RunAsInteractiveUser</span></span> | [<span data-ttu-id="8ab8a-142">Inteiro</span><span class="sxs-lookup"><span data-stu-id="8ab8a-142">Integer</span></span>](integer.md)     | <span data-ttu-id="8ab8a-143">N</span><span class="sxs-lookup"><span data-stu-id="8ab8a-143">N</span></span>   | <span data-ttu-id="8ab8a-144">S</span><span class="sxs-lookup"><span data-stu-id="8ab8a-144">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8ab8a-145">Colunas</span><span class="sxs-lookup"><span data-stu-id="8ab8a-145">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8ab8a-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span><span class="sxs-lookup"><span data-stu-id="8ab8a-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span></span>
</dt> <dd>

<span data-ttu-id="8ab8a-147">A coluna AppId da [tabela de classes](class-table.md) é uma chave estrangeira nessa coluna da tabela AppID.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-147">The AppId column of the [Class table](class-table.md) is a foreign key into this column of the AppId table.</span></span> <span data-ttu-id="8ab8a-148">Esta coluna contém o valor AppId que será gravado sob o CLSID e criará a chave de GUID AppId em HKCR \\ AppID.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-148">This column contains the AppId value that will be written under the CLSID and creates the AppId GUID key under HKCR\\AppId.</span></span>

</dd> <dt>

<span data-ttu-id="8ab8a-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="8ab8a-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span></span>
</dt> <dd>

<span data-ttu-id="8ab8a-150">Esta coluna contém o valor de "RemoteServerName" = <xxxx> que será gravado em HKCR \\ AppID \\ {AppID} \\ .</span><span class="sxs-lookup"><span data-stu-id="8ab8a-150">This column contains the value of "RemoteServerName"=<xxxx> that will be written under HKCR\\AppID\\{AppID}\\ .</span></span>

</dd> <dt>

<span data-ttu-id="8ab8a-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span><span class="sxs-lookup"><span data-stu-id="8ab8a-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span></span>
</dt> <dd>

<span data-ttu-id="8ab8a-152">Esta coluna contém o valor de LocalService que será gravado em HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="8ab8a-152">This column contains the value of LocalService that will be written under HKCR\\AppID\\{<appid>} "LocalService"=<xxx>.</span></span>

</dd> <dt>

<span data-ttu-id="8ab8a-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>Serviceparameters</span><span class="sxs-lookup"><span data-stu-id="8ab8a-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span></span>
</dt> <dd>

<span data-ttu-id="8ab8a-154">Esta coluna contém o valor de Serviceparameters que será gravado em HKCR \\ AppID \\ {AppID>} "serviceparameters".</span><span class="sxs-lookup"><span data-stu-id="8ab8a-154">This column contains the value of ServiceParameters that will be written under HKCR\\AppID\\{appid>} "ServiceParameters".</span></span>

</dd> <dt>

<span data-ttu-id="8ab8a-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="8ab8a-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span></span>
</dt> <dd>

<span data-ttu-id="8ab8a-156">Esta coluna contém o valor de DllSurrogate que será gravado em HKCR \\ AppID \\ { <appid> } "DllSurrogate" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="8ab8a-156">This column contains the value of DllSurrogate that will be written under HKCR\\AppId\\{<appid>} "DllSurrogate"=<xxx>.</span></span> <span data-ttu-id="8ab8a-157">Se essa coluna estiver presente, ela normalmente será uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-157">If this column is present it will typically be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="8ab8a-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="8ab8a-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span></span>
</dt> <dd>

<span data-ttu-id="8ab8a-159">Um valor inteiro diferente de zero nesse campo faz com que Windows Installer grave \\ o HKCR AppID \\ { <appid> } "ActivateAtStorage" = "Y" no registro.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-159">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{<appid>} "ActivateAtStorage"="Y" into the registry.</span></span> <span data-ttu-id="8ab8a-160">Se o campo for deixado vazio ou tiver um valor igual a zero, nenhum valor será gravado.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-160">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> <dt>

<span data-ttu-id="8ab8a-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="8ab8a-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span></span>
</dt> <dd>

<span data-ttu-id="8ab8a-162">Um valor inteiro diferente de zero nesse campo faz com que Windows Installer grave o HKCR \\ AppID \\ {AppID>} "runas" = "usuário interativo" no registro.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-162">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{appid>} "RunAs"="Interactive User" into the registry.</span></span> <span data-ttu-id="8ab8a-163">Se o campo for deixado vazio ou tiver um valor igual a zero, nenhum valor será gravado.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-163">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ab8a-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ab8a-164">Remarks</span></span>

<span data-ttu-id="8ab8a-165">Essa tabela é usada pela ação [RegisterClassInfo](registerclassinfo-action.md) e [ação UnregisterClassInfo](unregisterclassinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="8ab8a-165">This table is used by the [RegisterClassInfo action](registerclassinfo-action.md) and [UnregisterClassInfo action](unregisterclassinfo-action.md).</span></span>

<span data-ttu-id="8ab8a-166">Observe que a tabela AppId não tem uma coluna para registrar um nome padrão.</span><span class="sxs-lookup"><span data-stu-id="8ab8a-166">Note that the AppId table does not have a column for registering a Default name.</span></span> <span data-ttu-id="8ab8a-167">Portanto, nos casos em que você precisa escrever um nome amigável de usuário como o valor de nome padrão, você deve registrar-se usando a [tabela de registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ab8a-167">Therefore in cases where you need to write a user friendly name as the Default name value, you must register using the [Registry table](registry-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="8ab8a-168">Validação</span><span class="sxs-lookup"><span data-stu-id="8ab8a-168">Validation</span></span>

<dl>

[<span data-ttu-id="8ab8a-169">ICE03</span><span class="sxs-lookup"><span data-stu-id="8ab8a-169">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8ab8a-170">ICE06</span><span class="sxs-lookup"><span data-stu-id="8ab8a-170">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8ab8a-171">ICE32</span><span class="sxs-lookup"><span data-stu-id="8ab8a-171">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8ab8a-172">ICE33</span><span class="sxs-lookup"><span data-stu-id="8ab8a-172">ICE33</span></span>](ice33.md)  
[<span data-ttu-id="8ab8a-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="8ab8a-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="8ab8a-174">ICE69</span><span class="sxs-lookup"><span data-stu-id="8ab8a-174">ICE69</span></span>](ice69.md)  
</dl>

 

 



