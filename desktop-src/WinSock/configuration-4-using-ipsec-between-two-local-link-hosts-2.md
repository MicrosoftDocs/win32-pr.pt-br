---
description: Essa configuração cria uma associação de segurança (SA) IPsec entre dois hosts na mesma sub-rede para realizar a autenticação usando o algoritmo de hash Cabeçalho de Autenticação (AH) e Message Digest 5 (MD5).
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Configuração 3: usando o IPsec entre dois hosts de link local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e7a760b6ae1ba87678d6061881e5eb80faf88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090404"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a><span data-ttu-id="b2db0-103">Configuração 3: usando o IPsec entre dois hosts de link local</span><span class="sxs-lookup"><span data-stu-id="b2db0-103">Configuration 3: Using IPsec Between Two Local-link Hosts</span></span>

<span data-ttu-id="b2db0-104">Essa configuração cria uma associação de segurança (SA) IPsec entre dois hosts na mesma sub-rede para realizar a autenticação usando o algoritmo de hash Cabeçalho de Autenticação (AH) e Message Digest 5 (MD5).</span><span class="sxs-lookup"><span data-stu-id="b2db0-104">This configuration creates an IPsec Security Association (SA) between two hosts on the same subnet to perform authentication using the Authentication Header (AH) and the Message Digest 5 (MD5) hashing algorithm.</span></span> <span data-ttu-id="b2db0-105">Neste exemplo, a configuração mostrada protege todo o tráfego entre dois hosts vizinhos: host 1, com o endereço de link local FE80:: 2AA: FF: FE53: A92C e host 2, com o endereço de link local FE80:: 2AA: FF: FE92: D0F1.</span><span class="sxs-lookup"><span data-stu-id="b2db0-105">In this example, the configuration shown secures all traffic between two neighboring hosts: Host 1, with the link-local address FE80::2AA:FF:FE53:A92C, and Host 2, with the link-local address FE80::2AA:FF:FE92:D0F1.</span></span>

<span data-ttu-id="b2db0-106">**Para usar o IPsec entre dois hosts de link local**</span><span class="sxs-lookup"><span data-stu-id="b2db0-106">**To use IPsec between two local-link hosts**</span></span>

