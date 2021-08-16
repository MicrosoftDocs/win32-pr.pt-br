---
title: Aplicativos Direct2D com multithread
description: Descreve as práticas recomendadas para criar aplicativos Direct2D multithread.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5710435f263e7b0f735581e03416f1d01733711429ad95b3ed25e473aca6d936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636380"
---
# <a name="multithreaded-direct2d-apps"></a>Aplicativos Direct2D com multithread

Se você desenvolver [Direct2D](./direct2d-portal.md) aplicativos, talvez seja necessário acessar Direct2D recursos de mais de um thread. Em outros casos, talvez você queira usar multi-threading para obter melhor desempenho ou melhor capacidade de resposta (como usar um thread para exibição de tela e um thread separado para renderização offline).

Este tópico descreve as práticas recomendadas para o desenvolvimento de aplicativos Direct2D multithread [com](./direct2d-portal.md) pouca ou nenhuma [renderização Direct3D.](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) Defeitos de software causados por problemas de simultança podem ser difíceis de rastrear e é útil planejar sua política de multithreading e seguir as melhores práticas descritas aqui.

> [!Note]  
> Se você acessar dois [recursos Direct2D](./direct2d-portal.md) criados de duas fábricas de Direct2D thread único diferentes, isso não causará conflitos de acesso, desde que os contextos de dispositivos e dispositivos [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) subjacentes também sejam distintos. Ao falar sobre "acessar Direct2D recursos" neste artigo, isso realmente significa "acessar Direct2D recursos criados do mesmo dispositivo Direct2D" a menos que indicado o contrário.

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Desenvolvendo Thread-Safe aplicativos que chamam somente apIs Direct2D

Você pode criar uma [](./direct2d-portal.md) instância de fábrica Direct2D multithreaded. Você pode usar e compartilhar uma fábrica multithreaded e todos os seus recursos de mais de um thread, mas os acessos a esses recursos (por meio de chamadas Direct2D) são serializados por Direct2D, portanto, nenhum conflito de acesso ocorre. Se o aplicativo chamar somente Direct2D APIs, essa proteção será feita automaticamente Direct2D em um nível granular com sobrecarga mínima. O código para criar uma fábrica multithread aqui.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

A imagem aqui mostra como [Direct2D](./direct2d-portal.md) serializa dois threads que fazem chamadas usando apenas a API Direct2D dados.

