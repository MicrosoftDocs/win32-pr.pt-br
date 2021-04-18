---
description: As funções a seguir são usadas com o DDE de rede.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funções DDE de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807283"
---
# <a name="network-dde-functions"></a>Funções DDE de rede

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

As funções a seguir são usadas com o DDE de rede.



| Função                                                   | Descrição                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | Converte um código de erro retornado por uma função DDE de rede em uma cadeia de caracteres de erro que explica o código de erro retornado. |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | Recupera o descritor de segurança associado ao compartilhamento DDE.                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | Recupera as opções associadas a um compartilhamento DDE que está na lista de compartilhamentos confiáveis do usuário do servidor.                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | Determina se um aplicativo e uma cadeia de caracteres de tópico ("*AppName* \| *topicname*") usam a sintaxe correta.                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | Determina se um nome de compartilhamento usa a sintaxe apropriada.                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | Define o descritor de segurança associado ao compartilhamento DDE.                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | Concede o status confiável do compartilhamento DDE especificado no contexto do usuário atual.                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | Cria e adiciona um novo compartilhamento DDE ao Gerenciador de banco de dados de compartilhamento DDE (DSDM).                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | Exclui um compartilhamento DDE do DSDM.                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | Recupera a lista de compartilhamentos DDE disponíveis.                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | Recupera informações de compartilhamento de DDE.                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | Define informações de compartilhamento DDE.                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | Recupera os nomes de todos os compartilhamentos de DDE de rede que são confiáveis no contexto do processo de chamada.                 |



 

 

 



