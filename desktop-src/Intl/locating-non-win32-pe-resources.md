---
description: Localizando recursos não Win32 PE
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Localizando recursos não Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf706712b2e1be2dd8fb1598c1404a829251bb24db83db7c7d6deaa87a13d24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147169"
---
# <a name="locating-non-win32-pe-resources"></a>Localizando recursos não Win32 PE

Para localizar recursos não Win32 PE, seu aplicativo deve primeiro chamar a função [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) para localizar o arquivo de recurso específico do idioma do qual os recursos devem ser carregados. Se o aplicativo estiver seguindo as configurações de idioma do sistema, ele deverá chamar a função com o \_ nome do idioma \_ do MUI \| \_ \_ \_ idiomas da interface do usuário preferencial do MUI \_ especificados para *dwFlags* e **null** especificados para *pwszLanguage*. Se o aplicativo estiver seguindo as configurações de idioma específicas do aplicativo, ele usará **GetFileMUIPath** para determinar se existe um arquivo específico de idioma especificando o idioma no parâmetro *pwszLanguage* .

Após a chamada para [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), o aplicativo deve definir a funcionalidade personalizada para carregar o módulo de recurso e carregar recursos específicos dele. Por exemplo, se você estiver usando um arquivo de recurso de .txt ou .xml, o aplicativo deverá usar um analisador TXT ou XML para carregar o arquivo e, em seguida, analisar o conteúdo do arquivo para cada recurso necessário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[usando Interface de Usuário Multilíngue](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



