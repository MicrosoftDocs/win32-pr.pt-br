---
description: Explica considerações sobre a implementação de funções de exportação de filtro de senha.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Considerações sobre programação de filtro de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9270a08c51b4b3e6b07923ad9461dc2e2dd418c3be1f1a181c07f940d71ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005084"
---
# <a name="password-filter-programming-considerations"></a>Considerações sobre programação de filtro de senha

Ao implementar funções [*de exportação de filtro*](/windows/desktop/SecGloss/p-gly) de senha, tenha as seguintes considerações em mente:

-   Tome muito cuidado ao trabalhar com [*senhas de texto*](/windows/desktop/SecGloss/p-gly) não criptografado. Enviar senhas de texto não criptografado por redes pode comprometer a segurança. Os "farejadores" de rede podem observar facilmente o tráfego de senha de texto não criptografado.
-   Apague toda a memória usada para armazenar senhas chamando a [**função SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) antes de liberar memória.
-   Todos os buffers passados para a notificação de senha e rotinas de filtro devem ser tratados como somente leitura. A escrita de dados nesses buffers pode causar um comportamento instável.
-   Todas as rotinas de filtro e notificação de senha devem ser thread-safe. Use seções críticas ou outras técnicas de programação síncrona para proteger os dados quando apropriado.
-   A notificação e a filtragem de senha ocorrem somente no computador que ressalva a conta.
-   Todos os controladores de domínio podem ser escritos, portanto, os pacotes de filtro de senha devem estar presentes em todos os controladores de domínio.

    **Windows NT domínios 4.0:** A notificação em contas de domínio ocorre somente no controlador de domínio primário. Além do controlador de domínio primário, os pacotes de filtro de senha devem ser instalados em todos os controladores de domínio de backup para permitir que as notificações continuem no caso de alterações na função de servidor.

-   Todas as DLLs de filtro de senha são [*executados no contexto de segurança*](/windows/desktop/SecGloss/s-gly) da conta do sistema local.



| Para obter informações sobre                                                                                                                     | Consulte                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Como instalar e registrar sua própria DLL [*de filtro de*](/windows/desktop/SecGloss/p-gly) senha. | [Instalando e registrando uma DLL de filtro de senha](installing-and-registering-a-password-filter-dll.md) |
| A DLL de filtro de senha fornecida pela Microsoft.                                                                                            | [Imposição de senha forte e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)         |
| Exportar funções implementadas por uma DLL de filtro de senha.                                                                                    | [Funções de filtro de senha](management-functions.md)                          |



 

 

 
