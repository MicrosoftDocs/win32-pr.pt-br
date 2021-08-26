---
description: usando o modelo de classe DMO
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: usando o modelo de classe DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205ee51953aff35ef5b05790b45fcd0bdf3bcd753239a521e40ca796c21b0a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130896"
---
# <a name="using-the-dmo-class-template"></a>usando o modelo de classe DMO

DirectShow inclui um modelo de classe, [**IMediaObjectImpl**](imediaobjectimpl-class-template.md), para implementar DMOs. O modelo lida com muitas das tarefas "de escrituração", como a validação de parâmetros de entrada. Usando o modelo, você pode se concentrar na funcionalidade que é específica para seu DMO. Além disso, o modelo ajuda a garantir que você crie uma implementação robusta. O modelo é definido no arquivo de cabeçalho Dmoimpl. h, localizado no diretório de inclusão do SDK.

O modelo **IMediaObjectImpl** herda a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . para criar um DMO usando o modelo, defina uma nova classe que derive de **IMediaObjectImpl**. O modelo implementa todos os métodos **IMediaObject** . Na maioria dos casos, o modelo chama um método particular correspondente na classe derivada. O modelo fornece os seguintes recursos:

-   Verificação de parâmetro básica. Os métodos de modelo verificam se os parâmetros obrigatórios não são **nulos**, se os índices de fluxo estão dentro do intervalo e se os sinalizadores são válidos.
-   Bloqueio. Os métodos de modelo chamam dois métodos internos, **Lock** e **Unlock**, para serializar operações no DMO. esse recurso garante que o DMO seja thread-safe.
-   Tipos de mídia. O modelo armazena os tipos de mídia definidos pelo cliente e fornece métodos de acessador para os tipos de mídia.
-   Transmiti. O modelo impede o streaming até que o cliente defina os tipos de mídia para todos os fluxos não opcionais. Ele também garante que o método [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) seja chamado antes do início do streaming, o que garante que os recursos sejam alocados.

A classe derivada deve implementar a interface **IUnknown** ; o modelo não fornece essa interface. Você pode usar o Active Template Library (ATL) para implementar **IUnknown** ou pode fornecer alguma outra implementação. O modelo também não implementa o mecanismo de bloqueio. A classe derivada deve implementar os métodos **Lock** e **Unlock** . Se você criar sua classe usando ATL, poderá usar as implementações padrão da ATL.

**Declarando a classe derivada**

O modelo de classe **IMediaObjectImpl** é declarado da seguinte maneira:


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



Os três parâmetros de modelo são \_ derivados \_ , NUMBEROFINPUTS e NUMBEROFOUTPUTS. Defina \_ derivado \_ igual ao nome da sua classe. Os outros dois parâmetros definem o número de fluxos de entrada e fluxos de saída no DMO. por exemplo, para criar uma classe de DMO chamada CMyDmo que dá suporte a um fluxo de entrada e dois fluxos de saída, use a seguinte declaração:


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



O restante desta seção descreve como o modelo implementa os vários métodos no **IMediaObject**.

**Métodos para definir tipos de mídia**

Os métodos a seguir definem ou recuperam os tipos de mídia no DMO:

-   **Getparâmetrosdeentrada**, **GetOutputType**. Esses métodos retornam tipos de mídia preferenciais, por número de fluxo e índice de tipo. O modelo chama **InternalGetInputType** ou **InternalGetOutputType** na classe derivada.
-   **Setparâmetrosdeentrada**, **SetOutputType**. Esses métodos definem o tipo de mídia em um fluxo, testam um tipo de mídia ou desmarcam um tipo de mídia. Para validar o tipo de mídia, o modelo chama **InternalCheckInputType** ou **InternalCheckOutputType** na classe derivada. a classe derivada retorna S \_ OK para aceitar o tipo ou DMO \_ E \_ invalidatype para rejeitar o tipo. O modelo manipula a configuração ou a limpeza do tipo de mídia.
-   **GetInputCurrentType**, **GetOutputCurrentType**. esses métodos retornam o tipo de mídia atual para um fluxo, ou DMO \_ \_ tipo E \_ não \_ são definidos se nenhum tipo é definido. O modelo implementa completamente esses métodos.

