---
title: Usando o ADSI com o Exchange
description: Para o Exchange 2000, as informações para usar o ADSI com o Exchange estão contidas no SDK do Exchange 2000. Para obter mais informações, consulte tarefas de gerenciamento para ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI ADSI para Exchange
- ADSI para ADSI do Exchange, caixas de correio
- ADSI para ADSI do Exchange, caixas de correio, criando
- ADSI para ADSI do Exchange, caixas de correio, excluindo
- ADSI para ADSI do Exchange, caixas de correio, definindo descritor de segurança ativado
- ADSI para ADSI do Exchange, caixas de correio, localizando o servidor principal para
- ADSI para ADSI do Exchange, obtendo e modificando mensagens
- ADSI do ADSI do Exchange, descritores de segurança
- ADSI para ADSI do Exchange, descritores de segurança, manipulando
- ADSI para ADSI do Exchange, descritores de segurança, configuração
- ADSI ADSI para Exchange, contêiner de destinatários
- ADSI para ADSI do Exchange, exibindo as propriedades do objeto do Exchange
- ADSI do ADSI do Exchange, contêiner de destinatários, personalizado
- ADSI para ADSI do Exchange, Exchange Server
- ADSI para ADSI do Exchange, Exchange Server, exibindo e modificando o esquema
- ADSI para Exchange ADSI, Exchange Server, listando a versão do servidor
- ADSI para Exchange ADSI, Exchange Server, organização e nome do site
- ADSI para Exchange ADSI, Exchange Server, localizando caixa de correio Home Server
- ADSI do ADSI do Exchange, endereços de email, recuperando
- ADSI para ADSI do Exchange, listas de distribuição, criando
- ADSI para as entradas ADSI, ocultas ou excluídas do Exchange
- ADSI para ADSI do Exchange, recuperando alterações no serviço de diretório
- ADSI do ADSI do Exchange, tamanho da mensagem
- ADSI do ADSI do Exchange, Solucionando problemas
- ADSI de caixas de correio
- ADSI de caixas de correio, criando
- ADSI de caixas de correio, excluindo
- ADSI das caixas de correio, definindo descritor de segurança ativado
- caixa de correio ADSI, localizando o servidor inicial para
- ADSI de mensagens, obtendo e modificando
- ADSI do Exchange
- ADSI do Exchange, caixas de correio
- ADSI do Exchange, caixas de correio, criando
- ADSI do Exchange, caixas de correio, excluindo
- ADSI do Exchange, caixas de correio, configurando descritor de segurança ativado
- ADSI do Exchange, caixas de correio, localizando o servidor principal para
- ADSI do Exchange, obtenção e modificação de mensagens
- ADSI do Exchange, descritores de segurança
- ADSI do Exchange, descritores de segurança, manipulando
- ADSI do Exchange, descritores de segurança, configuração
- ADSI do Exchange, contêiner de destinatários
- ADSI do Exchange, exibindo as propriedades do objeto do Exchange
- ADSI do Exchange, contêiner de destinatários, personalizado
- ADSI do Exchange, Exchange Server
- Exchange ADSI, Exchange Server, exibindo e modificando o esquema
- ADSI do Exchange, Exchange Server, listando a versão do servidor
- Exchange ADSI, Exchange Server, organização e nome do site
- Exchange ADSI, Exchange Server, localizando caixa de correio Home Server
- ADSI do Exchange, endereços de email, recuperando
- ADSI do Exchange, listas de distribuição, criando
- Trocar entradas ADSI, ocultas ou excluídas
- ADSI do Exchange, recuperando alterações no serviço de diretório
- ADSI do Exchange, tamanho da mensagem
- ADSI do Exchange, Solucionando problemas
- descritores de segurança ADSI, para objetos do Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105753662"
---
# <a name="using-adsi-with-exchange"></a><span data-ttu-id="18e92-159">Usando o ADSI com o Exchange</span><span class="sxs-lookup"><span data-stu-id="18e92-159">Using ADSI with Exchange</span></span>

