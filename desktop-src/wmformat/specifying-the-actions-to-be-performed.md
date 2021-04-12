---
title: Especificando as ações a serem executadas
description: Especificando as ações a serem executadas
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- ASF (Advanced Systems Format), especificando ações
- ASF (formato de sistemas avançados), especificando ações
- DRM (gerenciamento de direitos digitais), especificando ações
- DRM (gerenciamento de direitos digitais), especificando ações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365597"
---
# <a name="specifying-the-actions-to-be-performed"></a>Especificando as ações a serem executadas

Quando você chama o [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) pela primeira vez para criar o objeto de leitor, o segundo parâmetro é um valor de bit que é **ou** de [**\_ direitos de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) . Use esse parâmetro para especificar quais ações o aplicativo executará no primeiro arquivo a ser aberto. Essas ações correspondem diretamente aos direitos que podem ser especificados na licença. Nas chamadas subsequentes para [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), você pode modificar os direitos que você está solicitando chamando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), especificando a constante definida para a propriedade [**\_ direitos de DRM**](drm-rights.md) e usando literais de cadeia de caracteres (do tipo **WCHAR**) separados por ponto e vírgula para identificar os direitos. O trecho de código a seguir solicita quatro direitos: executar o arquivo, copiá-lo para um dispositivo e reproduzi-lo como parte de uma lista de reprodução colaborativa.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> Não confunda a [**propriedade \_ direitos de DRM**](drm-rights.md) com a propriedade de [**\_ sinalizadores DRM**](drm-flags.md) , que é uma **DWORD** usada para especificar quais direitos aplicar a uma licença local do DRM versão 1 ao copiar o conteúdo de um CD.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




