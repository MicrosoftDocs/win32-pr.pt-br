---
description: Suporte à depuração de Visual Basic COM+ em contraste com o MTS
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: Suporte à depuração de Visual Basic COM+ em contraste com o MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038b29bbc6fbe5c8375f91f0006b85940f00b944
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798263"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>Suporte à depuração de Visual Basic COM+ em contraste com o MTS

COM+ remove ou reduz várias limitações de depuração com o Microsoft Visual Basic 6,0 e o MTS. A lista a seguir resume as alterações que você pode esperar com o COM+:

-   Depurando vários componentes — no COM+, você pode depurar cenários nos quais um cliente em execução em uma instância do IDE faz chamadas para qualquer número de DLLs em execução em outro como um grupo de projetos. Os objetos nos projetos de DLL agrupados podem chamar uns aos outros arbitrariamente, fluindo o contexto conforme necessário. É claro que isso também funciona quando as DLLs e o cliente estão no mesmo grupo de projetos na mesma instância do IDE.

-   Limitações de depuração em \_ eventos de inicialização de classe e de \_ término de classe — com o com+, você pode colocar o código nos eventos de inicialização de classe \_ e de classe \_ de um componente de aplicativo com+, mesmo que esse código tente acessar o objeto ou seu objeto de contexto correspondente. Você pode definir pontos de interrupção e usar inspeções. Você também pode definir pontos de interrupção no \_ evento classe Terminate.

    Embora não seja mais necessário como uma solução alternativa, você ainda pode implementar a interface [**controledeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) e usar seus métodos [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) se precisar executar o código durante a inicialização e o desligamento do seu componente. Agora você também pode colocar pontos de interrupção no código para os métodos **Deactivate** ou [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) .

-   Observando objetos do MTS — com o COM+, você pode adicionar inspeções para variáveis de objeto retornadas pelo COM+, incluindo valores de retorno dos métodos [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef), [**getObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)e [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) .

-   Maior estabilidade quando os componentes falham — no COM+, uma falha de componente deixará de ser interrompida sempre Visual Basic (que é executado no mesmo processo que o componente depurado). Por exemplo, o suporte para falhas de reativação JIT (just-in-time) agora permite que você examine o contexto do objeto durante a depuração.

-   O depurador pode reativar objetos liberados pelo COM+ — assim como no MTS, Visual Basic 6,0 pode reativar objetos COM+ enquanto você está Depurando uma única etapa por meio de um cliente. Por causa da maneira que Visual Basic 6,0 descobre informações sobre objetos, esse é o comportamento esperado. Por exemplo, considere o seguinte código:

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    Se obj. O método de teste chama [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), com+ imediatamente libera o obj da memória, mas obj ainda não foi definido como Nothing. Quando obj. Testes de retorno, o depurador de Visual Basic chama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em obj para a interface [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) . O wrapper de contexto associado a obj cria uma nova instância de MyApp. MyClass para atender à chamada de **QueryInterface** . Como resultado, você verá esse objeto não inicializado no depurador após o obj. O teste foi retornado. Esse objeto aparece apenas no depurador e é removido pela instrução subsequente para definir obj como Nothing.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Depurando componentes de Visual Basic compilados](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Depuração no IDE Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