<span data-ttu-id="18e92-160">Para o Exchange 2000, as informações para usar o ADSI com o Exchange estão contidas no SDK do Exchange 2000.</span><span class="sxs-lookup"><span data-stu-id="18e92-160">For Exchange 2000, information for using ADSI with Exchange is contained in the Exchange 2000 SDK.</span></span> <span data-ttu-id="18e92-161">Para obter mais informações, consulte [tarefas de gerenciamento para ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="18e92-161">For more information, see [Management Tasks for ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span></span>

<span data-ttu-id="18e92-162">As seguintes tarefas podem ser encontradas nesta seção:</span><span class="sxs-lookup"><span data-stu-id="18e92-162">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="18e92-163">Criando uma URL de usuário</span><span class="sxs-lookup"><span data-stu-id="18e92-163">Creating a user URL</span></span>
-   <span data-ttu-id="18e92-164">Criando caminhos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="18e92-164">Building Active Directory paths</span></span>
-   <span data-ttu-id="18e92-165">Enumerando servidores Exchange 2000 com ADSI</span><span class="sxs-lookup"><span data-stu-id="18e92-165">Enumerating Exchange 2000 servers with ADSI</span></span>
-   <span data-ttu-id="18e92-166">Manipulando atributos de extensão com ADSI</span><span class="sxs-lookup"><span data-stu-id="18e92-166">Manipulating extension attributes with ADSI</span></span>
-   <span data-ttu-id="18e92-167">Adicionando/removendo um objeto de Gerenciador com ADSI</span><span class="sxs-lookup"><span data-stu-id="18e92-167">Adding/removing a manager object with ADSI</span></span>
-   <span data-ttu-id="18e92-168">Enumerando Propriedades de objeto do Exchange com ADSI/ADO</span><span class="sxs-lookup"><span data-stu-id="18e92-168">Enumerating Exchange object properties with ADSI/ADO</span></span>
-   <span data-ttu-id="18e92-169">Recuperando um nome diferenciado do Exchange herdado com ADSI</span><span class="sxs-lookup"><span data-stu-id="18e92-169">Retrieving a legacy Exchange distinguished name with ADSI</span></span>
-   <span data-ttu-id="18e92-170">Localizando o nome da organização do Exchange usando ADSI</span><span class="sxs-lookup"><span data-stu-id="18e92-170">Finding the Exchange organization name using ADSI</span></span>
-   <span data-ttu-id="18e92-171">Localizando listas de endereços do Exchange com ADSI</span><span class="sxs-lookup"><span data-stu-id="18e92-171">Finding Exchange address lists with ADSI</span></span>
-   <span data-ttu-id="18e92-172">Criando uma lista de distribuição usando CDOEXM e ADSI</span><span class="sxs-lookup"><span data-stu-id="18e92-172">Creating a distribution list using CDOEXM and ADSI</span></span>
-   <span data-ttu-id="18e92-173">Definindo a restrição de mensagem em um servidor virtual SMTP usando ADSI</span><span class="sxs-lookup"><span data-stu-id="18e92-173">Setting message restriction on an SMTP virtual server using ADSI</span></span>

<span data-ttu-id="18e92-174">Para o Exchange 5,5, a referência do ADSI e o uso de informações podem ser encontradas no guia do [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) .</span><span class="sxs-lookup"><span data-stu-id="18e92-174">For Exchange 5.5, the ADSI reference and using information can be found in the [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) guide.</span></span>

<span data-ttu-id="18e92-175">As seguintes tarefas podem ser encontradas nesta seção:</span><span class="sxs-lookup"><span data-stu-id="18e92-175">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="18e92-176">Exibindo e modificando o esquema do Exchange Server</span><span class="sxs-lookup"><span data-stu-id="18e92-176">Viewing and modifying the Exchange Server Schema</span></span>
-   <span data-ttu-id="18e92-177">Exibindo as propriedades brutas de um objeto do Exchange</span><span class="sxs-lookup"><span data-stu-id="18e92-177">Viewing the raw properties of an Exchange object</span></span>
-   <span data-ttu-id="18e92-178">Criando uma caixa de correio do Exchange</span><span class="sxs-lookup"><span data-stu-id="18e92-178">Creating an Exchange mailbox</span></span>
-   <span data-ttu-id="18e92-179">Configurando o descritor de segurança em uma caixa de correio do Exchange</span><span class="sxs-lookup"><span data-stu-id="18e92-179">Setting the security descriptor on an Exchange mailbox</span></span>
-   <span data-ttu-id="18e92-180">Manipulando descritores de segurança e SIDs</span><span class="sxs-lookup"><span data-stu-id="18e92-180">Manipulating security descriptors and SIDs</span></span>
-   <span data-ttu-id="18e92-181">Excluindo um objeto de caixa de correio</span><span class="sxs-lookup"><span data-stu-id="18e92-181">Deleting a mailbox object</span></span>
-   <span data-ttu-id="18e92-182">Criando um destinatário personalizado</span><span class="sxs-lookup"><span data-stu-id="18e92-182">Creating a custom recipient</span></span>
-   <span data-ttu-id="18e92-183">Criando um contêiner de destinatários</span><span class="sxs-lookup"><span data-stu-id="18e92-183">Creating a recipients container</span></span>
-   <span data-ttu-id="18e92-184">Obtendo o nome da organização e do site de um servidor</span><span class="sxs-lookup"><span data-stu-id="18e92-184">Getting the organization and site name from a server</span></span>
-   <span data-ttu-id="18e92-185">Listando a versão do Exchange Server de todos os servidores na organização</span><span class="sxs-lookup"><span data-stu-id="18e92-185">Listing the Exchange server version of all the servers in the organization</span></span>
-   <span data-ttu-id="18e92-186">Localizando o servidor inicial de uma caixa de correio</span><span class="sxs-lookup"><span data-stu-id="18e92-186">Finding the home server of a mailbox</span></span>
-   <span data-ttu-id="18e92-187">Recuperando endereços de email</span><span class="sxs-lookup"><span data-stu-id="18e92-187">Retrieving email addresses</span></span>
-   <span data-ttu-id="18e92-188">Acessando entradas ocultas ou excluídas</span><span class="sxs-lookup"><span data-stu-id="18e92-188">Accessing hidden or deleted entries</span></span>
-   <span data-ttu-id="18e92-189">Recuperando alterações feitas no serviço de diretório</span><span class="sxs-lookup"><span data-stu-id="18e92-189">Retrieving changes made to the directory service</span></span>
-   <span data-ttu-id="18e92-190">Criando uma lista de distribuição com base nos resultados de uma consulta</span><span class="sxs-lookup"><span data-stu-id="18e92-190">Creating a distribution list from the results of a query</span></span>
-   <span data-ttu-id="18e92-191">Obtendo ou modificando o tamanho da mensagem</span><span class="sxs-lookup"><span data-stu-id="18e92-191">Getting or modifying message size</span></span>
-   <span data-ttu-id="18e92-192">Usando códigos de erro LDAP para solucionar problemas</span><span class="sxs-lookup"><span data-stu-id="18e92-192">Using LDAP error codes to troubleshoot problems</span></span>

 

 