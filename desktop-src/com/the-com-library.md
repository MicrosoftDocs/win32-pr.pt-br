---
title: A biblioteca COM
description: A biblioteca COM
ms.assetid: 51d4db4a-ad88-4627-8140-2f7906945752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a285a89ca659907c37f92b7d00f3e3e04d0acf51
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2020
ms.locfileid: "103917051"
---
# <a name="the-com-library"></a>A biblioteca COM

Qualquer processo que usa COM deve inicializar e cancelar a inicialização da biblioteca COM. Além de ser uma especificação, o COM também implementa alguns serviços importantes nessa biblioteca. Fornecido como um conjunto de DLLs e EXEs (principalmente Ole32.dll e Rpcss.exe) no Microsoft Windows, a biblioteca COM inclui o seguinte:

-   Um pequeno número de funções fundamentais que facilitam a criação de aplicativos COM, tanto o cliente quanto o servidor. Para clientes, o COM fornece funções básicas para a criação de objetos. Para servidores, o COM fornece o meio de expor seus objetos.

-   Implementação – os serviços do localizador por meio dos quais o COM determina, de um identificador de classe exclusivo (CLSID), qual servidor implementa essa classe e onde o servidor está localizado. Esse serviço inclui suporte para um nível de indireção, geralmente um registro do sistema, entre a identidade de uma classe de objeto e o empacotamento da implementação para que os clientes sejam independentes do empacotamento, o que pode ser alterado no futuro.

-   Chamadas de procedimento remoto transparentes quando um objeto está sendo executado em um servidor local ou remoto.

-   Um mecanismo padrão para permitir que um aplicativo controle como a memória é alocada dentro de seu processo, especialmente a memória que precisa ser passada entre os objetos de cooperabilidade para que ele possa ser liberado corretamente.

Para usar os serviços COM básicos, todos os threads COM de execução em clientes e servidores fora do processo devem chamar o [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou a função [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) antes de chamar qualquer outra função com, exceto as chamadas de alocação de memória. **CoInitializeEx** substitui a outra função, adicionando um parâmetro que permite que você especifique o modelo de Threading do thread: Apartment-Threaded ou Free-threaded. Uma chamada para **CoInitialize** simplesmente define o modelo de Threading como Apartment-Threaded.

Os aplicativos de documento OLE composto chamam a função [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) , que chama [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) e também faz alguma inicialização necessária para documentos compostos. Portanto, os threads que chamam **OleInitialize** não podem ser de thread livre. Para obter informações sobre Threading em clientes e servidores, consulte [processos, threads e Apartments](processes--threads--and-apartments.md).

Os servidores em processo não chamam as funções de inicialização porque estão sendo carregados em um processo que já fez isso. Como resultado, os servidores em processo devem definir seu modelo de threading no registro na chave [InprocServer32](inprocserver32.md) . Para obter informações detalhadas sobre problemas de Threading em servidores em processo, consulte [problemas de Threading do servidor em processo](in-process-server-threading-issues.md).

Também é importante cancelar a inicialização da biblioteca. Para cada chamada para [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), deve haver uma chamada correspondente para [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Para cada chamada para [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize), deve haver uma chamada correspondente para [**OleUninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize).

Os servidores em processo podem assumir que o processo no qual eles estão sendo carregados já realizou essas etapas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O Component Object Model](the-component-object-model.md)
</dt> </dl>

 

 




