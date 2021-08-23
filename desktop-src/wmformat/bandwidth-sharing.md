---
title: Compartilhamento de largura de banda
description: Compartilhamento de largura de banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows SDK de formato de mídia, compartilhamento de largura de banda
- ASF (Advanced Systems Format), compartilhamento de largura de banda
- ASF (formato de sistemas avançados), compartilhamento de largura de banda
- Windows SDK do formato de mídia, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- compartilhamento de largura de banda, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b01ff94e82f2ce3609a93278fef30c68e1a59445eea22f68f4b0a5d92371a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709406"
---
# <a name="bandwidth-sharing"></a>Compartilhamento de largura de banda

Você pode especificar fluxos em um arquivo que, quando agrupados, usem menos largura de banda do que a soma das taxas de bits declaradas combinadas. Ao especificar o compartilhamento de largura de banda no perfil, você esclarece a leitura de aplicativos de que a largura de banda disponível necessária para transmitir o arquivo não é o que ele poderia parecer.

nenhum dos objetos do SDK do formato de mídia Windows alterar seu comportamento em resposta às informações de compartilhamento de largura de banda, que é fornecida exclusivamente para que a leitura de aplicativos possa levá-la ao determinar se um arquivo pode ser reproduzido com entrega de largura de banda restrita.

O compartilhamento de largura de banda é configurado com um objeto de compartilhamento de largura de banda e é adicionado a um perfil antes de começar a gravar um arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Objeto de compartilhamento de largura de banda**](bandwidth-sharing-object.md)
</dt> <dt>

[**Interface IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**Interface IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**Usando o compartilhamento de largura de banda**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




