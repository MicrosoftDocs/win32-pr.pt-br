---
description: Os nomes de pares são usados pelo PNRP (Peer Name Resolution Protocol), pelo Gerenciador de identidades de mesmo nível e pela infraestrutura de agrupamento de pares.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Nomes de par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756706"
---
# <a name="peer-names"></a>Nomes de par

Os nomes de pares são usados pelo PNRP (Peer Name Resolution Protocol), pelo Gerenciador de identidades de mesmo nível e pela infraestrutura de agrupamento de pares. Os nomes de pares são nomes estáveis para recursos como computadores, usuários, grupos ou serviços. O PNRP usa nomes de pares para identificar nós em uma rede de mesmo nível.

> [!Note]  
> Um ponto de extremidade usado pela infraestrutura de pares é, na verdade, uma tupla que consiste em um endereço IPv4 ou IPv6, porta e protocolo (TCP ou UDP). Um nome de par pode ter mais de uma tupla.

 

Um nome de par é uma cadeia de caracteres de texto que tem o seguinte formato:

-   "Authority. classificador"

O valor de uma autoridade depende de se o nome é seguro ou não. O classificador de um nome de par é uma cadeia de caracteres. Um classificador pode ser qualquer nome que contenha 150 ou menos caracteres UNICODE. Os nomes de pares diferenciam maiúsculas de minúsculas e podem ser registrados como protegidos ou não seguros. A lista a seguir identifica alguns exemplos de nomes de pares:

-   "0. MyUnsecuredPeerName"
-   "0. davibarros. Games"
-   "6520c005f63fc1864b7d8f3cabebd4916ae7f33d. Davibarros

## <a name="secure-peer-names"></a>Nomes de pares seguros

Para um nome seguro, a autoridade é o hash do SHA (algoritmo de hash seguro) da chave pública do nome do par e resulta em uma cadeia de caracteres hexadecimal de 40 caracteres. Um nome de par seguro só pode ser registrado com PNRP pelo proprietário ou pelo delegado do proprietário do nome de par. Um nome de par protegido deve ser criado chamando [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).

## <a name="unsecured-peer-names"></a>Nomes de pares não seguros

Para um nome não seguro, a autoridade é zero (0) e o classificador é a única parte significativa do nome de par, que cria um nome de par não seguro sem uma [identidade](identity-manager-api.md)associada. Os nomes de pares não seguros são usados na resolução e no registro de nome PNRP. Os nomes de pares não seguros fornecem uma maneira útil de registrar e resolver recursos que não exigem resolução de nomes segura. No entanto, qualquer nó pode publicar qualquer nome não seguro. Os aplicativos preocupados com a segurança devem garantir que eles sejam robustos e protegidos em seu consumo de nomes de pares não seguros.

> [!Note]  
> Qualquer pessoa pode registrar um nome de par não seguro com o PNRP.

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a>PNRP e a instância de nome de par mais próxima

Pode haver mais de uma instância de um nome de par. Ao usar o [PNRP](pnrp-namespace-provider-api.md) para resolver um nome de par, há um conceito de uma instância de nome de par **mais próximo** , o que significa que o nome tem um local de serviço mais próximo do membro **saHint** especificado em [**PNRPINFO \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) ou [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)). Se nenhuma dica for fornecida, mais próximo de um dos endereços IP locais.

 

 
