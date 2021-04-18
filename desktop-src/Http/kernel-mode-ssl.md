---
title: SSL de modo kernel
description: SSL de modo kernel
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL de modo kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764695"
---
# <a name="kernel-mode-ssl"></a><span data-ttu-id="01929-104">SSL de modo kernel</span><span class="sxs-lookup"><span data-stu-id="01929-104">Kernel Mode SSL</span></span>

<span data-ttu-id="01929-105">O SSL do modo kernel foi introduzido no Windows Server 2003 com Service Pack 1 (SP1) com suporte limitado.</span><span class="sxs-lookup"><span data-stu-id="01929-105">Kernel mode SSL was introduced in Windows Server 2003 with Service Pack 1 (SP1) with limited support.</span></span> <span data-ttu-id="01929-106">Para computadores em execução no Windows Server 2003 com SP1, uma chave do registro deve ser definida para habilitar o SSL do kernel.</span><span class="sxs-lookup"><span data-stu-id="01929-106">For computers running on Windows Server 2003 with SP1 a registry key must be set to enable kernel SSL.</span></span> <span data-ttu-id="01929-107">Para computadores em execução no Windows Server 2008 e no Windows Vista, o suporte ao modo kernel completo para SSL é fornecido.</span><span class="sxs-lookup"><span data-stu-id="01929-107">For computers running on Windows Server 2008 and Windows Vista, full kernel mode support for SSL is provided.</span></span>

<span data-ttu-id="01929-108">As seções a seguir descrevem o suporte a SSL do modo kernel:</span><span class="sxs-lookup"><span data-stu-id="01929-108">The following sections describe kernel mode SSL support:</span></span>

-   <span data-ttu-id="01929-109">Modos de kernel SSL no Windows Server 2003 com SP1</span><span class="sxs-lookup"><span data-stu-id="01929-109">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>
-   <span data-ttu-id="01929-110">Modo kernel SSL no Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01929-110">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a><span data-ttu-id="01929-111">Modos de kernel SSL no Windows Server 2003 com SP1</span><span class="sxs-lookup"><span data-stu-id="01929-111">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>

<span data-ttu-id="01929-112">No Windows Server 2003 com SP1, a API do servidor HTTP fornece a opção de executar segurança SSL no modo kernel (o modo de usuário SSL é o padrão).</span><span class="sxs-lookup"><span data-stu-id="01929-112">In Windows Server 2003 with SP1, HTTP Server API provides the option of running SSL security in kernel mode (user mode SSL is the default).</span></span> <span data-ttu-id="01929-113">O recurso de modo kernel melhora o desempenho do SSL ao mover as operações de criptografia e descriptografia para o kernel, reduzindo assim o número de transições entre o modo kernel e o modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="01929-113">The kernel mode feature improves SSL performance by moving encryption and decryption operations to the kernel, thus reducing the number of transitions between kernel mode and user mode.</span></span>

<span data-ttu-id="01929-114">Os recursos a seguir não têm suporte quando o SSL é executado no modo kernel:</span><span class="sxs-lookup"><span data-stu-id="01929-114">The following features are not supported when SSL is run in kernel mode:</span></span>

-   <span data-ttu-id="01929-115">Certificados do cliente</span><span class="sxs-lookup"><span data-stu-id="01929-115">Client certificates</span></span>
-   <span data-ttu-id="01929-116">Codificações RC2</span><span class="sxs-lookup"><span data-stu-id="01929-116">RC2 ciphers</span></span>
-   <span data-ttu-id="01929-117">O protocolo PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="01929-117">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="01929-118">As alterações de configuração do certificado do servidor exigem uma reinicialização do serviço HTTP</span><span class="sxs-lookup"><span data-stu-id="01929-118">Server certificate configuration changes require a restart of the HTTP service</span></span>
-   <span data-ttu-id="01929-119">Suporte a criptografia e descarregamento em massa</span><span class="sxs-lookup"><span data-stu-id="01929-119">Bulk encryption and offload support</span></span>

## <a name="configuring-kernel-mode-ssl"></a><span data-ttu-id="01929-120">Configurando o modo kernel SSL</span><span class="sxs-lookup"><span data-stu-id="01929-120">Configuring Kernel Mode SSL</span></span>

<span data-ttu-id="01929-121">O SSL do modo kernel é controlado pelo valor do registro **EnableKernelSSL** e é habilitado pela definição do valor como 1.</span><span class="sxs-lookup"><span data-stu-id="01929-121">Kernel mode SSL is controlled by the **EnableKernelSSL** registry value and is enabled by setting the value to 1.</span></span> <span data-ttu-id="01929-122">Habilitar o modo kernel SSL desabilitará o modo de usuário SSL e exigirá que o serviço HTTP seja reiniciado para entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="01929-122">Enabling kernel mode SSL will disable user mode SSL and requires the HTTP service to be restarted to take effect.</span></span> <span data-ttu-id="01929-123">A chave do registro **EnableKernelSSL** está localizada em:</span><span class="sxs-lookup"><span data-stu-id="01929-123">The **EnableKernelSSL** registry key is located at:</span></span>

