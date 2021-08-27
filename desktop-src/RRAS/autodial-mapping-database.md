---
title: Banco de dados de mapeamento automático
description: O banco de dados de mapeamento automático mapeia endereços de rede para entradas de lista telefônica RAS.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e89bd065a136492281adb3424636a8820c76c76bf6867e70db75aecfa0f345d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036716"
---
# <a name="autodial-mapping-database"></a>Banco de dados de mapeamento automático

O banco de dados de mapeamento automático mapeia endereços de rede para entradas de lista telefônica RAS. O banco de dados pode incluir endereços IP (por exemplo, "172.21.167.35"), nomes de host da Internet (por exemplo, "www.microsoft.com") ou nomes NetBIOS (por exemplo, "products1"). Associado a cada endereço no banco de dados AutoDial é um conjunto de uma ou mais [**entradas RASAUTODIALENTRY.**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) Cada uma dessas entradas especifica uma entrada de livro telefônica que o RAS pode discar para se conectar ao endereço de um local de discagem da TAPI (Interface de Programação de Aplicativo de Telefonia) específica. Para obter mais informações sobre locais de discagem TAPI, consulte a documentação da TAPI.

O AutoDial cria automaticamente entradas no banco de dados de mapeamento AutoDial em duas situações:

-   Quando uma tentativa de se conectar a um endereço de rede falha

    Se não houver nenhuma entrada para o endereço no banco de dados de mapeamento e o computador não estiver conectado a uma rede, diretamente ou por meio de RAS, o AutoDial solicitará que o usuário especifique as informações necessárias para estabelecer uma conexão discada. Se o usuário fornece as informações e a operação de conexão discada é bem-sucedida, o AutoDial armazena as informações no banco de dados de mapeamento.

-   Quando o computador está conectado a uma rede por meio de RAS

    Sempre que o usuário se conecta a um endereço de rede, o AutoDial cria uma entrada no banco de dados. A entrada mapeia o endereço de rede para a entrada de phone-book que foi usada para estabelecer a conexão RAS.

Você pode usar a [**função RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) para adicionar um endereço ao banco de dados de mapeamento AutoDial, excluir um endereço do banco de dados ou alterar as entradas AutoDial associadas a um endereço existente no banco de dados. Você pode usar a [**função RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) para recuperar as entradas AutoDial associadas a um endereço de rede especificado no banco de dados de mapeamento AutoDial. A [**função RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) retorna uma lista de todos os endereços no banco de dados de mapeamento AutoDial.

 

 