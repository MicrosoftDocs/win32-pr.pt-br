---
title: Perfis de sistema localizados
description: Perfis de sistema localizados
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows SDK de formato de mídia, perfis de sistema
- ASF (Advanced Systems Format), perfis de sistema
- ASF (formato de sistemas avançados), perfis de sistema
- Windows SDK do formato de mídia, perfis de sistema localizados
- ASF (Advanced Systems Format), perfis de sistema localizados
- ASF (formato de sistemas avançados), perfis de sistema localizados
- perfis de sistema, localizados
- perfis de sistema localizados, lista de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe3ca0abbe0e5b92645f6adaa1f6ebfdc44d52064d6fb8e1389420d19651b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707706"
---
# <a name="localized-system-profiles"></a>Perfis de sistema localizados

a tabela a seguir lista os arquivos de perfil do sistema localizados incluídos com o SDK do formato de mídia Windows e os idiomas associados a cada um. Esses arquivos são instalados na \[ pasta SDKRoot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles. Para acessar um arquivo específico com os métodos **IWMProfileManagerLanguage** , você deve movê-lo para o diretório raiz do sistema junto com os arquivos de perfil do sistema padrão.



| Idioma              | Nome do arquivo    |
|-----------------------|--------------|
| Árabe                | WMPrfAra.prx |
| Chinês – simplificado  | WMPrfCHS.prx |
| Chinês – tradicional | WMPrfCHT.prx |
| Tcheco                 | WMPrfCsy.prx |
| Dinamarquês                | WMPrfDan.prx |
| Holandês                 | WMPrfNld.prx |
| Finlandês               | WMPrfFin.prx |
| Francês                | WMPrfFra.prx |
| Alemão                | WMPrfDeu.prx |
| Grego                 | WMPrfEll.prx |
| Hebraico                | WMPrfHeb.prx |
| Húngaro             | WMPrfHun.prx |
| Italiano               | WMPrfIta.prx |
| Japonês              | WMPrfJpn.prx |
| Coreano                | WMPrfKor.prx |
| Norueguês             | WMPrfNor.prx |
| Polonês                | WMPrfPlk.prx |
| Português – Brasil   | WMPrfPtb.prx |
| Português – Portugal | WMPrfPtg.prx |
| Russo               | WMPrfRus.prx |
| Eslovaco                | WMPrfSky.prx |
| Esloveno             | WMPrfSlv.prx |
| Espanhol               | WMPrfEsp.prx |
| Sueco               | WMPrfSve.prx |
| Turco               | WMPrfTrk.prx |



 

Você pode definir o idioma para o objeto do Gerenciador de perfis chamando o método [**IWMProfileManagerLanguage:: SetUserLanguageID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) . Para a maioria dos idiomas, apenas o identificador de idioma primário no LANGid é examinado. As exceções são para os idiomas chinês e Português, em que o identificador de idioma secundário também é usado. A tabela a seguir mostra como criar um LANGid para especificar no método **SetUserLanguageID** .



| Idioma primário-secundário | Macro MAKELANGID                                             |
|----------------------------|--------------------------------------------------------------|
| Chinês (simplificado)       | MAKELANGID (idioma \_ chinês, subidioma \_ chinês \_ simplificado)     |
| Chinês (tradicional)      | MAKELANGID (idioma \_ chinês, subidioma \_ chinês \_ Cingapura)      |
| Português (Brasil)        | MAKELANGID (idioma \_ Português do Brasil, SUBLANG \_ Português \_ brasileiro) |
| Português (Portugal)      | MAKELANGID (idioma \_ Português, SUBLANG \_ Português)            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> <dt>

[**Perfis de sistema**](system-profiles.md)
</dt> </dl>

 

 




