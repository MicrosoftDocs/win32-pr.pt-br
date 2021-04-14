---
description: QueryAccept (downstream)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: QueryAccept (downstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9015e0a246abb9fb996c0771e4bc935cccda054d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568707"
---
# <a name="queryaccept-downstream"></a>QueryAccept (downstream)

Esse mecanismo permite que um pino de saída proponha um novo formato a seu par downstream. O novo formato não deve exigir um tamanho de buffer maior. O pino de saída faz o seguinte:

1.  Chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) ou [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) no pino downstream, para verificar se o outro PIN pode aceitar o novo tipo de mídia (veja A ilustração, etapa A).
2.  Se o valor de retorno da etapa 1 for S \_ OK, o PIN anexará o tipo de mídia ao próximo exemplo. Para fazer isso, primeiro ele chama [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para obter o exemplo (B). Em seguida, ele chama [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) para anexar o tipo de mídia a esse exemplo (C). Ao anexar o tipo de mídia ao exemplo, o filtro indica que o formato foi alterado, começando com esse exemplo.
3.  O PIN entrega o exemplo (D).
4.  Quando o filtro downstream recebe o exemplo, ele chama [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) para recuperar o novo tipo de mídia.

    ![QueryAccept (downstream)](images/dynformat3.png)

Todos os Pins dão suporte ao `QueryAccept` método. No entanto, esse método é um pouco ambíguo, pois um valor de retorno de S \_ OK nem sempre garante que você possa alterar o formato enquanto o grafo estiver ativo. Alguns filtros podem retornar S \_ OK, mas rejeitar a alteração se o grafo estiver ativo. O método **DynamicQueryAccept** , que é suportado por alguns Pins de entrada, define explicitamente \_ os S OK para significar que o PIN pode alterar os formatos enquanto ativo. Se um PIN de entrada der suporte à interface **IPinConnection** , você deverá chamar **DynamicQueryAccept** em vez de `QueryAccept` .

Na maioria dos casos, esse mecanismo não permite alterações drásticas no formato, como a alteração da profundidade de bits. Uma situação na qual ela pode ser usada é quando um decodificador de vídeo alterna as paletas. Os detalhes básicos do formato permanecem os mesmos, como as dimensões de imagem e a profundidade de bits, mas o novo tipo de mídia tem um conjunto diferente de entradas de paleta.

**Observação de implementação**

Nas classes base do DirectShow, [**CBasePin:: QueryAccept**](cbasepin-queryaccept.md) chama o método **CheckMediaType** , que também é chamado durante a conexão inicial do PIN. No caso de um filtro de transformação, o método **CheckMediaType** do pino de entrada deve sempre verificar se o pino de saída está conectado e, nesse caso, se o tipo de mídia de entrada é compatível com o tipo de mídia de saída. Portanto, essa implementação provavelmente será válida para o `QueryAccept` . Caso contrário, você deve substituir `QueryAccept` para executar quaisquer verificações adicionais necessárias. Além disso, observe que a classe [**CTransformFilter**](ctransformfilter.md) encapsula essa lógica nos métodos **CheckInputType** e **CheckTransform** . A classe [**CTransInPlaceFilter**](ctransinplacefilter.md) , por outro lado, sempre chama `QueryAccept` o próximo filtro upstream ou downstream.

O método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) verifica um tipo de mídia no exemplo de entrada e, se houver um, chama **CheckMediaType**. No entanto, ele não atualiza o membro do **m \_ MT** do PIN, que mantém o tipo de mídia atual. Quando o filtro processa o exemplo, você deve verificar o exemplo para um tipo de mídia. Se houver um novo tipo, você provavelmente precisará armazená-lo, chamando **SetMediaType** no PIN ou definindo o valor de **m \_ MT** diretamente. Por outro lado, a classe [**CVideoTransformFilter**](cvideotransformfilter.md) , que é projetada para filtros de transformação de vídeo, armazena o tipo de mídia quando ele é alterado. Para obter detalhes, consulte o código-fonte para [**CVideoTransformFilter:: Receive**](cvideotransformfilter-receive.md) na biblioteca de classes base do DirectShow.

Em alguns casos, você pode simplesmente passar o `QueryAccept` downstream de chamada e, em seguida, anexar o tipo de mídia ao exemplo de saída e deixar que o filtro downstream manipule a alteração do formato.

 

 



