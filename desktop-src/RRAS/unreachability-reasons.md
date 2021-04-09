---
title: Motivos de inacessibilidade
description: A tabela a seguir lista os valores constantes que indicam por que uma interface está inacessível.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007898"
---
# <a name="unreachability-reasons"></a>Motivos de inacessibilidade

A tabela a seguir lista os valores constantes que indicam por que uma interface está inacessível.



| Valor                                       | Significado                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| \_administrador da interface MPR \_ \_ desabilitado             | O administrador desabilitou a interface.                                                  |
| \_ \_ falha na conexão da interface MPR \_         | Falha na tentativa de conexão anterior. Examine o membro **dwLastError** do código de erro. |
| \_restrição de \_ horas de discagem da interface MPR \_ \_ | A conexão discada não é permitida no momento atual.                                                   |
| \_interface \_ de MPR \_ sem \_ recursos          | Não há portas ou dispositivos disponíveis para uso.                                                     |
| serviço de interface de MPR em \_ \_ \_ pausa             | O serviço está em pausa.                                                                         |
| \_interface MPR \_ sem \_ sensor de mídia \_            | O cabo de rede está desconectado da placa de rede.                                       |
| INTERFACE de MPR \_ \_ sem \_ dispositivo                  | A placa de rede foi removida do computador.                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**INTERFACE de MPR \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**INTERFACE de MPR \_ \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**\_IFROW MIB**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**\_IFSTATUS MIB**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 