**Métodos informativos**

Os métodos a seguir fornecem informações sobre o DMO.

-   **GetInputMaxLatency**, **SetInputMaxLatency**. Esses métodos recuperam ou definem a latência máxima. O modelo chama **InternalGetInputMaxLatency** ou **InternalSetInputMaxLatency** na classe derivada.
-   **GetInputSizeInfo**, **GetOutputSizeInfo**. esses métodos retornam os requisitos de buffer do DMO para um fluxo especificado. se nenhum tipo de mídia tiver sido definido nesse fluxo, o modelo retornará DMO \_ E \_ tipo \_ não \_ definido. Caso contrário, ele chama **InternalGetInputSizeInfo** ou **InternalGetOutputSizeInfo** na classe derivada.
-   **GetInputStreamInfo**, **GetOutputStreamInfo**. Esses métodos retornam vários sinalizadores que indicam como o cliente deve formatar os dados. O modelo chama **InternalGetInputStreamInfo** ou **InternalGetOutputStreamInfo** na classe derivada.
-   **GetStreamCount**. Esse método retorna o número de fluxos de entrada e saída. O modelo implementa esse método, usando os parâmetros de modelo.

**Métodos para alocação de recursos**

-   o método **AllocateStreamingResources** aloca todos os recursos que o DMO precisa antes que o streaming comece. O método **FreeStreamingResources** libera os mesmos recursos. O modelo chama **InternalAllocateStreamingResources** e **InternalFreeStreamingResources**, respectivamente.

o cliente do DMO não é necessário para chamar esses métodos, mas o modelo chama **AllocateStreamingResources** automaticamente antes de iniciar o streaming. portanto, o DMO pode assumir que os recursos foram alocados corretamente pela hora em que o **ProcessInput** é chamado. o DMO deve chamar **FreeStreamingResources** em seu destruidor.

Além disso, quando o modelo chama **InternalAllocateStreamingResources**, ele define um sinalizador interno, para que ele não chame esse método novamente até chamar **InternalFreeStreamingResources**. Isso garante que os recursos não sejam novamente alocados acidentalmente, o que pode causar vazamentos de memória.

**Métodos para streaming**

Os métodos a seguir são usados para transmitir dados:

-   **GetInputStatus**. esse método indica se o DMO pode aceitar entrada no momento. O modelo chama **InternalAcceptingInput** na classe derivada. se o DMO puder aceitar a entrada, a classe derivada retornará S \_ OK e o modelo definirá o DMO \_ entrada \_ STATUSF \_ aceitar \_ bit de dados no parâmetro *dwFlags* . Caso contrário, a classe derivada retornará S \_ false e o modelo definirá *dwFlags* como zero.
-   **ProcessInput**. Esse método processa um buffer de entrada. O modelo chama **AllocateStreamingResources**, descrito anteriormente. Em seguida, ele chama **InternalAcceptingInput** na classe derivada. se o DMO puder aceitar nova entrada, o modelo chamará **InternalProcessInput**.
-   **ProcessOutput**. Esse método processa um conjunto de buffers de saída, um buffer para cada fluxo de saída. O modelo chama **AllocateStreamingResources** e, em seguida, **InternalProcessOutput**.
-   **Descontinuidade**. Esse método sinaliza uma descontinuidade em um fluxo de entrada. O modelo chama **InternalAcceptingInput** na classe derivada. Se esse método retornar S \_ OK, o modelo chamará **InternalDiscontinuity** na classe derivada.
-   **Liberar**. Esse método libera o DMO. O modelo chama **InternalFlush** na classe derivada. o DMO deve descartar os buffers de entrada que ele ainda mantém para ser processado.

