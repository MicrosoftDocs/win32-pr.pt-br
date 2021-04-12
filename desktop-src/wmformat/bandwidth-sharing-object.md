---
title: Objeto de compartilhamento de largura de banda
description: Objeto de compartilhamento de largura de banda
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- SDK do Windows Media Format, objetos de compartilhamento de largura de banda
- ASF (Advanced Systems Format), objetos de compartilhamento de largura de banda
- ASF (formato de sistemas avançados), objetos de compartilhamento de largura de banda
- objetos, objetos de compartilhamento de largura de banda
- compartilhamento de largura de banda, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365589"
---
# <a name="bandwidth-sharing-object"></a>Objeto de compartilhamento de largura de banda

Um objeto de compartilhamento de largura de banda é usado para indicar que dois ou mais fluxos, independentemente de suas taxas de bits individuais, nunca usarão mais do que uma quantidade especificada de largura de banda entre eles. Esse é um objeto puramente informativo; as taxas de bits definidas dentro dela não são impostas programaticamente por qualquer objeto desse SDK.

As informações de compartilhamento de largura de banda são uma parte opcional de um perfil. Objetos de compartilhamento de largura de banda podem ser criados para informações de compartilhamento de largura de banda existentes em um perfil ou podem ser criados em branco, prontos para receber novos dados. Os objetos de compartilhamento de largura de banda não podem existir independentemente de um objeto de perfil. Para salvar o conteúdo de um objeto de compartilhamento de largura de banda, você deve chamar [**IWMProfile3:: AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).

Para criar um objeto de compartilhamento de largura de banda, chame um dos métodos a seguir.



| Método                                                                                  | Descrição                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | Cria um objeto de compartilhamento de largura de banda sem nenhum dado.                                                                                                           |
| [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | Cria um objeto de compartilhamento de largura de banda preenchido com dados de um perfil. Usa o índice de compartilhamento de largura de banda para identificar as informações de compartilhamento de largura de banda desejada. |



 

Os dois métodos na tabela anterior definiram um ponteiro para uma interface **IWMBandwidthSharing** . A interface **IWMStreamList** é herdada por **IWMBandwidthSharing**, portanto, não é necessário chamar **QueryInterface** com esse objeto.

As interfaces a seguir têm suporte em cada objeto de compartilhamento de largura de banda.



| Interface                                          | Descrição                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | Gerencia as propriedades de um grupo de fluxos que compartilharão a largura de banda. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Gerencia a lista de fluxos que compartilharão a largura de banda.                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Compartilhamento de largura de banda**](bandwidth-sharing.md)
</dt> <dt>

[**Objeto do gerenciador de perfis**](profile-manager-object.md)
</dt> <dt>

[**Objeto de perfil**](profile-object.md)
</dt> </dl>

 

 