<span data-ttu-id="01929-124">**HKEY \_ \_** Parâmetros http do sistema de computador local \\  \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **EnableKernelSSL**</span><span class="sxs-lookup"><span data-stu-id="01929-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**HTTP**\\**Parameters**\\**EnableKernelSSL**</span></span>

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a><span data-ttu-id="01929-125">Modo kernel SSL no Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01929-125">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

<span data-ttu-id="01929-126">Para computadores em execução no Windows Server 2008 e no Windows Vista, a API do servidor HTTP apresenta a funcionalidade avançada do SSL.</span><span class="sxs-lookup"><span data-stu-id="01929-126">For computers running on Windows Server 2008 and Windows Vista, the HTTP Server API features enhanced SSL functionality.</span></span>

<span data-ttu-id="01929-127">Os novos recursos a seguir têm suporte:</span><span class="sxs-lookup"><span data-stu-id="01929-127">The following new features are supported:</span></span>

-   <span data-ttu-id="01929-128">Suporte completo a certificados do cliente no modo kernel SSL</span><span class="sxs-lookup"><span data-stu-id="01929-128">Full client certificate support in kernel mode SSL</span></span>
-   <span data-ttu-id="01929-129">SSL de modo kernel para todas as transações HTTP SSL</span><span class="sxs-lookup"><span data-stu-id="01929-129">Kernel mode SSL for all HTTP SSL transactions</span></span>
-   <span data-ttu-id="01929-130">Suporte a criptografia e descarregamento em massa</span><span class="sxs-lookup"><span data-stu-id="01929-130">Bulk encryption and offload support</span></span>
-   <span data-ttu-id="01929-131">O protocolo PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="01929-131">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="01929-132">Codificações RC2</span><span class="sxs-lookup"><span data-stu-id="01929-132">RC2 ciphers</span></span>
-   <span data-ttu-id="01929-133">Aumento do desempenho no modo de usuário SSL</span><span class="sxs-lookup"><span data-stu-id="01929-133">Increased performance over user mode SSL</span></span>

## <a name="configuration"></a><span data-ttu-id="01929-134">Configuração</span><span class="sxs-lookup"><span data-stu-id="01929-134">Configuration</span></span>

<span data-ttu-id="01929-135">O SSL do modo kernel é configurável por meio de dois valores de registro na chave parâmetros HTTP localizada em:</span><span class="sxs-lookup"><span data-stu-id="01929-135">Kernel mode SSL is configurable through two registry values under the HTTP Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

<span data-ttu-id="01929-136">Um usuário deve ter privilégios de administrador/sistema local para modificar os valores do registro e exibir, ou modificar, os arquivos de log e a pasta que os contém.</span><span class="sxs-lookup"><span data-stu-id="01929-136">A user must have Administrator/Local System privileges to modify the registry values and view, or modify, the log files and the folder that contains them.</span></span>

<span data-ttu-id="01929-137">As informações de configuração nos valores do registro são lidas quando o driver da API do servidor HTTP é iniciado.</span><span class="sxs-lookup"><span data-stu-id="01929-137">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="01929-138">Como resultado, se as configurações forem alteradas, o driver deverá ser interrompido e reiniciado para ler os novos valores.</span><span class="sxs-lookup"><span data-stu-id="01929-138">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="01929-139">Isso pode ser feito usando os seguintes comandos de console:</span><span class="sxs-lookup"><span data-stu-id="01929-139">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="01929-140">**net stop http**</span><span class="sxs-lookup"><span data-stu-id="01929-140">**net stop http**</span></span>

<span data-ttu-id="01929-141">**net start http**</span><span class="sxs-lookup"><span data-stu-id="01929-141">**net start http**</span></span>