1.  <span data-ttu-id="b2db0-107">No host 1, Crie arquivos de associação de segurança em branco (SAD) e de política de segurança (SPD) usando o comando ipsec6 c.</span><span class="sxs-lookup"><span data-stu-id="b2db0-107">On Host 1, create blank security association (SAD) and security policy (SPD) files by using the ipsec6 c command.</span></span> <span data-ttu-id="b2db0-108">Neste exemplo, o comando Ipsec6.exe é Ipsec6 c Test.</span><span class="sxs-lookup"><span data-stu-id="b2db0-108">In this example, the Ipsec6.exe command is ipsec6 c test.</span></span> <span data-ttu-id="b2db0-109">Isso cria dois arquivos para configurar manualmente associações de segurança (Test. Sad) e políticas de segurança (Test. SPD).</span><span class="sxs-lookup"><span data-stu-id="b2db0-109">This creates two files to manually configure security associations (Test.sad) and security policies (Test.spd).</span></span>
2.  <span data-ttu-id="b2db0-110">No host 1, edite o arquivo SPD para adicionar uma política de segurança que protege todo o tráfego entre o host 1 e o host 2.</span><span class="sxs-lookup"><span data-stu-id="b2db0-110">On Host 1, edit the SPD file to add a security policy that secures all traffic between Host 1 and Host 2.</span></span>

    <span data-ttu-id="b2db0-111">A tabela a seguir mostra a política de segurança adicionada ao arquivo Test. SPD antes da primeira entrada para este exemplo (a primeira entrada no arquivo Test. SPD não foi modificada).</span><span class="sxs-lookup"><span data-stu-id="b2db0-111">The following table shows the security policy added to the Test.spd file before the first entry for this example (the first entry in the Test.spd file was not modified).</span></span>

    | <span data-ttu-id="b2db0-112">Nome do campo de arquivo SPD</span><span class="sxs-lookup"><span data-stu-id="b2db0-112">SPD file field name</span></span> | <span data-ttu-id="b2db0-113">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="b2db0-113">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="b2db0-114">**Política**</span><span class="sxs-lookup"><span data-stu-id="b2db0-114">**Policy**</span></span>          | <span data-ttu-id="b2db0-115">2</span><span class="sxs-lookup"><span data-stu-id="b2db0-115">2</span></span>                          |
    | <span data-ttu-id="b2db0-116">**RemoteIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-116">**RemoteIPAddr**</span></span>    | <span data-ttu-id="b2db0-117">**FE80:: 2AA: FF: FE92: D0F1**</span><span class="sxs-lookup"><span data-stu-id="b2db0-117">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="b2db0-118">**LocalIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-118">**LocalIPAddr**</span></span>     | \*                         |
    | <span data-ttu-id="b2db0-119">**RemotePort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-119">**RemotePort**</span></span>      | \*                         |
    | <span data-ttu-id="b2db0-120">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="b2db0-120">**Protocol**</span></span>        | \*                         |
    | <span data-ttu-id="b2db0-121">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-121">**LocalPort**</span></span>       | \*                         |
    | <span data-ttu-id="b2db0-122">**IPSecProtocol**</span><span class="sxs-lookup"><span data-stu-id="b2db0-122">**IPSecProtocol**</span></span>   | <span data-ttu-id="b2db0-123">**NELES**</span><span class="sxs-lookup"><span data-stu-id="b2db0-123">**AH**</span></span>                     |
    | <span data-ttu-id="b2db0-124">**IPSecmode**</span><span class="sxs-lookup"><span data-stu-id="b2db0-124">**IPSecMode**</span></span>       | <span data-ttu-id="b2db0-125">**PORTA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-125">**TRANSPORT**</span></span>              |
    | <span data-ttu-id="b2db0-126">**RemoteGWIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-126">**RemoteGWIPAddr**</span></span>  | \*                         |
    | <span data-ttu-id="b2db0-127">**SABundleIndex**</span><span class="sxs-lookup"><span data-stu-id="b2db0-127">**SABundleIndex**</span></span>   | <span data-ttu-id="b2db0-128">**NONE**</span><span class="sxs-lookup"><span data-stu-id="b2db0-128">**NONE**</span></span>                   |
    | <span data-ttu-id="b2db0-129">**Direção**</span><span class="sxs-lookup"><span data-stu-id="b2db0-129">**Direction**</span></span>       | <span data-ttu-id="b2db0-130">**Bidirect**</span><span class="sxs-lookup"><span data-stu-id="b2db0-130">**BIDIRECT**</span></span>               |
    | <span data-ttu-id="b2db0-131">**Ação**</span><span class="sxs-lookup"><span data-stu-id="b2db0-131">**Action**</span></span>          | <span data-ttu-id="b2db0-132">**USAR**</span><span class="sxs-lookup"><span data-stu-id="b2db0-132">**APPLY**</span></span>                  |
    | <span data-ttu-id="b2db0-133">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="b2db0-133">**InterfaceIndex**</span></span>  | <span data-ttu-id="b2db0-134">0</span><span class="sxs-lookup"><span data-stu-id="b2db0-134">0</span></span>                          |

    

     

    <span data-ttu-id="b2db0-135">Coloque um ponto e vírgula no final da linha Configurando essa política de segurança.</span><span class="sxs-lookup"><span data-stu-id="b2db0-135">Place a semicolon at the end of the line configuring this security policy.</span></span> <span data-ttu-id="b2db0-136">As entradas de política devem ser colocadas em ordem numérica decrescente.</span><span class="sxs-lookup"><span data-stu-id="b2db0-136">The policy entries must be placed in decreasing numerical order.</span></span>

