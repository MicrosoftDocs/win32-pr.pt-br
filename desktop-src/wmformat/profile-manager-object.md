---
title: Objeto do gerenciador de perfis
description: Objeto do gerenciador de perfis
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- SDK do Windows Media Format, objetos do Gerenciador de perfis
- ASF (Advanced Systems Format), objetos do Gerenciador de perfis
- ASF (formato de sistemas avançados), objetos do Gerenciador de perfis
- objetos, objetos do Gerenciador de perfis
- perfis, objetos
- perfis, objetos do Gerenciador de perfis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105780684"
---
# <a name="profile-manager-object"></a>Objeto do gerenciador de perfis

Um perfil é um conjunto de parâmetros de mídia usados para criar um arquivo ASF. O objeto Gerenciador de perfis cria objetos de perfil para edição. Os objetos de perfil podem ser criados sem dados ou criados a partir de dados de perfil existentes. O objeto Gerenciador de perfis também fornece métodos para enumerar codecs com suporte e consultar esses codecs para obter informações.

O objeto Gerenciador de perfis é criado pela função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , que define um ponteiro para uma interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . As outras interfaces do objeto do Gerenciador de perfis podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte do objeto Gerenciador de perfis.



| Interface                                                      | Descrição                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | Recupera informações sobre os codecs com suporte e seus formatos.                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | Recupera os nomes dos codecs com suporte e as descrições de seus formatos. Herda todos os métodos de **IWMCodecInfo**.          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | Recupera as propriedades do codec e os codecs de consultas para recursos com suporte. Herda todos os métodos de **IWMCodecInfo** e **IWMCodecInfo2**. |
| [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | Cria novos perfis, carrega perfis existentes e salva perfis personalizados.                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | Controla a versão dos perfis de sistema enumerados pelo Gerenciador de perfis. Herda todos os métodos de **IWMProfileManager**.             |
| [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | Controla o idioma dos perfis de sistema analisados pelo Gerenciador de perfis.                                                                  |



 

## <a name="remarks"></a>Comentários

Quando um objeto do Gerenciador de perfis é criado, ele analisa todos os perfis de sistema, o que pode levar vários segundos. Criar e liberar um Gerenciador de perfis toda vez que você precisar usá-lo afetará negativamente o desempenho. Você deve criar um Gerenciador de perfis uma vez no aplicativo e liberá-lo somente quando não precisar mais usá-lo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto de perfil**](profile-object.md)
</dt> <dt>

[**Perfis**](profiles.md)
</dt> </dl>

 

 




