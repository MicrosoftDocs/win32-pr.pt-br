---
description: recursos de depuração e rastreamento e soquetes de Windows 2.
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Recursos de depuração e rastreamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0617aa8fc18e90b0c3e366a7ab14f1457cb26471865bfcc97682801a858565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741363"
---
# <a name="debug-and-trace-facilities"></a>Recursos de depuração e rastreamento

Windows Soquetes 2 os desenvolvedores de aplicativos precisam isolar bugs em:

-   O aplicativo.
-   O *Ws2 \_32.dll* ou uma das DLLs de Shim de compatibilidade.
-   O provedor de serviços.

Windows Os soquetes 2 atendem a essa necessidade por meio de vários componentes e recursos:

-   suporte integrado para rastreamento de Winsock no Windows Vista e posterior.
-   uma versão de depuração especialmente elaborada do *\_32.dllWs2* no Windows Vista.
-   um recurso de depuração e rastreamento primitivo separado para uso no Windows Server 2003 e no Windows XP.

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>Rastreamento de Winsock usando o rastreamento de eventos para Windows

o suporte integrado para rastreamento de Winsock usando o rastreamento de eventos para Windows (ETW) está incluído no Windows Vista e posterior. esse é o método preferencial para rastrear chamadas do Winsock no Windows Vista e versões posteriores. O rastreamento de Winsock usando o ETW é leve e funciona em versões comerciais do Windows. Nenhum software ou componente adicional é necessário. esse recurso só precisa ser habilitado no Windows Vista e posterior. Para obter informações mais detalhadas, consulte os tópicos de [rastreamento do Winsock](winsock-tracing.md) .

## <a name="using-a-debug-version-of-ws2_32dll"></a>Usando uma versão de depuração do ws2 \_32.dll

a combinação de uma versão de depuração do *\_32.dlldo Ws2* no Windows Vista e no rastreamento do Winsock permite que todas as chamadas de procedimento na API do Windows sockets 2 ou SPI sejam monitoradas e, em certa medida, controladas.

se uma versão do SDK (Software Development Kit) do Microsoft Windows para Windows Vista estiver instalada no local padrão, as versões de depuração do *\_32.dlldo Ws2* para várias arquiteturas estarão localizadas na seguinte pasta:

**C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ NoRedist**

uma versão verificada do *\_32.dllWs2* que corresponde à versão do Windows e do Service Pack que você está testando deve ser usada. Lembre-se de que os patches de segurança podem ter sido aplicados que atualizaram o *Ws2 \_32.dll* no sistema de teste. o SDK do Windows para Windows Vista e as assinaturas de DVD/CD anteriores do Software Development Kit (SDK) do Platform incluem compilações marcadas para as várias versões do Windows. Você deve usar a mesma versão verificada do *\_32.dllWs2* como a versão comercial que foi usada no sistema que está sendo testado. Observe também que o comportamento em execução em uma compilação verificada não será o mesmo que executar com uma compilação de varejo.

**Observação**  o SDK do Windows para Windows Server 2008 e posterior não inclui mais versões de depuração especiais do *\_32.dlldo Ws2*. Os desenvolvedores devem usar o rastreamento do Winsock usando o ETW, já que esse recurso não requer compilações de depuração.

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>recurso de depuração e rastreamento do Winsock no Windows Server 2003 e Windows XP

versões mais antigas do Windows antes de Windows 8 e Windows Server 2012 dão suporte a um recurso de depuração e rastreamento primitivo separado que é incluído como um exemplo com o SDK do Windows e o SDK da plataforma mais antigo. o recurso de depuração/rastreamento só deve ser usado no Windows Server 2003 e no Windows XP em que não há suporte para o rastreamento de Winsock.

se o SDK do Windows para Windows 7 for instalado no local padrão, esse recurso de rastreamento de Winsock primitivo será instalado na seguinte pasta:

**C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ NetDs \\ winsock \\ dt \_ dll**

O arquivo de *DbgSpec.doc* nesta pasta fornece documentação sobre esse recurso de rastreamento primitivo. O código de exemplo na \_ pasta DLL de DT precisa ser compilado para usar esse recurso. Os desenvolvedores são livres para usar o código-fonte para desenvolver versões da DLL de depuração/rastreamento que atendam às suas necessidades específicas.

Observe que esse recurso de rastreamento de Winsock primitivo funcionará apenas com a versão de depuração do *Ws2 \_32.dll* instalada. portanto, você precisará obter uma versão verificada do *\_32.dllWs2* que corresponde à versão do Windows e do Service Pack em que você está testando.

Uma limitação desse recurso de rastreamento de DLL do DT primitivo \_ é que o código de exemplo usa um bloqueio global (seção crítica) para cada chamada de função do Winsock. Portanto, esse recurso não é útil para lidar com condições de corrida. O código de exemplo precisaria ser consideravelmente reescrito para tornar esse recurso de rastreamento útil para lidar com os problemas de Winsock mais reais (substituindo os bloqueios globais). Este código de exemplo permite que os desenvolvedores rastreiem as chamadas de procedimento, os procedimentos retornados, os valores de parâmetro e os valores de retorno.

Os desenvolvedores podem usar esse mecanismo primitivo para rastrear chamadas de procedimento, retornos de procedimento, valores de parâmetro e valores de retorno. Valores de parâmetro e valores de retorno podem ser alterados em retorno de procedimento ou chamada de procedimento. Se desejado, uma chamada de procedimento pode ser impedida ou redirecionada. Com acesso a esse nível de informações e controle, um desenvolvedor é capaz de isolar melhor um problema no aplicativo, *Ws2 \_32.dll* ou provedor de serviços.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> </dl>

 

 



