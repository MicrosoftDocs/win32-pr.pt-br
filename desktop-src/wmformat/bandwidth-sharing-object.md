---
title: Objeto de compartilhamento de largura de banda
description: Objeto de compartilhamento de largura de banda
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows SDK de Formato de Mídia, objetos de compartilhamento de largura de banda
- FORMATO DE SISTEMAS Avançados (ASF), objetos de compartilhamento de largura de banda
- ASF (Formato de Sistemas Avançados), objetos de compartilhamento de largura de banda
- objetos, objetos de compartilhamento de largura de banda
- compartilhamento de largura de banda,sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 449a1e43a8f5c7212f1e9c4240d85eb11c9ee39209fab4313b373a56d017b2dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055596"
---
# <a name="bandwidth-sharing-object"></a>Objeto de compartilhamento de largura de banda

Um objeto de compartilhamento de largura de banda é usado para indicar que dois ou mais fluxos, independentemente de suas taxas de bits individuais, nunca usarão mais de uma quantidade especificada de largura de banda entre eles. Este é um objeto puramente informacional; as taxas de bits definidas dentro dele não são impostas programaticamente por nenhum objeto desse SDK.

As informações de compartilhamento de largura de banda são uma parte opcional de um perfil. Objetos de compartilhamento de largura de banda podem ser criados para informações de compartilhamento de largura de banda existentes em um perfil ou podem ser criados vazios, prontos para receber novos dados. Objetos de compartilhamento de largura de banda não podem existir independentemente de um objeto de perfil. Para salvar o conteúdo de um objeto de compartilhamento de largura de banda, você deve chamar [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).

Para criar um objeto de compartilhamento de largura de banda, chame um dos métodos a seguir.



| Método                                                                                  | Descrição                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | Cria um objeto de compartilhamento de largura de banda sem dados.                                                                                                           |
| [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | Cria um objeto de compartilhamento de largura de banda populado com dados de um perfil. Usa o índice de compartilhamento de largura de banda para identificar as informações de compartilhamento de largura de banda desejadas. |



 

Ambos os métodos na tabela anterior definiram um ponteiro para uma interface **IWMBandwidthSharing.** A interface **IWMStreamList** é herdada por **IWMBandwidthSharing,** portanto, não há necessidade de chamar **QueryInterface** com esse objeto.

As interfaces a seguir têm suporte em cada objeto de compartilhamento de largura de banda.



| Interface                                          | Descrição                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | Gerencia as propriedades de um grupo de fluxos que compartilharão largura de banda. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Gerencia a lista de fluxos que compartilharão largura de banda.                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Compartilhamento de largura de banda**](bandwidth-sharing.md)
</dt> <dt>

[**Objeto do gerenciador de perfis**](profile-manager-object.md)
</dt> <dt>

[**Objeto Profile**](profile-object.md)
</dt> </dl>

 

 




