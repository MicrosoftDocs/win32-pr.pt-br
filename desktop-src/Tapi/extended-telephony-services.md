---
description: A API contém um mecanismo que permite aos fornecedores do provedor de serviços estender a API de telefonia usando extensões específicas do dispositivo.
ms.assetid: 02749ce5-40db-487e-b51e-e3692266342c
title: Serviços de telefonia estendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403f57904138b3797069222875086b0a4990b8e625f701f380120d65c235784e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140699"
---
# <a name="extended-telephony-services"></a>Serviços de telefonia estendidos

A API contém um mecanismo que permite aos fornecedores do provedor de serviços estender a API de telefonia usando extensões específicas do dispositivo. Serviços de telefonia estendidos (ou serviços específicos do dispositivo) incluem todas as extensões para a API definida por um provedor de serviços específico. Como a API define apenas o mecanismo de extensão, o provedor de serviços deve especificar completamente a definição do comportamento do serviço de Extended-Telephony.

## <a name="tapi-2x-extended-telephony"></a>Telefonia de TAPI 2. x estendida

O mecanismo de extensão permite que os fornecedores do provedor de serviços definam novos valores para alguns tipos de enumeração e sinalizadores de bits e adicionem Membros à maioria das estruturas de dados. A interpretação de extensões é desligada do identificador de extensão do provedor de serviços, um identificador para a especificação do conjunto de extensões com suporte, que pode cruzar vários fabricantes. Funções e mensagens especiais, como [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) e [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) , são fornecidas na API para permitir que um aplicativo se comunique diretamente com um provedor de serviços. O provedor de serviços também define os parâmetros para cada função.

Os fornecedores não precisam se registrar para serem atribuídos a identificadores de extensão. Em vez disso, um utilitário chamado EXTIDGEN (Extidgen.exe) é fornecido no SDK (Software Development Kit) da plataforma que permite a geração local de identificadores de extensão. Esse identificador exclusivo é composto por um endereço de adaptador Ethernet, um número aleatório e a hora do dia. Um identificador é atribuído a um conjunto de extensões (antes da distribuição), não a cada instância individual de uma implementação dessas extensões.

 

 
