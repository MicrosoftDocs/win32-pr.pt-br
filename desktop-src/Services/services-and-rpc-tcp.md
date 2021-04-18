---
description: A partir do Windows Vista, o SCM (Gerenciador de controle de serviços) dá suporte a chamadas de procedimento remotos em Protocolo RPC/TCP e pipes nomeados (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Serviços e RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fdb2ef3b21f280ba4e5078d302813de41a5a43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762891"
---
# <a name="services-and-rpctcp"></a>Serviços e RPC/TCP

A partir do Windows Vista, o SCM (Gerenciador de controle de serviços) dá suporte a chamadas de procedimento remotos em Protocolo RPC/TCP e pipes nomeados (RPC/NP). Por padrão, as funções SCM do lado do cliente usam RPC/TCP.

O RPC/TCP é apropriado para a maioria dos aplicativos que usam funções SCM remotamente, como ferramentas de administração ou monitoramento remoto. No entanto, para compatibilidade e desempenho, alguns aplicativos podem precisar desabilitar RPC/TCP definindo os valores de registro descritos neste tópico.

Quando um serviço chama uma função SCM remota, o SCM do lado do cliente tenta primeiro usar RPC/TCP para se comunicar com o SCM do lado do servidor. Se o servidor estiver executando uma versão do Windows que dá suporte a RPC/TCP e permitir o tráfego RPC/TCP, a conexão RPC/TCPP terá sucesso. Se o servidor estiver executando uma versão do Windows que não dá suporte a RPC/TCP, ou der suporte a RPC/TCP, mas estiver operando atrás de um firewall que permita apenas o tráfego de pipe nomeado, a conexão RPC/TCP atingirá o tempo limite e o SCM tentará novamente a conexão com RPC/NP. Isso terá sucesso eventualmente, mas pode levar algum tempo (normalmente mais de 20 segundos), fazendo com que a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) pareça bloqueada.

O TCP não carrega as credenciais de usuário especificadas com um comando **net use** . Portanto, se RPC/TCP estiver habilitado e **sc.exe** for usado para tentar acessar o serviço especificado, o comando poderá falhar com acesso negado. Desabilitar o RPC/TCP no lado do cliente faz com que o comando **sc.exe** use um pipe nomeado que transporta as credenciais do usuário, para que o comando seja bem sucedido. Para obter informações sobre sc.exe, consulte [controlando um serviço usando SC](controlling-a-service-using-sc.md).

> [!Note]  
> Um serviço não deve fornecer credenciais explícitas para um comando **net use** , pois essas credenciais podem ser compartilhadas inadvertidamente fora dos limites de serviço. Em vez disso, o serviço deve usar a [representação do cliente](/windows/desktop/SecAuthZ/client-impersonation) para representar o usuário.

 

### <a name="rpctcp-registry-values"></a>Valores do registro RPC/TCP

O RPC/TCP é controlado pelos valores de registro **SCMApiConnectionParam**, **DisableRPCOverTCP** e **DisableRemoteScmEndpoints** , que estão todos sob a chave de controle **HKEY \_ \_ local** \\ **System** \\ **CurrentControlSet** \\  . Todos esses valores têm um tipo de \_ dados reg DWORD. Os procedimentos a seguir mostram como usar esses valores de registro para controlar RPC/TCP.

O procedimento a seguir descreve como desabilitar o RPC/TCP no lado do cliente.

**Para desabilitar RPC/TCP no lado do cliente**

1.  Combine o valor do registro **SCMApiConnectionParam** com o valor de Mask 0x80000000.
2.  Reinicie o aplicativo que chama a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) .

O procedimento a seguir descreve como desabilitar o TCP no lado do servidor.

**Para desabilitar o TCP no lado do servidor**

1.  Defina o valor do registro **DisableRPCOverTCP** como 1.
2.  Reinicie o servidor.

O procedimento a seguir descreve como desabilitar RPC/TCP e RPC/NP no servidor (por exemplo, para reduzir a superfície de ataque).

**Para desabilitar RPC/TCP e RPC/NP no servidor**

1.  Defina o valor do registro **DisableRemoteScmEndpoints** como 1.
2.  Reinicie o servidor.

O valor do registro **SCMApiConnectionParam** também pode ser usado para especificar o intervalo de tempo limite de RPC/TCP, em milissegundos. Por exemplo, um valor de 30.000 especifica um intervalo de tempo limite de 30 segundos. O padrão é 21.000 (21 segundos).

 

 