3.  <span data-ttu-id="b2db0-137">No host 1, edite o arquivo triste, adicionando entradas SA para proteger todo o tráfego entre o host 1 e o host 2.</span><span class="sxs-lookup"><span data-stu-id="b2db0-137">On Host 1, edit the SAD file, adding SA entries to secure all traffic between Host 1 and Host 2.</span></span> <span data-ttu-id="b2db0-138">Duas associações de segurança devem ser criadas, uma para o tráfego para o host 2 e outra para o tráfego do host 2.</span><span class="sxs-lookup"><span data-stu-id="b2db0-138">Two security associations must be created, one for traffic to Host 2 and one for traffic from Host 2.</span></span>

    <span data-ttu-id="b2db0-139">A tabela a seguir mostra a primeira entrada SA adicionada ao arquivo Test. sad para este exemplo (para o tráfego para o host 2).</span><span class="sxs-lookup"><span data-stu-id="b2db0-139">The following table shows the first SA entry added to the Test.sad file for this example (for traffic to Host 2).</span></span>

    | <span data-ttu-id="b2db0-140">Nome do campo de arquivo triste</span><span class="sxs-lookup"><span data-stu-id="b2db0-140">SAD file field name</span></span> | <span data-ttu-id="b2db0-141">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="b2db0-141">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="b2db0-142">**SAEntry**</span><span class="sxs-lookup"><span data-stu-id="b2db0-142">**SAEntry**</span></span>         | <span data-ttu-id="b2db0-143">2</span><span class="sxs-lookup"><span data-stu-id="b2db0-143">2</span></span>                          |
    | <span data-ttu-id="b2db0-144">**SPI**</span><span class="sxs-lookup"><span data-stu-id="b2db0-144">**SPI**</span></span>             | <span data-ttu-id="b2db0-145">3001</span><span class="sxs-lookup"><span data-stu-id="b2db0-145">3001</span></span>                       |
    | <span data-ttu-id="b2db0-146">**SADestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-146">**SADestIPAddr**</span></span>    | <span data-ttu-id="b2db0-147">**FE80:: 2AA: FF: FE92: D0F1**</span><span class="sxs-lookup"><span data-stu-id="b2db0-147">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="b2db0-148">**DestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-148">**DestIPAddr**</span></span>      | <span data-ttu-id="b2db0-149">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-149">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-150">**SrcIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-150">**SrcIPAddr**</span></span>       | <span data-ttu-id="b2db0-151">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-151">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-152">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="b2db0-152">**Protocol**</span></span>        | <span data-ttu-id="b2db0-153">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-153">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-154">**DestPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-154">**DestPort**</span></span>        | <span data-ttu-id="b2db0-155">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-155">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-156">**SrcPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-156">**SrcPort**</span></span>         | <span data-ttu-id="b2db0-157">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-157">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-158">**AuthAlg**</span><span class="sxs-lookup"><span data-stu-id="b2db0-158">**AuthAlg**</span></span>         | <span data-ttu-id="b2db0-159">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="b2db0-159">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="b2db0-160">**Chaves**</span><span class="sxs-lookup"><span data-stu-id="b2db0-160">**KeyFile**</span></span>         | <span data-ttu-id="b2db0-161">**Test. Key**</span><span class="sxs-lookup"><span data-stu-id="b2db0-161">**Test.key**</span></span>               |
    | <span data-ttu-id="b2db0-162">**Direção**</span><span class="sxs-lookup"><span data-stu-id="b2db0-162">**Direction**</span></span>       | <span data-ttu-id="b2db0-163">**SA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-163">**OUTBOUND**</span></span>               |
    | <span data-ttu-id="b2db0-164">**SecPolicyIndex**</span><span class="sxs-lookup"><span data-stu-id="b2db0-164">**SecPolicyIndex**</span></span>  | <span data-ttu-id="b2db0-165">2</span><span class="sxs-lookup"><span data-stu-id="b2db0-165">2</span></span>                          |

    

     

    <span data-ttu-id="b2db0-166">Coloque um ponto e vírgula no final da linha Configurando esse SA.</span><span class="sxs-lookup"><span data-stu-id="b2db0-166">Place a semicolon at the end of the line configuring this SA.</span></span>

    <span data-ttu-id="b2db0-167">A tabela a seguir mostra a segunda entrada SA adicionada ao arquivo Test. sad para este exemplo (para o tráfego do host 2).</span><span class="sxs-lookup"><span data-stu-id="b2db0-167">The following table shows the second SA entry added to the Test.sad file for this example (for traffic from Host 2).</span></span>

    | <span data-ttu-id="b2db0-168">Nome do campo de arquivo triste</span><span class="sxs-lookup"><span data-stu-id="b2db0-168">SAD file field name</span></span> | <span data-ttu-id="b2db0-169">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="b2db0-169">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="b2db0-170">**SAEntry**</span><span class="sxs-lookup"><span data-stu-id="b2db0-170">**SAEntry**</span></span>         | <span data-ttu-id="b2db0-171">1</span><span class="sxs-lookup"><span data-stu-id="b2db0-171">1</span></span>                          |
    | <span data-ttu-id="b2db0-172">**SPI**</span><span class="sxs-lookup"><span data-stu-id="b2db0-172">**SPI**</span></span>             | <span data-ttu-id="b2db0-173">3000</span><span class="sxs-lookup"><span data-stu-id="b2db0-173">3000</span></span>                       |
    | <span data-ttu-id="b2db0-174">**SADestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-174">**SADestIPAddr**</span></span>    | <span data-ttu-id="b2db0-175">**FE80:: 2AA: FF: FE53: A92C**</span><span class="sxs-lookup"><span data-stu-id="b2db0-175">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="b2db0-176">**DestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-176">**DestIPAddr**</span></span>      | <span data-ttu-id="b2db0-177">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-177">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-178">**SrcIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-178">**SrcIPAddr**</span></span>       | <span data-ttu-id="b2db0-179">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-179">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-180">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="b2db0-180">**Protocol**</span></span>        | <span data-ttu-id="b2db0-181">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-181">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-182">**DestPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-182">**DestPort**</span></span>        | <span data-ttu-id="b2db0-183">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-183">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-184">**SrcPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-184">**SrcPort**</span></span>         | <span data-ttu-id="b2db0-185">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-185">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-186">**AuthAlg**</span><span class="sxs-lookup"><span data-stu-id="b2db0-186">**AuthAlg**</span></span>         | <span data-ttu-id="b2db0-187">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="b2db0-187">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="b2db0-188">**Chaves**</span><span class="sxs-lookup"><span data-stu-id="b2db0-188">**KeyFile**</span></span>         | <span data-ttu-id="b2db0-189">**Test. Key**</span><span class="sxs-lookup"><span data-stu-id="b2db0-189">**Test.key**</span></span>               |
    | <span data-ttu-id="b2db0-190">**Direção**</span><span class="sxs-lookup"><span data-stu-id="b2db0-190">**Direction**</span></span>       | <span data-ttu-id="b2db0-191">**ENTRADA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-191">**INBOUND**</span></span>                |
    | <span data-ttu-id="b2db0-192">**SecPolicyIndex**</span><span class="sxs-lookup"><span data-stu-id="b2db0-192">**SecPolicyIndex**</span></span>  | <span data-ttu-id="b2db0-193">2</span><span class="sxs-lookup"><span data-stu-id="b2db0-193">2</span></span>                          |

    

     

    <span data-ttu-id="b2db0-194">Coloque um ponto e vírgula no final da linha Configurando esse SA.</span><span class="sxs-lookup"><span data-stu-id="b2db0-194">Place a semicolon at the end of the line configuring this SA.</span></span> <span data-ttu-id="b2db0-195">As entradas SA devem ser colocadas em ordem numérica decrescente.</span><span class="sxs-lookup"><span data-stu-id="b2db0-195">The SA entries must be placed in decreasing numerical order.</span></span>

