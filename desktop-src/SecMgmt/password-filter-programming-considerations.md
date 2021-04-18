---
description: Explica considerações sobre a implementação de funções de exportação de filtro de senha.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Considerações sobre programação de filtro de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778666"
---
# <a name="password-filter-programming-considerations"></a>Considerações sobre programação de filtro de senha

Ao implementar funções de exportação de [*filtro de senha*](/windows/desktop/SecGloss/p-gly) , tenha em mente as seguintes considerações:

-   Tome muito cuidado ao trabalhar com senhas de [*texto sem formatação*](/windows/desktop/SecGloss/p-gly) . O envio de senhas de texto sem formatação por redes pode comprometer a segurança. Os "farejadores" de rede podem facilmente inspecionar o tráfego de senha de texto não criptografado.
-   Apague toda a memória usada para armazenar senhas chamando a função [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) antes de liberar memória.
-   Todos os buffers passados para a notificação de senha e as rotinas de filtro devem ser tratados como somente leitura. Gravar dados nesses buffers pode causar comportamento instável.
-   Todas as notificações de senha e as rotinas de filtro devem ser thread-safe. Use seções críticas ou outras técnicas de programação síncronas para proteger os dados quando apropriado.
-   A notificação e a filtragem de senha ocorrem somente no computador que hospeda a conta.
-   Todos os controladores de domínio são graváveis, portanto, os pacotes de filtro de senha devem estar presentes em todos os controladores de domínio.

    **Domínios do Windows NT 4,0:** A notificação em contas de domínio só ocorre no controlador de domínio primário. Além do controlador de domínio primário, os pacotes de filtro de senha devem ser instalados em todos os controladores de domínio de backup para permitir que as notificações continuem no caso de alterações na função do servidor.

-   Todas as DLLs de filtro de senha são executadas no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) da conta do sistema local.



| Para obter informações sobre                                                                                                                     | Consulte                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Como instalar e registrar sua própria DLL de [*filtro de senha*](/windows/desktop/SecGloss/p-gly) . | [Instalando e registrando uma DLL de filtro de senha](installing-and-registering-a-password-filter-dll.md) |
| A DLL de filtro de senha fornecida pela Microsoft.                                                                                            | [Imposição de senha forte e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| Funções de exportação implementadas por uma DLL de filtro de senha.                                                                                    | [Funções de filtro de senha](management-functions.md)                          |



 

 

 
