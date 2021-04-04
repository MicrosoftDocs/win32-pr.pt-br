---
title: Compartilhamento de largura de banda
description: Compartilhamento de largura de banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- SDK do Windows Media Format, compartilhamento de largura de banda
- ASF (Advanced Systems Format), compartilhamento de largura de banda
- ASF (formato de sistemas avançados), compartilhamento de largura de banda
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- compartilhamento de largura de banda, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007132"
---
# <a name="bandwidth-sharing"></a>Compartilhamento de largura de banda

Você pode especificar fluxos em um arquivo que, quando agrupados, usem menos largura de banda do que a soma das taxas de bits declaradas combinadas. Ao especificar o compartilhamento de largura de banda no perfil, você esclarece a leitura de aplicativos de que a largura de banda disponível necessária para transmitir o arquivo não é o que ele poderia parecer.

Nenhum dos objetos do Windows Media Format SDK alteram seu comportamento em resposta a informações de compartilhamento de largura de banda, que é fornecida exclusivamente para que a leitura de aplicativos possa levá-lo ao determinar se um arquivo pode ser reproduzido com entrega de largura de banda restrita.

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

 

 




