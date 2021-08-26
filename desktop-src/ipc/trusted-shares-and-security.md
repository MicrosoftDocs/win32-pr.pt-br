---
description: O DDE de rede usa compartilhamentos confiáveis e descritores de segurança para controlar o acesso a compartilhamentos.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Compartilhamentos confiáveis e segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bed3b520597f6cabe95929d2ee5bf9c29af6bb6c524d2aa136f4c86392cbb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014676"
---
# <a name="trusted-shares-and-security"></a>Compartilhamentos confiáveis e segurança

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

O DDE de rede usa compartilhamentos confiáveis e descritores de segurança para controlar o acesso a compartilhamentos.

## <a name="trusted-shares"></a>Compartilhamentos confiáveis

Quando um usuário cliente se conecta a um compartilhamento DDE de um computador remoto, o DDE de rede aceita a solicitação somente se as seguintes instruções são verdadeiras:

-   O usuário que criou o compartilhamento concedeu o status confiável ao compartilhamento chamando [**NDdeSetTrustedShare.**](nddesettrustedshare.md) Somente o criador do compartilhamento pode conceder status confiável ao compartilhamento. Nem mesmo um administrador pode conceder o status confiável a um compartilhamento DDE criado por um usuário diferente.
-   No momento, o usuário que criou o compartilhamento está conectado ao computador servidor.

O processo de concessão de status confiável a um compartilhamento adiciona o compartilhamento à lista de compartilhamentos confiáveis do usuário conectado no DSDM. Isso cria uma relação de confiança entre o servidor e seus clientes. Depois que um compartilhamento DDE tiver um status confiável, os clientes poderão se conectar a ele desde que o usuário que criou o compartilhamento seja conectado. Quando o cliente se conecta ao compartilhamento de um computador remoto, o DDE de rede aceita a solicitação somente se o compartilhamento estiver listado na lista de compartilhamentos confiáveis do usuário conectado no DSDM.

## <a name="security"></a>Segurança

O DDE de rede executa uma verificação de segurança adicional quando o cliente solicita dados ou um link. Ele verifica se o servidor concedeu ao usuário remoto a permissão necessária para a operação. O servidor controla o acesso ao compartilhamento por meio do *parâmetro pSD* da [**função NDdeShareAdd.**](nddeshareadd.md) Esse parâmetro especifica o descritor de segurança. Se esse parâmetro for **NULL,** a função criará um descritor de segurança padrão que concede acesso completo ao criador do compartilhamento e concede permissão de leitura e link a todos os outros usuários. Para conceder ou negar permissões adicionais a usuários individuais ou grupos de usuários, crie e use um descritor de segurança. Para obter mais informações sobre descritores de segurança, consulte [**Controle de acesso**](/windows/desktop/SecAuthZ/access-control).

Para obter o descritor de segurança para um compartilhamento DDE existente, chame a [**função NDdeGetShareSecurity.**](nddegetsharesecurity.md) Você pode editar as informações e atualizar o descritor de segurança para o compartilhamento usando a [**função NDdeSetShareSecurity.**](nddesetsharesecurity.md)

 

 
