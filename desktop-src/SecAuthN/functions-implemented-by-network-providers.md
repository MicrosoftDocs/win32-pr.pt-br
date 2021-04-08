---
description: As funções a seguir são implementadas por uma DLL de provedor de rede para se comunicar com o roteador de vários provedores (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Funções implementadas por provedores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922529"
---
# <a name="functions-implemented-by-network-providers"></a>Funções implementadas por provedores de rede

As funções a seguir são implementadas por uma DLL de provedor de rede para se comunicar com o [*roteador de vários provedores*](/windows/desktop/SecGloss/m-gly) (MPR). Observe que somente as [funções Capabilities](capabilities-functions.md) devem ser implementadas por um provedor de rede. A implementação dos outros tipos de funções é opcional e depende dos requisitos do provedor de rede.



| Conjunto de funções                                                                                    | Descrição                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funções de recursos](capabilities-functions.md)<br/>                                 | Permite que o chamador determine os recursos do provedor de rede.<br/>                                                                |
| [Funções de nome de usuário](user-name-functions.md)<br/>                                       | Solicita ao provedor de rede o nome de usuário associado a uma conexão.<br/>                                                            |
| [Funções de redirecionamento de dispositivo](device-redirecting-functions.md)<br/>                     | Permite que um provedor de rede redirecione dispositivos, letras de unidade e portas LPT que são padrão no sistema operacional Microsoft MS-DOS.<br/> |
| [Funções de caixa de diálogo específicas do provedor](provider-specific-dialog-box-functions.md)<br/> | Permite que um provedor de rede exiba ou atue em informações específicas da rede.<br/>                                                            |
| [Funções administrativas](administrative-functions.md)<br/>                             | Permite que um provedor de rede exiba ou atue em diretórios de rede especiais.<br/>                                                             |
| [Funções de enumeração](enumeration-functions.md)<br/>                                   | Permite que o usuário procure recursos de rede.<br/>                                                                                            |



 

Para obter mais informações sobre como criar e registrar um provedor de rede, consulte [implementando um provedor de rede](implementing-a-network-provider.md) e [registrando provedores de rede e gerenciadores de credenciais](registering-network-providers-and-credential-managers.md).

 