<span data-ttu-id="01929-142">A tabela a seguir lista os valores de configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="01929-142">The following table lists registry configuration values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01929-143">Valor do registro</span><span class="sxs-lookup"><span data-stu-id="01929-143">Registry Value</span></span></th>
<th><span data-ttu-id="01929-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="01929-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01929-145">EnableKernelSSL</span><span class="sxs-lookup"><span data-stu-id="01929-145">EnableKernelSSL</span></span></td>
<td><span data-ttu-id="01929-146"><strong>Windows Server 2008 e Windows Vista:</strong> Esse valor de registro é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="01929-146"><strong>Windows Server 2008 and Windows Vista:</strong> This registry value is obsolete.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01929-147">EnableSslCloseNotify</span><span class="sxs-lookup"><span data-stu-id="01929-147">EnableSslCloseNotify</span></span></td>
<td><span data-ttu-id="01929-148">Um valor <strong>DWORD</strong> que é definido como <strong>true</strong> para habilitar o Close-notificar ou <strong>false</strong> para desabilitar o requisito de fechamento de notificação.</span><span class="sxs-lookup"><span data-stu-id="01929-148">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable close-notify, or <strong>FALSE</strong> to disable the close-notify requirement.</span></span> <span data-ttu-id="01929-149">O fechamento da notificação é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="01929-149">Close-notify is disabled by default.</span></span><br/> <span data-ttu-id="01929-150">Quando fechar-Notify estiver habilitado, o aplicativo cliente será solicitado a enviar uma mensagem de aviso de fechamento antes de fechar as conexões TCP.</span><span class="sxs-lookup"><span data-stu-id="01929-150">When close-notify is enabled, the client application is required to send a close-notify message before closing TCP connections.</span></span> <span data-ttu-id="01929-151">A API do servidor HTTP também envia um aviso de fechamento antes de fechar a conexão.</span><span class="sxs-lookup"><span data-stu-id="01929-151">The HTTP Server API also sends a close-notify before closing the connection.</span></span><br/> <span data-ttu-id="01929-152">Quando fechar-Notify estiver habilitado e o cliente enviar uma mensagem de aviso de fechamento, a API do servidor HTTP reutilizará a sessão SSL em conexões futuras com o cliente.</span><span class="sxs-lookup"><span data-stu-id="01929-152">When close-notify is enabled, and the client sends a close-notify message, the HTTP Server API will reuse the SSL session on future connections to the client.</span></span> <span data-ttu-id="01929-153">Se o cliente não enviar um aviso de fechamento, a API do servidor HTTP não reutilizará a mesma sessão SSL em conexões futuras.</span><span class="sxs-lookup"><span data-stu-id="01929-153">If the client does not send a close-notify, the HTTP Server API will not reuse the same SSL session on future connections.</span></span> <span data-ttu-id="01929-154">Assim, um handshake SSL completo é disparado na nova conexão, reduzindo o desempenho.</span><span class="sxs-lookup"><span data-stu-id="01929-154">Thus, a full SSL handshake is triggered on the new connection thereby reducing performance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="01929-155">Habilitar o fechamento da notificação ajuda a reduzir os ataques de truncamento em relação às solicitações e respostas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="01929-155">Enabling close-notify helps mitigate truncation attacks against the HTTPS requests and responses.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="01929-156">Quando fechar-notificar está desabilitado, a API do servidor HTTP reutiliza a sessão SSL para conexões futuras.</span><span class="sxs-lookup"><span data-stu-id="01929-156">When close-notify is disabled, the HTTP Server API reuses the SSL session for future connections.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01929-157">DisableSslCertChainCacheOnlyUrlRetrieval</span><span class="sxs-lookup"><span data-stu-id="01929-157">DisableSslCertChainCacheOnlyUrlRetrieval</span></span></td>
<td><span data-ttu-id="01929-158">Um valor <strong>DWORD</strong> definido como <strong>true</strong> para habilitar a API do servidor http para recuperar certificados intermediários da Internet ou do repositório local ou <strong>false</strong> para recuperar certificados intermediários somente do repositório local.</span><span class="sxs-lookup"><span data-stu-id="01929-158">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable the HTTP Server API to retrieve intermediate certificates from either the Internet, or the local store, or <strong>FALSE</strong> to retrieve intermediate certificates from the local store only.</span></span> <span data-ttu-id="01929-159">O valor padrão do registro é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="01929-159">The default registry value is <strong>FALSE</strong>.</span></span><br/> <span data-ttu-id="01929-160">Por padrão, a API do servidor HTTP cria uma cadeia de certificados de cliente recuperando os certificados intermediários do repositório de autoridade de certificação intermediária na conta do computador local.</span><span class="sxs-lookup"><span data-stu-id="01929-160">By default, the HTTP Server API builds a client certificate chain by retrieving the intermediate certificates from the Intermediate Certificate Authority store under the local machine account.</span></span> <span data-ttu-id="01929-161">Definir esse valor como <strong>true</strong> permite que a API do servidor http recupere os certificados intermediários não apenas do armazenamento local, mas também da autoridade de certificação intermediária na Internet.</span><span class="sxs-lookup"><span data-stu-id="01929-161">Setting this value to <strong>TRUE</strong> enables the HTTP Server API to retrieve the intermediate certificates not only from the local store, but also from the Intermediate Certificate Authority on the Internet.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