O modelo não fornece nenhum suporte direto para a interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .

**Métodos para bloqueio**

o bloqueio é usado para proteger o estado do DMO em um ambiente multi-threaded. Em um projeto ATL, o método [**IMediaObject:: Lock**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) causa um conflito de nome com o método de **bloqueio** ATL. Para resolver o conflito, o modelo renomeia o método **IMediaObject** para **DMOLock**. Ao compilar a classe derivada, defina corrigir \_ nome do bloqueio \_ antes de incluir o arquivo de cabeçalho DMO. h:


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



Essa diretiva faz com que o pré-processador substitua **DMOLock** por **bloqueio** na declaração da interface **IMediaObject** . Os aplicativos ainda podem invocar o método usando o nome **Lock**, pois a ordem vtable não é alterada. O método **DMOLock** chama **Lock** ou **Unlock** na classe derivada. Se você estiver usando a ATL para implementar a classe derivada, esses métodos já serão definidos pela ATL, portanto, nenhum código adicional será necessário. Se você não estiver usando a ATL, deverá fornecer os métodos **Lock** e **Unlock** em sua classe derivada.

o modelo bloqueia automaticamente o DMO em cada um dos métodos **IMediaObject** . a classe derivada pode precisar bloquear o DMO dentro de outros métodos públicos que ele implementa (por exemplo, se ele dá suporte a **IMediaObjectInPlace**). O modelo de classe também fornece uma classe auxiliar interna, [**IMediaObjectImpl:: Lockit**](imediaobjectimpl-lockit.md), que é útil para bloquear e desbloquear o DMO.

**Resumo**

Para os seguintes métodos **IMediaObject** , o modelo chama um método correspondente com a mesma assinatura na classe derivada. A classe derivada deve implementar cada um dos métodos mostrados na segunda coluna.



| Método IMediaObject            | Método de classe derivada                   |
|--------------------------------|----------------------------------------|
| **AllocateStreamingResources** | **InternalAllocateStreamingResources** |
| **Descontinuidade**              | **InternalDiscontinuity**              |
| **Liberar**                      | **InternalFlush**                      |
| **FreeStreamingResources**     | **InternalFreeStreamingResources**     |
| **GetInputMaxLatency**         | **InternalGetInputMaxLatency**         |
| **GetInputSizeInfo**           | **InternalGetInputSizeInfo**           |
| **GetInputStreamInfo**         | **InternalGetInputStreamInfo**         |
| **GetInputType**               | **InternalGetInputType**               |
| **GetOutputSizeInfo**          | **InternalGetOutputSizeInfo**          |
| **GetOutputStreamInfo**        | **InternalGetOutputStreamInfo**        |
| **GetOutputType**              | **InternalGetOutputType**              |
| **ProcessInput**               | **InternalProcessInput**               |
| **ProcessOutput**              | **InternalProcessOutput**              |
| **SetInputMaxLatency**         | **InternalSetInputMaxLatency**         |



 

Para os demais métodos **IMediaObject** , não há uma correspondência um-para-um entre métodos de modelo e métodos de classe derivada. A tabela a seguir resume quais métodos são totalmente implementados pelo modelo e quais métodos chamam outros métodos na classe derivada.



| Método IMediaObject                   | Método de classe derivada                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **GetInputCurrentType**               | Totalmente implementado                                                                |
| **GetOutputCurrentType**              | Totalmente implementado                                                                |
| **GetStreamCount**                    | Totalmente implementado                                                                |
| **GetInputStatus**                    | [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))        |
| **Bloqueio** (implementado como **DMOLock**) | [**Bloquear**](/previous-versions/ms809100(v=msdn.10)), [ **desbloquear**](/previous-versions/ms809101(v=msdn.10)) |
| **SetInputType**                      | [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))        |
| **Setoutputtypetype**                     | [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modelo de classe IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> <dt>

[Escrevendo um DMO](writing-a-dmo.md)
</dt> </dl>

 

 
