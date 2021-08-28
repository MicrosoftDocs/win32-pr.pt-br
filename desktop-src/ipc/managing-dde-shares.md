---
description: O DDE de rede fornece funções que permitem excluir um compartilhamento, obter ou definir informações de compartilhamento ou enumerar compartilhamentos.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Gerenciando compartilhamentos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa89b890c9cf2b140f669b5e4dfa556cd11f978d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472162"
---
# <a name="managing-dde-shares"></a>Gerenciando compartilhamentos DDE

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

O DDE de rede fornece funções que permitem excluir um compartilhamento, obter ou definir informações de compartilhamento ou enumerar compartilhamentos.




| Tarefa | Procedimento | 
|------|-----------|
| Excluir um compartilhamento DDE | Use a <a href="nddesharedel.md"><strong>função NDdeShareDel.</strong></a> | 
| Obter informações de compartilhamento de DDE | Use a <a href="nddesharegetinfo.md"><strong>função NDdeShareGetInfo.</strong></a> | 
| Definir informações de compartilhamento de DDE | Use a <a href="nddesharesetinfo.md"><strong>função NDdeShareSetInfo.</strong></a> | 
| Enumerar compartilhamentos DDE | Use a <a href="nddeshareenum.md"><strong>função NDdeShareEnum.</strong></a> Você também pode enumerar os compartilhamentos de DDE confiáveis usando a <a href="nddetrustedshareenum.md"><strong>função NDdeTrustedShareEnum.</strong></a><br /> | 
| Enumerar usuários conectados | Use a <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>função NetSessionEnum.</strong></a> | 
| Alterar o nome do compartilhamento DDE | Exclua o compartilhamento antigo e crie um novo compartilhamento.<ol><li>Recupere as informações de compartilhamento <a href="nddesharegetinfo.md"><strong>usando NDdeShareGetInfo</strong></a>.</li><li>Remova o compartilhamento usando <a href="nddesharedel.md"><strong>NDdeShareDel.</strong></a></li><li>Altere <strong>o membro lpszShareName</strong> da estrutura <a href="nddeshareinfo-str.md"><strong>NDINFOAREINFO</strong></a> retornada por <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo.</strong></a></li><li>Passe a estrutura <a href="nddeshareinfo-str.md"><strong>NDSHAAREINFO modificada</strong></a> <a href="nddeshareadd.md"><strong>para NDdeShareAdd.</strong></a></li></ol> | 




 

 

