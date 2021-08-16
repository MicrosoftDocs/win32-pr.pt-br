---
title: Diretrizes para escrever DLLs de EAP
description: DLLs ou Plug-ins EAP podem ser escritos para otimizar seu desempenho em cenários diferentes.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c786da1ca026039ffd052f1213b2904dbfa602ee67c6d74aed7a0fe11fd9d566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499151"
---
# <a name="guidelines-for-writing-eap-dlls"></a>Diretrizes para escrever DLLs de EAP

DLLs ou Plug-ins EAP podem ser escritos para otimizar seu desempenho em cenários diferentes.

## <a name="general-guidelines"></a>Diretrizes gerais

-   Para criar uma conexão criptografada, os plug-ins EAP devem gerar chaves de criptografia e devolvê-las por meio dos atributos RADIUS específicos do fornecedor da Microsoft MS-MPPE-Send-Keys e MS-MPPE-Recv-Keys. Consulte a seção Comentários em [**PPP \_ EAP \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) para obter mais informações.

## <a name="wireless-guidelines"></a>Diretrizes sem fio

Veja a seguir diretrizes e recomendações para escrever um Plug-in EAP que dá suporte à autenticação de máquinas em cenários sem fio (802.1X). Esta seção não se aplica a cenários de VPN e discagem.

-   Para não bloquear a execução autônoma de sistemas, os plug-ins de EAP não devem fazer nenhuma chamada de interface do usuário.
-   A implementação do Plug-in EAP da etapa de autenticação do computador deve ser concluída o mais rápido possível para que não atrapalhe a inicialização do sistema operacional.
    > [!Note]  
    > Se o protocolo EAP não dá suporte à autenticação de computador, ele deve verificar o sinalizador de autenticação do computador, **\_ \_ \_ \_ AUTH** de MÁQUINA DE SINALIZADOR RAS EAP usado no campo **fFlags** em [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)e retornar um erro.

     

 

 




