---
description: QueryAccept (Downstream)
ms.assetid: 3ca30f62-c320-40ea-9bf5-022abad912c4
title: QueryAccept (Downstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ec5c26209839f0dcd8351cc9a7ca84227faa2289d44d46c2c321fce0429e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747726"
---
# <a name="queryaccept-downstream"></a>QueryAccept (Downstream)

Esse mecanismo permite que um pino de saída propaponha um novo formato para seu par downstream. O novo formato não deve exigir um tamanho de buffer maior. O pino de saída faz o seguinte:

1.  Chama [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) ou [**IPinConnection::D ynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) no pino downstream para verificar se o outro pin pode aceitar o novo tipo de mídia (consulte ilustração, etapa A).
2.  Se o valor de retorno da etapa 1 for S OK, o pino anexa o \_ tipo de mídia ao próximo exemplo. Para fazer isso, primeiro ele chama [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para obter a amostra (B). Em seguida, ele [**chama IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) para anexar o tipo de mídia a esse exemplo (C). Ao anexar o tipo de mídia ao exemplo, o filtro indica que o formato foi alterado, começando com esse exemplo.
3.  O pino fornece o exemplo (D).
4.  Quando o filtro downstream recebe o exemplo, ele chama [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) para recuperar o novo tipo de mídia.

    ![queryaccept (downstream)](images/dynformat3.png)

Todos os pinos são suportados pelo `QueryAccept` método . No entanto, esse método é um pouco ambíguo, porque um valor de retorno de S OK nem sempre garante que você possa alterar o formato enquanto \_ o grafo estiver ativo. Alguns filtros podem retornar S \_ OK, mas rejeitar a alteração se o grafo estiver ativo. O **método DynamicQueryAccept,** que é suportado por alguns pinos de entrada, define explicitamente S OK para significar que o pino pode alterar formatos enquanto estiver \_ ativo. Se um pino de entrada for compatível com a interface **IPinConnection,** você deverá chamar **DynamicQueryAccept em vez** de `QueryAccept` .

Na maioria dos casos, esse mecanismo não permite alterações drásticas no formato, como alterar a profundidade do bit. Uma situação na qual ele pode ser usado é quando um decodificador de vídeo alterna paletas. Os detalhes básicos do formato permanecem os mesmos, como as dimensões de imagem e a profundidade do bit, mas o novo tipo de mídia tem um conjunto diferente de entradas de paleta.

**Observação de implementação**

Nas classes DirectShow base, [**CBasePin::QueryAccept**](cbasepin-queryaccept.md) chama o **método CheckMediaType,** que também é chamado durante a conexão de pino inicial. No caso de um filtro de transformação, o método **CheckMediaType** do pino de entrada sempre deve verificar se o pino de saída está conectado e se o tipo de mídia de entrada é compatível com o tipo de mídia de saída. Portanto, essa implementação provavelmente será válida para `QueryAccept` . Caso não seja, você deve `QueryAccept` substituir para executar quaisquer verificações adicionais necessárias. Além disso, observe que a [**classe CTransformFilter**](ctransformfilter.md) encapsula essa lógica nos métodos **CheckInputType** e **CheckTransform.** A [**classe CTransInPlaceFilter,**](ctransinplacefilter.md) por outro lado, sempre chama no próximo `QueryAccept` filtro upstream ou downstream.

O [**método CBaseInputPin::Receive**](cbaseinputpin-receive.md) verifica se há um tipo de mídia no exemplo de entrada e, se houver, chama **CheckMediaType**. No entanto, ele não atualiza o membro **\_ mt** do pino, que contém o tipo de mídia atual. Quando o filtro processa o exemplo, você deve verificar o exemplo para um tipo de mídia. Se houver um novo tipo, provavelmente você precisará armazená-lo, chamando **SetMediaType** no pino ou definindo o valor **de \_ mt** diretamente. Por outro lado, a classe [**CVideoTransformFilter,**](cvideotransformfilter.md) projetada para filtros de transformação de vídeo, armazena o tipo de mídia quando ele muda. Para obter detalhes, consulte o código-fonte [**de CVideoTransformFilter::Receive**](cvideotransformfilter-receive.md) na biblioteca DirectShow classe base.

Em alguns casos, você pode simplesmente passar a chamada downstream, anexar o tipo de mídia ao exemplo de saída e permitir que o filtro downstream manipular a `QueryAccept` alteração de formato.

 

 



