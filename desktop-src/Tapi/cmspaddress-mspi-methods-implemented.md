---
description: A seguir estão os métodos MSPI padrão que todas as MSPs devem implementar. A documentação principal para esses métodos existe na seção de referência da MSPI (interface do provedor de serviços de mídia).
ms.assetid: 22d4828e-f439-44ca-aa6c-f7f18c5fd64f
title: Métodos CMSPAddress MSPI implementados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed19bbacc13990d052c35bda68f97db80ff68ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760168"
---
# <a name="cmspaddress-mspi-methods-implemented"></a>Métodos CMSPAddress MSPI implementados

A seguir estão os métodos MSPI padrão que todas as MSPs devem implementar. A documentação principal para esses métodos existe na seção de [referência da MSPI (interface do provedor de serviços de mídia)](media-service-provider-interface-mspi-reference.md) .



| Métodos CMSPAddress                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inicializar**](/windows/desktop/api/msp/nf-msp-itmspaddress-initialize)                                                | (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Chamado por TAPI3 quando este MSP é criado pela primeira vez.                                                                                                                                                                                                                                                                                                   |
| [**Desligar**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown)                                                    | (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Chamado por TAPI3 quando este endereço não está mais em uso.                                                                                                                                                                                                                                                                                         |
| [**ReceiveTSPData**](/windows/desktop/api/msp/nf-msp-itmspaddress-receivetspdata)                                        | (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Chamado por TAPI3 quando o TSP envia dados para este objeto de endereço MSP.                                                                                                                                                                                                                                                                               |
| [**GetEvent**](/windows/desktop/api/msp/nf-msp-itmspaddress-getevent)                                                    | (Interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)) Chamado por TAPI3 para obter informações detalhadas sobre um evento.                                                                                                                                                                                                                                                                                       |
| [**obter \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals)                        | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Wrapper de automação OLE para a função auxiliar [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                            |
| [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals)               | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Wrapper de enumeração para a função auxiliar [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals).                                                                                                                                                                                                                               |
| [**obter \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)          | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Wrapper de automação OLE para a função auxiliar [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                              |
| [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Wrapper de enumeração para a função auxiliar [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses).                                                                                                                                                                                                                 |
| [**Createterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)                                   | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Esse método é chamado pelo aplicativo para criar um terminal dinâmico. Ele agenda um item de trabalho no thread de trabalho do MSP, que, quando executado, solicita que o Gerenciador de terminal crie um terminal dinâmico. A classe derivada pode substituir esse método para ter sua própria maneira de criar um terminal dinâmico.                                |
| [**GetDefaultStaticTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-getdefaultstaticterminal)               | (Interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)) Esse método é chamado pelo aplicativo para obter o terminal estático padrão para um tipo e uma direção especificados. Ele atualiza a lista de terminais padrão (se necessário) e retorna o ponteiro de interface. A classe derivada pode substituir esse método para ter sua própria maneira de decidir qual terminal é o padrão. Bloqueia as listas de terminal. |



 

 

 
