---
description: Objetos de ativação
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: Objetos de ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401b4643e7e19c8cf0b7235218eaed2e355565fdb82a9d3756558e1f11991cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035593"
---
# <a name="activation-objects"></a>Objetos de ativação

Um *objeto de ativação* é um objeto auxiliar que é usado para criar outro objeto, um pouco semelhante a uma fábrica de classes. Os objetos de ativação expõem a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

Um objeto de ativação permite que você adie a criação do objeto de destino, pois você pode manter um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) sem criar o objeto de destino. Os objetos de ativação também podem ser serializados e, portanto, usados para criar o objeto de destino em outro processo. Por exemplo, os objetos de ativação são usados para realizar marshaling de componentes de pipeline do processo do aplicativo para o processo PMP (caminho de mídia protegido). Os objetos de ativação também são usados por determinadas funções de enumeração que retornam uma lista de ponteiros **IMFActivate** . Antes que o aplicativo crie o objeto de destino, ele pode obter informações sobre o objeto examinando atributos no objeto de ativação.

Para criar o objeto de destino a partir de um objeto de ativação, chame o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) . O chamador deve chamar [**IMFActivate:: shutdownobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) quando for feito usando o objeto criado. Geralmente, o aplicativo cria o objeto de ativação e a sessão de mídia chama **activateobject**. Nesse caso, a sessão de mídia, não o aplicativo, deve chamar **shutdownobject**. Em outras situações, o aplicativo recebe um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) da sessão de mídia e o aplicativo chama **Activateobject** e **shutdownobject**. (Por exemplo, consulte [como reproduzir arquivos de mídia protegidos](how-to-play-protected-media-files.md).)

Os objetos de ativação podem ter atributos e a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) herda a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Alguns objetos de ativação usam atributos para configurar o objeto criado. Os atributos específicos com suporte de cada objeto são documentados na referência para a função de criação do objeto de ativação. Defina os atributos usando o ponteiro **IMFActivate** que você recebe da função.

Para reprodução protegida, os objetos de ativação são empacotados para o processo de PMP. Para dar suporte ao marshaling, um objeto de ativação deve expor a interface **IPersistStream** . Além disso, o objeto de ativação e o objeto criado devem ser componentes confiáveis se o PMP estiver sendo executado em um processo protegido. Isso não é um requisito quando o PMP é carregado em um processo desprotegido.

Para usar um objeto de pipeline personalizado (como um coletor de mídia) dentro do processo de PMP, você deve implementar um objeto de ativação para o seu objeto de pipeline:

-   O objeto de ativação deve expor [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e **IPersistStream**.
-   O método **IPersist:: GetClassID** do objeto de ativação deve retornar o CLSID do objeto de ativação.
-   Opcionalmente, você pode implementar os métodos **IPersistStream:: Save** e **IPersistStream:: Load** para empacotar os dados necessários para configurar o objeto de ativação.

Quando a sessão de mídia carrega a topologia dentro do processo de PMP, ela chama **CoCreateInstance** para criar uma nova instância do objeto de ativação. Em seguida, ele chama [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar o objeto de pipeline.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



