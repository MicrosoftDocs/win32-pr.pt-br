---
title: Trabalhando com modelos de conformidade do dispositivo
description: Trabalhando com modelos de conformidade do dispositivo
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- perfis, modelos de conformidade do dispositivo
- perfis, modelos de conformidade
- codecs, modelos de conformidade do dispositivo
- codecs, modelos de conformidade
- modelos de conformidade do dispositivo, sobre
- modelos de conformidade
- modelos, modelos de conformidade do dispositivo
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo
- ASF (formato de sistemas avançados), modelos de conformidade do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084348"
---
# <a name="working-with-device-conformance-templates"></a>Trabalhando com modelos de conformidade do dispositivo

Devido à grande flexibilidade dos arquivos ASF, muitas vezes é difícil determinar se um arquivo é apropriado para reprodução em um dispositivo específico. Por exemplo, os arquivos escritos para reprodução local em computadores desktop não são ideais para uso em dispositivos portáteis. Os modelos de conformidade do dispositivo permitem que os aplicativos identifiquem rapidamente o tipo de dispositivo de reprodução para o qual um arquivo foi projetado. Se o modelo de conformidade do dispositivo não corresponder ao dispositivo, o aplicativo poderá informar ao usuário que o arquivo não é apropriado para o dispositivo. Dessa forma, o usuário pode ter a garantia de uma melhor experiência de reprodução.

Se você estiver gravando arquivos exclusivamente para uso em computadores pessoais, os modelos de conformidade do dispositivo não serão tão de um fator na criação de perfis. A principal finalidade desses modelos é garantir que os arquivos criados para uso com hardware especial sejam compatíveis com uma gama completa de dispositivos, e não apenas um único dispositivo.

Um modelo de conformidade do dispositivo é uma asserção de que um arquivo ASF contém dados codificados dentro de determinados parâmetros. Para obter mais informações sobre as configurações apropriadas para os modelos individuais, consulte [parâmetros de modelo de conformidade do dispositivo](device-conformance-template-parameters.md).

Os seguintes codecs dão suporte a modelos de conformidade do dispositivo:

-   Vídeo do Windows Media 9
-   Windows Media Audio 9 e posterior
-   Windows Media Audio 9 Professional e posterior
-   Voz do Windows Media Audio 9

Você não precisa executar nenhuma etapa especial para usar modelos de conformidade do dispositivo. O codec grava automaticamente uma cadeia de caracteres de modelo para cada fluxo apropriado no arquivo. O codec decidirá qual modelo usar, com base nas definições de configuração de fluxo no perfil. Há alguma sobreposição nos parâmetros do modelo de conformidade do dispositivo, portanto, convém solicitar um modelo específico em vez de permitir que o codec atribua um para você. Você pode especificar qual modelo deseja definindo a \_ Propriedade g wszDecoderComplexityRequested com os métodos da interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) do objeto de configuração de fluxo apropriado.

Quando um arquivo ASF é gravado, o modelo de conformidade do dispositivo real para cada fluxo é definido como o valor passado ao gravador pelo codec. Ao abrir um arquivo para leitura, você pode descobrir em qual modelo os fluxos do arquivo estão em conformidade usando os métodos da interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) para recuperar o \_ atributo de nível de fluxo g wszDeviceConformanceTemplate. Para obter mais informações sobre atributos, consulte [trabalhando com metadados](working-with-metadata.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando perfis**](designing-profiles.md)
</dt> <dt>

[**Parâmetros do modelo de conformidade do dispositivo**](device-conformance-template-parameters.md)
</dt> </dl>

 

 




