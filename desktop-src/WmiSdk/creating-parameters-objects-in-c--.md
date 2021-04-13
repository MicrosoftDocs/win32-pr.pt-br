---
description: 'Os métodos IWbemServices:: ExecMethod ou ExecMethodAsync exigem a \_ \_ classe de sistema Parameters como um contêiner em pInParams se o método que eles estão executando tiver argumentos de entrada.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Criando objetos de parâmetros em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165336"
---
# <a name="creating-parameters-objects-in-c"></a>Criando objetos de parâmetros em C++

Os métodos [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) exigem a classe de sistema [**\_ \_ Parameters**](--parameters.md) como um contêiner em *pInParams* se o método que eles estão executando tiver argumentos de entrada.

O procedimento a seguir descreve como criar uma instância da classe de sistema [**\_ \_ Parameters**](--parameters.md) para armazenar informações de parâmetro.

**Para criar uma instância de \_ \_ parâmetros**

1.  Determine o caminho de classe da classe que contém a definição do método.
2.  Usando o caminho de classe e o ponteiro de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) passado de [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), chame [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar as classes de parâmetro de entrada e saída.

    O método [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retorna um ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para acessar cada uma dessas classes.

3.  Usando o ponteiro [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para a classe de saída, chame [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) para criar uma instância da classe.
4.  Preencha a instância de classe definindo as propriedades que correspondem aos valores de saída e, se houver um valor de retorno para o método, a propriedade [ReturnValue](creating-a-method.md) .
5.  Passe a instância de [**\_ \_ parâmetros**](--parameters.md) de volta para o chamador por meio do método [**IWbemObjectSink:: indicativo**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

Depois que um provedor de método determina que os parâmetros de entrada estão corretos, o método apontado por *strMethodName* pode ainda passar ou falhar. Alguns provedores de método geram um segundo thread para implementar o método para que o êxito ou a falha real do método acabe sendo relatado para o chamador por meio de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Observe que **IWbemObjectSink:: SetStatus** não recebe o código de retorno do método do provedor. No entanto, ele recebe o código de retorno do mecanismo de retorno de chamada real e só é útil para verificar se a chamada ocorreu ou se falhou por motivos mecânicos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando um método](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult:: getresultobject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



