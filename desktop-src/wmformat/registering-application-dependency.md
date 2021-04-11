---
title: Registrando a dependência do aplicativo (SDK do Windows Media Format 11)
description: Registrando dependência de aplicativo
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- SDK do Windows Media Format, registrando dependências do aplicativo
- registrando dependências de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008674"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a>Registrando a dependência do aplicativo (SDK do Windows Media Format 11)

Os aplicativos que usam APIs fornecidas pelo SDK do Windows Media Format ou do Windows Media Player dependem dos componentes de tempo de execução dessas tecnologias. Você pode registrar seu aplicativo como dependente desses componentes como parte da instalação do seu aplicativo.

Ao registrar seu aplicativo, você pode escolher um dos dois níveis de dependência: bloqueio ou dependente. Quando um ou mais aplicativos são registrados com uma dependência de bloqueio em um dos componentes de tempo de execução, o componente será bloqueado de uma reversão para uma versão anterior. Os aplicativos dependentes que não estão registrados como bloqueios não bloqueiam a reversão. Em vez disso, antes da reversão ser executada, o usuário receberá uma mensagem informando que os aplicativos dependem do componente.

Para registrar seu aplicativo, você deve definir um valor no registro que identifica seu aplicativo. O valor do registro a ser definido depende do componente no qual seu aplicativo é dependente. Você também pode definir dois valores adicionais por dependência para fornecer informações extras sobre seu aplicativo.

Os seguintes valores de registro são usados para registrar a dependência no tempo de execução do SDK do Windows Media Format:

-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ aplicativo, "*app*", "*app \_ String*"
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ descritor, "*app*", "*ref \_ Descriptor*"
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ versão, "*aplicativo*",*" \_ versão do WMF*"

O seguinte valor de registro é usado para registrar a dependência no tempo de execução do SDK do Windows Media Player:

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

Versão do Windows Media Player exigida pelo seu aplicativo.

*versão do WMF \_*

Versão do SDK do Windows Media Format exigida pelo seu aplicativo.

Os três valores de registro de exemplo a seguir demonstram como configurar os valores para seu aplicativo:

-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ app, "SouthridgeVideo", "Southridge Video Player"
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ descritor, "SouthridgeVideo", "SOUTHRIDGE Video Player usa o Windows Media Format SDK para reproduzir arquivos de vídeo".
-   HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ versão, "SouthridgeVideo", "9.0.0.2600"

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Considerações sobre o projeto**](project-considerations.md)
</dt> </dl>

 

 




