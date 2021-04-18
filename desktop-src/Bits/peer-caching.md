---
title: Cache de pares
description: A partir do Serviço de Transferência Inteligente em Segundo Plano (BITS) 4,0, o serviço BITS foi estendido para permitir o cache de sistemas pares de nível de sub-rede para dados de URL baixados usando o Windows BranchCache.
ms.assetid: 4197eed3-1812-4440-99e7-9462635ef6ad
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3c87e6013bb37610e934c13414bd2636407108ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105755715"
---
# <a name="peer-caching"></a>Cache de pares

A partir do Serviço de Transferência Inteligente em Segundo Plano (BITS) 4,0, o serviço BITS foi estendido para permitir o cache de sistemas pares de nível de sub-rede para dados de URL baixados usando o Windows BranchCache. Os clientes do BITS podem recuperar dados de outros computadores em sua própria sub-rede que já baixaram os dados, em vez de recuperar os dados de servidores remotos. Para obter mais informações sobre o Windows BranchCache, consulte a [visão geral do BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

Se um administrador habilitar o Windows BranchCache em computadores cliente e servidor em uma organização por meio de uma política de grupo ou de definições de configuração local, o BITS usará o Windows BranchCache para transferências de dados.

-   [Configuração para o cache de pares de BITS 4,0](#configuration-for-bits-40-peer-caching)
-   [Desabilitando o Windows BranchCache](#disabling-windows-branchcache)
-   [Verificação e monitoramento](#verification-and-monitoring)
-   [Cache de pares em BITS 3,0](#peer-caching-in-bits-30)

## <a name="configuration-for-bits-40-peer-caching"></a>Configuração para o cache de pares de BITS 4,0

A configuração a seguir é necessária para o cache de pares em BITS 4,0 para funcionar:

-   O Windows BranchCache deve ser habilitado no cliente por meio de uma política de grupo ou definições de configuração local. Para obter mais informações, consulte [configuração do cliente BranchCache](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10)).
    > [!Note]  
    > O recurso Windows BranchCache está desabilitado por padrão.

     

-   O recurso Windows BranchCache é um componente opcional que deve ser instalado no servidor. Para obter mais informações, consulte [configuração do servidor do BranchCache](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
-   O servidor também deve habilitar o recurso Windows BranchCache, embora a política de grupo ou as definições de configuração local. Para obter mais informações, consulte [configuração do servidor do BranchCache](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
    > [!Note]  
    > O recurso Windows BranchCache está desabilitado por padrão.

     

A política de grupo BITS padrão permite o cache de sistemas pares. Se o Windows BranchCache estiver habilitado globalmente em um computador, esse recurso também será habilitado para trabalhos de transferência de BITS. Para obter mais informações sobre as políticas de grupo específicas de BITS, consulte [políticas de grupo](group-policies.md).

## <a name="disabling-windows-branchcache"></a>Desabilitando o Windows BranchCache

Um administrador pode usar uma política de grupo para desabilitar o uso do Windows BranchCache. (Consulte [políticas de grupo](group-policies.md).) Se o Windows BranchCache estiver desabilitado, os clientes do BITS recuperarão dados somente de servidores remotos.

Um aplicativo também pode desabilitar o Windows BranchCache por trabalho chamando o método [**IBackgroundCopyJob4:: SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) e definindo o sinalizador de **\_ \_ \_ cache de ramificação BG Disable** .

> [!Note]  
> Essas configurações não afetam o uso do Windows BranchCache por aplicativos que não sejam BITS. Essas configurações não se aplicam a transferências de BITS por SMB. O BITS não controla nenhuma configuração para transferências do Windows BranchCache por SMB.

 

## <a name="verification-and-monitoring"></a>Verificação e monitoramento

Há várias maneiras de verificar e monitorar as estatísticas de cache de mesmo nível. Os administradores podem chamar o método [**IBackgroundCopyFile4:: GetPeerDownloadStats**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) para consultar a quantidade de dados baixados de pares e de servidores de origem. Os administradores também podem verificar o log de eventos para a [ID de evento 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10)), que fornece informações específicas do trabalho.

O recurso Windows BranchCache também fornece vários mecanismos para verificar e monitorar as estatísticas de cache de mesmo nível. Para obter mais informações, consulte [verificação e monitoramento](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) e [contadores de desempenho](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10)).

O modelo de cache de sistemas pares que usa o Windows BranchCache substitui o modelo de cache de sistemas pares usado em BITS 3,0. Para obter mais informações sobre o Windows BranchCache, consulte o seguinte:

-   [BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))
-   [Visão geral do BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))
-   [Serviços do Windows 7](../win7devguide/services.md)
-   [API de distribuição de pares](../p2psdk/peer-distribution.md)

## <a name="peer-caching-in-bits-30"></a>Cache de pares em BITS 3,0

> [!Note]  
> A partir do Windows 7, o modelo de cache de pares BITS 3,0 é preterido. Se o BITS 4,0 estiver instalado, o modelo de cache de pares de BITS 3,0 estará indisponível.

 

Se o administrador habilitar o cache de sistemas pares e o trabalho permitir o download de conteúdo de um par, o BITS tentará baixar o conteúdo de um ou mais pares. O download de um par é muito mais rápido do que baixar conteúdo da Internet. O cache de pares é desabilitado por padrão e os trabalhos devem permitir explicitamente o download de conteúdo de pares. Um administrador pode usar uma política de grupo para habilitar o cache de sistemas pares. Depois de habilitar o cache de sistemas pares, o administrador pode desabilitar o download de um par ou fornecer conteúdo a um par.

Um aplicativo também pode habilitar o cache de pares chamando o método [**IBitsPeerCacheAdministration:: SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) . No entanto, essas configurações são substituídas pelas configurações da política de grupo, se definidas.

Quando o cache de pares está habilitado, o BITS cria uma lista de pares que estão na mesma sub-rede e pertencem ao mesmo domínio. A lista não incluirá pares de um domínio confiável. O cache de pares pode ser habilitado somente em um ambiente de domínio.

O BITS descobre os pares fazendo o seguinte:

-   Escutando servidores pares que se anunciam. Um servidor de mesmo nível se anunciará quando for iniciado. O BITS adicionará o servidor de mesmo nível à lista se o cliente precisar de mais pontos em sua lista.
-   Transmitir uma solicitação de servidores pares quando ele precisar de mais pares em sua lista de pares. Os servidores pares que estão disponíveis para atender o conteúdo respondem à solicitação.

O BITS removerá os servidores pares da lista de pares se o servidor faz o seguinte:

-   Falha na autenticação
-   Está offline (não disponível) por muito tempo
-   Fornece um certificado com erros

Quando um trabalho solicita conteúdo de um par, o BITS escolhe aleatoriamente um subconjunto de pares da lista de pares e pergunta se eles têm o conteúdo. O BITS pode baixar conteúdo somente de servidores de mesmo nível autenticados. O cliente e o servidor se autenticam inicialmente usando o Kerberos e, em seguida, trocam certificados autoassinados para autenticação durante a descoberta e download de conteúdo.

O BITS baixa o conteúdo do primeiro par autenticado para responder à solicitação. Se um par não contiver todo o conteúdo, o BITS baixará o que ele pode de um ou mais dos pares antes de baixar o restante do servidor de origem. Se nenhum dos pares tiver o conteúdo ou se ocorrer um erro durante o download de um par, o BITS baixará o conteúdo do servidor de origem.

O conteúdo baixado fica disponível para servir a outros pares somente depois que o aplicativo valida o conteúdo dos arquivos. Se o aplicativo não validar explicitamente o arquivo, o arquivo será validado implicitamente quando o aplicativo concluir o trabalho.

Por padrão, um servidor de mesmo nível pode fornecer conteúdo a apenas três clientes simultaneamente. Se o servidor estiver atualmente ocupado atendendo a três clientes, haverá um atraso ao responder a outras solicitações. O BITS limita a largura de banda usada para fornecer conteúdo a 1 Mbps. Você pode usar a política de grupo [MaxBandwidthServed](group-policies.md) para alterar o limite.

> [!Note]  
> Esse recurso tem suporte apenas em redes de domínio; Não há suporte para o cache de pares em grupos de armazenamento ou redes domésticas.

Consulte também [administrando o cache par](/windows/desktop/Bits/administering-the-peer-cache)
 

 

 