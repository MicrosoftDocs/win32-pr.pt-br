---
title: Banco de dados de mapeamento de discagem automática
description: O banco de dados de mapeamento de discagem automática mapeia endereços de rede para entradas do catálogo telefônico RAS.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511f15f98848559a892e8c20e766d47a07780fbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823807"
---
# <a name="autodial-mapping-database"></a>Banco de dados de mapeamento de discagem automática

O banco de dados de mapeamento de discagem automática mapeia endereços de rede para entradas do catálogo telefônico RAS. O banco de dados pode incluir endereços IP (por exemplo, "172.21.167.35"), nomes de host da Internet (por exemplo, "www.microsoft.com") ou nomes NetBIOS (por exemplo, "products1"). Associado a cada endereço no banco de dados de discagem automática é um conjunto de uma ou mais entradas [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) . Cada uma dessas entradas especifica uma entrada de catálogo telefônico que o RAS pode discar para se conectar ao endereço de um local de discagem da TAPI (interface de programação de aplicativo) de telefonia específica. Para obter mais informações sobre locais de discagem TAPI, consulte a documentação da TAPI.

A AutoDiscagem cria automaticamente entradas no banco de dados de mapeamento de discagem automática em duas situações:

-   Quando uma tentativa de conexão com um endereço de rede falha

    Se não houver nenhuma entrada para o endereço no banco de dados de mapeamento e o computador não estiver conectado a uma rede, diretamente ou por meio do RAS, a discagem automática solicitará que o usuário especifique as informações necessárias para estabelecer uma conexão discada. Se o usuário fornecer as informações e a operação de conexão discada for bem-sucedida, a discagem automática armazenará as informações no banco de dados de mapeamento.

-   Quando o computador está conectado a uma rede por meio de RAS

    Sempre que o usuário se conecta a um endereço de rede, a discagem automática cria uma entrada no banco de dados. A entrada mapeia o endereço de rede para a entrada do catálogo telefônico que foi usada para estabelecer a conexão RAS.

Você pode usar a função [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) para adicionar um endereço ao banco de dados de mapeamento de AutoDiscagem, excluir um endereço do banco de dados ou alterar as entradas de discagem automática associadas a um endereço existente no banco de dados. Você pode usar a função [**RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) para recuperar as entradas de discagem automática associadas a um endereço de rede especificado no banco de dados de mapeamento de discagem automática. A função [**RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) retorna uma lista de todos os endereços no banco de dados de mapeamento de AutoDiscagem.

 

 