---
title: Configurando computadores para RPC sobre HTTP
description: Para usar o HTTP como um protocolo de transporte para RPC, o proxy RPC em execução no IIS (servidor de informações da Internet) deve ser configurado na rede do programa do servidor.
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4628339afe09e2b6e9a6f216504f411550d37b7a285614e507c89a4a8052c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022466"
---
# <a name="configuring-computers-for-rpc-over-http"></a>Configurando computadores para RPC sobre HTTP

Para usar o HTTP como um protocolo de transporte para RPC, o proxy RPC em execução no IIS (servidor de informações da Internet) deve ser configurado na rede do programa do servidor. Esta seção descreve as opções de configuração. para obter recomendações sobre práticas recomendadas de programação e configuração ao usar rpc sobre http, consulte [Recomendações de implantação rpc sobre http](rpc-over-http-deployment-recommendations.md). A tarefa principal é configurar o proxy RPC para aceitar e encaminhar conexões RPC sobre HTTP a um programa de servidor RPC sobre HTTP.

O IIS deve primeiro ser instalado no computador que executa o proxy RPC. Depois que o IIS é instalado, o proxy RPC é instalado. o IIS e o Proxy RPC podem ser instalados simultaneamente de **adicionar/remover Windows componentes** no painel de controle. o proxy RPC é instalado dos **serviços de rede** e é chamado de **RPC sobre Proxy HTTP** na instalação do Windows. se o Proxy do IIS e do RPC forem instalados ao mesmo tempo, o Windows garantirá que eles sejam instalados na ordem correta.

> [!Note]  
> Após a conclusão da instalação, o IIS deverá ser reiniciado se estiver em execução durante o processo de instalação.

 

Após a instalação do proxy RPC, algumas tarefas adicionais de configuração devem ser executadas:

1.  Abra o snap-in do MMC do IIS e configure o diretório virtual do proxy RPC para exigir segurança, conforme explicado em [Segurança RPC sobre http](rpc-over-http-security.md). Esta etapa será necessária apenas se você planeja usar RPC sobre HTTP v2.
2.  Se o IIS não tiver um certificado instalado, um certificado válido deverá ser obtido e instalado para esse computador a fim de usar o SSL ao se comunicar com o proxy RPC. Esta etapa é relevante apenas para RPC sobre HTTP v2. Como o RPC sobre HTTP v1 não oferece suporte a SSL, essa etapa pode ser omitida para RPC sobre HTTP v1.
3.  Defina a chave **ValidPorts** conforme descrito em [Segurança RPC sobre http](rpc-over-http-security.md).

Quando essas tarefas de configuração são concluídas, o RPC sobre proxy HTTP está pronto para encaminhar solicitações do cliente RPC sobre HTTP para o servidor RPC sobre HTTP.

## <a name="rpc-over-http-registry-keys"></a>Chaves de registro RPC sobre HTTP

Esta seção explica as chaves de registro adicionais usadas para configurar o cliente, o servidor ou o proxy RPC em uma conexão RPC sobre HTTP. Geralmente, essas chaves não são necessárias; Eles são fornecidos aqui para fins de integridade.

**HKLM \\ software \\ Microsoft \\ RPC \\ DefaultChannelLifetime**

DWORD. Substitui o tempo de vida padrão do canal. Usado no cliente e no proxy RPC. O tempo de vida do canal é expresso em bytes. Se não for especificado, 1GB será usado. Usado somente no RPC sobre HTTP v2. Quando alterado no proxy RPC, o IIS deve ser reiniciado para que a alteração entre em vigor.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ ClientReceiveWindow**

DWORD. Quando presente, especifica a janela de recebimento usada pelo cliente para os dados recebidos do proxy RPC. O valor mínimo válido é 8K. O máximo é 1GB. Se o valor não estiver presente, 64K será usado. Usado somente no RPC sobre HTTP v2.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ InProxyReceiveWindow**

DWORD. Quando presente, especifica a janela de recebimento usada pelo proxy RPC para os dados recebidos do cliente. O valor mínimo válido é 8K. O máximo é 1GB. Se o valor não estiver presente, 64K será usado. Usado somente no RPC sobre HTTP v2. Quando são feitas alterações nesse valor, o IIS deve ser reiniciado para que a alteração entre em vigor.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ OutProxyReceiveWindow**

DWORD. Quando presente, especifica a janela de recebimento usada pelo proxy RPC para os dados recebidos do servidor. O valor mínimo válido é 8K. O máximo é 1GB. Se o valor não estiver presente, 64K será usado. Usado somente no RPC sobre HTTP v2. Quando são feitas alterações nesse valor, o IIS deve ser reiniciado para que a alteração entre em vigor.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ ServerReceiveWindow**

DWORD. Quando presente, especifica a janela de recebimento usada pelo servidor para os dados recebidos do proxy RPC. O valor mínimo válido é 8K. O máximo é 1GB. Se o valor não estiver presente, 64K será usado. Usado somente no RPC sobre HTTP v2. Quando são feitas alterações nesse valor, o IIS deve ser reiniciado para que a alteração entre em vigor.

\-

**HKLM \\ Software \\ policies \\ Microsoft \\ Windows NT \\ Rpc \\ MinimumConnectionTimeout**

DWORD. Quando presente, especifica o tempo limite mínimo de conexão usado pelo cliente e proxy de RPC, em segundos. O tempo limite real usado é o menor desse valor e o tempo limite de conexão ociosa do IIS. Se zero, ou a chave não estiver presente, o tempo limite de conexão ociosa do IIS será usado. Usado somente no RPC sobre HTTP v2. Quando são feitas alterações nesse valor no proxy RPC, o IIS deve ser reiniciado para que a alteração entre em vigor.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ UseProxyForIPAddrIfRDNSFails**

Quando presente e definido como diferente de zero e um endereço IP numérico é fornecido como o endereço de proxy RPC, um cliente RPC sobre HTTP tentará reverter a resolução de nome e, se isso falhar, tentará conectar-se ao proxy RPC por meio de um proxy HTTP. pode ser usado para emular o comportamento de Windows NT em instalações que exigem tal comportamento. Ignorado para RPC sobre HTTP v2. Usado somente quando RPC sobre HTTP v1 é usado. com suporte apenas no Windows 2000 com Service Pack 3 (SP3) e posterior.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RpcProxy \\ AllowAnonymous**

DWORD. Quando não estiver presente ou definido como zero, o proxy RPC verificará se a conexão é autenticada e se é seguro (SSL ou outra forma de criptografia é usada). Se for false, a conexão será rejeitada. Se esse valor contiver conexões diferentes de zero, anônimas e não criptografadas serão permitidas. Essa configuração é uma adição a qualquer configuração de diretório virtual. Por exemplo, se o acesso anônimo estiver desabilitado no nível do diretório virtual, mas **AllowAnonymous** for diferente de zero, o acesso anônimo ainda será bloqueado no nível do IIS. Usado no proxy RPC somente no RPC sobre HTTP v2. Quando são feitas alterações nesse valor no proxy RPC, o IIS deve ser reiniciado para que a alteração entre em vigor.

> [!WARNING]
> A Microsoft recomenda enfaticamente a definição do valor de **AllowAnonymous** em sistemas de produção para considerações de segurança. A única razão pela qual essa chave deve ser definida é para teste em redes fechadas sem acesso externo. Qualquer sistema conectado à Internet e executando o proxy RPC com a chave **AllowAnonymous** definida como um valor diferente de zero pode ser vulnerável a ataques.

 

 

 




