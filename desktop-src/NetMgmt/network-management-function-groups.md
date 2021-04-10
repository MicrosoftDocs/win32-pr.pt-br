---
title: Grupos de funções de gerenciamento de rede
description: As funções de gerenciamento de rede podem ser divididas nos grupos a seguir.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bce5c0fb3dd70facb0ebbbb2479b968d428c49e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007718"
---
# <a name="network-management-function-groups"></a>Grupos de funções de gerenciamento de rede

As funções de gerenciamento de rede podem ser divididas nos seguintes grupos:

-   [Funções de alerta](alert-functions.md)
-   [Funções ApiBuffer](apibuffer-functions.md)
-   [Funções de serviço de diretório](directory-service-functions.md)
-   [Funções de Sistema de Arquivos Distribuído (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Obter funções](get-functions.md)
-   [Funções de grupo](group-functions.md)
-   [Funções de grupo local](local-group-functions.md)
-   [Funções de mensagem](message-functions.md)
-   [Funções de netfile](netfile-functions.md)
-   [Funções do utilitário remoto](remote-utility-functions.md)
-   [Funções de agendamento](schedule-functions.md)
-   [Funções de servidor](server-functions.md)
-   [Funções de transporte de servidor e estação de trabalho](server-and-workstation-transport-functions.md)
-   [Funções de sessão](session-functions.md)
-   [Funções de compartilhamento](share-functions.md)
-   [Funções de estatísticas](/windows/desktop/NetShare/statistics-functions)
-   [Usar funções](use-functions.md)
-   [Funções de usuário](user-functions.md)
-   [Funções modais do usuário](user-modal-functions.md)
-   [Funções de usuário da estação de trabalho e estação de trabalho](workstation-and-workstation-user-functions.md)

Se estiver programando para Active Directory, você poderá chamar determinados métodos de interface ADSI para obter a mesma funcionalidade que pode obter ao chamar determinadas funções de gerenciamento de rede. Para obter mais informações, consulte [mapeando interfaces ADSI para as funções de gerenciamento de rede](mapping-adsi-interfaces-to-the-network-management-functions.md).

O sistema também fornece um conjunto independente de rede de funções de rede ([funções WNet](/windows/desktop/WNet/wnet-functions)) que permitem que as funções de rede funcionem entre os produtos de diferentes fornecedores de rede. Se seu aplicativo puder ser convertido para usar uma função WNet, você deverá executar a conversão. Há motivos para fazer a alteração:

-   As funções WNet são independentes de rede, enquanto as funções de gerenciamento de rede funcionam apenas em redes Microsoft.
-   Algumas das funções podem não ter suporte em versões futuras dos sistemas operacionais da Microsoft, caso tenham sido substituídas. A Microsoft não planeja remover funções específicas, a menos que a funcionalidade equivalente ou melhor esteja disponível.

 

 