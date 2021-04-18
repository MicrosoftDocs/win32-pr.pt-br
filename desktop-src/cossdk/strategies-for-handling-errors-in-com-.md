---
description: Este tópico identifica várias estratégias de tratamento de erros para ter em mente ao desenvolver componentes para COM+.
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: Estratégias para lidar com erros no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca64546683fa45ac8df3bcb47534d8de482798
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781316"
---
# <a name="strategies-for-handling-errors-in-com"></a>Estratégias para lidar com erros no COM+

Este tópico identifica várias estratégias de tratamento de erros para ter em mente ao desenvolver componentes para COM+.

-   **Retornar um valor HRESULT para todos os métodos em todas as interfaces de componente.**  O COM+ usa valores **HRESULT** para relatar erros na realização de chamadas de função ou chamadas de método de interface. Um **HRESULT** indica se um método teve êxito ou falhou e identifica o recurso associado ao erro, como RPC, Win32 ou ITF para erros específicos da interface. Além disso, as APIs do sistema fornecem uma pesquisa de um **HRESULT** para uma cadeia de caracteres que descreve a condição de erro. Usar métodos que retornam valores **HRESULT** é fundamental para componentes bem escritos e é essencial para o processo de depuração. O Microsoft Visual Basic define automaticamente cada método com um **HRESULT** como um retorno. No Microsoft Visual C++, você deve retornar explicitamente um **HRESULT**. Para obter informações adicionais sobre HRESULTs, consulte [estrutura de códigos de erro com](/windows/desktop/com/structure-of-com-error-codes).
-   **Inicie o objeto da coleção ErrorInfo por qualquer que seja o que a ferramenta de desenvolvimento fornece.** Os objetos de coleção [**errorInfo**](errorinfo.md) geralmente são chamados de exceções com porque permitem que um objeto passe (ou lance) informações de erro avançadas para seu chamador, mesmo entre limites de apartamento. O valor desse objeto de erro genérico é que ele complementa um HRESULT, estendendo o tipo de informações de erro que você pode retornar a um chamador. Cada objeto da coleção **errorInfo** retorna uma descrição contextual, a origem do erro e o identificador da interface do método que originou o erro. Você também pode incluir ponteiros para uma entrada em um arquivo de ajuda. A automação fornece três interfaces para gerenciar o objeto de erro. Seu componente deve implementar a interface de automação **ISupportErrorInfo** para anunciar seu suporte para a coleção **errorInfo** . Quando ocorre um erro, o componente usa a interface de automação **ICreateErrorInfo** para inicializar um objeto de erro. Depois que o chamador inspeciona o HRESULT e descobre que a chamada do método falhou, ele consulta o objeto para ver se ele dá suporte à coleção **errorInfo** . Se tiver, o chamador usará a interface de automação **IErrorInfo** para recuperar as informações de erro. Visual Basic programadores têm acesso fácil ao objeto de coleção **errorInfo** , que é exposto por meio do objeto Err. Você pode gerar erros com a função de aumento de Err e capturar erros com a instrução **On Error** . A camada de tempo de execução Visual Basic cuida do mapeamento para você. Se você estiver usando o suporte ao compilador COM do Visual C++, você poderá usar a \_ \_ classe Error de elevação com \_ para relatar um erro e a \_ classe de \_ erro com para recuperar informações de erro. O COM+ não propagará as exceções C++ tradicionais como informações de **IErrorInfo** estendidas. Para obter informações adicionais sobre o objeto da coleção **errorInfo** , consulte "tratamento de erros" no guia de automação.
    > [!Note]  
    > COM requer que todos os objetos de coleção [**errorInfo**](errorinfo.md) sejam empacotados por valor, implicando que os componentes que implementam a interface de automação **IErrorInfo** também devem implementar e dar suporte à interface [**IMarshal**](/windows/desktop/api/objidl/nn-objidl-imarshal) . A implementação da interface **IMarshal** deve dar suporte a marshaling por valor para o componente.

     

-   **Use transações para gerenciar falhas de recursos compartilhados.** As transações automáticas podem reduzir significativamente a quantidade de código de tratamento de erros que você deve escrever ao usar gerenciadores de recursos gerenciados por Estado. No entanto, as transações não eliminam a necessidade de tratamento de erros completamente. Você ainda precisa retornar códigos de erro de seus métodos de interface e verificar esses códigos de erro no chamador para evitar o trabalho desnecessário para uma transação destinada. Para obter informações adicionais sobre como combinar o tratamento de erros com o processamento de transações, consulte [acelerando as transações notificando o objeto raiz](speeding-transactions-by-notifying-the-root-object.md).
-   **Gerar erros explicitamente.** Evite permitir que informações de erro deixem um objeto, a menos que o objeto gere explicitamente o erro. Pegue todos os erros gerados pela ferramenta e manipule-os no código do componente. Na pior das hipóteses, inclua um manipulador padrão para relatar erros inesperados de maneira consistente.
-   **Use o \_ intervalo ITF de erros para relatar erros específicos da interface.** Os erros específicos da interface devem estar no \_ intervalo de erros ITF, entre 0x0200 e 0xFFFF. Você pode definir um código de erro personalizado em Visual Basic como um deslocamento de vbObjectError. Use a \_ macro Make HRESULT em C++ para introduzir um código de erro específico da interface, conforme mostrado no exemplo a seguir:

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Política de FailFast e isolamento de falhas](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Localizando a origem de um erro](finding-the-source-of-an-error.md)
</dt> <dt>

[Como o COM+ modifica valores de retorno](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretando códigos de erro](interpreting-error-codes.md)
</dt> <dt>

[Solução de problemas](troubleshooting.md)
</dt> </dl>

 

 
