---
title: Mapeando interfaces ADSI para as funções de gerenciamento de rede
description: As interfaces de serviço de Active Directory (ADSI) são um conjunto de interfaces COM usadas para acessar os recursos dos serviços de diretório de diferentes provedores de rede.
ms.assetid: dfa81c58-3ce4-40ee-8bfc-a19a13781992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ec1a1055d3d016bf8b7b1bd3f357810b7ddd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294492"
---
# <a name="mapping-adsi-interfaces-to-the-network-management-functions"></a>Mapeando interfaces ADSI para as funções de gerenciamento de rede

As interfaces de serviço de Active Directory (ADSI) são um conjunto de interfaces COM usadas para acessar os recursos dos serviços de diretório de diferentes provedores de rede. A ADSI apresenta um conjunto único de interfaces de serviço de diretório para gerenciar recursos de rede em um ambiente de computação distribuído.

Se estiver programando para Active Directory, você poderá chamar determinados métodos de interface ADSI para obter a mesma funcionalidade que pode obter ao chamar determinadas funções de gerenciamento de rede.

A tabela a seguir lista funções de gerenciamento de rede e grupos de funções e as interfaces ADSI para as quais as funções mapeiam.



| Funções                                                                  | Interfaces                                                                                             |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum), [ **NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations) |
| [Netgroup](group-functions.md)\*                                          | [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [Netlocal](local-group-functions.md)\*                               | [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetServer](server-functions.md)\*                                        | [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                                                  |
| [NetSession](session-functions.md)\*                                      | [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)   |
| [NetShare](share-functions.md)\*                                          | [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)                                                                |
| [Netuser](user-functions.md)\*                                            | [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser), [ **IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                   |
| [NetUserModals](user-modal-functions.md)\*                                | [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)                                                                      |



 

Para obter mais informações sobre serviços de diretório e programação com ADSI, consulte [Active Directory interfaces de serviço](/windows/desktop/ADSI/active-directory-service-interfaces-adsi). Para obter informações sobre as propriedades personalizadas que o provedor de WinNT disponibiliza para a classe de usuário e os métodos de propriedade da interface [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) , o provedor de WinNT não oferece suporte a, consulte [ADSI WinNT Provider](/windows/desktop/ADSI/adsi-winnt-provider).

 

 