4.  <span data-ttu-id="b2db0-196">No host 1, crie um arquivo de texto que contenha uma cadeia de texto usada para autenticar a SAs criada com o host 2.</span><span class="sxs-lookup"><span data-stu-id="b2db0-196">On Host 1, create a text file that contains a text string used to authenticate the SAs created with Host 2.</span></span> <span data-ttu-id="b2db0-197">Neste exemplo, o arquivo Test. Key é criado com o conteúdo "Este é um teste".</span><span class="sxs-lookup"><span data-stu-id="b2db0-197">In this example, the file Test.key is created with the contents "This is a test".</span></span> <span data-ttu-id="b2db0-198">Você deve incluir aspas duplas em volta da cadeia de caracteres de chave para que a chave seja lida pela ferramenta Ipsec6.</span><span class="sxs-lookup"><span data-stu-id="b2db0-198">You must include double quotes around the key string in order for the key to be read by the ipsec6 tool.</span></span>

    <span data-ttu-id="b2db0-199">O Microsoft IPv6 Technology Preview só dá suporte a chaves configuradas manualmente para a autenticação de SAs IPsec.</span><span class="sxs-lookup"><span data-stu-id="b2db0-199">The Microsoft IPv6 Technology Preview only supports manually configured keys for the authentication of IPsec SAs.</span></span> <span data-ttu-id="b2db0-200">As chaves manuais são configuradas criando arquivos de texto que contêm a cadeia de caracteres de texto da chave manual.</span><span class="sxs-lookup"><span data-stu-id="b2db0-200">The manual keys are configured by creating text files that contain the text string of the manual key.</span></span> <span data-ttu-id="b2db0-201">Neste exemplo, a mesma chave para a SAs é usada em ambas as direções.</span><span class="sxs-lookup"><span data-stu-id="b2db0-201">In this example, the same key for the SAs is used in both directions.</span></span> <span data-ttu-id="b2db0-202">Você pode usar chaves diferentes para SAs de entrada e saída criando arquivos de chave diferentes e fazendo referência a eles com o campo KeyFile no arquivo triste.</span><span class="sxs-lookup"><span data-stu-id="b2db0-202">You can use different keys for inbound and outbound SAs by creating different key files and referencing them with the KeyFile field in the SAD file.</span></span>

