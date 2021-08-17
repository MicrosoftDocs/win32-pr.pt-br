---
description: As funções a seguir são usadas com o DDE de rede.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Funções DDE de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b37e83dd6b335e1acd2e77010fa61d0da5e3e26af5b46eef54d5ee20cf2eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756305"
---
# <a name="network-dde-functions"></a>Funções DDE de rede

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

As funções a seguir são usadas com o DDE de rede.



| Função                                                   | Descrição                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | Converte um código de erro retornado por uma função DDE de rede em uma cadeia de caracteres de erro que explica o código de erro retornado. |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | Recupera o descritor de segurança associado ao compartilhamento DDE.                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | Recupera as opções associadas a um compartilhamento DDE que está na lista de compartilhamentos confiáveis do usuário do servidor.                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | Determina se uma cadeia de caracteres de aplicativo e tópico ("*AppName* \| *TopicName*") usa a sintaxe adequada.                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | Determina se um nome de compartilhamento usa a sintaxe adequada.                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | Define o descritor de segurança associado ao compartilhamento DDE.                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | Concede o status confiável de compartilhamento de DDE especificado dentro do contexto do usuário atual.                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | Cria e adiciona um novo compartilhamento DDE ao DSDM (gerenciador de banco de dados de compartilhamento DDE).                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | Exclui um compartilhamento DDE do DSDM.                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | Recupera a lista de compartilhamentos DDE disponíveis.                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | Recupera informações de compartilhamento de DDE.                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | Define informações de compartilhamento de DDE.                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | Recupera os nomes de todos os compartilhamentos DDE de rede confiáveis no contexto do processo de chamada.                 |



 

 

 



