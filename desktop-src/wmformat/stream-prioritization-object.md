---
title: Objeto de priorização de fluxo
description: Objeto de priorização de fluxo
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows SDK de Formato de Mídia, objetos de priorização de fluxo
- FORMATO DE SISTEMAS Avançados (ASF), objetos de priorização de fluxo
- ASF (Formato de Sistemas Avançados), objetos de priorização de fluxo
- objetos, objetos de priorização de fluxo
- objetos de priorização de fluxo
- fluxos, objetos de priorização de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0d8ce386dfa6d3eed64361d77326c515feadb2a6aa05eb697e402d120a55ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699963"
---
# <a name="stream-prioritization-object"></a>Objeto de priorização de fluxo

Um objeto de priorização de fluxo é usado para especificar uma ordem de importância para os fluxos em um perfil. Quando a reprodução completa não for possível devido a limitações de taxa de bits, os fluxos de prioridade mais baixa serão os primeiros a serem descartados.

Objetos de priorização de fluxo podem ser criados para dados de priorização de fluxo existentes em um perfil ou podem ser criados vazios, prontos para receber novos dados. Objetos de priorização de fluxo não podem existir independentemente de um objeto de perfil. Para salvar o conteúdo de um objeto de priorização de fluxo, você deve chamar [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization). Para criar um objeto de priorização de fluxo, use um dos métodos a seguir.



| Método                                                                                          | Descrição                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Cria um objeto de priorização de fluxo sem dados.                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Cria um objeto de priorização de fluxo populado com dados do perfil. |



 

Ambos os métodos na tabela anterior definiram um ponteiro para uma interface **IWMStreamPrioritization.** Essa é a única interface com suporte pelo objeto de priorização de fluxo.



| Interface                                                  | Descrição                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Gerencia a lista de fluxos dentro do objeto de priorização de fluxo. |



 

## <a name="remarks"></a>Comentários

Somente uma priorização de fluxo pode existir para um determinado perfil. Se você criar uma nova priorização de fluxo para um perfil que já contém uma priorização de fluxo, a antiga será excluída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto Profile**](profile-object.md)
</dt> <dt>

[**Usando a priorização de fluxo**](using-stream-prioritization.md)
</dt> </dl>

 

 




