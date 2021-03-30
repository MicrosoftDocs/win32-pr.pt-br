---
title: Aplicativos Direct2D com multithread
description: Descreve as práticas recomendadas para a criação de aplicativos Direct2D multithread.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be979b867edd6d36583959c4a595dbd507ca94f
ms.sourcegitcommit: c3243ec4ada05b7faf9d563853cb667ecef825e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2020
ms.locfileid: "103642972"
---
# <a name="multithreaded-direct2d-apps"></a>Aplicativos Direct2D com multithread

Se você desenvolver aplicativos [Direct2D](./direct2d-portal.md) , talvez seja necessário acessar os recursos do Direct2D de mais de um thread. Em outros casos, talvez você queira usar multithreading para obter melhor desempenho ou melhor capacidade de resposta (como usar um thread para exibição de tela e um thread separado para renderização offline).

Este tópico descreve as práticas recomendadas para o desenvolvimento de aplicativos [Direct2D](./direct2d-portal.md) multithread com pouca ou nenhuma renderização [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) . Os defeitos de software causados por problemas de simultaneidade podem ser difíceis de rastrear e é útil planejar sua política de multithread e seguir as práticas recomendadas descritas aqui.

> [!Note]  
> Se você acessar dois recursos de [Direct2D](./direct2d-portal.md) criados de duas fábricas de Direct2D de thread único diferentes, isso não causará conflitos de acesso, contanto que os dispositivos [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) subjacentes e contextos de dispositivo também sejam distintos. Ao falar sobre "acessando recursos de Direct2D" neste artigo, isso significa, na verdade, "acessando recursos Direct2D criados no mesmo dispositivo Direct2D", a menos que declarado de outra forma.

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Desenvolvendo Thread-Safe aplicativos que chamam apenas APIs Direct2D

Você pode criar uma instância de fábrica [Direct2D](./direct2d-portal.md) de vários threads. Você pode usar e compartilhar uma fábrica multithread e todos os seus recursos de mais de um thread, mas o acesso a esses recursos (por meio de chamadas Direct2D) são serializados por Direct2D, portanto, nenhum conflito de acesso ocorre. Se seu aplicativo chamar apenas APIs Direct2D, essa proteção será feita automaticamente pelo Direct2D em um nível granular com sobrecarga mínima. O código para criar uma fábrica multi-threaded aqui.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

A imagem aqui mostra como o [Direct2D](./direct2d-portal.md) serializa dois threads que fazem chamadas usando apenas a API Direct2D.

