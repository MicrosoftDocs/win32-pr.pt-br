---
title: registrando a dependência de aplicativo (Windows SDK do formato de mídia 11)
description: saiba como registrar seu aplicativo com componentes de tempo de execução de APIs fornecidas pelo SDK do Windows Media Format 11.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows SDK do formato de mídia, registrando dependências do aplicativo
- registrando dependências de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc0d1e6c9c5583ea235c196c244d9969aec65128dc206720cfacc907ae0067b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845901"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>registrando a dependência de aplicativo (Windows SDK do formato de mídia 11)

os aplicativos que usam APIs fornecidas pelo sdk do formato de mídia Windows ou sdk do Windows Media Player são dependentes dos componentes de tempo de execução dessas tecnologias. Você pode registrar seu aplicativo como dependente desses componentes como parte da instalação do seu aplicativo.

Ao registrar seu aplicativo, você pode escolher um dos dois níveis de dependência: bloqueio ou dependente. Quando um ou mais aplicativos são registrados com uma dependência de bloqueio em um dos componentes de tempo de execução, o componente será bloqueado de uma reversão para uma versão anterior. Os aplicativos dependentes que não estão registrados como bloqueios não bloqueiam a reversão. Em vez disso, antes da reversão ser executada, o usuário receberá uma mensagem informando que os aplicativos dependem do componente.

Para registrar seu aplicativo, você deve definir um valor no registro que identifica seu aplicativo. O valor do registro a ser definido depende do componente no qual seu aplicativo é dependente. Você também pode definir dois valores adicionais por dependência para fornecer informações extras sobre seu aplicativo.

os valores de registro a seguir são usados para registrar a dependência no tempo de execução do SDK do formato de mídia Windows:

-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ aplicativo, "*app*", "*app \_ String*"
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ descritor, "*app*", "*ref \_ Descriptor*"
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ versão, "*aplicativo*",*" \_ versão do WMF*"

o seguinte valor de registro é usado para registrar dependência no tempo de execução Windows Media Player SDK:

-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *\_ tipo de referência* \\ aplicativo, "*app*", "*app \_ String*"
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *referência de \_ tipo ref* \\ , "*app*", "*ref \_ Descriptor*"
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *\_ tipo de referência* \\ versão, "*aplicativo*",*" \_ versão do WMP*"

As seguintes variáveis são usadas nos valores de registro listados acima:

*tipo de referência \_*

Substituir por BlockingRefCounts para dependência de bloqueio ou com DependentRefCounts para dependência sem bloqueio.

*APP*

Nome ou descritor curto do seu aplicativo. Essa cadeia de caracteres não será usada em mensagens exibidas para o usuário. Esse valor é o identificador usado em todos os três valores de registro associados a cada um dos componentes de tempo de execução.

*Cadeia de caracteres do aplicativo \_*

Descritor do seu aplicativo. Essa cadeia de caracteres pode ser usada em mensagens exibidas para o usuário.

*\_descritor de referência*

Descrição de como seu aplicativo usa o componente. Esse valor pode incluir no máximo 256 caracteres.

*versão do WMP \_*

versão do Windows Media Player exigida pelo seu aplicativo.

*versão do WMF \_*

versão do SDK do formato de mídia Windows exigido pelo seu aplicativo.

Os três valores de registro de exemplo a seguir demonstram como configurar os valores para seu aplicativo:

-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ app, "SouthridgeVideo", "Southridge Video Player"
-   HKEY \_ CLASSES \_ raiz \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ descritor, "SouthridgeVideo", "Southridge Video Player usa o SDK do formato de mídia Windows para reproduzir arquivos de vídeo."
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ versão, "SouthridgeVideo", "9.0.0.2600"

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Project Considere**](project-considerations.md)
</dt> </dl>

 

 




