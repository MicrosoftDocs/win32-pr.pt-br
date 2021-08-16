---
description: Este tópico lista as categorias comuns de problemas que você pode encontrar ao escrever aplicativos de Direct3D e como evitá-los.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Solução de problemas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637ac4b43e8947a6011e35ae9a36db7829ed47fd4d5740f93778116e4ee8f9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044074"
---
# <a name="troubleshooting-direct3d-9"></a>Solução de problemas (Direct3D 9)

Este tópico lista as categorias comuns de problemas que você pode encontrar ao escrever aplicativos de Direct3D e como evitá-los.

## <a name="device-creation"></a>Criação de dispositivo

Se o aplicativo falhar durante a criação do dispositivo, verifique os erros comuns a seguir.

-   Certifique-se de verificar os recursos do dispositivo, particularmente as profundidades de renderização.
-   Examine o código de erro. D3DERR \_ OUTOFVIDEOMEMORY sempre é possível.
-   Use a depuração de DLLs (bibliotecas de vínculo dinâmico) do DirectX e examine as mensagens de saída no depurador.

## <a name="using-lit-vertices"></a>Usando vértices acesos

Os aplicativos que usam vértices acesos devem desabilitar o mecanismo de iluminação Direct3D definindo o \_ estado de renderização de iluminação D3DRS como **false**. Por padrão, quando a iluminação está habilitada, o sistema define a cor de qualquer vértice que não contenha um vetor normal como 0 (preto), mesmo se o vértice de entrada contiver um valor de cor diferente de zero. Como os vértices acesos Não, por sua natureza, contêm um vértice normal, todas as informações de cores passadas para o Direct3D serão perdidas durante a renderização se o mecanismo de iluminação estiver habilitado.

Obviamente, a cor do vértice é importante para qualquer aplicativo que executa sua própria iluminação. Para impedir que o sistema impondo os valores padrão, certifique-se de definir a \_ iluminação D3DRS como **false**.

Se o aplicativo for executado, mas nada estiver visível, verifique os erros comuns a seguir.

-   Verifique se os triângulos não são degenerados.
-   Verifique se os triângulos não estão sendo refigurados.
-   Certifique-se de que suas transformações sejam consistentes internamente.
-   Verifique as configurações do visor para ter certeza de que eles permitem que os triângulos sejam vistos.

## <a name="debugging"></a>Depuração

A depuração de um aplicativo Direct3D pode ser desafiadora. Experimente as técnicas a seguir, além de verificar todos os valores de retorno, um pedaço especialmente importante de conselhos na programação do Direct3D, que depende de implementações de hardware muito diferentes.

-   Alterne para Debug DLLs.
-   Forçar um dispositivo somente de software, desativando a aceleração de hardware mesmo quando ela estiver disponível.
-   Forçar superfícies na memória do sistema.
-   Crie uma opção para ser executada em uma janela, para que você possa usar um depurador integrado.

A segunda e terceira opções dessa lista podem ajudá-lo a evitar o bloqueio de Win16 que, de outra forma, pode fazer com que o depurador trave.

Além disso, tente adicionar as entradas a seguir a Win.ini.


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Inicialização do Borland Floating-Point

Compiladores da Borland reportam exceções de ponto flutuante de uma maneira que é incompatível com o Direct3D. Para resolver esse problema, inclua um \_ manipulador de exceção matherr como o seguinte:


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a>Validação de parâmetro

Por motivos de desempenho, a versão de depuração do tempo de execução do modo do Direct3D Immediate executa mais validação de parâmetro do que a versão comercial, que às vezes não executa nenhuma validação. Isso permite que os aplicativos executem uma depuração robusta com o componente de tempo de execução de depuração mais lento antes de usar a versão de varejo mais rápida para o ajuste de desempenho e a versão final.

Embora vários métodos de modo do Direct3D Immediate imponham limites nos valores que eles podem aceitar, esses limites geralmente são verificados e aplicados pela versão de depuração do tempo de execução do modo do Direct3D Immediate. Os aplicativos devem estar em conformidade com esses limites ou resultados imprevisíveis e indesejáveis podem ocorrer durante a execução na versão comercial do Direct3D. Por exemplo, o método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) aceita um parâmetro (primitiveCount) que indica o número de primitivos que o método processará. O método só pode aceitar valores entre 0 e D3DMAXNUMPRIMITIVES. Na versão de depuração do Direct3D, se você passar mais de D3DMAXNUMPRIMITIVES primitivos, o método falhará normalmente, imprimindo uma mensagem de erro no log de erros e retornando um valor de erro para seu aplicativo. Por outro lado, se o seu aplicativo fizer o mesmo erro quando ele estiver em execução com a versão de varejo do tempo de execução, o comportamento será indefinido. Por motivos de desempenho, o método não valida os parâmetros, resultando em comportamento imprevisível e de situação completamente quando eles não são válidos. Em alguns casos, a chamada pode funcionar e, em outros casos, pode causar uma falha de memória no Direct3D. Se uma chamada inválida funciona consistentemente com uma configuração de hardware específica e a versão do DirectX, não há nenhuma garantia de que ela continuará a funcionar em outro hardware ou em versões posteriores do DirectX.

Se seu aplicativo encontrar falhas não explicadas ao executar com o arquivo de tempo de execução do Direct3D de varejo, teste em relação à versão de depuração e examine de forma mais detalhada os casos em que seu aplicativo passa parâmetros inválidos. Use o miniaplicativo do painel de controle do DirectX, alterne para o tempo de execução de depuração, se necessário, e marque a opção "interromper no D3DError". essa opção forçará o tempo de execução a usar o método Windows DebugBreak para forçar o aplicativo a parar quando um bug de aplicativo for detectado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