![diagrama de dois threads serializados.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Desenvolvendo Thread-Safe aplicativos Direct2D com chamadas Direct3D ou DXGI mínimas

É mais do que vezes que um aplicativo [Direct2D](./direct2d-portal.md) também faz algumas chamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi. Por exemplo, um thread de exibição será desenhado em Direct2D e apresentará o uso de uma [**cadeia de permuta dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

Nesse caso, garantir a segurança de thread é mais complicado: algumas chamadas [Direct2D](./direct2d-portal.md) indiretamente acessam os recursos subjacentes do [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) , que podem ser acessados simultaneamente por outro thread que chama Direct3D ou dxgi. Como essas chamadas de Direct3D ou DXGI estão fora do reconhecimento e do controle do Direct2D's, você precisa criar uma fábrica de Direct2D multithread, mas deve fazer o mor para evitar conflitos de acesso.

O diagrama aqui mostra um conflito de acesso ao recurso do [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) devido ao thread T0 acessando um recurso indiretamente por meio de uma chamada [Direct2D](./direct2d-portal.md) e T2 acessando o mesmo recurso diretamente por meio de uma chamada Direct3D ou dxgi.

> [!Note]  
> A proteção de thread que o [Direct2D](./direct2d-portal.md) fornece (o bloqueio azul nessa imagem) não ajuda nesse caso.

 

![diagrama de proteção de thread.](images/multi-thread2.png)

Para evitar conflitos de acesso de recursos aqui, recomendamos que você adquira explicitamente o bloqueio que o [Direct2D](./direct2d-portal.md) usa para sincronização de acesso interno e aplique esse bloqueio quando um thread precisar fazer chamadas [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi que possam causar conflito de acesso, como mostrado aqui. Em particular, você deve tomar cuidado especial com o código que usa exceções ou um sistema de início com base em códigos de retorno HRESULT. Por esse motivo, recomendamos que você use um padrão RAII (aquisição de recursos é inicialização) para chamar os métodos [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) .

> [!Note]  
> É importante que você emparelhe as chamadas para os métodos [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) , caso contrário, o aplicativo pode ser bloqueado.

 

O código aqui mostra um exemplo de quando bloquear e, em seguida, desbloqueá-las em chamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi.


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
> Algumas chamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi (notavelmente [**IDXGISwapChain::P reenviada**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)) podem adquirir bloqueios e/ou disparar retornos de chamada no código da função ou método de chamada. Você deve estar ciente disso e verificar se esse comportamento não causa deadlocks. Para obter mais informações, consulte o tópico [visão geral do dxgi](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) .

 

![diagrama de bloqueio de thread Direct2D e Direct3D.](images/multi-thread3.png)

Quando você usa os métodos [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) e [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) , as chamadas são protegidas pelo [Direct2D](./direct2d-portal.md) automático e pelo bloqueio explícito, de modo que o aplicativo não atinge o conflito de acesso.

Há outras abordagens para contornar esse problema. No entanto, é recomendável que você proteja explicitamente as chamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi com o bloqueio [Direct2D](./direct2d-portal.md) porque ela geralmente fornece melhor desempenho, pois protege a simultaneidade em um nível muito mais refinado e com menor sobrecarga na capa Direct2D's.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Garantindo a atomicidade de operações com estado

Embora os recursos de segurança de thread do [DirectX](/previous-versions//ee663301(v=vs.85)) possam ajudar a garantir que duas chamadas de API individuais sejam feitas simultaneamente, você também deve garantir que os threads que fazem chamadas de API com estado não interfiram uns com os outros. Veja um exemplo.

1.  Há duas linhas de texto que você deseja renderizar na tela (por thread 0) e fora da tela (por thread 1): \# a linha 1 é "A é maior" e a linha \# 2 é "do que B", e ambas serão desenhadas usando um pincel preto sólido.
2.  O thread 1 desenha a primeira linha de texto.
3.  O thread 0 reage a uma entrada do usuário, atualiza as linhas de texto para "B é menor" e "de A", respectivamente, e alterou a cor do pincel para vermelho sólido para seu próprio desenho;
4.  O thread 1 continua desenhando a segunda linha de texto, que agora é "de A", com o pincel de cor vermelha;
5.  Por fim, obtemos duas linhas de texto no destino de desenho fora da tela: "A é maior" em preto e "do que" em vermelho.

![um diagrama de threads de tela ativados e desativados.](images/multi-thread4.png)

Na linha superior, o thread 0 desenha com cadeias de texto atuais e o pincel preto atual. O thread 1 termina apenas o desenho fora da tela na metade superior.

Na linha intermediária, o thread 0 responde à interação do usuário, atualiza as cadeias de caracteres de texto e o pincel e, em seguida, atualiza a tela. Neste ponto, o thread 1 está bloqueado. Na linha inferior, a renderização final fora da tela após o thread 1 retoma o desenho da metade inferior com um pincel alterado e uma cadeia de caracteres de texto alterada.

Para resolver esse problema, recomendamos que você tenha um contexto separado para cada thread, de modo que:

-   Você deve criar uma cópia do contexto do dispositivo para que os recursos mutáveis (ou seja, os recursos que podem variar durante a exibição ou impressão, como conteúdo de texto ou o pincel de cor sólida no exemplo) não sejam alterados quando você renderiza. Neste exemplo, você deve manter uma cópia dessas duas linhas de texto e o pincel de cor antes de desenhar. Ao fazer isso, você garante que cada thread tenha conteúdo completo e consistente para desenhar e apresentar.
-   Você deve compartilhar recursos pesados (como bitmaps e grafos de efeitos complexos) que são inicializados uma vez e nunca são modificados em threads para aumentar o desempenho.
-   Você pode compartilhar recursos leves (como pincéis de cor sólida e formatos de texto) que são inicializados uma vez e nunca são modificados em threads ou não

## <a name="summary"></a>Resumo

Ao desenvolver aplicativos [Direct2D](./direct2d-portal.md) multithread, você deve criar uma fábrica de Direct2D multithread e, em seguida, derivar todos os recursos de Direct2D dessa fábrica. Se um thread fizer chamadas de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi, você também deverá adquirir explicitamente e aplicar o bloqueio Direct2D para proteger essas chamadas de Direct3D ou dxgi. Além disso, você deve garantir a integridade do contexto tendo uma cópia de recursos mutáveis para cada thread.