5.  <span data-ttu-id="b2db0-203">No host 2, Crie arquivos de associação de segurança em branco (SAD) e de política de segurança (SPD) usando o comando ipsec6 c.</span><span class="sxs-lookup"><span data-stu-id="b2db0-203">On Host 2, create blank security association (SAD) and security policy (SPD) files by using the ipsec6 c command.</span></span> <span data-ttu-id="b2db0-204">Neste exemplo, o comando Ipsec6.exe é Ipsec6 c Test.</span><span class="sxs-lookup"><span data-stu-id="b2db0-204">In this example, the Ipsec6.exe command is ipsec6 c test.</span></span> <span data-ttu-id="b2db0-205">Isso cria dois arquivos com entradas em branco para configurar manualmente associações de segurança (Test. Sad) e políticas de segurança (Test. SPD).</span><span class="sxs-lookup"><span data-stu-id="b2db0-205">This creates two files with blank entries for manually configuring security associations (Test.sad) and security policies (Test.spd).</span></span>

    <span data-ttu-id="b2db0-206">Para simplificar o exemplo, os mesmos nomes de arquivo para os arquivos triste e SPD são usados no host 2.</span><span class="sxs-lookup"><span data-stu-id="b2db0-206">To simplify the example, the same file names for the SAD and SPD files are used on Host 2.</span></span> <span data-ttu-id="b2db0-207">Você pode optar por usar nomes de arquivo diferentes em cada host.</span><span class="sxs-lookup"><span data-stu-id="b2db0-207">You can choose to use different file names on each host.</span></span>

6.  <span data-ttu-id="b2db0-208">No host 2, edite o arquivo SPD para adicionar uma política de segurança que protege todo o tráfego entre o host 2 e o host 1.</span><span class="sxs-lookup"><span data-stu-id="b2db0-208">On Host 2, edit the SPD file to add a security policy that secures all traffic between Host 2 and Host 1.</span></span>

    <span data-ttu-id="b2db0-209">A tabela a seguir mostra a entrada de política de segurança adicionada antes da primeira entrada para o arquivo Test. SPD para este exemplo (a primeira entrada no arquivo Test. SPD não foi modificada).</span><span class="sxs-lookup"><span data-stu-id="b2db0-209">The following table shows the security policy entry added before the first entry to the Test.spd file for this example (the first entry in the Test.spd file was not modified).</span></span>

    | <span data-ttu-id="b2db0-210">Nome do campo de arquivo SPD</span><span class="sxs-lookup"><span data-stu-id="b2db0-210">SPD file field name</span></span> | <span data-ttu-id="b2db0-211">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="b2db0-211">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="b2db0-212">**Política**</span><span class="sxs-lookup"><span data-stu-id="b2db0-212">**Policy**</span></span>          | <span data-ttu-id="b2db0-213">2</span><span class="sxs-lookup"><span data-stu-id="b2db0-213">2</span></span>                          |
    | <span data-ttu-id="b2db0-214">**RemoteIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-214">**RemoteIPAddr**</span></span>    | <span data-ttu-id="b2db0-215">**FE80:: 2AA: FF: FE53: A92C**</span><span class="sxs-lookup"><span data-stu-id="b2db0-215">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="b2db0-216">**LocalIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-216">**LocalIPAddr**</span></span>     | \*                         |
    | <span data-ttu-id="b2db0-217">**RemotePort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-217">**RemotePort**</span></span>      | \*                         |
    | <span data-ttu-id="b2db0-218">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="b2db0-218">**Protocol**</span></span>        | \*                         |
    | <span data-ttu-id="b2db0-219">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-219">**LocalPort**</span></span>       | \*                         |
    | <span data-ttu-id="b2db0-220">**IPSecProtocol**</span><span class="sxs-lookup"><span data-stu-id="b2db0-220">**IPSecProtocol**</span></span>   | <span data-ttu-id="b2db0-221">**NELES**</span><span class="sxs-lookup"><span data-stu-id="b2db0-221">**AH**</span></span>                     |
    | <span data-ttu-id="b2db0-222">**IPSecmode**</span><span class="sxs-lookup"><span data-stu-id="b2db0-222">**IPSecMode**</span></span>       | <span data-ttu-id="b2db0-223">**PORTA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-223">**TRANSPORT**</span></span>              |
    | <span data-ttu-id="b2db0-224">**RemoteGWIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-224">**RemoteGWIPAddr**</span></span>  | \*                         |
    | <span data-ttu-id="b2db0-225">**SABundleIndex**</span><span class="sxs-lookup"><span data-stu-id="b2db0-225">**SABundleIndex**</span></span>   | <span data-ttu-id="b2db0-226">**NONE**</span><span class="sxs-lookup"><span data-stu-id="b2db0-226">**NONE**</span></span>                   |
    | <span data-ttu-id="b2db0-227">**Direção**</span><span class="sxs-lookup"><span data-stu-id="b2db0-227">**Direction**</span></span>       | <span data-ttu-id="b2db0-228">**Bidirect**</span><span class="sxs-lookup"><span data-stu-id="b2db0-228">**BIDIRECT**</span></span>               |
    | <span data-ttu-id="b2db0-229">**Ação**</span><span class="sxs-lookup"><span data-stu-id="b2db0-229">**Action**</span></span>          | <span data-ttu-id="b2db0-230">**USAR**</span><span class="sxs-lookup"><span data-stu-id="b2db0-230">**APPLY**</span></span>                  |
    | <span data-ttu-id="b2db0-231">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="b2db0-231">**InterfaceIndex**</span></span>  | <span data-ttu-id="b2db0-232">0</span><span class="sxs-lookup"><span data-stu-id="b2db0-232">0</span></span>                          |

    

     

    <span data-ttu-id="b2db0-233">Coloque um ponto e vírgula no final da linha Configurando essa política de segurança.</span><span class="sxs-lookup"><span data-stu-id="b2db0-233">Place a semicolon at the end of the line configuring this security policy.</span></span> <span data-ttu-id="b2db0-234">As entradas de política devem ser colocadas em ordem numérica decrescente.</span><span class="sxs-lookup"><span data-stu-id="b2db0-234">The policy entries must be placed in decreasing numerical order.</span></span>

