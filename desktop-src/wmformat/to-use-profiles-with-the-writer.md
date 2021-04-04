---
title: Usar perfis com o gravador
description: Usar perfis com o gravador
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK, gravando arquivos ASF
- SDK do Windows Media Format, criando arquivos ASF
- SDK do Windows Media Format, formato de sistemas avançados (ASF)
- ASF (Advanced Systems Format), gravando arquivos
- ASF (formato de sistemas avançados), gravando arquivos
- ASF (Advanced Systems Format), criando arquivos
- ASF (formato de sistemas avançados), criando arquivos
- perfis, criando arquivos ASF
- perfis, gravando arquivos ASF
- perfis, criação de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007233"
---
# <a name="to-use-profiles-with-the-writer"></a>Usar perfis com o gravador

O gravador usa dados de perfil para criar arquivos ASF. Você deve especificar um perfil para uso antes de fazer qualquer outra coisa com o gravador.

Você pode definir um perfil do sistema para uso com o gravador passando a ID do perfil para o método [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .

Para especificar um perfil personalizado para uso com o gravador, você deve obter uma interface [**IWMProfile**](iwmprofile.md) para um objeto que contém os dados de perfil desejados. Você pode usar um dos métodos de carregamento da interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) para fazer isso. Depois de ter uma interface **IWMProfile** válida, você pode passar um ponteiro para ele para o método [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) . Para obter mais informações sobre configurações de perfil, consulte [trabalhando com perfis](working-with-profiles.md).

Se você fizer alterações no objeto de perfil usando a interface **IWMProfile** depois de definir o perfil no gravador, deverá chamar **setprofile** novamente ou as alterações não serão refletidas no gravador. No entanto, chamar **Setprofile** redefinirá todos os atributos de cabeçalho, portanto, certifique-se de definir todos os atributos de cabeçalho necessários depois de chamar esse método.

A função de exemplo a seguir define o perfil como "Windows Media Video 8 para modems dial-up (56 Kbps)":


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> Não há nenhum perfil de sistema predefinido que use os codecs de áudio do Windows Media e vídeo 9 Series. Para obter mais informações, consulte [reutilizando configurações de fluxo](reusing-stream-configurations.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




