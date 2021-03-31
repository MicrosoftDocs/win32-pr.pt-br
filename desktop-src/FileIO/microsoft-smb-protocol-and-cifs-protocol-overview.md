---
description: Descreve a implementação da Microsoft do protocolo SMB.
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Visão geral de protocolo CIFS e protocolo Microsoft SMB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30326221694ce843733f6da7a6ad49c8dff336ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920872"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Visão geral de protocolo CIFS e protocolo Microsoft SMB

O protocolo SMB é um protocolo de compartilhamento de arquivos de rede e, conforme implementado no Microsoft Windows, é conhecido como protocolo SMB da Microsoft. O conjunto de pacotes de mensagens que define uma versão específica do protocolo é chamado de dialeto. O protocolo CIFS (Common Internet File System) é um dialeto de SMB. Tanto o SMB quanto o CIFS também estão disponíveis em VMS, em várias versões do UNIX e em outros sistemas operacionais.

A referência técnica ao CIFS está disponível na Microsoft Corporation em [protocolo de acesso a arquivos CIFS (Common Internet File System)](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b).

Embora sua principal finalidade seja o compartilhamento de arquivos, a funcionalidade adicional do protocolo Microsoft SMB inclui o seguinte:

-   [Negociação de dialeto](microsoft-smb-protocol-dialects.md)
-   Determinar outros servidores de protocolo Microsoft SMB na rede ou navegação na rede
-   Imprimindo em uma rede
-   [Arquivo, diretório e compartilhamento de autenticação de acesso](microsoft-smb-protocol-authentication.md)
-   Bloqueio de arquivo e registro
-   Notificação de alteração de arquivo e diretório
-   Manipulação de atributo de arquivo estendido
-   Suporte de Unicode
-   [Bloqueios oportunistas](opportunistic-locks.md)

No modelo de rede OSI, o protocolo SMB da Microsoft é usado com mais frequência como uma camada de aplicativo ou um protocolo de camada de apresentação e se baseia em protocolos de nível inferior para transporte. O protocolo de camada de transporte em que o protocolo SMB da Microsoft é usado com mais frequência é NetBIOS sobre TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))). No entanto, o protocolo SMB da Microsoft também pode ser usado sem um protocolo de transporte separado a combinação do protocolo Microsoft SMB/NBT geralmente é usada para compatibilidade com versões anteriores.

O protocolo SMB da Microsoft é uma implementação de cliente-servidor e consiste em um conjunto de pacotes de dados, cada um contendo uma solicitação enviada pelo cliente ou uma resposta enviada pelo servidor. Esses pacotes podem ser amplamente classificados da seguinte maneira:

-   Os pacotes de controle de sessão estabelecem e descontinuam uma conexão com os recursos do servidor compartilhado.
-   Os pacotes de acesso a arquivos acessam e manipulam arquivos e diretórios no servidor remoto.
-   Os pacotes de mensagem geral enviam dados para filas de impressão, processadores de mensagens e pipes nomeados e fornecem dados sobre o status das filas de impressão.

Alguns pacotes de mensagens podem ser agrupados e enviados em uma transmissão para reduzir a latência de resposta e aumentar a largura de banda da rede. Isso é chamado de "envio em lote". A seção [cenário de intercâmbio de pacotes do protocolo Microsoft SMB](microsoft-smb-protocol-packet-exchange-scenario.md) descreve um exemplo de uma sessão do protocolo SMB da Microsoft que usa o envio em lote de pacotes.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                             | Descrição                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dialetos do protocolo SMB da Microsoft](microsoft-smb-protocol-dialects.md)<br/>                                 | Para estabelecer uma conexão entre um cliente e um servidor usando o protocolo SMB da Microsoft, primeiro você deve determinar o dialeto com o nível mais alto de funcionalidade que o cliente e o servidor dão suporte.<br/>                                                      |
| [Autenticação do protocolo SMB da Microsoft](microsoft-smb-protocol-authentication.md)<br/>                     | O modelo de segurança usado no protocolo SMB da Microsoft é idêntico ao usado por outras variantes de SMB e consiste em dois níveis de usuário e compartilhamento de segurança. Um compartilhamento é um arquivo, diretório ou impressora que pode ser acessado pelos clientes do protocolo Microsoft SMB.<br/> |
| [Cenário de intercâmbio de pacotes do protocolo SMB da Microsoft](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | Exemplo de um intercâmbio de pacotes do protocolo SMB da Microsoft entre um cliente e um servidor.<br/>                                                                                                                                                                               |



 

 

