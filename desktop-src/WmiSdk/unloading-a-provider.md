---
description: Depois que o WMI for concluído com um provedor, ele descarregará o provedor da memória.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Descarregando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b831f69ba27ab3e173920cc57e7500ef543bb327a04dc5c04dc8b0b9cef31ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049954"
---
# <a name="unloading-a-provider"></a>Descarregando um provedor

Depois que o WMI for concluído com um provedor, ele descarregará o provedor da memória. O principal motivo pelo qual o WMI descarrega um provedor é conservar recursos do sistema. Portanto, você deve adicionar código que permita que o WMI descarregue seu provedor de maneira eficiente. Ele leva em qualquer lugar do intervalo especificado no controle de cache para duas vezes esse intervalo para que o WMI descarregue um provedor.

O WMI descarrega um provedor de uma das seguintes maneiras:

-   Descarregue um provedor depois que o provedor concluir as tarefas fornecidas a ele.
-   Descarregue rapidamente todos os provedores quando o usuário desligar o sistema. Observe que o WMI descarrega provedores em processo quando o serviço WMI é desligado da linha de comando.

Embora o primeiro cenário seja mais comum, você deve escrever seu provedor para ambas as possibilidades.

As seções a seguir são discutidas neste tópico:

-   [Descarregando um provedor ocioso](#unloading-an-idle-provider)
-   [Acessando o tempo ocioso para um provedor](#accessing-the-idle-time-for-a-provider)
-   [Descarregando um provedor que também é um cliente WMI](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Descarregando um provedor durante o desligamento](#unloading-a-provider-during-shutdown)
-   [Tópicos relacionados](#related-topics)

## <a name="unloading-an-idle-provider"></a>Descarregando um provedor ocioso

O WMI executa as seguintes ações quando descarrega um provedor ocioso:

-   Determina se o provedor está ocioso.

    O WMI usa a **propriedade ClearAfter** para determinar por quanto tempo um provedor pode permanecer ocioso antes de descarregar esse provedor. Para obter mais informações, [consulte Acessando o tempo ocioso para um provedor](#accessing-the-idle-time-for-a-provider).

-   Chama o [**método Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) do provedor.

    Se o provedor era um provedor puro, [**a versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) remove completamente o provedor da memória ativa. No entanto, um provedor não depuração pode continuar a ser executado depois que o WMI chama **Release**.

## <a name="accessing-the-idle-time-for-a-provider"></a>Acessando o tempo ocioso para um provedor

A quantidade mínima de tempo que um provedor permanece ativo é determinada pela **propriedade ClearAfter.** Você pode encontrar **ClearAfter** em instâncias de classes derivadas da classe de sistema WMI [**\_ \_ CacheControl**](--cachecontrol.md) no \\ namespace raiz.

A lista a seguir descreve as classes derivadas de [**\_ \_ CacheControl,**](--cachecontrol.md)que controla o descarregamento do provedor:

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

Você pode alterar a quantidade mínima de tempo que o WMI permite que um provedor permaneça inativo editando a propriedade **ClearAfter** na instância de controle de cache para um tipo específico de provedor. Por exemplo, para limitar a quantidade de tempo que um provedor de propriedades pode permanecer ocioso, você editaria a propriedade **ClearAfter** de uma instância [**\_ \_ PropertyProviderCacheControl**](--propertyprovidercachecontrol.md) no \\ namespace raiz.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Descarregando um provedor que também é um cliente WMI

Seu provedor pode precisar permanecer um cliente do WMI depois de concluir as funções de provedor que ele foi chamado para executar. Por exemplo, um provedor de push pode precisar emitir consultas para o WMI. Para obter mais informações, consulte [Determinando o status de push ou pull.](determining-push-or-pull-status.md) Nesse caso, a **propriedade Pure** da instância [**\_ \_ win32Provider**](--win32provider.md) que representa o provedor deve ser definida como **TRUE.** Se a **propriedade Pure** estiver definida como **FALSE**, o provedor se preparará para descarregar chamando [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os pontos de interface pendentes quando o WMI chamar o método Release de sua interface primária. Para obter mais informações, consulte a seção Comentários [**\_ \_ em Win32Provider**](--win32provider.md).

O procedimento a seguir descreve como implementar um método de versão para a interface primária do seu provedor.

**Para descarregar um provedor**

1.  Libere todos os ponteiros de interface mantidos no WMI quando o WMI chamar o [**método Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) da interface primária do provedor.

    Normalmente, um provedor mantém ponteiros para as interfaces [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) fornecidas em [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize).

2.  Se a **propriedade Pure** na instância [**\_ \_ win32Provider**](--win32provider.md) associada estiver definida como **FALSE**, o provedor poderá fazer a transição para a função de aplicativo cliente depois que o WMI chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). No entanto, o WMI não pode descarregar um provedor que está operando como um sistema cliente, o que aumenta a sobrecarga do sistema.

    Um provedor com **Pure** definido como **TRUE** existe somente para solicitações de serviço. Portanto, esse tipo de provedor não pode assumir a função de um aplicativo cliente e o WMI pode descarregá-lo.

## <a name="unloading-a-provider-during-shutdown"></a>Descarregando um provedor durante o desligamento

Em circunstâncias normais, o uso das diretrizes em Descarregando um provedor que também é um cliente WMI permite que [o WMI](#unloading-a-provider-that-is-also-a-wmi-client) descarregue seu provedor corretamente. No entanto, você pode encontrar situações em que o WMI não consegue desafocar os procedimentos de descarregamento normais, como quando o usuário opta por desligar o sistema. Usando um modelo de transação de armazenamento de dados, além de implementar uma boa estratégia de limpeza, você pode garantir que seu provedor seja descarregado corretamente.

O usuário pode parar o WMI a qualquer momento. Nessa situação, o WMI não descarrega nenhum provedor nem chama o ponto de entrada [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) em nenhum provedor em processo. Além disso, se um provedor em processo estiver no meio de uma chamada de método no momento do desligamento, o WMI poderá possivelmente encerrar o thread em execução no meio da chamada. Nessa circunstância, o WMI não chama rotinas que normalmente lidam com a limpeza, como um destruidor de objeto. No máximo, o WMI chamará [**apenas DllMain.**](/windows/desktop/Dlls/dllmain)

Quando o sistema operacional desliga o WMI, o sistema libera automaticamente toda a memória alocada para um provedor em processo. O sistema operacional também fecha a maioria dos recursos mantidos pelo provedor, como alças de arquivo, alças de janela e assim por diante. O provedor não precisa tomar nenhuma ação específica para fazer isso acontecer.

Como o WMI pode ser desligado no meio de uma chamada, um provedor não deve deixar fontes de dados em um estado inconsistente. Deixar seus dados em um estado inconsistente não é um problema para provedores somente leitura. No entanto, os provedores com funcionalidades de gravação podem querer implementar algum tipo de modelo de transação para permitir uma replicação segura após um encerramento repentino.

Embora o sistema operacional possa liberar alguns recursos gerais do sistema, o sistema não libera automaticamente todos os recursos. Por exemplo, o sistema operacional pode não liberar um soquete ou uma conexão de banco de dados. Em vez disso, o provedor pode precisar limpar esses recursos manualmente. Para evitar esses problemas, você pode implementar seu provedor fora do processo ou adicionar código de limpeza.

A solução mais simples é implementar seu provedor fora do processo. Um provedor fora do processo não é encerrado quando o WMI é desligado, embora o WMI libere o provedor após um tempo de tempo de COM. Provedores para os quais problemas de robustez de limpeza e encerramento são mais importantes do que o desempenho pode estar fora do processo.

Se você tiver que colocar o código de limpeza em seu provedor, terá duas opções. Um local para executar esse tipo de limpeza é [**DllMain**](/windows/desktop/Dlls/dllmain), a função de ponto de entrada DLL que o sistema operacional chama ao descarregar a DLL. O código de limpeza pode ser adicionado diretamente **ao DllMain**, executando-o em resposta ao **PROCESSO de DLL \_ \_ DETACH.** Implementar o código de limpeza **em DllMain** pode ser um pouco difícil de organizar, especialmente em ambientes de programação, como MFC ou ATL. Para obter mais informações, consulte o Base de Dados de Conhecimento Microsoft artigo Q148791, " How *to Provide Your Own DllMain in an MFC Regular DLL.*" (Esse recurso pode não estar disponível em alguns idiomas e países ou regiões.)

Como alternativa, você também pode colocar o código de limpeza no destruidor de uma classe global. Para obter mais informações, consulte Descarregando um provedor. O Windows sistema operacional não aloca objetos globais no heap. Em vez disso, o sistema operacional chama os destruidores durante o descarregamento de DLL.

A seguir está um procedimento de limpeza simples que pode caber dentro de um objeto global para WMI.


```C++
class CMyCleanup
{
    ~CMyCleanup()
    {
        CloseHandle(m_hOpenFile);
        CloseDatabaseConnection(g_hDatabase);
    }
} g_Cleanup;
```



Há muitas restrições sobre o que pode ser feito no código de limpeza com qualquer abordagem. Por exemplo, nem threads nem DLLs que não estão vinculadas implicitamente podem ser acessados de qualquer maneira. Além disso, você não pode fazer chamadas COM em nenhuma circunstância.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo Descritores de Segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Proteger seu provedor](securing-your-provider.md)
</dt> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 
