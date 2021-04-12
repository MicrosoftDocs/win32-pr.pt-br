---
title: Implementando e ativando um manipulador com dados adicionais fornecidos pelo servidor
description: Implementando e ativando um manipulador com dados adicionais fornecidos pelo servidor
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78a3e39c85c37c52dfa3f09ef41f0a71b5f431
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104297822"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>Implementando e ativando um manipulador com dados adicionais fornecidos pelo servidor

Se o servidor quiser incluir alguns dados adicionais no pacote para o manipulador usar, o servidor deverá implementar as interfaces [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) e [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) . O servidor deve agregar o marshaler padrão e deve delegar a primeira parte do marshaling para o marshaler padrão agregado, incluindo [**IMarshal:: GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass), e deve adicionar seu próprio tamanho de dados ao tamanho retornado pelo [**IMarshal:: GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)do marshaler padrão. O marshaler padrão chama [**IStdMarshalInfo:: GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) para obter o CLSID do manipulador a ser criado. Depois que o marshaler padrão tiver feito seu marshaling, o servidor gravará seus próprios dados adicionais no fluxo. As estruturas resultantes, com dados adicionais no fluxo, são mostradas na ilustração a seguir:

![Diagrama que mostra estruturas com dados adicionais no fluxo.](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>Estruturas de Server-Side com dados adicionais no fluxo

Isso permite a chamada de COM para [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) no lado do cliente a capacidade de ignorar todos os dados não lidos e deixar o fluxo na posição apropriada seguindo todos os dados de interface empacotados se o manipulador não puder ser criado.

## <a name="client-side-structures-with-extra-data-in-stream"></a>Estruturas de Client-Side com dados adicionais no fluxo

Como no caso em que não há nenhum dado de servidor extra no fluxo, a chamada COM do lado do cliente para [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) criará a identidade e o manipulador. O manipulador deve implementar [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) e deve delegar as chamadas de **IMarshal** para o marshaler padrão agregado primeiro e, em seguida, realizar marshaling ou unmarshaling de quaisquer dados extras fornecidos pelo servidor. O [**UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) do manipulador será chamado para cada Unmarshal, independentemente de ele ter desempacotado a interface antes ou não. Nesse caso, o servidor não chama [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) , mas o manipulador deve. A estrutura resultante do lado do cliente é mostrada na ilustração a seguir.

![Diagrama que mostra a estrutura do lado do cliente.](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O manipulador de Client-Side leve](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 