7.  <span data-ttu-id="b2db0-235">No host 2, edite o arquivo triste, adicionando entradas SA para proteger todo o tráfego entre o host 2 e o host 1.</span><span class="sxs-lookup"><span data-stu-id="b2db0-235">On Host 2, edit the SAD file, adding SA entries to secure all traffic between Host 2 and Host 1.</span></span> <span data-ttu-id="b2db0-236">Duas associações de segurança devem ser criadas-uma para o tráfego para o host 1 e outra para o tráfego do host 1.</span><span class="sxs-lookup"><span data-stu-id="b2db0-236">Two security associations must be created-one for traffic to Host 1 and one for traffic from Host 1.</span></span>

    <span data-ttu-id="b2db0-237">A tabela a seguir mostra a primeira SA adicionada ao arquivo Test. sad para este exemplo (para o tráfego do host 1).</span><span class="sxs-lookup"><span data-stu-id="b2db0-237">The following table shows the first SA added to the Test.sad file for this example (for traffic from Host 1).</span></span>

    | <span data-ttu-id="b2db0-238">Nome do campo de arquivo triste</span><span class="sxs-lookup"><span data-stu-id="b2db0-238">SAD file field name</span></span> | <span data-ttu-id="b2db0-239">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="b2db0-239">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="b2db0-240">**SAEntry**</span><span class="sxs-lookup"><span data-stu-id="b2db0-240">**SAEntry**</span></span>         | <span data-ttu-id="b2db0-241">2</span><span class="sxs-lookup"><span data-stu-id="b2db0-241">2</span></span>                          |
    | <span data-ttu-id="b2db0-242">**SPI**</span><span class="sxs-lookup"><span data-stu-id="b2db0-242">**SPI**</span></span>             | <span data-ttu-id="b2db0-243">3001</span><span class="sxs-lookup"><span data-stu-id="b2db0-243">3001</span></span>                       |
    | <span data-ttu-id="b2db0-244">**SADestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-244">**SADestIPAddr**</span></span>    | <span data-ttu-id="b2db0-245">**FE80:: 2AA: FF: FE92: D0F1**</span><span class="sxs-lookup"><span data-stu-id="b2db0-245">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="b2db0-246">**DestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-246">**DestIPAddr**</span></span>      | <span data-ttu-id="b2db0-247">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-247">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-248">**SrcIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-248">**SrcIPAddr**</span></span>       | <span data-ttu-id="b2db0-249">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-249">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-250">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="b2db0-250">**Protocol**</span></span>        | <span data-ttu-id="b2db0-251">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-251">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-252">**DestPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-252">**DestPort**</span></span>        | <span data-ttu-id="b2db0-253">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-253">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-254">**SrcPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-254">**SrcPort**</span></span>         | <span data-ttu-id="b2db0-255">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-255">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-256">**AuthAlg**</span><span class="sxs-lookup"><span data-stu-id="b2db0-256">**AuthAlg**</span></span>         | <span data-ttu-id="b2db0-257">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="b2db0-257">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="b2db0-258">**Chaves**</span><span class="sxs-lookup"><span data-stu-id="b2db0-258">**KeyFile**</span></span>         | <span data-ttu-id="b2db0-259">**Test. Key**</span><span class="sxs-lookup"><span data-stu-id="b2db0-259">**Test.key**</span></span>               |
    | <span data-ttu-id="b2db0-260">**Direção**</span><span class="sxs-lookup"><span data-stu-id="b2db0-260">**Direction**</span></span>       | <span data-ttu-id="b2db0-261">**ENTRADA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-261">**INBOUND**</span></span>                |
    | <span data-ttu-id="b2db0-262">**SecPolicyIndex**</span><span class="sxs-lookup"><span data-stu-id="b2db0-262">**SecPolicyIndex**</span></span>  | <span data-ttu-id="b2db0-263">2</span><span class="sxs-lookup"><span data-stu-id="b2db0-263">2</span></span>                          |

    

     

    <span data-ttu-id="b2db0-264">Coloque um ponto e vírgula no final da linha Configurando esse SA.</span><span class="sxs-lookup"><span data-stu-id="b2db0-264">Place a semicolon at the end of the line configuring this SA.</span></span>

    <span data-ttu-id="b2db0-265">A tabela a seguir mostra a segunda entrada SA adicionada ao arquivo Test. sad para este exemplo (para o tráfego para o host 1).</span><span class="sxs-lookup"><span data-stu-id="b2db0-265">The following table shows the second SA entry added to the Test.sad file for this example (for traffic to Host 1).</span></span>

    | <span data-ttu-id="b2db0-266">Nome do campo de arquivo triste</span><span class="sxs-lookup"><span data-stu-id="b2db0-266">SAD file field name</span></span> | <span data-ttu-id="b2db0-267">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="b2db0-267">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="b2db0-268">**SAEntry**</span><span class="sxs-lookup"><span data-stu-id="b2db0-268">**SAEntry**</span></span>         | <span data-ttu-id="b2db0-269">1</span><span class="sxs-lookup"><span data-stu-id="b2db0-269">1</span></span>                          |
    | <span data-ttu-id="b2db0-270">**SPI**</span><span class="sxs-lookup"><span data-stu-id="b2db0-270">**SPI**</span></span>             | <span data-ttu-id="b2db0-271">3000</span><span class="sxs-lookup"><span data-stu-id="b2db0-271">3000</span></span>                       |
    | <span data-ttu-id="b2db0-272">**SADestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-272">**SADestIPAddr**</span></span>    | <span data-ttu-id="b2db0-273">**FE80:: 2AA: FF: FE53: A92C**</span><span class="sxs-lookup"><span data-stu-id="b2db0-273">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="b2db0-274">**DestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-274">**DestIPAddr**</span></span>      | <span data-ttu-id="b2db0-275">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-275">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-276">**SrcIPAddr**</span><span class="sxs-lookup"><span data-stu-id="b2db0-276">**SrcIPAddr**</span></span>       | <span data-ttu-id="b2db0-277">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-277">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-278">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="b2db0-278">**Protocol**</span></span>        | <span data-ttu-id="b2db0-279">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-279">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-280">**DestPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-280">**DestPort**</span></span>        | <span data-ttu-id="b2db0-281">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-281">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-282">**SrcPort**</span><span class="sxs-lookup"><span data-stu-id="b2db0-282">**SrcPort**</span></span>         | <span data-ttu-id="b2db0-283">**POLÍTICA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-283">**POLICY**</span></span>                 |
    | <span data-ttu-id="b2db0-284">**AuthAlg**</span><span class="sxs-lookup"><span data-stu-id="b2db0-284">**AuthAlg**</span></span>         | <span data-ttu-id="b2db0-285">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="b2db0-285">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="b2db0-286">**Chaves**</span><span class="sxs-lookup"><span data-stu-id="b2db0-286">**KeyFile**</span></span>         | <span data-ttu-id="b2db0-287">**Test. Key**</span><span class="sxs-lookup"><span data-stu-id="b2db0-287">**Test.key**</span></span>               |
    | <span data-ttu-id="b2db0-288">**Direção**</span><span class="sxs-lookup"><span data-stu-id="b2db0-288">**Direction**</span></span>       | <span data-ttu-id="b2db0-289">**SA**</span><span class="sxs-lookup"><span data-stu-id="b2db0-289">**OUTBOUND**</span></span>               |
    | <span data-ttu-id="b2db0-290">**SecPolicyIndex**</span><span class="sxs-lookup"><span data-stu-id="b2db0-290">**SecPolicyIndex**</span></span>  | <span data-ttu-id="b2db0-291">2</span><span class="sxs-lookup"><span data-stu-id="b2db0-291">2</span></span>                          |

    

     

    <span data-ttu-id="b2db0-292">Coloque um ponto e vírgula no final da linha Configurando esse SA.</span><span class="sxs-lookup"><span data-stu-id="b2db0-292">Place a semicolon at the end of the line configuring this SA.</span></span> <span data-ttu-id="b2db0-293">As entradas SA devem ser colocadas em ordem numérica decrescente.</span><span class="sxs-lookup"><span data-stu-id="b2db0-293">The SA entries must be placed in decreasing numerical order.</span></span>

