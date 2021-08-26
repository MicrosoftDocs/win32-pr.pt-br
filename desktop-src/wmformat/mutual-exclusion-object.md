---
title: Objeto de exclusão mútua
description: Objeto de exclusão mútua
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows SDK de Formato de Mídia, objetos de exclusão mútua
- ASF (Advanced Systems Format), objetos de exclusão mútua
- ASF (Formato de Sistemas Avançados), objetos de exclusão mútua
- objetos, objetos de exclusão mútua
- exclusão mútua, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d7e780ac18dcad7ef04f9bb50d3a7389851156866980b21fbe0c231bcb057d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929926"
---
# <a name="mutual-exclusion-object"></a>Objeto de exclusão mútua

Um objeto de exclusão mútua é usado para especificar um número de fluxos, dos quais apenas um pode ser entregue por vez. Isso pode ser usado de várias maneiras, como o fornecimento de um fluxo de áudio em várias linguagens como a trilha para um fluxo de vídeo.

A exclusão mútua é uma parte opcional de um perfil. Objetos de exclusão mútua podem ser criados para informações de exclusão mútua existentes em um perfil ou podem ser criados vazios, prontos para receber novos dados. Objetos de exclusão mútua não podem existir independentemente de um objeto de perfil. Para salvar o conteúdo de um objeto de exclusão mútua, você deve chamar [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

Para criar um objeto de exclusão mútua, use um dos métodos a seguir.



| Método                                                                              | Descrição                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Cria um objeto de exclusão mútua sem dados.                                                                                                         |
| [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Cria um objeto de exclusão mútua populado com dados de um perfil. Usa o índice de exclusão mútua para identificar as informações de exclusão mútua desejadas. |



 

Ambos os métodos na tabela anterior definiram um ponteiro para uma interface **IWMMutualExclusion.** A interface **IWMStreamList** é herdada por **IWMMutualExclusion** e nunca precisa ser acessada diretamente. A outra interface do objeto de exclusão mútua pode ser obtida chamando o **método QueryInterface.**

As interfaces a seguir têm suporte em cada objeto de exclusão mútua.



| Interface                                          | Descrição                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | Define e recupera o tipo de exclusão mútua a ser usado.                                                                                            |
| [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | Organiza fluxos em registros, que podem ser usados para criar cenários complexos de exclusão mútua. Herda todos os métodos de **IWMMutualExclusion**. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Gerencia a lista de fluxos mutuamente exclusivos.                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exclusão mútua**](mutual-exclusion.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto do gerenciador de perfis**](profile-manager-object.md)
</dt> </dl>

 

 




