---
description: A partir do Windows Vista, o SCM (gerenciador de controle de serviço) dá suporte a chamadas de procedimento remoto em protocolo RPC/TCP e pipes nomeados (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Serviços e RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d4ddfe95e114a972c600c9bef44864aa99fbe4ec412312d03e08fa7d7fe15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888553"
---
# <a name="services-and-rpctcp"></a>Serviços e RPC/TCP

A partir do Windows Vista, o SCM (gerenciador de controle de serviço) dá suporte a chamadas de procedimento remoto em protocolo RPC/TCP e pipes nomeados (RPC/NP). As funções SCM do lado do cliente usam RPC/TCP por padrão.

RPC/TCP é apropriado para a maioria dos aplicativos que usam funções SCM remotamente, como ferramentas de administração remota ou monitoramento. No entanto, para compatibilidade e desempenho, alguns aplicativos talvez precisem desabilitar o RPC/TCP definindo os valores do Registro descritos neste tópico.

Quando um serviço chama uma função SCM remota, o SCM do lado do cliente primeiro tenta usar RPC/TCP para se comunicar com o SCM do lado do servidor. Se o servidor estiver executando uma versão do Windows que dá suporte a RPC/TCP e permite o tráfego RPC/TCP, a conexão RPC/TCPP terá êxito. Se o servidor estiver executando uma versão do Windows que não dá suporte a RPC/TCP ou dá suporte a RPC/TCP, mas está operando atrás de um firewall que permite apenas o tráfego de pipe nomeado, a conexão RPC/TCP esgota e o SCM recupera a conexão com RPC/NP. Isso será bem-sucedido eventualmente, mas poderá levar algum tempo (normalmente mais de 20 segundos), fazendo com que a [**função OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) apareça bloqueada.

O TCP não carrega credenciais de usuário especificadas com um **comando net use.** Portanto, se RPC/TCP estiver  habilitado esc.exefor usado para tentar acessar o serviço especificado, o comando poderá falhar com o acesso negado. Desabilitar RPC/TCP no lado do cliente faz com que o comando **sc.exe** use um pipe nomeado que transporta credenciais de usuário, portanto, o comando terá êxito. Para obter informações sobre sc.exe, consulte [Controlando um serviço usando SC](controlling-a-service-using-sc.md).

> [!Note]  
> Um serviço não deve fornecer credenciais explícitas para um comando **net use,** porque essas credenciais podem ser compartilhadas inadvertidamente fora dos limites do serviço. Em vez disso, o serviço deve usar [a representação do cliente](/windows/desktop/SecAuthZ/client-impersonation) para representar o usuário.

 

### <a name="rpctcp-registry-values"></a>Valores do Registro RPC/TCP

O RPC/TCP é controlado pelos valores de registro **SCMApiConnectionParam**, **DisableRPCOverTCP** e **DisableRemoteScmEndpoints,** que estão todos na chave de controle CurrentControlSet do **sistema HKEY \_ LOCAL \_** \\  \\  \\  MACHINE. Todos esses valores têm um tipo de dados REG \_ DWORD. Os procedimentos a seguir mostram como usar esses valores do Registro para controlar o RPC/TCP.

O procedimento a seguir descreve como desabilitar o RPC/TCP no lado do cliente.

**Para desabilitar o RPC/TCP no lado do cliente**

1.  Combine o **valor do Registro SCMApiConnectionParam** com o valor de máscara 0x80000000.
2.  Reinicie o aplicativo que chama [**a função OpenSCManager.**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)

O procedimento a seguir descreve como desabilitar o TCP no lado do servidor.

**Para desabilitar o TCP no lado do servidor**

1.  De definir o valor do Registro **DisableRPCOverTCP** como 1.
2.  Reinicie o servidor.

O procedimento a seguir descreve como desabilitar RPC/TCP e RPC/NP no servidor (por exemplo, para reduzir a superfície de ataque).

**Para desabilitar RPC/TCP e RPC/NP no servidor**

1.  Defina **o valor do Registro DisableRemoteScmEndpoints** como 1.
2.  Reinicie o servidor.

O valor do registro **SCMApiConnectionParam** também pode ser usado para especificar o intervalo de tempo-máximo de RPC/TCP, em milissegundos. Por exemplo, um valor de 30.000 especifica um intervalo de tempo-tempo de 30 segundos. O padrão é 21.000 (21 segundos).

 

 