![diagrama de dois threads serializados.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Desenvolvendo Thread-Safe Direct2D aplicativos com chamadas mínimas do Direct3D ou DXGI

É mais do que frequentemente que um [Direct2D](./direct2d-portal.md) aplicativo também faz algumas [chamadas Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou DXGI. Por exemplo, um thread de exibição será desenhar em Direct2D, em seguida, apresentar usando uma [**cadeia de permuta DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

Nesse caso, garantir a segurança de thread [](./direct2d-portal.md) é mais complicado: algumas chamadas Direct2D acessam indiretamente os recursos subjacentes do [Direct3D,](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) que podem ser acessados simultaneamente por outro thread que chama Direct3D ou DXGI. Como essas chamadas Direct3D ou DXGI estão fora do controle e do reconhecimento do Direct2D, você precisa criar uma fábrica de Direct2D multithread, mas deve fazer mais para evitar conflitos de acesso.

O diagrama aqui mostra um conflito de acesso a recursos [direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) devido ao thread T0 acessar um recurso [indiretamente](./direct2d-portal.md) por meio de uma chamada Direct2D e T2 acessar o mesmo recurso diretamente por meio de uma chamada Direct3D ou DXGI.

> [!Note]  
> A proteção de [thread Direct2D](./direct2d-portal.md) fornece (o bloqueio azul nesta imagem) não ajuda nesse caso.

 

![diagrama de proteção de thread.](images/multi-thread2.png)

Para evitar conflitos de acesso a recursos aqui, recomendamos que você adquira explicitamente o bloqueio que o [Direct2D](./direct2d-portal.md) usa para sincronização de acesso interno e aplique esse bloqueio quando um thread precisar fazer chamadas [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou DXGI que possam causar conflito de acesso, conforme mostrado aqui. Em particular, você deve tomar cuidado especial com o código que usa exceções ou um sistema inicial com base em códigos de retorno HRESULT. Por esse motivo, recomendamos que você use um padrão DEIS (Resource Acquisition Is Initialization) para chamar os [**métodos Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave)

> [!Note]  
> É importante que você emparelhe chamadas para os [**métodos Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) caso contrário, seu aplicativo poderá fazer deadlock.

 

O código aqui mostra um exemplo de quando bloquear e, em seguida, e desbloquear em torno [de chamadas Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou DXGI.


```C++
void MyApp::DrawFromThread2()
{
    // We are accessing Direct3D resources directly without Direct2D's knowledge, so we
    // must manually acquire and apply the Direct2D factory lock.
    ID2D1Multithread* m_D2DMultithread;
    m_D2DFactory->QueryInterface(IID_PPV_ARGS(&m_D2DMultithread));
    m_D2DMultithread->Enter();
    
    // Now it is safe to make Direct3D/DXGI calls, such as IDXGISwapChain::Present
    MakeDirect3DCalls();

    // It is absolutely critical that the factory lock be released upon
    // exiting this function, or else any consequent Direct2D calls will be blocked.
    m_D2DMultithread->Leave();
}
```



> [!Note]  
> Algumas [chamadas Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou DXGI (notavelmente [**IDXGISwapChain::P resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)) podem adquirir bloqueios e/ou disparar retornos de chamada no código da função ou método de chamada. Você deve estar ciente disso e garantir que esse comportamento não cause deadlocks. Para obter mais informações, consulte o [tópico Visão geral do DXGI.](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)

 

![Diagrama de bloqueio de thread direct2d e direct3d.](images/multi-thread3.png)

Quando você usa os métodos [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) as [](./direct2d-portal.md) chamadas são protegidas pelo Direct2D automático e pelo bloqueio explícito, para que o aplicativo não entre em conflito de acesso.

Há outras abordagens para resolver esse problema. No entanto, recomendamos que você proteja explicitamente as chamadas [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou DXGI com o bloqueio [Direct2D,](./direct2d-portal.md) pois ele geralmente fornece melhor desempenho, pois protege a simulta em um nível muito mais fino e com menor sobrecarga sob Direct2D cobertura.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Garantindo a atomicidade de operações com estado

Embora os recursos de segurança de thread do [DirectX](/previous-versions//ee663301(v=vs.85)) possam ajudar a garantir que nenhuma chamada à API individual seja feita simultaneamente, você também deve garantir que os threads que fazem chamadas à API com estado não interfiram entre si. Veja um exemplo.

1.  Há duas linhas de texto que você deseja renderizar na tela (por Thread 0) e fora da tela (por Thread 1): a linha 1 é "A é maior" e a Linha \# \# 2 é "que B", ambas desenhadas usando um pincel preto sólido.
2.  O thread 1 desenha a primeira linha de texto.
3.  O thread 0 reage a uma entrada do usuário, atualiza ambas as linhas de texto para "B é menor" e "que A", respectivamente, e alterou a cor do pincel para vermelho sólido para seu próprio desenho;
4.  O thread 1 continua desenhando a segunda linha de texto, que agora é "que A", com o pincel de cor vermelho;
5.  Por fim, temos duas linhas de texto no destino de desenho fora da tela: "A é maior" em preto e "que A" em vermelho.

![um diagrama de threads na tela e fora da tela.](images/multi-thread4.png)

Na linha superior, Thread 0 desenha com cadeias de caracteres de texto atuais e o pincel preto atual. O thread 1 só termina o desenho fora da tela na metade superior.

Na linha intermediária, o Thread 0 responde à interação do usuário, atualiza as cadeias de caracteres de texto e o pincel e atualiza a tela. Neste ponto, o Thread 1 está bloqueado. Na linha inferior, a renderização final fora da tela após o Thread 1 retoma o desenho da metade inferior com um pincel alterado e uma cadeia de caracteres de texto alterada.

Para resolver esse problema, recomendamos que você tenha um contexto separado para cada thread, para que:

-   Você deve criar uma cópia do contexto do dispositivo para que os recursos mutáveis (ou seja, recursos que podem variar durante a exibição ou impressão, como o conteúdo do texto ou o pincel de cor sólida no exemplo) não mudem quando você renderizar. Neste exemplo, você deve manter uma cópia dessas duas linhas de textos e o pincel de cor antes de desenhar. Ao fazer isso, você garante que cada thread tenha conteúdo completo e consistente para desenhar e apresentar.
-   Você deve compartilhar recursos de peso pesado (como bitmaps e grafos de efeito complexo) que são inicializados uma vez e nunca modificados entre threads para aumentar o desempenho.
-   Você pode compartilhar recursos leves (como pincéis de cores sólidas e formatos de texto) que são inicializados uma vez e nunca modificados entre threads ou não

## <a name="summary"></a>Resumo

Ao desenvolver aplicativos [](./direct2d-portal.md) Direct2D multithread, você deve criar uma fábrica de Direct2D multithread e, em seguida, derivar todos os Direct2D dessa fábrica. Se um thread fizer chamadas [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou DXGI, você também deverá adquirir explicitamente e aplicar o bloqueio Direct2D para proteger essas chamadas Direct3D ou DXGI. Além disso, você deve garantir a integridade do contexto tendo uma cópia de recursos mutáveis para cada thread.
