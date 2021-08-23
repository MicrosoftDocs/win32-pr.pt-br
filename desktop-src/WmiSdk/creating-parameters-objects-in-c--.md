---
description: Os métodos IWbemServices::ExecMethod ou ExecMethodAsync exigirão a classe de sistema PARAMETERS como um contêiner em \_ pInParams se o método que eles estão executando tiver argumentos de \_ entrada.
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Criando objetos de parâmetros em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa97753eab9554e402a91cfce72a6435d44298b6b68a83de96fd4beccd83bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244516"
---
# <a name="creating-parameters-objects-in-c"></a>Criando objetos de parâmetros em C++

Os métodos [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) exigirão a classe de sistema [**\_ \_ PARAMETERS**](--parameters.md) como um contêiner em *pInParams* se o método que eles estão executando tiver argumentos de entrada.

O procedimento a seguir descreve como criar uma instância da classe do sistema [**\_ \_ PARAMETERS**](--parameters.md) para manter informações de parâmetro.

**Para criar uma instância de \_ \_ PARAMETERS**

1.  Determine o caminho de classe para a classe que contém a definição do método.
2.  Usando o caminho da classe e o ponteiro [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) passado de [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), chame [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar as classes de parâmetro de entrada e saída.

    O [**método GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retorna um [**ponteiro IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para acessar cada uma dessas classes.

3.  Usando o [**ponteiro IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para a classe de saída, chame [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) para criar uma instância da classe .
4.  Preencha a instância de classe definindo as propriedades que correspondem aos valores de saída e, se houver um valor de retorno para o método , a [propriedade ReturnValue.](creating-a-method.md)
5.  Passe a [**\_ \_ instância PARAMETERS**](--parameters.md) de volta para o chamador por meio do [**método IWbemObjectSink::Indicate.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)

Depois que um provedor de método determina que os parâmetros de entrada estão corretos, o método apontado por *strMethodName* ainda pode passar ou falhar. Alguns provedores de método geram um segundo thread para implementar o método para que o êxito ou a falha real do método termine sendo relatado ao chamador por meio [**de IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Observe que **IWbemObjectSink::SetStatus** não recebe o código de retorno do método do provedor. No entanto, ele recebe o código de retorno do mecanismo de retorno de chamada real e só é útil para verificar se a chamada ocorreu ou se ela falhou por motivos mecânicos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando um método](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult::GetResultObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



