---
title: Priorização de fluxo
description: Priorização de fluxo
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- SDK do Windows Media Format, priorização de fluxo
- ASF (Advanced Systems Format), priorização de fluxo
- ASF (formato de sistemas avançados), priorização de fluxo
- SDK do Windows Media Format, ordem de prioridade para fluxos
- ASF (Advanced Systems Format), ordem de prioridade para fluxos
- ASF (formato de sistemas avançados), ordem de prioridade para fluxos
- fluxos, priorização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007128"
---
# <a name="stream-prioritization"></a>Priorização de fluxo

Ao criar um arquivo ASF, você pode especificar uma ordem de prioridade para seus fluxos de constituintes. Se você transmitir um arquivo priorizado e a largura de banda disponível não for suficiente para fornecer todos os fluxos, o leitor removerá os fluxos na ordem de prioridade inversa. Dessa forma, você pode garantir que os fluxos mais importantes em seu arquivo não serão descartados devido a problemas de rede.

A priorização de fluxo é configurada com um objeto de priorização de fluxo e adicionada ao perfil. Um perfil pode conter apenas um objeto de priorização de fluxo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3::RemoveStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**Interface IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**Usando a priorização de fluxo**](using-stream-prioritization.md)
</dt> </dl>

 

 




