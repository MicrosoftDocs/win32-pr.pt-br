---
title: Implementando e ativando um manipulador sem dados de servidor adicionais
description: Implementando e ativando um manipulador sem dados de servidor adicionais
ms.assetid: 9d91260a-4cec-4a10-bb57-d02999efae47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6866b40e1257a865aa5068ffd46611c411498877
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "103923024"
---
# <a name="implementing-and-activating-a-handler-with-no-extra-server-data"></a>Implementando e ativando um manipulador sem dados de servidor adicionais

Para criar uma instância do seu manipulador, se for um que não obtém dados de servidor adicionais, o servidor deve implementar [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) , mas não [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). **IStdMarshalInfo** tem um método, [**GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler), que recupera o CLSID do manipulador de objetos a ser usado no processo de destino. COM chama isso quando chama [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) para você e ativa o manipulador no lado do cliente.

Em seguida, as implementações de servidor e de manipulador devem chamar a função [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) . Essa função cria um marshaler padrão em cada lado (chamado de Gerenciador de proxy no lado do cliente e um Gerenciador de stub no lado do servidor).

O servidor chama [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passando o sinalizador SMEXF \_ Server. Isso cria um marshaler padrão do lado do servidor (Gerenciador de stub). A estrutura do lado do servidor é mostrada na ilustração a seguir:

![Diagrama que mostra a estrutura do lado do servidor.](images/b47b3bc0-3e7d-4be4-9767-7ae436bd1b21.png)

## <a name="server-side-structure"></a>Estrutura de Server-Side

O manipulador chama [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passando o manipulador SMEXF do sinalizador \_ . Isso cria um marshaler padrão do lado do cliente (Gerenciador de proxy) e o agrega com o manipulador no lado do cliente. O tempo de vida de ambos são gerenciados pelo objeto de identidade de controle (implementando [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)) que o sistema implementa quando o manipulador chama **CoGetStdMarshalEx**. A estrutura do lado do cliente é mostrada na ilustração a seguir.

![Diagrama que mostra a estrutura do lado do cliente.](images/24ae70ef-dfa8-4784-90ac-dc6cfb043ee5.png)

## <a name="client-side-structure"></a>Estrutura de Client-Side

Conforme mostrado na ilustração anterior, o manipulador é, na verdade, Sandwich entre o Gerenciador de proxy e a identidade/controle desconhecida. Isso dá ao controle do sistema o tempo de vida do objeto, oferecendo ao controle do manipulador as interfaces expostas. A linha tracejada entre a identidade e o Gerenciador de proxy indica que os dois compartilham a forte integração por meio de interfaces privadas internas.

Quando COM chama [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) para o cliente, ele cria a instância do manipulador, agregando-a com a identidade. O manipulador criará o marshaler padrão (por meio da chamada para [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passando o controle desconhecido que ele recebeu quando foi criado). O manipulador não implementa [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , mas apenas retorna **IMarshal** do marshaler padrão. Mesmo que o manipulador implemente **IMarshal**, ele não será chamado durante um desempacotamento.

Se dois threads simultaneamente desempacotarem o mesmo objeto pela primeira vez, é possível que dois manipuladores sejam criados temporariamente. Um será lançado posteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O manipulador de Client-Side leve](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 