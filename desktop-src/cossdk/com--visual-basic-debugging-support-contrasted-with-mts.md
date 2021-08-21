---
description: Suporte à depuração de Visual Basic COM+ contrastado com o MTS
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: Suporte à depuração de Visual Basic COM+ contrastado com o MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c278fbe414b2e58c5dd4aa8a3b2d694ed8ba49b0523e118f69116ec7061868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102468"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>Suporte à depuração de Visual Basic COM+ contrastado com o MTS

O COM+ remove ou reduz várias limitações de depuração com o Microsoft Visual Basic 6.0 e o MTS. A lista a seguir resume as alterações que você pode esperar com COM+:

-   Depurando vários componentes— No COM+, você pode depurar cenários em que um cliente em execução em uma instância do IDE faz chamadas para qualquer número de DLLs em execução em outro como um grupo de projetos. Os objetos nos projetos de DLL agrupados podem chamar um ao outro arbitrariamente, fluindo o contexto conforme necessário. É claro que isso também funciona quando as DLLs e o cliente estão no mesmo grupo de projetos na mesma instância do IDE.

-   Limitações de depuração em inicialização de classe e eventos de finalização de classe — com COM+, você pode colocar o código nos eventos Inicializar e Encerrar Classe de um componente de aplicativo \_ COM+, mesmo se esse código tentar acessar o objeto ou seu objeto de contexto \_ \_ \_ correspondente. Você pode definir pontos de interrupção lá e usar relógios. Você também pode definir pontos de interrupção no evento \_ Class Terminate.

    Embora ele não seja mais necessário como uma solução alternativa, você ainda poderá implementar a interface [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) e usar seus métodos [**Ativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e [**Desativar**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) se precisar executar código durante a inicialização e o desligamento do componente. Agora você também pode colocar pontos de interrupção no código para os métodos **Deactivate** ou [**CanBePooled.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)

-   Observando objetos MTS — com COM+, você pode adicionar relógios para variáveis de objeto retornadas por COM+, incluindo valores retornados dos métodos [**SafeRef,**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)e [**IObjectContext::CreateInstance.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)

-   Maior estabilidade quando os componentes falham – no COM+, uma falha de componente não será mais parada Visual Basic (que é executado no mesmo processo que o componente depurado). Por exemplo, o suporte para falhas de reativação JIT (Just-In-Time) agora permite que você veja o contexto do objeto durante a depuração.

-   O depurador pode reativar objetos liberados pelo COM+— Assim como no MTS, o Visual Basic 6.0 pode reativar objetos COM+ enquanto você está depurando uma etapa única por meio de um cliente. Devido à maneira como o Visual Basic 6.0 descobre informações sobre objetos, esse é o comportamento esperado. Por exemplo, considere o seguinte código:

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    Se obj. O método de teste [**chama IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), COM+ libera imediatamente obj da memória, mas obj ainda não foi definido como Nothing. Quando obj. O teste retorna, Visual Basic depurador chama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em obj para a interface [**IProvideClassInfo.**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) O wrapper de contexto associado ao obj cria uma nova instância de MyApp.MyClass para a chamada **QueryInterface.** Como resultado, você verá esse objeto não reinicializado no depurador após obj. O teste retornou. Esse objeto aparece apenas no depurador e é removido pela instrução subsequente para definir obj como Nothing.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Depurando componentes Visual Basic compilados](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Depuração no Visual Basic IDE](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
