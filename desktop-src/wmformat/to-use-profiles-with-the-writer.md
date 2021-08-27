---
title: Usar perfis com o gravador
description: Usar perfis com o gravador
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows SDK de Formato de Mídia, escrevendo arquivos ASF
- Windows SDK de Formato de Mídia, criando arquivos ASF
- Windows SDK de Formato de Mídia, FORMATO DE SISTEMAS Avançados (ASF)
- ASF (Advanced Systems Format), escrevendo arquivos
- ASF (Formato de Sistemas Avançados), escrevendo arquivos
- ASF (Advanced Systems Format), criando arquivos
- ASF (Formato de Sistemas Avançados), criando arquivos
- perfis, criando arquivos ASF
- perfis, escrevendo arquivos ASF
- perfis, criação de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0184469215dd109bcc4ca120e2db9cbead8b9bd250cb017456f9d7d08ea46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027264"
---
# <a name="to-use-profiles-with-the-writer"></a>Usar perfis com o gravador

O autor usa dados de perfil para criar arquivos ASF. Você deve especificar um perfil para uso antes de fazer qualquer outra coisa com o autor.

Você pode definir um perfil do sistema para uso com o autor passando a ID do perfil para o [**método IWMWriter::SetProfileByID.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)

Para especificar um perfil personalizado para uso com o autor, você deve obter uma interface [**IWMProfile**](iwmprofile.md) para um objeto que contém os dados de perfil desejados. Você pode usar um dos métodos de carregamento da interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) para fazer isso. Depois de ter uma interface **IWMProfile** válida, você pode passar um ponteiro para ela para o [**método IWMWriter::SetProfile.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) Para obter mais informações sobre configurações de perfil, consulte [Trabalhando com perfis](working-with-profiles.md).

Se você fizer alterações no objeto de perfil usando a interface **IWMProfile** depois de definir o perfil no autor, deverá chamar **SetProfile** novamente ou as alterações não serão refletidas no autor. No entanto, **chamar SetProfile** redefinirá todos os atributos de header, portanto, defina todos os atributos de header necessários depois de chamar esse método.

A função de exemplo a seguir define o perfil como "Windows Vídeo de Mídia 8 para Modems Discados (56 Kbps)":


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
> Não há perfis de sistema predefinidos que usam os codecs Windows Media Audio e Video 9 Series. Para obter mais informações, consulte [Reutiling Stream Configurations](reusing-stream-configurations.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




