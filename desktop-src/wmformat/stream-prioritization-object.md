---
title: Objeto de priorização de fluxo
description: Objeto de priorização de fluxo
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- SDK do Windows Media Format, objetos de priorização de fluxo
- ASF (Advanced Systems Format), objetos de priorização de fluxo
- ASF (formato de sistemas avançados), objetos de priorização de fluxo
- objetos, objetos de priorização de fluxo
- objetos de priorização de fluxo
- fluxos, objetos de priorização de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105793982"
---
# <a name="stream-prioritization-object"></a>Objeto de priorização de fluxo

Um objeto de priorização de fluxo é usado para especificar uma ordem de importância para os fluxos em um perfil. Quando a reprodução completa não é possível devido a limitações de taxa de bits, os fluxos de prioridade mais baixos serão os primeiros a serem descartados.

Os objetos de priorização de fluxo podem ser criados para dados de priorização de fluxo existentes em um perfil ou podem ser criados em branco, prontos para receber novos dados. Os objetos de priorização de fluxo não podem existir independentemente de um objeto de perfil. Para salvar o conteúdo de um objeto de priorização de fluxo, você deve chamar [**IWMProfile3:: SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization). Para criar um objeto de priorização de fluxo, use um dos métodos a seguir.



| Método                                                                                          | Descrição                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Cria um objeto de priorização de fluxo sem nenhum dado.                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Cria um objeto de priorização de fluxo populado com dados do perfil. |



 

Os dois métodos na tabela anterior definiram um ponteiro para uma interface **IWMStreamPrioritization** . Essa é a única interface suportada pelo objeto de priorização de fluxo.



| Interface                                                  | Descrição                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Gerencia a lista de fluxos dentro do objeto de priorização de fluxo. |



 

## <a name="remarks"></a>Comentários

Pode existir apenas uma priorização de fluxo para um determinado perfil. Se você criar uma nova priorização de fluxo para um perfil que já contém uma priorização de fluxo, a antiga será excluída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto de perfil**](profile-object.md)
</dt> <dt>

[**Usando a priorização de fluxo**](using-stream-prioritization.md)
</dt> </dl>

 

 