8.  <span data-ttu-id="b2db0-294">No host 2, crie um arquivo de texto que contenha uma cadeia de texto usada para autenticar a SAs criada com o host 1.</span><span class="sxs-lookup"><span data-stu-id="b2db0-294">On Host 2, create a text file that contains a text string used to authenticate the SAs created with Host 1.</span></span> <span data-ttu-id="b2db0-295">Neste exemplo, o arquivo Test. Key é criado com o conteúdo "Este é um teste".</span><span class="sxs-lookup"><span data-stu-id="b2db0-295">In this example, the file Test.key is created with the contents "This is a test".</span></span> <span data-ttu-id="b2db0-296">Você deve incluir aspas duplas em volta da cadeia de caracteres de chave para que a chave seja lida pela ferramenta Ipsec6.</span><span class="sxs-lookup"><span data-stu-id="b2db0-296">You must include double quotes around the key string in order for the key to be read by the ipsec6 tool.</span></span>
9.  <span data-ttu-id="b2db0-297">No host 1, adicione as políticas de segurança e SAs configuradas dos arquivos SPD e SAD usando o comando ipsec6 a.</span><span class="sxs-lookup"><span data-stu-id="b2db0-297">On Host 1, add the configured security policies and SAs from the SPD and SAD files using the ipsec6 a command.</span></span> <span data-ttu-id="b2db0-298">Neste exemplo, o comando ipsec6 a Test é executado no host 1.</span><span class="sxs-lookup"><span data-stu-id="b2db0-298">In this example, the ipsec6 a test command is run on Host 1.</span></span>
10. <span data-ttu-id="b2db0-299">No host 2, adicione as políticas de segurança e SAs configuradas dos arquivos SPD e SAD usando o comando ipsec6 a.</span><span class="sxs-lookup"><span data-stu-id="b2db0-299">On Host 2, add the configured security policies and SAs from the SPD and SAD files by using the ipsec6 a command.</span></span> <span data-ttu-id="b2db0-300">Neste exemplo, o comando ipsec6 a Test é executado no host 2.</span><span class="sxs-lookup"><span data-stu-id="b2db0-300">In this example, the ipsec6 a test command is run on Host 2.</span></span>
11. <span data-ttu-id="b2db0-301">Execute ping no host 1 do host 2 com o comando ping6.</span><span class="sxs-lookup"><span data-stu-id="b2db0-301">Ping Host 1 from Host 2 with the ping6 command.</span></span>

    <span data-ttu-id="b2db0-302">Se você capturar o tráfego usando Monitor de Rede da Microsoft ou outro farejador de pacote, deverá ver a troca de mensagens de eco e de resposta de eco ICMPv6 com um Cabeçalho de Autenticação entre o cabeçalho IPv6 e o cabeçalho ICMPv6.</span><span class="sxs-lookup"><span data-stu-id="b2db0-302">If you capture the traffic using Microsoft Network Monitor or another packet sniffer, you should see the exchange of ICMPv6 Echo Request and Echo Reply messages with an Authentication Header between the IPv6 header and the ICMPv6 header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2db0-303">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2db0-303">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2db0-304">Configurações recomendadas para IPv6</span><span class="sxs-lookup"><span data-stu-id="b2db0-304">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="b2db0-305">Sub-rede única com endereços de link local</span><span class="sxs-lookup"><span data-stu-id="b2db0-305">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="b2db0-306">Tráfego IPv6 entre nós em sub-redes diferentes de uma rede IPv4 (6to4)</span><span class="sxs-lookup"><span data-stu-id="b2db0-306">IPv6 traffic between nodes on different subnets of an IPv4 internetwork (6to4)</span></span>](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



