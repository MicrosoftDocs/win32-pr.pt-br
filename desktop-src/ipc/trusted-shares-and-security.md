---
description: O DDE de rede usa compartilhamentos confiáveis e descritores de segurança para controlar o acesso a compartilhamentos.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Compartilhamentos e segurança confiáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899be51745b2b27c22212c3ceeaceea016fa8d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761783"
---
# <a name="trusted-shares-and-security"></a>Compartilhamentos e segurança confiáveis

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

O DDE de rede usa compartilhamentos confiáveis e descritores de segurança para controlar o acesso a compartilhamentos.

## <a name="trusted-shares"></a>Compartilhamentos confiáveis

Quando um usuário cliente se conecta a um compartilhamento DDE de um computador remoto, o DDE de rede aceita a solicitação somente se as seguintes instruções forem verdadeiras:

-   O usuário que criou o compartilhamento concedeu status confiável ao compartilhamento chamando [**NDdeSetTrustedShare**](nddesettrustedshare.md). Somente o criador do compartilhamento pode conceder status confiável ao compartilhamento. Nem mesmo um administrador pode conceder status confiável a um compartilhamento DDE criado por um usuário diferente.
-   O usuário que criou o compartilhamento está conectado no momento ao computador do servidor.

O processo de conceder status confiável a um compartilhamento adiciona o compartilhamento à lista de compartilhamentos confiáveis do usuário conectado no DSDM. Isso cria uma relação de confiança entre o servidor e seus clientes. Quando um compartilhamento DDE tiver um status confiável, os clientes poderão se conectar a ele, desde que o usuário que criou o compartilhamento esteja conectado. Quando o cliente se conecta ao compartilhamento de um computador remoto, o DDE de rede aceita a solicitação somente se o compartilhamento estiver listado na lista de compartilhamentos confiáveis do usuário conectado no DSDM.

## <a name="security"></a>Segurança

O DDE de rede executa uma verificação de segurança adicional quando o cliente solicita dados ou um link. Ele verifica se o servidor concedeu ao usuário remoto a permissão necessária para a operação. O servidor controla o acesso ao compartilhamento por meio do parâmetro *PSD* da função [**NDdeShareAdd**](nddeshareadd.md) . Esse parâmetro especifica o descritor de segurança. Se esse parâmetro for **nulo**, a função criará um descritor de segurança padrão que concede acesso completo ao criador do compartilhamento e concede permissão de leitura e vinculação a todos os outros usuários. Para conceder ou negar permissões adicionais a usuários individuais ou grupos de usuários, crie e use um descritor de segurança. Para obter mais informações sobre descritores de segurança, consulte [**controle de acesso**](/windows/desktop/SecAuthZ/access-control).

Para obter o descritor de segurança para um compartilhamento DDE existente, chame a função [**NDdeGetShareSecurity**](nddegetsharesecurity.md) . Você pode editar as informações e, em seguida, atualizar o descritor de segurança para o compartilhamento usando a função [**NDdeSetShareSecurity**](nddesetsharesecurity.md) .

 

 
