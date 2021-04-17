---
title: Diretrizes para gravar DLLs EAP
description: As DLLs ou plug-ins de EAP podem ser escritos para otimizar seu desempenho em diferentes cenários.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105791607"
---
# <a name="guidelines-for-writing-eap-dlls"></a>Diretrizes para gravar DLLs EAP

As DLLs ou plug-ins de EAP podem ser escritos para otimizar seu desempenho em diferentes cenários.

## <a name="general-guidelines"></a>Diretrizes gerais

-   Para criar uma conexão criptografada, os plug-ins EAP devem gerar chaves de criptografia e retorná-las por meio dos atributos RADIUS específicos do fornecedor da Microsoft MS-MPPE-Send-Keys e MS-MPPE-recv-Keys. Consulte a seção comentários na [**\_ \_ saída do PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) para obter mais informações.

## <a name="wireless-guidelines"></a>Diretrizes sem fio

Veja a seguir as diretrizes e recomendações para a gravação de um plug-in EAP que dá suporte à autenticação de computadores em cenários sem fio (802.1 X). Esta seção não se aplica a cenários de VPN e dial-up.

-   Para não bloquear a execução de sistemas autônomos, os plug-ins EAP não devem fazer nenhuma chamada de interface do usuário.
-   A implementação do plug-in do EAP da etapa de autenticação do computador deve ser concluída o mais rapidamente possível para que não atrapalhe a inicialização do sistema operacional.
    > [!Note]  
    > Se o protocolo EAP não oferecer suporte à autenticação de computador, ele deverá verificar o sinalizador de autenticação do computador, o **sinalizador de EAP do RAS \_ \_ \_ \_ auth Authentication** usado no campo **fFlags** na [**\_ \_ entrada PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)e retornar um erro.

     

 

 




