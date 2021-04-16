---
description: Depois que o WMI é concluído com um provedor, ele descarrega o provedor da memória.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Descarregando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123d8c4f6b9d9155cdc22dc435635466956bdb0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505665"
---
# <a name="unloading-a-provider"></a>Descarregando um provedor

Depois que o WMI é concluído com um provedor, ele descarrega o provedor da memória. O principal motivo pelo qual o WMI descarrega um provedor é conservar os recursos do sistema. Portanto, você deve adicionar código que permita que o WMI descarregue seu provedor de maneira eficiente. Ele leva em qualquer lugar do intervalo especificado no controle de cache para duas vezes esse intervalo para que o WMI descarregue um provedor.

O WMI descarrega um provedor de uma das seguintes maneiras:

-   Descarregar um provedor depois que o provedor concluir as tarefas fornecidas a ele.
-   Descarregar rapidamente todos os provedores quando o usuário desligar o sistema. Observe que o WMI descarrega provedores em processo quando o serviço WMI é desligado da linha de comando.

Embora o primeiro cenário seja mais comum, você deve escrever seu provedor para ambas as possibilidades.

As seções a seguir são discutidas neste tópico:

-   [Descarregando um provedor ocioso](#unloading-an-idle-provider)
-   [Acessando o tempo ocioso de um provedor](#accessing-the-idle-time-for-a-provider)
-   [Descarregando um provedor que também é um cliente WMI](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Descarregando um provedor durante o desligamento](#unloading-a-provider-during-shutdown)
-   [Tópicos relacionados](#related-topics)

## <a name="unloading-an-idle-provider"></a>Descarregando um provedor ocioso

O WMI executa as seguintes ações quando descarrega um provedor ocioso:

-   Determina se o provedor está ocioso.

    O WMI usa a propriedade **ClearAfter** para determinar por quanto tempo um provedor pode permanecer ocioso antes de descarregar esse provedor. Para obter mais informações, consulte [acessando o tempo ocioso de um provedor](#accessing-the-idle-time-for-a-provider).

-   Chama o método [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) do provedor.

    Se o provedor era um provedor puro, o [**lançamento**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) remove completamente o provedor da memória ativa. No entanto, um provedor não puro pode continuar a ser executado após a **liberação** de chamadas do WMI.

## <a name="accessing-the-idle-time-for-a-provider"></a>Acessando o tempo ocioso de um provedor

A quantidade mínima de tempo que um provedor permanece ativo é determinada pela propriedade **ClearAfter** . Você pode encontrar **ClearAfter** em instâncias de classes derivadas do [**\_ \_ CacheControl**](--cachecontrol.md) da classe do sistema WMI no \\ namespace raiz.

A lista a seguir descreve as classes que são derivadas de [**\_ \_ CacheControl**](--cachecontrol.md), que controla o descarregamento do provedor:

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

Você pode alterar a quantidade mínima de tempo que o WMI permite que um provedor permaneça inativo editando a propriedade **ClearAfter** na instância de controle de cache para um tipo específico de provedor. Por exemplo, para limitar a quantidade de tempo que um provedor de propriedade pode permanecer ocioso, edite a propriedade **ClearAfter** de uma instância [**\_ \_ PropertyProviderCacheControl**](--propertyprovidercachecontrol.md) no \\ namespace raiz.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Descarregando um provedor que também é um cliente WMI

Seu provedor pode precisar permanecer um cliente do WMI depois de concluir as funções de provedor que ele foi chamado para executar. Por exemplo, um provedor de push pode precisar emitir consultas para o WMI. Para obter mais informações, consulte [determinando o status de Push ou pull](determining-push-or-pull-status.md). Nesse caso, a propriedade **pura** da instância [**\_ \_ Win32Provider**](--win32provider.md) que representa o provedor deve ser definida como **true**. Se a propriedade **pura** for definida como **false**, o provedor se prepara para descarregar chamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os pontos de interface pendentes quando o WMI chama o método Release de sua interface primária. Para obter mais informações, consulte a seção comentários em [**\_ \_ Win32Provider**](--win32provider.md).

O procedimento a seguir descreve como implementar um método de liberação para a interface primária do seu provedor.

**Para descarregar um provedor**

1.  Libere todos os ponteiros de interface mantidos no WMI quando o WMI chama o método [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) da interface primária do seu provedor.

    Normalmente, um provedor contém ponteiros para as interfaces [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) fornecidas em [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize).

2.  Se a propriedade **pura** na instância do [**\_ \_ Win32Provider**](--win32provider.md) associada for definida como **false**, o provedor poderá fazer a transição para a função do aplicativo cliente após a [**liberação**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)de chamadas WMI. No entanto, o WMI não pode descarregar um provedor que esteja operando como um sistema cliente, o que aumenta a sobrecarga do sistema.

    Um provedor com **puro** definido como **true** existe somente para solicitações de serviço. Portanto, esse tipo de provedor não pode assumir a função de um aplicativo cliente e o WMI pode descarregá-lo.

## <a name="unloading-a-provider-during-shutdown"></a>Descarregando um provedor durante o desligamento

Em circunstâncias normais, o uso das diretrizes no [descarregamento de um provedor que também é um cliente WMI](#unloading-a-provider-that-is-also-a-wmi-client) permite que o WMI descarregue seu provedor corretamente. No entanto, você pode se deparar com situações em que o WMI não consegue instigar os procedimentos normais de descarregamento, como quando o usuário opta por desligar o sistema. Usando um modelo de transação de armazenamento de dados, além de implementar uma boa estratégia de limpeza, você pode garantir que seu provedor seja descarregado corretamente.

O usuário pode parar o WMI a qualquer momento. Nessa situação, o WMI não descarrega nenhum provedor ou chama o ponto de entrada do [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) em qualquer fornecedor em processo. Além disso, se um provedor em processo estiver no meio de uma chamada de método no momento do desligamento, o WMI poderá encerrar o thread em execução no meio da chamada. Nessa circunstância, o WMI não chama rotinas que normalmente lidam com a limpeza, como um destruidor de objeto. No máximo, o WMI chamará somente [**DllMain**](/windows/desktop/Dlls/dllmain) .

Quando o sistema operacional desliga o WMI, o sistema libera automaticamente toda a memória alocada para um provedor em processo. O sistema operacional também fecha a maioria dos recursos mantidos pelo provedor, como identificadores de arquivos, identificadores de janela e assim por diante. O provedor não precisa executar nenhuma ação específica para fazer isso acontecer.

Como o WMI pode ser desligado no meio de uma chamada, um provedor não deve deixar as fontes de dados em um estado inconsistente. Deixar seus dados em um estado inconsistente não é um problema para provedores somente leitura. No entanto, os provedores com recursos de gravação podem querer implementar algum tipo de modelo de transação para permitir uma reversão segura após um encerramento abrupta.

Embora o sistema operacional possa liberar alguns recursos gerais do sistema, o sistema não libera automaticamente todos os recursos. Por exemplo, o sistema operacional pode não liberar um soquete ou uma conexão de banco de dados. Em vez disso, o provedor pode precisar limpar manualmente esses recursos. Para evitar esses problemas, você pode implementar seu provedor fora do processo ou pode adicionar o código de limpeza.

A solução mais simples é implementar seu provedor fora do processo. Um provedor fora do processo não é eliminado quando o WMI é desligado, embora o WMI libere o provedor após um tempo limite de COM. Provedores para os quais os problemas de robustez de limpeza e término são mais importantes do que o desempenho pode estar fora do processo.

Se for necessário posicionar o código de limpeza em seu provedor, você terá duas opções. Um lugar para executar esse tipo de limpeza é [**DllMain**](/windows/desktop/Dlls/dllmain), a função do ponto de entrada de dll que o sistema operacional chama ao descarregar a dll. O código de limpeza pode ser adicionado diretamente ao **DllMain**, executando-o em resposta à **\_ \_ desanexação do processo de dll**. A implementação do código de limpeza no **DllMain** pode ser um pouco difícil de organizar, especialmente em ambientes de programação como MFC ou ATL. Para obter mais informações, consulte o artigo Q148791 da base de dados de conhecimento Microsoft, "*como fornecer seu próprio DllMain em uma DLL regular do MFC".* (Esse recurso pode não estar disponível em alguns idiomas e países ou regiões.)

Como alternativa, você também pode posicionar o código de limpeza no destruidor de uma classe global. Para obter mais informações, consulte Descarregando um provedor. O sistema operacional Windows não aloca objetos globais no heap. Em vez disso, o sistema operacional chama os destruidores durante o descarregamento da DLL.

Veja a seguir um procedimento de limpeza simples que pode ser ajustado dentro de um objeto global para WMI.


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



Há muitas restrições quanto ao que pode ser feito no código de limpeza com qualquer uma das abordagens. Por exemplo, nem threads nem quaisquer DLLs que não estejam vinculadas implicitamente podem ser acessados de qualquer forma. Além disso, você não pode fazer chamadas COM em nenhuma circunstância.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protegendo seu provedor](securing-your-provider.md)
</dt> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 
